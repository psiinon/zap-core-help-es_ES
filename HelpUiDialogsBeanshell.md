# BeanShell Console dialog #

### Introducción / Qué es la BeanShell ###

La [BeanShell][] es un shell interactivo de Java que puede ser utilizado para ejecutar scripts de BeanShell. Estos scripts son una forma simplificada de Java que utilizan muchos elementos de la sintaxis de Java, pero en un formato de scripting más simple. Cualquier código en Java es también código válido en BeanShell. La integración de BeanShell en OWASP ZAP te permite escribir scripts utilizando las funciones y conjuntos de datos de ZAP. Esto puede ser una herramienta muy poderosa para analizar aplicaciones web.

### BeanShell Consola ###

La consola se inicia desde el menú de Herramientas, y contiene una pantalla dividida en la que la mitad superior consta de la consola interactiva BeanShell y la mitad inferior es un editor de texto sencillo. Para scripts complejos, te recomendamos utilizar un editor de Java. Los scripts pueden ser cargados, guardados y evaluados desde el editor.

Cuando el BeanShell se inicia una cantidad de objetos de ZAP se encuentran disponibles para su uso, entre ellos:

 *  el singletón *Model*, a través del objeto llamado ***model***
 *  el árbol de sitios actuales *SiteTree* a través del objeto ***sites***
 *  una instancia de *HttpSender* a través del objeto ***sender***

Ten en cuenta que BeanShell es débilmente tipado. Por lo tanto, no es necesario declarar variables antes de utilizarlas - esto hace que los scripts sean un poco más concisos que en lenguaje Java regular. Pero de todas maneras, si quieres definir el tipo puedes hacerlo.

### Utilizando el Mapa del Sitio ###

Iniciemos con algo útil y usual: Iterar a través de todos los nodos de sitio y chequear por la existencia de un archivo. Un script ya ha sido creado que para este fin, escoge *Cargar* y selecciona el archivo *example.tree.bsh*.

``````````
import org.apache.commons.httpclient.URI;
import org.parosproxy.paros.network.HttpMessage;
import org.parosproxy.paros.model.*;

Tree () {
	
	find (SiteNode node, String resource) {
		if (node == null) return;
		ref = node.getHistoryReference();
		if ((ref != null) && (!node.isLeaf())) {
			checkExists(ref, resource);    
		}
		for (i=0;i<node.getChildCount();i++) {   
			try {
				find (node.getChildAt(i), resource);
			} catch (Exception e) {
				e.printStackTrace();
			}
		}
	}
	
	checkExists(ref, resource) {
		u = ref.getHttpMessage().getRequestHeader().getURI().toString() + "/" + resource;
		msg = ref.getHttpMessage();
		msg.getRequestHeader().setURI(new URI(u));
		sender.sendAndReceive(msg, true);
		if (msg.getResponseHeader().getStatusCode() == 200) {
			print("Found: "+msg.getRequestHeader().getURI().toString());
		}
	}

	return this;
}
``````````

Antes de hacer click en Evaluar, primero navega a un sitio a través de ZAP para rellenar el árbol:

Ahora haz click en evaluar para ejecutar el script que está en el editor. Si no hay errores, puedes ahora empezar utilizando el objeto definido en el script al realizar estos comandos:

``````````
t = Tree();
``````````

Construye un nuevo objeto Tree y le asigna una referencia a *t*.

``````````
t.find(sites.getRoot(), "index.html");
``````````

Llama al método *find* en t, que toma un *SiteNode* como el primer argumento y un recurso a encontrar como el segundo. En este caso, el método iterará por todos los nodos en el árbol, debido a que iniciamos en la raíz, y encontrará los archivos index.html.

En vez de iterar por todos los nodos, también podemos iniciar en un nodo específico al usar el método *findChild*.

Esto debería darte una idea del poder de BeanShell en ZAP. Pero para explotarlo por completo, necesitarás familiarizarte con la API interna y las características de BeanShell. El BeanShell ha sido configurado para permitir accesso completo a todos los objetos y métodos internos - incluso los privados.

### Petición HTTP simple ###

En el siguiente ejemplo, crearemos y enviaremos una solicitud HTTP directamente en la consola interactiva:

``````````
Por determinar
``````````

Para utilizar por completo el poder de BeanShell, debes familiarizarte con los mecanismos internos de ZAP. El objeto *sender* es la misma instancia utilizada por el [Editor Manual de Solicitudes][] y por lo tanto utilizará automáticamente las configuraciones de proxy establecidas en los ajustes de ZAP.

``````````
Por determinar
``````````

### Consejos ###

Utiliza el comando *unset(String)* para liberar cualquier variable, método u objeto declarado. Esto es útil si deseas reemplazar la declaración de un método en el espacio de variables actual. Ten en cuenta que el comando toma un argumento de tipo String, no un Objeto, así que para liberar el objeto *t* que utilizamos arriba, deberías utilizaR: *unset("t");* y no *unset(t);*

## Acceso vía ##

<table> 
 <tbody>
  <tr>
   <td>&nbsp;&nbsp;&nbsp;&nbsp;</td>
   <td> <a href="HelpUiTlmenuTools" rel="nofollow">Men&uacute; Herramientas en el nivel superior</a></td>
   <td>'BeanShell Console' menu item</td>
  </tr> 
 </tbody>
</table>

## Vease también ##

<table> 
 <tbody>
  <tr>
   <td>&nbsp;&nbsp;&nbsp;&nbsp;</td>
   <td> <a href="HelpUiOverview" rel="nofollow">UI Overview</a></td>
   <td>Para una vista general sobre la interfaz de usuario</td>
  </tr> 
  <tr>
   <td>&nbsp;&nbsp;&nbsp;&nbsp;</td>
   <td> <a href="HelpUiDialogsDialogs" rel="nofollow">Cuadros de di&aacute;logo</a></td>
   <td>para detalles de los cuadros de di&aacute;logos o popups </td>
  </tr> 
 </tbody>
</table>


[BeanShell]: http://www.beanshell.org/
[Editor Manual de Solicitudes]: HelpUiDialogsMan_req