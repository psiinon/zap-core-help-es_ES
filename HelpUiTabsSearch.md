# Pestaña Buscar #

La pestaña Buscar permite buscar expresiones regulares en todos los URLs, solicitudes, respuestas, encabezados y en otras funcionalidades proporcionadas por complementos.

Introduzca la expresión regular que se desee buscar en el cuadro de búsqueda y presione retorno o haga clic en el botón buscar: ![049.png][]

Un menú desplegable permite elegir si buscar en las URLs, las solicitudes, las respuestas o en todo.

Todas las URLs, solicitudes o respuestas que contienen el patrón de búsqueda se mostrarán en la pestaña.
Puede hallar útil agregar .\* al término de la búsqueda, esto puede dar mas contexto. Por ejemplo password.\*

Se puede utilizar los botones ![107.png][] siguiente y ![108.png][]anterior para ver términos encontrados en las pestañas [Solicitud][] y [Respuesta][].


También se puede ir directamente a una instancia específica haciendo clic en la línea correspondiente en la lista de resultados.

## Menú de botón derecho ##

Al hacer click derecho sobre un nodo se abrirá un menú que le permitirá:

### Atacar ###

El menú de ataque tiene los siguientes submenús:

#### Active Scan... ####

This will launch the [Active Scan dialog][] which allows you to initiate an [active scan][] with the starting point set to the request you selected.


#### Spider... ####

This will launch the [Spider dialog][] which allows you to initiate the [spider][] with the starting point set to the request you selected.


### Include in Context ###

This menu allows you to include the selected nodes and all of their subordinates in the specified [context][].
You also have the option to create a new context.
The [Session Contexts][] dialog will be displayed to allow you to make any additional changes.

### Exclude from Context ###

This menu allows you to exclude the selected nodes and all of their subordinates from the specified [context][].
The [Session Contexts][] dialog will be displayed to allow you to make any additional changes.

### Flag as context ###

This menu has the following submenus for each of the [contexts][context] you have defined:

#### *Context name* Form-based Auth Login request ####

This identifies the specified node as a login request for the specified context.
You may only have one node identified as such in any one context.
The [Session Context Authentication][] screen will be displayed to allow you to make any additional changes.

#### *Context name* Data driven node ####

This identifies the specified node as [Data driven content][] for the specified context.
The [Session Context Structure][] screen will be displayed to allow you to make any additional changes.

### Excluir de ###

This menu has the following submenus:

#### Proxy ####

This will exclude the selected nodes from the proxy. They will still be proxied via ZAP but will not be shown in any of the tabs.
This can be used to ignore URLs that you know are not relevant to the system you are currently testing.
The nodes can be included again via the [Session Properties][] dialog

#### Scanner ####

This will prevent the selected nodes from being actively scanned.
The nodes can be included again via the [Session Properties][] dialog

#### Spider ####

This will prevent the selected nodes from being spidered.
The nodes can be included again via the [Propiedades de la Sesión][Session Properties] dialog

### Reenviar... ###

This will bring up the [Resend dialog][] which allows you to resend the request after making any changes to it that you want to.

### Nueva alerta... ###

This will bring up the [Add Alert dialog][] which allows you to manually record a new [alert][] against this request.

### Show in History tab ###

This will show the selected node in the [History tab][].

### Mostrar en la pestaña Sitios ###

This will show the selected message in the [Sites tab][].

### Ver en el navegador ###

This will open the URL of the selected node in your default browser.

## Vease también ##

<table> 
 <tbody>
  <tr>
   <td>&nbsp;&nbsp;&nbsp;&nbsp;</td>
   <td> <a href="HelpUiOverview" rel="nofollow">UI Overview</a></td>
   <td>Para una vista general sobre la interfaz de usuario</td>
  </tr> 
 </tbody>
</table>


[049.png]: https://github.com/zaproxy/zap-core-help/wiki/images/16/049.png
[107.png]: https://github.com/zaproxy/zap-core-help/wiki/images/16/107.png
[108.png]: https://github.com/zaproxy/zap-core-help/wiki/images/16/108.png
[Solicitud]: HelpUiTabsRequest
[Respuesta]: HelpUiTabsResponse
[Active Scan dialog]: HelpUiDialogsAdvascan
[active scan]: HelpStartConceptsAscan
[Spider dialog]: HelpUiDialogsSpider
[spider]: HelpStartConceptsSpider
[context]: HelpStartConceptsContexts
[Session Contexts]: HelpUiDialogsSessionContexts
[Session Context Authentication]: HelpUiDialogsSessionContext-auth
[Data driven content]: HelpStartConceptsDdc
[Session Context Structure]: HelpUiDialogsSessionContext-struct
[Session Properties]: HelpUiDialogsSessionSessprop
[Resend dialog]: HelpUiDialogsResend
[Add Alert dialog]: HelpUiDialogsAddalert
[alert]: HelpStartConceptsAlerts
[History tab]: HelpUiTabsHistory
[Sites tab]: HelpUiTabsSites