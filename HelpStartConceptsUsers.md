# Usuarios #

Los usuarios son las representaciones de ZAP de los usuarios de sitios web/webapps. Permiten ciertas acciones a realizar desde el punto de vista de un usuario de las webapps. Para cada **[contexto][]**, un conjunto de usuarios puede ser definido, que luego puede ser utilizado en acciones relacionadas con el contexto. Por lo general, durante diversas exploraciones pueden enviarse los mensajes de solicitud desde el punto de vista de un usuario.

El concepto de usuarios está firmemente ligado a los conceptos de [Administración de sesiones][Administraci_n de sesiones] y [autenticación][autenticaci_n]. Cuando un usuario primero se utiliza en algún lugar en ZAP, se realiza una autenticación (según el método de autenticación definido para el contexto) y una sesión es creada y configurada para este usuario (según la sesión de gestión definidos para el contexto). Después de eso, se modifican las solicitudes enviadas desde el punto de vista de un usuario (si es necesario) y de tal manera que el servidor web identifica como enviados por un usuario de la aplicación o sitio web autenticado. Si en cualquier momento un mensaje es enviado desde la perspectiva de un usuario y la respuesta recibida parece no autenticada (como identificado con *Ha iniciado sesión en* y *Conectado a* [indicadores de autenticación][autenticaci_n]), se realiza una autenticación de nuevo y la sesión es actualizado en consecuencia.

Para realizar la autenticación de un usuario de un sitio web o en una aplicación Web, el método de autenticación define cómo realiza la autentificación (el proceso), mientras que las credenciales necesarias (los identificadores exactas) dependen del usuario, así, en ZAP, que son el config medido en los usuarios.

## Configura a través ##

<table> 
 <tbody>
  <tr> 
   <td>&nbsp;&nbsp;&nbsp;&nbsp;</td> 
   <td><a href="HelpUiDialogsSessionContexts#users" rel="nofollow">Session Contexts Dialog</a></td> 
   <td></td> 
  </tr> 
 </tbody>
</table>

## Vease también ##

<table> 
 <tbody>
  <tr> 
   <td>&nbsp;&nbsp;&nbsp;&nbsp;</td> 
   <td><a href="https://youtu.be/cR4gw-cPZOA" rel="nofollow">Tutorial de YouTube</a></td> 
   <td>de las caracter&iacute;sticas de autenticaci&oacute;n, manejo de sesiones y de gesti&oacute;n de usuarios de ZAP [enlace externo a https://youtu.be/cR4gw-cPZOA].</td> 
  </tr> 
  <tr> 
   <td>&nbsp;&nbsp;&nbsp;&nbsp;</td> 
   <td><a href="HelpStartConceptsAuthentication" rel="nofollow">Servicio de Autenticaci&oacute;n</a></td> 
   <td>para un resumen de la autenticaci&oacute;n en ZAP</td> 
  </tr> 
  <tr> 
   <td>&nbsp;&nbsp;&nbsp;&nbsp;</td> 
   <td><a href="HelpUiOverview" rel="nofollow">UI Overview</a></td> 
   <td>Para una vista general sobre la interfaz de usuario</td> 
  </tr> 
  <tr> 
   <td>&nbsp;&nbsp;&nbsp;&nbsp;</td> 
   <td><a href="HelpStartConceptsConcepts" rel="nofollow">Caracteristicas</a></td> 
   <td>proporcionado por ZAP</td> 
  </tr> 
  <tr> 
   <td>&nbsp;&nbsp;&nbsp;&nbsp;</td> 
   <td><a href="HelpUiDialogsSessionContexts" rel="nofollow">Session Contexts Dialog</a></td> 
   <td>para una descripci&oacute;n general de las Propiedades de Sesi&oacute;n</td> 
  </tr> 
 </tbody>
</table>


[contexto]: HelpStartConceptsContexts
[Administraci_n de sesiones]: HelpStartConceptsSessionManagement
[autenticaci_n]: HelpStartConceptsAuthentication