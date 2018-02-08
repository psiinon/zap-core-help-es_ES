# Manual Request Editor dialog #

Este diálogo te ermite crear una solicitud desde cero que será enviada al destino especificado.

## pestaña Petición ##

Esto muestra la cabecera y datos de la solicitud, bien sea en uno o dos paneles dependiendo de las opciones seleccionadas.

Un 'Método' pull down le permite cambiar entre los métodos HTTP.
Ten en cuenta que cuando el método se cambia a un POST entonces cualquier parámetro de la URL es movido al cuerpo, y que cuando el método se cambia de un POST entonces cualquier parámetro en el cuerpo es movido a la URL.

Pull downs le permiten seleccionar diferentes [Vistas][] para la cabecera y cuerpo de la Solicitud.

### ![view_split.png][]  Pantalla dividida para el encabezado y el cuerpo ###

Esto cambia la visualización para uitlizar paneles diferentes para la cabecera y el cuerpo.


### ![view_all.png][]  Visualización combinada para el encabezado y el cuerpo ###

Esto cambia la visualización para que la cabecera y el cuerpo se muestren en un solo panel.


### ![cookie.png][]  Use current tracking session ###

See the 'Enable session tracking (Cookie)' menu item in the [Editar menú][Editar men].


### ![118.png][]  Seguir redirección ###

Si se selecciona, sigue automáticamente cualquier redirección enviada al navegador.


### ![layout_tabbed.png][]  Request and Response tabs side by side ###

Esto cambia la presentación de manera que las pestañas de solicitud y respuesta están lado a lado.
Esto incrementa la información que puede ser mostrada pero significa que no se pueden ver al mismo tiempo la solicitud y la respuesta.

### ![layout_vertical_split.png][]  Request shown above Response ###

Esto cambia la presentación de manera que el panel de solicitud se muestra sobre el panel de respuesta.
Esto disminuye la información que puede ser mostrada pero significa que se pueden ver al mismo tiempo la solicitud y la respuesta.

### ![layout_horizontal_split.png][]  Request and Response panels side by side ###

Esto cambia la presentación de manera que el panel de solicitud se muestra a la izquierda del panel de respuesta.
Esto disminuye la información que puede ser mostrada pero significa que se pueden ver al mismo tiempo la solicitud y la respuesta.

## pestaña Respuesta ##

Esto muestra la información enviada al navegador en respuesta a la solicitud enviada, ya sea en uno o dos paneles dependiendo de las opciones seleccionadas.

Pull downs allow you to select different [Views][Vistas] for the Response header and body.

## Menú de botón derecho ##

Al hacer clic derecho se abrirá un menú que permite:

### Encontrar... ###

Esto abre el [cuadro de diálogo Encontrar][cuadro de di_logo Encontrar].

### Encode/Decode... ###

This will bring up the [Encode/Decode dialog][Encode_Decode dialog].
Si se ha resaltado cualquier texto, este se incluirá automáticamente en el cuadro de diálogo.

## Acceso vía ##

<table> 
 <tbody>
  <tr>
   <td>&nbsp;&nbsp;&nbsp;&nbsp;</td>
   <td> <a href="HelpUiTlmenuTools" rel="nofollow">Top level Tools menu</a></td>
   <td>'Manual Request Editor ...' menu item</td>
  </tr> 
 </tbody>
</table>

## Vease también ##

<table> 
 <tbody>
  <tr>
   <td>&nbsp;&nbsp;&nbsp;&nbsp;</td>
   <td> <a href="HelpUiOverview" rel="nofollow">UI Overview</a></td>
   <td>for an overview of the user interface</td>
  </tr> 
  <tr>
   <td>&nbsp;&nbsp;&nbsp;&nbsp;</td>
   <td> <a href="HelpUiDialogsDialogs" rel="nofollow">Dialogs</a></td>
   <td>for details of the dialogs or popups </td>
  </tr> 
 </tbody>
</table>


[Vistas]: HelpUiViews
[view_split.png]: https://github.com/zaproxy/zap-core-help/wiki/images/view_split.png
[view_all.png]: https://github.com/zaproxy/zap-core-help/wiki/images/view_all.png
[cookie.png]: https://github.com/zaproxy/zap-core-help/wiki/images/fugue/cookie.png
[Editar men]: HelpUiTlmenuEdit
[118.png]: https://github.com/zaproxy/zap-core-help/wiki/images/16/118.png
[layout_tabbed.png]: https://github.com/zaproxy/zap-core-help/wiki/images/layout_tabbed.png
[layout_vertical_split.png]: https://github.com/zaproxy/zap-core-help/wiki/images/layout_vertical_split.png
[layout_horizontal_split.png]: https://github.com/zaproxy/zap-core-help/wiki/images/layout_horizontal_split.png
[cuadro de di_logo Encontrar]: HelpUiDialogsFind
[Encode_Decode dialog]: HelpUiDialogsEnc_dec