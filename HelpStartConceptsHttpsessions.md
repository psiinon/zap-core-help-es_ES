# Sesiones HTTP #

Esta herramienta realiza un seguimiento de las sesiones HTTP existente en un sitio particular y le permite Zaproxy todas las solicitudes que en una sesión especial de la fuerza. Básicamente, permite al usuario cambiar fácilmente entre sesiones de usuario en un sitio y crear una nueva sesión sin "destruir" a los ya existentes.

Se basa en el concepto de Tokens de sesión, que son los parámetros de mensaje HTTP (por ahora sólo Cookies) que permiten a un servidor HTTP conectar un mensaje de solicitud con sus peticiones anteriores o los datos almacenados. En el caso de Zaproxy, conceptualmente, tokens de sesión han sido clasificados en 2 categorías: default sesión fichas y tokens de sesión del sitio. Los tokens de sesión por defecto son los que el usuario puede configurar en la [pantalla de opciones][] y son fichas que, por defecto, automáticamente se consideran tokens de sesión para cualquier sitio (por ejemplo. phpsessid, jsessionid, etc). Los tokens de sesión del sitio son un conjunto de fichas para un sitio particular y generalmente se establecen utilizando los menús emergentes disponibles en la [Ficha Parámetros][Ficha Par_metros].

Esta herramienta detecta automáticamente, con los tokens de sesión definido o los tokens de sesión por defecto automáticamente detectado, alguna sesión HTTP que existe en la comunicación. Las sesiones detectadas se muestran en la [pestaña de sesiones HTTP][pesta_a de sesiones HTTP].

El usuario puede, utilizando el botón disponible en la [pestaña de sesiones HTTP][pesta_a de sesiones HTTP], crear una nueva sesión sin destruir la existente, o puede forzar una de las sesiones como 'activos'. Cuando una sesión está 'activa', todas las solicitudes salientes enviadas al sitio correspondiente se modifican, los tokens de sesión está establecidos para que coincida con la sesión activa. De esta manera, el usuario puede forzar fácilmente algunos mensajes que 'parte de' una determinada sesión y después cambian y enviar mensajes en otra sesión.

El Spider es configurado usando la  href="../../ui/dialogs/options/spider.html">Pantalla de opciones de Spider.

## Acceso vía ##

<table> 
 <tbody>
  <tr> 
   <td>&nbsp;&nbsp;&nbsp;&nbsp;</td> 
   <td><a href="HelpUiTabsHttpsessions" rel="nofollow">Sesiones HTTP pesta&ntilde;a</a></td> 
   <td></td> 
  </tr> 
 </tbody>
</table>

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
   <td><a href="HelpUiDialogsOptionsHttpsessions" rel="nofollow">HTTP Pantalla de opciones de sesi&oacute;n</a></td> 
   <td>para una vista general de las opciones de la herramienta</td> 
  </tr> 
  <tr> 
   <td>&nbsp;&nbsp;&nbsp;&nbsp;</td> 
   <td><a href="HelpUiTabsParams" rel="nofollow">Pesta&ntilde;a de Par&aacute;metros</a></td> 
   <td>para un resumen de la Pesta&ntilde;a de Par&aacute;metros</td> 
  </tr> 
 </tbody>
</table>


[pantalla de opciones]: HelpUiDialogsOptionsHttpsessions
[Ficha Par_metros]: HelpUiTabsParams
[pesta_a de sesiones HTTP]: HelpUiTabsHttpsessions