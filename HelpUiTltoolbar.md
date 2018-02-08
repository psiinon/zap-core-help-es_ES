# Barra de herramientas del Nivel Superior #

Esta barra de herramientas proporciona un conjunto de controles para la funcionalidad comúnmente utilizada.

## Modo Desplegable ##

Esto le permite cambiar el [modo][] actual.

## ![171.png][]  Nueva Sesión ##

Este botón es el mismo que el elemento del [Menú de archivos][Men_ de archivos] 'Nueva Sesión'.

## ![047.png][]  Abrir Sesión ##

Este botón es el mismo que el elemento del [Menú de archivos][Men_ de archivos] 'Abrir sesión'.

## ![096.png][]  Sesión Persist ##

Este botón es el mismo que el [File menu][Men_ de archivos] 'Persist Session...' menu item.

## ![camera.png][]  Sesión Snapshot ##

Este botón es el mismo que el [File menu][Men_ de archivos] 'Snapshot Session' menu item.

## ![024.png][]  Propiedades de Sesión ##

Este botón es el mismo que el [File menu][Men_ de archivos] 'Properties...' menu item.

## ![041.png][]  Opciones ##

Este botón es el mismo que el [Tools menu][] 'Options...' menu item.

## ![ui-tab-show.png][]  Mostrar Todas las Tabs ##

Este botón revela todas las tabs ocultas.

## ![ui-tab-hide.png][]  Ocultar Tabs Sin Fijar ##

Este botón oculta todas las tabs que están 'unpinned'. Las tabs se pueden fijar y soltar mediante el ícono pequeño 'pin' que se muestra cuando se selecciona la tab.

## ![ui_tab_text.png][]  Mostrar Nombres e Iconos de Tabs ##

Este botón alterna la visualización de los nombres de las tabs.

## ![expand_sites.png][]  Expandir tab de sitios ##

Esto cambia la visualización para que la ventana 'tree' que contiene la tab del Sitio se extienda por toda la longitud del lado izquierdo.
Esto reducirá la cantidad de espacio disponible para la ventana de 'information'.

## ![expand_info.png][]  Expandir tabs de información ##

Esto cambia la visualización de modo que la ventana de 'information' se extiende por toda la longitud de la parte inferior.
Esto reducirá la cantidad de espacio disponible para la ventana 'tree'.

## ![expand_full.png][]  Diseño completo ##

Esto cambia la visualización para que la tab seleccionada ocupe toda la pantalla.
Esto es útil cuando se usa ZAP en pantallas pequeñas.

## ![layout_tabbed.png][]  Tabs de solicitud y respuesta una al lado de la otra ##

Esto cambia la visualización para que las tabs de solicitud y respuesta estén una al lado de la otra.
Esto aumenta la información que se puede mostrar pero significa que no puede ver tanto la solicitud como la respuesta al mismo tiempo.

## ![layout_vertical_split.png][]  Solicitud mostrada arriba de la respuesta ##

Esto cambia la visualización para que el panel de solicitud se muestre sobre el panel de respuesta.
Esto disminuye la información que se puede mostrar, pero significa que puede ver tanto la solicitud como la respuesta al mismo tiempo.

## ![layout_horizontal_split.png][]  Paneles de solicitud y respuesta al lado lateral ##

Esto cambia la visualización para que el panel de solicitud se muestre a la izquierda del panel de respuesta.
Esto disminuye la información que se puede mostrar, pero significa que puede ver tanto la solicitud como la respuesta al mismo tiempo.

## ![152.png][] /  ![151.png][]  Configurar/ Desconfigurar interrupción en todas las solicitudes y respuestas ##

Esto configura o desconfigura un [punto de ruptura][] 'global' que atrapará y mostrará la siguiente solicitud o respuesta en la [pestaña de interrupción][pesta_a de interrupci_n].
Puedes cambiar cualquier parte de la solicitud o respuesta que quieras y enviarla a la aplicación destino al presionar cualquiera de estos botones 'Paso' o 'Continuar'.
Puedes cambiar entre un unico botón de interrupción 'combinado' y con éste separar los que se refieren a las solicitudes y los de las respuestas por medio de la [Pantalla de opciones de interrupción.][Pantalla de opciones de interrupci_n.]

