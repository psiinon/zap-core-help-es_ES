# Spider(Araña) #

Spider es una herramienta que es usada para descubrir automáticamente nuevos recursos (URLs) en un sitio en particular. Comienza con una lista de URLs a visitar, llamadas semillas, las cuales dependen de como se inicia spider. Spider visita estas URLs, identifica todos los hipervinculos en la página y los agrega a la lista de URLs a visitar y el proceso continua recursivamente mientras se encuentran nuevos recursos.

The Spider puede configurarse y comenzar a usar el [ diálogo Spider .][di_logo Spider .]

[Mientras se procesa una URL, Spider realiza peticiones para extraer el recurso y luego parsear la respuesta, identificando hipervinculos. De acuerdo al tipo de respuesta presenta distintos comportamientos:

HTML

Procesa los siguientes tags, para identificar links a nuevos recursos: ][di_logo Spider .]

 *  Base - Proper handling
    
    A, Link, Area - 'href' attribute
    
    Frame, IFrame, Script, Img - 'src' attribute
    
    Meta - 'http-equiv' for 'location' and 'refresh'
    
    Form - proper handling of Forms with both GET and POST method. The fields values are generated validly, including [HTML 5.0 input types][].
 *  Comments - Valid tags found in comments are also analyzed, if specified in the [Options Spider screen][]

#### Archivos Robots.txt ####

If set in the [la pantalla de opciones del Spider][Options Spider screen], también analiza el archivo 'Robots.txt' y trata de identificar nuevos recursos usando las siguientes reglas. hay que destacar que el Spider no sigue las reglas especificadas en el archivo 'Robots.txt'.

#### Formato OData Atom ####

El contenido de OData usando el formato Atom tiene soporte. Todos los links incluidos (relativos o absolutos) son procesados.

#### Respuesta Non-HTML (No HTML) ####

Son analizadas las respuestas del texto buscando el patrón de URL

#### Respuestas Non-Text (No texto) ####

Actualmente, Spider no procesa este tipo de recursos.

## Otros aspectos ##

 *  Para comprobar si una URL fue visitada, puede configurar el comportamiento de como se manejan los parámetros en la pantalla de opciones del Spider.
 *  Al comprobar si una URL fue visitada, hay algunos parámetros en común los cuales son ignorados: jsessionid, phpsessid, aspsessionid, utm\_\*
 *  El comportamiento del spider con respecto a las cookies depende de cómo se inicia el spider y qué opciones están habilitadas. Para obtener más detalles, consulte la pantalla Opciones del spider.

El Spider es configurado usando la  href="../../ui/dialogs/options/spider.html">Pantalla de opciones de Spider.

## Vease también ##

<table> 
 <tbody>
  <tr> 
   <td>&nbsp;&nbsp;&nbsp;&nbsp;</td> 
   <td><a href="HelpUiOverview" rel="nofollow">UI Overview</a></td> 
   <td>Para una vista general sobre la interfaz de usuario</td> 
  </tr> 
  <tr> 
   <td>&nbsp;&nbsp;&nbsp;&nbsp;</td> 
   <td><a href="HelpStartConceptsConcepts" rel="nofollow">Caracteristicas</a></td> 
   <td>proporcionado por ZAP</td> 
  </tr> 
  <tr> 
   <td>&nbsp;&nbsp;&nbsp;&nbsp;</td> 
   <td><a href="HelpUiDialogsOptionsSpider" rel="nofollow">Pantalla de opciones de Spider</a></td> 
   <td>Para una vista general de las opciones del Spider</td> 
  </tr> 
 </tbody>
</table>


[di_logo Spider .]: HelpUiDialogsSpider
[HTML 5.0 input types]: http://www.w3schools.com/html5/html5_form_input_types.asp
[Options Spider screen]: HelpUiDialogsOptionsSpider