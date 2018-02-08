# Pantalla de opciones JVM #

Esta pantalla te permite configurar las opciones JMV usadas al empezar en ZAP.

### Opciones de JMV ###

Un formato libre de texto que será añadido a la línea de comando de llamada de Java cuando se invoque ZAP, bien sea por vía zap.sh o zap.bat.

La opción fue añadida para que el tamaño máximo del grupo de asignación de la memoria pueda ser establecido, el cuál es de la forma: -Xmx*n* dónde *n* representa el tamaño en bytes.
Buenos valores en este campo podrían ser:

 *  \-Xmx256m
 *  \-Xmx512m
 *  \-Xmx1024m

A diferencia de otras opciones de ZAP, estas ocurren en el archivo ".ZAP\_JVM.properties" en el directorio ZAP predeterminado del usuario, el cual depende del Sistema Operativo que se utiliza:

 *  Windows 7/8: C:\\Users\\*<username>*\\OWASP ZAP
 *  Windows XP: C:\\Documents and Settings\\*<username>*\\OWASP ZAP
 *  Linux: ~/.ZAP
 *  Sistema Operativo Mac: ~/Library/Application Support/ZAP

Si usted cometiese un error mientras se configuran estas opciones, entonces, ZAP podría fallas al iniciar.
Si eso ocurre, borrando este archivo se debe solucionar el problema.

Notese que estas opciones so son empleadas al iniciar ZAP desde Windows exe.

## Vease también ##

<table> 
 <tbody>
  <tr>
   <td>&nbsp;&nbsp;&nbsp;&nbsp;</td>
   <td><a href="HelpUiOverview" rel="nofollow">Resumen de la interfaz de usuario</a></td>
   <td>para una vista general de la interfaz de usuario</td>
  </tr> 
  <tr>
   <td>&nbsp;&nbsp;&nbsp;&nbsp;</td>
   <td><a href="HelpUiDialogsOptionsOptions" rel="nofollow">Opciones de dialogo</a></td>
   <td>para m&aacute;s detalles de otras pantallas de opciones de di&aacute;logos</td>
  </tr> 
 </tbody>
</table>

## Enlaces externos ##

<table> 
 <tbody>
  <tr>
   <td>&nbsp;&nbsp;&nbsp;&nbsp;</td>
   <td><a href="https://docs.oracle.com/javase/8/docs/technotes/tools/windows/java.html#BABDJJFI" rel="nofollow">Opciones de Java 8</a></td>
  </tr> 
 </tbody>
</table>