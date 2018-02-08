# Versión 1.2.0 #

Se hicieron los siguientes cambios en esta versión:

## Cambios significativos: ##

### Pérdida de memoria ###

Pérdidas de memoria se han corregido en el [escaneo activo][] y en la [spider][].

### invocar aplicaciones ###

Ahora se pueden invocar aplicaciones externas desde las pestañas Sitios e Historias.

### Escaneo Pasivo ###

Se mostrará la [Escaneo Pasivo][] ahora busca las vulnerabilidades, tales como:

<table> 
 <tbody>
  <tr>
   <td>&nbsp;&nbsp;&nbsp;&nbsp;</td>
   <td>Autocompletar formularios con campos de contrase&ntilde;a</td>
  </tr> 
  <tr>
   <td>&nbsp;&nbsp;&nbsp;&nbsp;</td>
   <td>Galletas sin la bandera de &quot;HttpOnly&quot;</td>
  </tr> 
  <tr>
   <td>&nbsp;&nbsp;&nbsp;&nbsp;</td>
   <td>Galletas de SSL sin la bandera 'segura'</td>
  </tr> 
  <tr>
   <td>&nbsp;&nbsp;&nbsp;&nbsp;</td>
   <td>Autenticaci&oacute;n local</td>
  </tr> 
 </tbody>
</table>

## Cambios menores: ##

### Mis informes ###

Un nuevo elemento de menú "Generar XML informe..." está incluido ahora en el nivel superior [Reportes][] menú.

### Manual cuadros de diálogo Editor de solicitar y enviar ###

Las solicitudes presentadas por los [Editor Manual de Peticiones][] y en la [Reenviar][] cuadros de diálogo aparecen ahora en la [Sitios][] y en la [Historia][] pestañas.
Tire un 'Método' nueva le permite cambiar entre los métodos HTTP, éste mueve automáticamente parámetros entre la URL y el cuerpo cuando un método POST es seleccionado o deseleccionado.

### Alertas de interfaz de usuario ###

Se mostrará la [Sitios][] ficha ahora muestra cualquier alerta como banderas a la derecha de los nombres de nodo.
La alerta se cuenta la [pie][] ahora muestran el número de diferentes tipos de alertas, más que el número total de casos.

### Opción de retardo activa escáner ###

El retardo en milisegundos entre cada uno [escaneo activo][] solicitud puede establecerse a través de la [Pantalla de opciones de escaneo activo][]. Esto aumentará el tiempo que lleva de una exploración activa pero reducirá la carga en el destino.

### Cambios ###

Se mostrará la [Sitios][] ficha ahora toma todo el lado izquierdo - esto puede cambiar nuevamente el [Pantalla de opciones][Pantalla de opciones de escaneo activo] es necesaria

La barra de herramientas en el [Petición][Petici_n], [Respuesta][] y en la [Punto de interrupción][Punto de interrupci_n] fichas y el [Editor Manual de Peticiones][] y en la [Reenviar][] cuadros de diálogo es ahora en la parte superior en lugar de la parte inferior.

La alerta se cuenta la [pie][] ahora se muestran en el lado derecho.



## Vease también ##

<table> 
 <tbody>
  <tr>
   <td>&nbsp;&nbsp;&nbsp;&nbsp;</td>
   <td> <a href="HelpIntro" rel="nofollow">Introducci&oacute;n</a></td>
   <td>Introducci&oacute;n a ZAP</td>
  </tr> 
  <tr>
   <td>&nbsp;&nbsp;&nbsp;&nbsp;</td>
   <td> <a href="HelpReleasesReleases" rel="nofollow">Lanzamientos</a></td>
   <td>el conjunto completo de los comunicados de</td>
  </tr> 
  <tr>
   <td>&nbsp;&nbsp;&nbsp;&nbsp;</td>
   <td> <a href="HelpCredits" rel="nofollow">Cr&eacute;ditos</a></td>
   <td>las personas y grupos que han hecho posible esta versi&oacute;n</td>
  </tr> 
 </tbody>
</table>


[escaneo activo]: HelpStartConceptsAscan
[spider]: HelpStartConceptsSpider
[Escaneo Pasivo]: HelpStartConceptsPscan
[Reportes]: HelpUiTlmenuReport
[Editor Manual de Peticiones]: HelpUiDialogsMan_req
[Reenviar]: HelpUiDialogsResend
[Sitios]: HelpUiTabsSites
[Historia]: HelpUiTabsHistory
[pie]: HelpUiFooter
[Pantalla de opciones de escaneo activo]: HelpUiDialogsOptionsAscan
[Petici_n]: HelpUiTabsRequest
[Respuesta]: HelpUiTabsResponse
[Punto de interrupci_n]: HelpUiTabsBreak