## ![105.png][] /  ![105r.png][]  Configurar/ Desconfigurar en todas las solicitudes ##

Esto configura o desconfigura un [punto de quiebre][punto de ruptura] 'global' que atrapará y enseñara la siguiente solicitud en la [pestaña de interrupción][pesta_a de interrupci_n].
Usted podrá entonces cambiar cualquier parte de la solicitud que quiera enviar y mandarla a la aplicación destino presionando el botón de 'Paso' o el de 'Continuar'.
Alternativamente puedes presionar el botón 'Declinar' para deshacerte de la solicitud.
Puedes cambiar entre un unico botón de interrupción 'combinado' y con éste separar los que se refieren a las solicitudes y los de las respuestas por medio de la [Pantalla de opciones de interrupción.][Pantalla de opciones de interrupci_n.]

## ![106.png][] /  ![106r.png][]  Configurar/ Desconfigurar en todas las respuestas ##

Esto configura o desconfigura un [punto de quiebre][punto de ruptura] 'global' que atrapará y enseñara la siguiente respuesta en la [pestaña de interrupción][pesta_a de interrupci_n].
Usted puede cambiar cualquier parte de la respuesta que desee y enviarla a su buscador presionando el botón de 'Paso' o el de 'Continuar'.
Alternativamente puedes Alternativamente puedes presionar el botón 'Declinar' para deshacerte de la solicitud.
Puedes cambiar entre un unico botón de interrupción 'combinado' y con éste separar los que se refieren a las solicitudes y los de las respuestas por medio de la [Pantalla de opciones de interrupción.][Pantalla de opciones de interrupci_n.]

## ![143.png][]  Paso ##

Esto le permite a la solicitud o respuesta atrapada continuar a la aplicación o al buscador sin ningún cambio que le hayas hecho.
El [punto de ruptura][] 'global' permanecerá configurado de manera que la siguiente respuesta o solicitud también sea atrapada.
Este botón solo se encuentra habilitado cuano una respuesta o una solicitud es atrapada.

## ![131.png][]  Continue ##

El 'global' [break point][punto de ruptura] será unset para que ZAP no vuelva a detectar las solicitudes y respuestas posteriores a menos que haya establecido puntos de interrupción en URLs específicas.
Este botón solo está habilitado cuando una solicitud o respuesta es trapped.

## ![150.png][]  Drop ##

Esto elimina la solicitud o respuesta trapped para que no se transfiera a la aplicación o a tu navegador.
Este botón solo está habilitado cuando una solicitud o respuesta es trapped.

## ![break_add.png][]  Añadir un custom HTTP break point ##

Esto muestra el [Add break point][] diálogo que le permite especificar los criterios para un [break point][punto de ruptura].

## ![equalizer.png][]  Escanear Políticas Manager ##

Muesta la [Scan Policy Manager][] como un diálogo que permite la configuración de [scan policies][].

## ![block.png][]  Complementos Manage ##

Esto muestra los [Manage Add-ons][] diálogos que le permiten descubrir, instalar y actualizar complementos del mercado en línea.
También le permite desinstalar complementos.

## ![forcedUserOff.png][] /  ![forcedUserOn.png][]  Modo de usuario forzado On / Off ##

Esto cambia el modo de usuario forzado on y off.
El botón solo está habilitado cuando ha definido un usuario forzado para al menos un [context][], que se puede hacer a través de [Session Contexts][] dialogo.

Tome en cuenta que [add-ons][] puede agregar botones adicionales.

## Vease también ##

    [ IU ][IU]


<table> 
 <tbody>
  <tr>
   <td>&nbsp;&nbsp;&nbsp;&nbsp;</td>
   <td> <a href="HelpStartStart" rel="nofollow">Empezar</a></td>
   <td>Para detalles de como empezar a usar ZAP</td>
  </tr> 
  <tr>
   <td>&nbsp;&nbsp;&nbsp;&nbsp;</td>
   <td> <a href="HelpUiDialogsDialogs" rel="nofollow">Cuadros de di&aacute;logo</a></td>
   <td>para detalles de los cuadros de di&aacute;logos o popups </td>
  </tr> 
  <tr>
   <td>&nbsp;&nbsp;&nbsp;&nbsp;</td>
   <td> <a href="HelpIntro" rel="nofollow">Introducci&oacute;n</a></td>
   <td>Introducci&oacute;n a ZAP</td>
  </tr> 
 </tbody>
