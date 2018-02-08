# Options Extensions screen #

Esta pantalla te permite habilitar/deshabilitar extensiones disponibles en ZAP, bien sea incluidas en el núcleo o agregadas por [complementos][].

### Habilitar/Deshabilitar Extensiones ###

Las extensiones habilitadas serán cargadas por ZAP, agregando las funcionalidades de estas extensiones. Las extensiones deshabilitadas no se cargarán.

### Core Extensions ###

Core extensions are extensions that if disabled will impair ZAP's minimal functionality. Extensions marked as core cannot be disabled.

*Note: Core extensions can be disabled through the configuration file, although it's not recommend.*

### Dependencias de Extensiones ###

Las extensiones pueden depender de otras extensiones para trabajar. Cuando algunas de estas extensiones (dependencias) se deshabilita, ZAP deshabilitará automáticamente todas las extensiones que dependen de ella. Así que es posible que al deshabilitar una extensión otras extensiones (que dependen de ella) también sean deshabilitadas. Las extensiones deshabilitadas automáticamente no se podrán habilitar hasta que todas las dependencias se habiliten.

*Nota: Deberás reiniciar ZAP para que los cambios tengan efecto.*

## Vease también ##

<table> 
 <tbody>
  <tr> 
   <td>&nbsp;&nbsp;&nbsp;&nbsp;</td> 
   <td><a href="HelpUiOverview" rel="nofollow">UI Overview</a></td> 
   <td>Para una vista general sobre la interfaz de usuario</td> 
  </tr> 
  <tr> 
   <td>&nbsp;&nbsp;&nbsp;&nbsp;</td> 
   <td><a href="HelpUiDialogsOptionsOptions" rel="nofollow">Options dialogs</a></td> 
   <td>for details of the other Options dialog screens</td> 
  </tr> 
 </tbody>
</table>


[complementos]: HelpStartConceptsAddons