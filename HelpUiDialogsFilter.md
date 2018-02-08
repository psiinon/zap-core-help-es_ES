# Filtros #

**NOTA: Los filtros han sido reemplazados por el complemento Replacer y los scripts que son más potentes y flexibles.
Los filtros se eliminarán en una versión futura de ZAP.**

Esto permite establecer [filters][] que son aplicados a solicitudes y respuestas.

Los siguientes filtros son compatibles por defecto.

## Cambiar el agente de usuario a otros navegadores ##

## Detectar contenido potencialmente malicioso o inseguro en respuestas HTTP ##

## Detectar y alertar intentos de modificación con 'Set-cookie' en respuestas HTTP ##

## Evitar la caché del navegador (strip off IfModifiedSince) ##

## Registrar las cookies enviadas por el navegador ##

## Registrar en el archivo consultas únicas GET ##

## Registrar en el archivo consultas únicas POST ##

## Registrar en el archivo solicitudes y respuestas ##

## Reemplazar el cuerpo de solicitudes HTTP utilizando patrones definidos ##

## Reemplazar el encabezado de solicitudes HTTP utilizando patrones definidos ##

## Reemplazar el cuerpo de respuestas HTTP utilizando patrones definidos ##

## Reemplazar el encabezado de respuestas HTTP utilizando patrones definidos ##

## Enviar el ID de las solicitudes en la sesión de ZAP ##

This filter will add a special header tag to each request send to the server. So you can track ZAP's requests, when investigating your own web application. It's helpful to have a distinct id for multiple requests, when parsing for example HTTP server's log files.

Request header is modified like this (example):

``````````
X-ZAP-RequestID: <sessionName>–<number>
``````````

 *  `sessionName` está encodeado el nombre de la sesión
 *  `number` comienza con uno, y se incrementa en cada solicitud. Es válida sólo por cada sesión

## Acceso vía ##

<table> 
 <tbody>
  <tr>
   <td>&nbsp;&nbsp;&nbsp;&nbsp;</td>
   <td> <a href="HelpUiTlmenuTools" rel="nofollow">Men&uacute; Herramientas en el nivel superior</a></td>
   <td>Men&uacute; 'Filtros...'</td>
  </tr> 
 </tbody>
</table>

## Vease también ##

<table> 
 <tbody>
  <tr>
   <td>&nbsp;&nbsp;&nbsp;&nbsp;</td>
   <td> <a href="HelpUiOverview" rel="nofollow">Visi&oacute;n general de la IU</a></td>
   <td>Para una vista general sobre la interfaz de usuario</td>
  </tr> 
  <tr>
   <td>&nbsp;&nbsp;&nbsp;&nbsp;</td>
   <td> <a href="HelpUiDialogsDialogs" rel="nofollow">Cuadros de di&aacute;logo</a></td>
   <td>para detalles de los cuadros de di&aacute;logos o popups </td>
  </tr> 
 </tbody>
</table>


[filters]: HelpStartConceptsFilters