</table>


[modo]: HelpStartConceptsModes
[171.png]: https://github.com/zaproxy/zap-core-help/wiki/images/16/171.png
[Men_ de archivos]: HelpUiTlmenuFile
[047.png]: https://github.com/zaproxy/zap-core-help/wiki/images/16/047.png
[096.png]: https://github.com/zaproxy/zap-core-help/wiki/images/16/096.png
[camera.png]: https://github.com/zaproxy/zap-core-help/wiki/images/fugue/camera.png
[024.png]: https://github.com/zaproxy/zap-core-help/wiki/images/16/024.png
[041.png]: https://github.com/zaproxy/zap-core-help/wiki/images/16/041.png
[Tools menu]: HelpUiTlmenuTools
[ui-tab-show.png]: https://github.com/zaproxy/zap-core-help/wiki/images/fugue/ui-tab-show.png
[ui-tab-hide.png]: https://github.com/zaproxy/zap-core-help/wiki/images/fugue/ui-tab-hide.png
[ui_tab_text.png]: https://github.com/zaproxy/zap-core-help/wiki/images/ui_tab_text.png
[expand_sites.png]: https://github.com/zaproxy/zap-core-help/wiki/images/expand_sites.png
[expand_info.png]: https://github.com/zaproxy/zap-core-help/wiki/images/expand_info.png
[expand_full.png]: https://github.com/zaproxy/zap-core-help/wiki/images/expand_full.png
[layout_tabbed.png]: https://github.com/zaproxy/zap-core-help/wiki/images/layout_tabbed.png
[layout_vertical_split.png]: https://github.com/zaproxy/zap-core-help/wiki/images/layout_vertical_split.png
[layout_horizontal_split.png]: https://github.com/zaproxy/zap-core-help/wiki/images/layout_horizontal_split.png
[152.png]: https://github.com/zaproxy/zap-core-help/wiki/images/16/152.png
[151.png]: https://github.com/zaproxy/zap-core-help/wiki/images/16/151.png
[punto de ruptura]: HelpStartConceptsBreakpoints
[pesta_a de interrupci_n]: HelpUiTabsBreak
[Pantalla de opciones de interrupci_n.]: HelpUiDialogsOptionsBreakpoints
[105.png]: https://github.com/zaproxy/zap-core-help/wiki/images/16/105.png
[105r.png]: https://github.com/zaproxy/zap-core-help/wiki/images/16/105r.png
[106.png]: https://github.com/zaproxy/zap-core-help/wiki/images/16/106.png
[106r.png]: https://github.com/zaproxy/zap-core-help/wiki/images/16/106r.png
[143.png]: https://github.com/zaproxy/zap-core-help/wiki/images/16/143.png
[131.png]: https://github.com/zaproxy/zap-core-help/wiki/images/16/131.png
[150.png]: https://github.com/zaproxy/zap-core-help/wiki/images/16/150.png
[break_add.png]: https://github.com/zaproxy/zap-core-help/wiki/images/16/break_add.png
[Add break point]: HelpUiDialogsAddbreak
[equalizer.png]: https://github.com/zaproxy/zap-core-help/wiki/images/fugue/equalizer.png
[Scan Policy Manager]: HelpUiDialogsScanpolicymgr
[scan policies]: HelpStartConceptsScanpolicy
[block.png]: https://github.com/zaproxy/zap-core-help/wiki/images/fugue/block.png
[Manage Add-ons]: HelpUiDialogsManageaddons
[forcedUserOff.png]: https://github.com/zaproxy/zap-core-help/wiki/images/fugue/forcedUserOff.png
[forcedUserOn.png]: https://github.com/zaproxy/zap-core-help/wiki/images/fugue/forcedUserOn.png
[context]: HelpStartConceptsContexts
[Session Contexts]: HelpUiDialogsSessionContexts
[add-ons]: HelpStartConceptsAddons
[IU]: HelpUiOverview