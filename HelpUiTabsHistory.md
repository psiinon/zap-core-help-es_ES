# Pestaña Historial #

La pestaña Historial muestra una lista de todas las solicitudes en el orden en que fueron hechas.
Por cada petición podrá observar:

<table> 
 <tbody>
  <tr>
   <td>&nbsp;&nbsp;&nbsp;&nbsp;</td> 
   <td>El index de la petici&oacute;n - cada petici&oacute;n est&aacute; numerada, empezando por el n&uacute;mero 1</td>
  </tr> 
  <tr>
   <td>&nbsp;&nbsp;&nbsp;&nbsp;</td> 
   <td>El m&eacute;todo HTML, por ejemplo GET o POST</td>
  </tr> 
  <tr>
   <td>&nbsp;&nbsp;&nbsp;&nbsp;</td> 
   <td>La URL solicitada</td>
  </tr> 
  <tr>
   <td>&nbsp;&nbsp;&nbsp;&nbsp;</td> 
   <td>El c&oacute;digo de respuesta HTTP</td>
  </tr> 
  <tr>
   <td>&nbsp;&nbsp;&nbsp;&nbsp;</td> 
   <td>Un breve resumen de lo que significa el c&oacute;digo de respuesta HTTP</td>
  </tr> 
  <tr>
   <td>&nbsp;&nbsp;&nbsp;&nbsp;</td> 
   <td>La duraci&oacute;n total de la solicitud</td>
  </tr> 
  <tr>
   <td>&nbsp;&nbsp;&nbsp;&nbsp;</td> 
   <td>Cualquier <a href="HelpStartConceptsAlerts" rel="nofollow">alerta</a> en la solicitud</td>
  </tr> 
  <tr>
   <td>&nbsp;&nbsp;&nbsp;&nbsp;</td> 
   <td>Las <a href="HelpStartConceptsNotes" rel="nofollow">notas</a> que haya agregado a petici&oacute;n</td>
  </tr> 
  <tr>
   <td>&nbsp;&nbsp;&nbsp;&nbsp;</td> 
   <td>Las <a href="HelpStartConceptsTags" rel="nofollow">etiquetas</a> en la solicitud</td>
  </tr> 
 </tbody>
</table>

Al seleccionar una petición, ésta será mostrada en la [pestaña Petición][pesta_a Petici_n] y en la [pestaña Respuesta][pesta_a Respuesta] ubicadas mas arriba.


## La barra de herramientas de filtro ##

Una barra de herramientas de filtro es proporcionada para restringir cuáles solicitudes se muestran.
Al hacer clic sobre el ![054.png][] botón Filtro muestra el [cuadro de diálogo Filtro de Historial][cuadro de di_logo Filtro de Historial].
Un resumen del filtro aplicado se muestra a la derecha del botón.

## Menú de botón derecho ##

Al hacer click derecho sobre un nodo se abrirá un menú que le permitirá:

### Atacar ###

El menú de ataque tiene los siguientes submenús:

#### Análisis Activo... ####

Esto abrirá el cuadro de diálogo [Análisis Activo][An_lisis Activo] que permite iniciar un [análisis activo][an_lisis activo] con el punto de partida configurado a la solicitud seleccionada.


#### Rastreador... ####

Esto abrirá el cuadro de diálogo [Spider(Araña)][Spider_Ara_a] que permite iniciar el [rastreador][] con el punto de partida configurado a la solicitud seleccionada.


### Incluir en contexto ###

Este menú permite incluir los nodos seleccionados y todos sus subordinados en el [contexto especificado][].
También tienes la opción de crear un nuevo contexto.
El cuadro de diálogo de [Contextos de sesión][Contextos de sesi_n] se mostrará para permitir hacer cualquier cambio adicional.

### Excluir del Contexto ###

