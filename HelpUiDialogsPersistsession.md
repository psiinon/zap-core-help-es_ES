# Persist Session dialog #

Este cuadro de diálogo se muestra de forma predeterminada cuando se inicia una nueva sesión, la que siempre sucede cuando ZAP comienza.
Le permite especificar cómo desea que esta sesión persistió, también puede establecer la elección por defecto para que no se le pedirá de nuevo.

La persistencia de una sesión de éste será almacenado en una base de datos local que se puede acceder en una fecha posterior.
Usted no necesita mantener 'guardar', una sesión como todo lo que sucede en la sesión que continuamente se registran.
Es mucho más rápido para persistir de una sesión en el inicio, pero siempre puede persistir una sesión más tarde si es necesario.
Si cierra ZAP sin la persistencia de la sesión, a continuación, usted no será capaz de acceder a él de nuevo.

### Sí, quiero conservar esta sesión con el nombre basado en la marca de tiempo actual ###

Eligió esta opción si desea ZAP para almacenar la sesión en el directorio por defecto con un nombre basado en la hora actual.

### Sí, quiero conservar esta sesión pero quiero especificar el nombre y la ubicación ###

Eligió esta opción si desea especificar exactamente donde ZAP debe almacenar la sesión.

### No, no quiero persistir en esta sesión en este momento en el tiempo ###

Eligió esta opción si no desea ZAP para almacenar la sesión.
Usted puede optar por guardarlo en un momento posterior mediante la [Persist Session...][] menu item.

### Remember my choice and do not ask me again. ###

Check this box if you want ZAP to remember your decision and not prompt you again.
You can change your decision via the [Options database][] screen.

## See also ##

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


[Persist Session...]: HelpUiTlmenuFile
[Options database]: HelpUiDialogsOptionsDatabase