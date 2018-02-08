# Reenviar #

Este cuadro de diálogo le permite volver a enviar una solicitud después de realizar cualquier cambio que desee.

## Solicitar ficha ##

Esto muestra el encabezado de solicitud y datos, ya sea en uno o dos paneles dependiendo de las opciones seleccionadas.

Un 'Método' pull down le permite cambiar entre los métodos HTTP.
Tenga en cuenta que cuando el método se cambia a un POSTE, a continuación, cualquiera de los parámetros de la URL se mueven en el cuerpo, y cuando el método se cambia de un POST, a continuación, los parámetros en el cuerpo se trasladó a la dirección URL.

Pull downs le permiten seleccionar diferentes [Vistas][] para la Solicitud de la cabecera y el cuerpo.

### ![view_split.png][]  Pantalla dividida para la cabecera y el cuerpo ###

This changes the display so that separate panes are used for the header and body.


### ![view_all.png][]  Visualización combinada para encabezado y cuerpo ###

Esto cambia la visualización para que la cabecera y el cuerpo se muestren en un solo panel.


### ![cookie.png][]  Utilizar la sesión actual de rastreo ###

Ver el elemento del menú "Habilitar la sesión de rastreo (Cookie)" en el [Editar menú][Editar men].


### ![118.png][]  Seguir redirección ###

Si es seleccionado, sigue automáticamente cualquier redirección enviada al navegador.


### ![layout_tabbed.png][]  Request and Response tabs side by side ###

This changes the display so that the request and response tabs are side by side.
This increases the information that can be displayed but means you cannot see both the request and response at the same time.

### ![layout_vertical_split.png][]  Request shown above Response ###

This changes the display so that the request panel is shown above the response panel.
This decreases the information that can be displayed but means you can see both the request and response at the same time.

### ![layout_horizontal_split.png][]  Request and Response panels side by side ###

This changes the display so that the request panel is shown to the left of the response panel.
This decreases the information that can be displayed but means you can see both the request and response at the same time.

## Response tab ##

This shows the data sent to your browser in response to the request that you submitted, either in one or two panels depending on the options chosen.

Pull downs allow you to select different [Views][Vistas] for the Response header and body.

## Right click menu ##

Right clicking will bring up a menu which will allow you to:

### Find... ###

This will bring up the [Find dialog][].

### Encode/Decode... ###

This will bring up the [Encode/Decode dialog][Encode_Decode dialog].
Si has resaltado algún teto entonces será incluido automáticamente en el cuadro de diálogo.

## Accessed via ##

<table> 
 <tbody>
  <tr>
   <td>&nbsp;&nbsp;&nbsp;&nbsp;</td>
   <td> <a href="HelpUiTabsSites" rel="nofollow">Pesta&ntilde;a de Sitios</a></td>
   <td>'Resend...' right click menu item</td>
  </tr> 
  <tr>
   <td>&nbsp;&nbsp;&nbsp;&nbsp;</td>
   <td> <a href="HelpUiTabsHistory" rel="nofollow">Pesta&ntilde;a de Historia</a></td>
   <td>'Resend...' right click menu item</td>
  </tr> 
 </tbody>
</table>

## Véase también ##

<table> 
 <tbody>
  <tr>
   <td>&nbsp;&nbsp;&nbsp;&nbsp;</td>
   <td> <a href="HelpUiOverview" rel="nofollow">Resumen de la interfaz de usuario</a></td>
   <td>para tener una visi&oacute;n general de la interfaz de usuario</td>
  </tr> 
  <tr>
   <td>&nbsp;&nbsp;&nbsp;&nbsp;</td>
   <td> <a href="HelpUiDialogsDialogs" rel="nofollow">Cuadros de di&aacute;logo</a></td>
   <td>para detalles de los cuadros de di&aacute;logos o pop-ups </td>
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
[Find dialog]: HelpUiDialogsFind
[Encode_Decode dialog]: HelpUiDialogsEnc_dec