Este menú permite incluir los nodos seleccionados y todos sus subordinados en el [contexto][contexto especificado].
El cuadro de diálogo de [Contextos de sesión][Contextos de sesi_n] se mostrará para permitir hacer cualquier cambio adicional.

### Marcar como un contexto ###

Este menú tiene los siguientes submenús para cada uno de los [contextos][contexto especificado] que se han definido:

#### *Context name* Form-based Auth Login request ####

Esto identifica el nodo especificado como una petición de inicio de sesión para el contexto especificado.
Puedes tener solo un nodo identificado de esta manera en algún contexto.
Se mostrará la [Session Context Authentication][] screen will be displayed to allow you to make any additional changes.

#### *Context name* Data driven node ####

This identifies the specified node as [Contenido manejado por datos][] for the specified context.
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

Esto evitará que los nodos seleccionados sean rastreados.
Los nodos pueden ser incluidos a través del cuadro de dialogo [Propiedades de la Sesión][Propiedades de la Sesi_n] .

### Administrar Tags... ###

Esto hará que aparezca el cuadro de dialogo [Manage Tags dialog][] que le permite cambiar las [etiquetas][] asociadas con la petición.

### Nota... ###

Esto hará que aparezca el cuadro de dialogo [Add Note dialog][] que le permitirá guardar [notes][] relacionadas con la petición.

### Eliminar ###

Esto eliminará el nodo de ZAP junto con todos sus hijos.
Sin embargo estos pueden ser re agregados, para evitarlo use los menús 'Excluir de'.

### Parada... ###

Esto hará que aparezca el cuadro de dialogo [Add Break Point dialog][] which allows you to set a break point on that URL.


### Alertas para este nodo ###

Si la URL seleccionada tiene [alertas][] asociadas, serán mostradas bajo este menú.
Seleccionar una de las alertas hará que se muestre en pantalla.

### Reenviar... ###

This will bring up the [Resend dialog][] which allows you to resend the request after making any changes to it that you want to.

### New Alert... ###

Esto hará que aparezca el cuadro de dialogo [Add Alert dialog][] which allows you to manually record a new [alert][alertas] against this request.

### Show in Sites tab ###

This will show the selected message in the [Sites tab][].

### Open URL in Browser ###

La dirección URL del nodo seleccionado se abrirá en el navegador por defecto.

### Generate anti CSRF test form ###

This will open a URL which will give you a generated form for testing for CSRF issues.
It will only be enabled for POST requests, if the API is enabled and if Java supports the opening of URLs in a browser on your platform.

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


[pesta_a Petici_n]: HelpUiTabsRequest
[pesta_a Respuesta]: HelpUiTabsResponse
[054.png]: https://github.com/zaproxy/zap-core-help/wiki/images/16/054.png
[cuadro de di_logo Filtro de Historial]: HelpUiDialogsHist_filter
[An_lisis Activo]: HelpUiDialogsAdvascan
[an_lisis activo]: HelpStartConceptsAscan
[Spider_Ara_a]: HelpUiDialogsSpider
[rastreador]: HelpStartConceptsSpider
[contexto especificado]: HelpStartConceptsContexts
[Contextos de sesi_n]: HelpUiDialogsSessionContexts
[Session Context Authentication]: HelpUiDialogsSessionContext-auth
[Contenido manejado por datos]: HelpStartConceptsDdc
[Session Context Structure]: HelpUiDialogsSessionContext-struct
[Propiedades de la Sesi_n]: HelpUiDialogsSessionSessprop
[Manage Tags dialog]: HelpUiDialogsManagetags
[etiquetas]: HelpStartConceptsTags
[Add Note dialog]: HelpUiDialogsAddnote
[notes]: HelpStartConceptsNotes
[Add Break Point dialog]: HelpUiDialogsAddbreak
[alertas]: HelpStartConceptsAlerts
[Resend dialog]: HelpUiDialogsResend
[Add Alert dialog]: HelpUiDialogsAddalert
[Sites tab]: HelpUiTabsSites