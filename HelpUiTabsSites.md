# Pestaña Sitios #

La pestaña Sitios muestra todos los URLs visitados en una estructura de árbol.
Se puede seleccionar cualquier nodo del árbol para mostrar la solicitud y la respuesta para ese URL en las pestañas relevantes.


## Menú de botón derecho ##

Al hacer click derecho sobre un nodo se abrirá un menú que le permitirá:

### Atacar ###

El menú de ataque tiene los siguientes submenús:

#### Active Scan... ####

This will launch the [Escaneo Activo][] dialog which allows you to initiate an [escaneo activo][] with the starting point set to the request you selected.


#### Spider... ####

This will launch the [Spider(Araña)][Spider_Ara_a] dialog which allows you to initiate the [spider][] with the starting point set to the request you selected.


### Include in Context ###

This menu allows you to include the selected nodes and all of their subordinates in the specified [context][].
You also have the option to create a new context.
Se mostrará la [Session Contexts][] dialog will be displayed to allow you to make any additional changes.

### Exclude from Context ###

This menu allows you to exclude the selected nodes and all of their subordinates from the specified [context][].
Se mostrará la [Session Contexts][] dialog will be displayed to allow you to make any additional changes.

### Flag as context ###

This menu has the following submenus for each of the [contexts][context] you have defined:

#### *Context name* Form-based Auth Login request ####

This identifies the specified node as a login request for the specified context.
You may only have one node identified as such in any one context.
Se mostrará la [Session Context Authentication][] screen will be displayed to allow you to make any additional changes.

#### *Context name* Data driven node ####

This identifies the specified node as [Data driven content][] for the specified context.
Se mostrará la [Session Context Structure][] screen will be displayed to allow you to make any additional changes.

### Excluir de ###

Este menú tiene los siguientes submenús:

#### Proxy ####

Esto excluirá los nodos seleccionados desde el proxy. Aunque seguirán siendo procesadas vía ZAP no aparecerán en ninguna de las pestañas.
Esto puede usarse para ignorar las URLs que no son relevantes para el sistema que actualmente está probando.
Los nodos pueden ser incluidos a través del cuadro de dialogo [Propiedades de la Sesión][Propiedades de la Sesi_n] .

#### Escáner ####

Esto evitará que los nodos seleccionados sean escaneados activamente.
Los nodos pueden ser incluidos a través del cuadro de dialogo [Propiedades de la Sesión][Propiedades de la Sesi_n] .

#### Spider(Araña) ####

This will prevent the selected nodes from being spidered.
Los nodos pueden ser incluidos a través del cuadro de dialogo [Session Properties][Propiedades de la Sesi_n] .

### Eliminar ###

Esto eliminará el nodo de ZAP junto con todos sus hijos.
Sin embargo estos pueden ser re agregados, para evitarlo use los menús 'Excluir de'.

### Parada... ###

This will bring up a new window which will allow you to set a [break point][] on that URL.
The break point is defined via a regular expression. If you visit a URL which matches this expression then ZAP will intercept it and allow you to change either the request and/or the response.

### Alertas para este nodo ###

Si la URL seleccionada tiene [alerts][] asociadas, serán mostradas bajo este menú.
Seleccionar una alerta hará que se muestre en pantalla.

### Reenviar... ###

Esto hará que aparezca el cuadro de dialogo [Resend dialog][] que le permite enviar la solicitud después de hacer los cambios que desee.

### Nueva alerta... ###

Esto hará que aparezca el cuadro de dialogo [Add Alert dialog][] el que le permitirá agregar una nueva [alert][alerts] de forma automática en la petición.

### Show in History tab ###

Esto mostrará el nodo seleccionado en la [Pestaña de historia][Pesta_a de historia].

### Ver en el navegador ###

La dirección URL del nodo seleccionado se abrirá en el navegador por defecto.

### Generar formulario de prueba anti CSRF ###

Esto abrirá una URL que le presentará un formulario generado para detectar problemas CSRF.
Sólo se activará para solicitudes POST si la API está habilidata y Java soporta la apertura de URLs en un navegador en su plataforma.

### Actualizar el árbol de sitios ###

En ocasiones el árbol de Sitios puede mostrarse incorrectamente - esta opción lo ajustará.

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


[Escaneo Activo]: HelpUiDialogsAdvascan
[escaneo activo]: HelpStartConceptsAscan
[Spider_Ara_a]: HelpUiDialogsSpider
[spider]: HelpStartConceptsSpider
[context]: HelpStartConceptsContexts
[Session Contexts]: HelpUiDialogsSessionContexts
[Session Context Authentication]: HelpUiDialogsSessionContext-auth
[Data driven content]: HelpStartConceptsDdc
[Session Context Structure]: HelpUiDialogsSessionContext-struct
[Propiedades de la Sesi_n]: HelpUiDialogsSessionSessprop
[break point]: HelpStartConceptsBreakpoints
[alerts]: HelpStartConceptsAlerts
[Resend dialog]: HelpUiDialogsResend
[Add Alert dialog]: HelpUiDialogsAddalert
[Pesta_a de historia]: HelpUiTabsHistory