# Pestaña de Análisis Activo #

La pestaña de Análisis Activo permite realizar un [análisis activo][an_lisis activo].

El botón de "Administrador de Políticas de Análisis" ![equalizer.png][] muestra el cuadro de diálogo [Administrador de Políticas de Análisis][Administrador de Pol_ticas de An_lisis] que permite la configuración de [políticas de análisis][pol_ticas de an_lisis].

El botón "Nuevo Análisis" abre el [cuadro de diálogo Análisis Activo][cuadro de di_logo An_lisis Activo] que permite especificar exactamente que debería ser escaneado.

La barra de herramientas proporciona un conjunto de botones que permite iniciar, detener, pausar y reanudar el análisis seleccionado.
Una barra de progreso muestra hasta qué punto el análisis del sitio seleccionado ha progresado.
El valor "Análisis actuales" muestra cuántos análisis están actualmente activos. Al pasar sobre este valor se mostrará una lista de los sitios análizados en un popup.
El botón "Mostrar detalles del progreso del análisis" ![system-monitor.png][] abre el [cuadro de diálogo Progreso del Análisis][cuadro de di_logo Progreso del An_lisis] que permite ver los detalles sobre cuáles reglas se están ejecutando, saltar reglar individuales y ver una gráfica de las respuestas.

## Menú de botón derecho ##

Al hacer click derecho sobre un nodo se abrirá un menú que permitirá:

### Excluir de ###

Este menú tiene los siguientes submenús:

#### Proxy ####

Esto excluirá los nodos seleccionados desde el proxy. Aunque seguirán siendo procesadas mediante ZAP pero no aparecerán en ninguna de las pestañas.
Esto puede utilizarse para ignorar URLs que se sabe que no son relevantes para el sistema que se está actualmente analizando.
Los nodos pueden ser incluidos a través del cuadro de diálogo [Propiedades de la Sesion][] .

#### Escáner ####

Esto evitará que los nodos seleccionados ser analizados activamente.
The nodes can be included again via the [Session Properties][Propiedades de la Sesion] dialog

#### Spider(Araña) ####

Esto evitará que los nodos seleccionados sean rastreados.
The nodes can be included again via the [Session Properties][Propiedades de la Sesion] dialog

### Reenviar... ###

Esto abre el [cuadro de diálogo Reenviar][cuadro de di_logo Reenviar] que permite reenviar la solicitud después de hacer los cambios que desee.

### Nueva alerta... ###

Esto abre el [cuadro de diálogo Agregar Alerta][cuadro de di_logo Agregar Alerta] que permite registrar manualmente una nueva [alerta][] contra esta solicitud.

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
  <tr>
   <td>&nbsp;&nbsp;&nbsp;&nbsp;</td>
   <td> <a href="HelpUiDialogsOptionsAscan" rel="nofollow">Options Active Scan screen</a></td>
   <td>for details of the active scan configuration</td>
  </tr> 
 </tbody>
</table>


[an_lisis activo]: HelpStartConceptsAscan
[equalizer.png]: https://github.com/zaproxy/zap-core-help/wiki/images/fugue/equalizer.png
[Administrador de Pol_ticas de An_lisis]: HelpUiDialogsScanpolicymgr
[pol_ticas de an_lisis]: HelpStartConceptsScanpolicy
[cuadro de di_logo An_lisis Activo]: HelpUiDialogsAdvascan
[system-monitor.png]: https://github.com/zaproxy/zap-core-help/wiki/images/fugue/system-monitor.png
[cuadro de di_logo Progreso del An_lisis]: HelpUiDialogsScanprogress
[Propiedades de la Sesion]: HelpUiDialogsSessionSessprop
[cuadro de di_logo Reenviar]: HelpUiDialogsResend
[cuadro de di_logo Agregar Alerta]: HelpUiDialogsAddalert
[alerta]: HelpStartConceptsAlerts
[Sites tab]: HelpUiTabsSites