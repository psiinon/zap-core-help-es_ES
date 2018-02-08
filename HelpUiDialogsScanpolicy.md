# Scan Policy Dialog #

Esto te permite habilitar y deshabilitar las reglas que corren al realizar un [escaneo activo][].
La primera pantalla te permite definir los niveles por defecto al igual que los niveles para todas las reglas en una categoría en particular.

La pantalla de categoría te permite definir los niveles para cada regla individual.


Nota que las reglas del [escaneo pasivo][] ya no se gestionan por este cuadro de diálogo sino que se administan a traves de las [Opciones de Reglas de Escaneo Pasivo][].

### Umbral ###

Esto controla qué tanto ZAP puede reportar vulnerabilidades potenciales.


 *  Si seleccionas Apagado entonces el escaner no se ejecutará.
 *  Si seleccionas Bajo entonces más problemas potenciales se mostrarán lo que puede aumentar el número de falsos positivos.
 *  Si seleccionas Alto entonces menos problemas potenciales serán generados lo que puede decir que algunos problemas reales sean omitidos (falsos negativos).

### Fuerza ###

Esto controla el número de ataques que ZAP realizará.
Si seleccionas Bajo entonces menos ataques se realizarán lo que será más rápido pero puede omitir algunos problemas.
Si seleccionas Alto entonces más ataques serán realizados lo que puede encontrar más problemas pero tomará más tiempo.
El nivel Extremo solo debe ser usado para partes pequeñas de una aplicación ya que puede resultar en un número extremadamente grande de ataques realizados, lo que puede tomar una longitud considerable de tiempo.

## Acceso vía ##

<table> 
 <tbody>
  <tr>
   <td>&nbsp;&nbsp;&nbsp;&nbsp;</td>
   <td><a href="HelpUiDialogsScanpolicymgr" rel="nofollow">Scan Policy Manager dialog</a></td>
   <td></td>
  </tr> 
 </tbody>
</table>

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
   <td> <a href="HelpUiDialogsDialogs" rel="nofollow">Cuadros de di&aacute;logo</a></td>
   <td>para detalles de los cuadros de di&aacute;logos o popups </td>
  </tr> 
 </tbody>
</table>


[escaneo activo]: HelpStartConceptsAscan
[escaneo pasivo]: HelpStartConceptsPscan
[Opciones de Reglas de Escaneo Pasivo]: HelpUiDialogsOptionsPscanrules