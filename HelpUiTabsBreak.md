# Pestaña de interrupción #

La pestaña de interrupción permite cambiar una solicitud o respuesta cuando ha sido capturado por ZAP a través del [punto de interrupción][punto de interrupci_n].
Permite cambiar los elementos que normalmente no se pueden cambiar a través el navegador, incluyendo:

<table> 
 <tbody>
  <tr>
   <td>&nbsp;&nbsp;&nbsp;&nbsp;</td> 
   <td>El encabezado</td>
  </tr> 
  <tr>
   <td>&nbsp;&nbsp;&nbsp;&nbsp;</td> 
   <td>Campos ocultos</td>
  </tr> 
  <tr>
   <td>&nbsp;&nbsp;&nbsp;&nbsp;</td> 
   <td>Campos deshabilitados</td>
  </tr> 
  <tr>
   <td>&nbsp;&nbsp;&nbsp;&nbsp;</td> 
   <td>Campos que utilizan javascript para filtrar caracteres ilegales</td>
  </tr> 
 </tbody>
</table>

Esta funcionalidad es clave para poner a prueba la aplicación.

Los dos paneles solo contendrán algo si ZAP captura una solicitud o una respuesta.
Se puede cambiar cualquier cosa en estos dos paneles y luego reenviar la solicitud o respuesta utilizando los botones en la [Barra de herramientas de nivel superior][].

Los pull downs permiten seleccionar diferentes [vistas][] para el encabezado y cuerpo de la solicitud o respuesta.

Cuando la pestaña de Interrupción no está en uso su icono es una cruz gris:   ![101grey.png][] .
Cuando se presiona un [punto de interrupción][punto de interrupci_n] la pestaña cambia a una cruz roja:  ![101.png][] .


## Menú de botón derecho ##

Al hacer clic derecho sobre un nodo se abrirá un menú que permitirá:

### Buscar... ###

This will bring up the [Find dialog][].

### Codificar/Descodificar/Hash... ###

This will bring up the [Encode/Decode/Hash dialog][Encode_Decode_Hash dialog].
If you have highlighted any text then this will be automatically included in the dialog.

### Copiar ###

This will copy the selected string to the clipboard.

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
   <td> <a href="HelpUiTabsBreakpoints" rel="nofollow">Break Points tab</a></td>
   <td>for details of how to change or delete break points</td>
  </tr> 
 </tbody>
</table>


[punto de interrupci_n]: HelpStartConceptsBreakpoints
[Barra de herramientas de nivel superior]: HelpUiTltoolbar
[vistas]: HelpUiViews
[101grey.png]: https://github.com/zaproxy/zap-core-help/wiki/images/16/101grey.png
[101.png]: https://github.com/zaproxy/zap-core-help/wiki/images/16/101.png
[Find dialog]: HelpUiDialogsFind
[Encode_Decode_Hash dialog]: HelpUiDialogsEnc_dec