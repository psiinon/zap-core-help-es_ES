# El menú Editar #

Este menú se encarga de encontrar cadenas en pestañas específicas, buscando cadenas por todas las solicitudes y respuestas y gestionando el rastreo de sesión.

### Buscar... ###

Esto abre el [Cuadro de diálogo Encontrar][Cuadro de di_logo Encontrar] que permite encontrar una cadena en la ventana seleccionada actual.


### Habilitar seguimiento de la sesión (Cookie) ###

Esto permite rastrear los detalles de la sesión almacenada en cookies.
Esta opción debe seleccionarse para habilitar la casilla "Utilizar la sesión de rastreo actual" en los cuadros de diálogos [Reenviar][] y en la [Editor de solicitudes manuales][].
El rastreo de sesión asegura que cualquier solicitud sea enviada con los detalles de la sesión actualizados.
Por ejemplo, se puede registrar una sesión cuando se ingrese como un usuario y que cierre sesión e ingresar como otro usuario.
Si reenvias una solicitud desde la primera sesión sin el rastreo de sesión entonces utilizará las cookies de la primera sesión.
Si se reenvia la misma solicitud con el rastreo de sesión entonces utilizará las cookies de la segunda sesión.

### Reiniciar estado de la sesión ###

Esto borra el rastreo de la sesión.


### Buscar... ###

Esto selecciona el [Pestaña de búsquedas][Pesta_a de b_squedas] el cual le permite buscar expresiones regulares en todos los enlaces, solicitudes y respuestas..

### Siguiente ###

Esto selecciona la siguiente ocurrencia de la última cadena buscada.
El mensaje relevante se seleccionará en la pestaña Buscar y la cadena se mostrará y resaltará en la pestaña [Solicitud][] o [Respuesta][] según corresponda.

### Anterior ###

Esto selecciona las ocurrencias anteriores de la última cadena buscada.
El mensaje relevante será seleccionado en la pestaña de búsqueda y la cadena será mostrada [Petición][Solicitud] o [Respuesta][] según la pestaña que corresponda.

Tome en cuenta que los [add-ons][] pueden agregar elementos adicionales al menú.

## Vease también ##

<table> 
 <tbody>
  <tr>
   <td>&nbsp;&nbsp;&nbsp;&nbsp;</td>
   <td> <a href="HelpUiTlmenuTlmenu" rel="nofollow">Men&uacute; del nivel superior</a></td>
   <td></td>
  </tr> 
  <tr>
   <td>&nbsp;&nbsp;&nbsp;&nbsp;</td>
   <td> <a href="HelpUiOverview" rel="nofollow">UI Overview</a></td>
   <td>Para una vista general sobre la interfaz de usuario</td>
  </tr> 
 </tbody>
</table>


[Cuadro de di_logo Encontrar]: HelpUiDialogsFind
[Reenviar]: HelpUiDialogsResend
[Editor de solicitudes manuales]: HelpUiDialogsMan_req
[Pesta_a de b_squedas]: HelpUiTabsSearch
[Solicitud]: HelpUiTabsRequest
[Respuesta]: HelpUiTabsResponse
[add-ons]: HelpStartConceptsAddons