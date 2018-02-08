# Opciones Database screen #

Esta pantalla le permite configurar las opciones de alertas:

### Compacto (en la salida) ###

Te permite compactar la base de datos cuando ZAP esté cerrado; compactar la base de datos asegura un uso mínimo de espacio en disco pero también significa que ZAP tardará más en salir.

### Registro de recuperación ###

Controla si el registro de recuperación de la base de datos se encuentra habilitado o no.
Mejora el rendimiento de la base de datos si se deshabilita pero puede ocasionar pérdida de datos si ZAP se cierra abrúptamente.
Nota: la sesión actual no será afectada por cambios, estos tomarán efectos en sesiones nuevas y abiertas.

### El tamaño máximo permitido de la solicitud del cuerpo ###

Permite el mayor tamaño de cuerpo de la petición en bytes que ZAP.

### Tamaño corporal de respuesta máxima ###

Permite el mayor tamaño de cuerpo de la petición en bytes que ZAP.

### Indicar opciones de permanencia en la nueva sesión ###

Si está marcado, entonces [Persist Session dialog][] se mostrará cuando se crea una nueva sesión

### Opción por defecto ###

La opción predeterminada para sesiones nuevas: si el aviso anterior está habilitado, se seleccionará la opción predeterminada.
Si el aviso no está habilitado, esta es la acción que se tomará.

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
   <td> <a href="HelpUiDialogsOptionsOptions" rel="nofollow">Options dialogs</a></td>
   <td>for details of the other Options dialog screens</td>
  </tr> 
 </tbody>
</table>


[Persist Session dialog]: HelpUiDialogsPersistsession