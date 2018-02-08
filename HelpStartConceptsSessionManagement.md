# Administrador de sesiones #

ZAP maneja varios tipos de administración de sesiones (llamados  **Métodos de administración de sesiones ) que se pueden usar para sitios web / aplicaciones web. Cada [Context][] tienene un Asministración de Sesiones. Método definido que dicta cómo se guardan las sesiones.** 

Hasta el momento, solo se han implementado los métodos de administración de sesiones de autenticación basada en cookies y HTTP, pero el sistema admite la adición sencilla de nuevos métodos, de acuerdo con las necesidades del usuario.

### Administración de sesiones basadas en cookies ###

En el caso de este método, la sesión se rastrea a través de cookies. Actualmente, los tokens de sesión que se utilizan se importan de la extensión [ HTTP Sessions . ][HTTP Sessions .]

[ ][HTTP Sessions .]

###  Gestión de sesión de autenticación de HTTP ###

En el caso de este método, la sesión se administra con un encabezado de solicitud HTTP`Authorization`.

## Configura a través ##

<table> 
 <tbody>
  <tr> 
   <td>&nbsp;&nbsp;&nbsp;&nbsp;</td> 
   <td><a href="HelpUiDialogsSessionContexts#sm" rel="nofollow">Sesi&oacute;n Dialogo contextual</a></td> 
   <td></td> 
  </tr> 
 </tbody>
</table>

## Vease también ##

<table> 
 <tbody>
  <tr> 
   <td>&nbsp;&nbsp;&nbsp;&nbsp;</td> 
   <td><a href="https://youtu.be/cR4gw-cPZOA" rel="nofollow">Tutorial de Youtube</a></td> 
   <td>de la autenticaci&oacute;n, Administraci&oacute;n de Sesiones y caracter&iacute;sticas de administraci&oacute;n de usuarios de ZAP [v&iacute;nculo externo a https://youtu.be/cR4gw-cPZOA].</td> 
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
   <td><a href="HelpUiDialogsSessionContexts" rel="nofollow">Dialogo de contextos de sesi&oacute;n </a></td> 
   <td>para una descripci&oacute;n de las Propiedades de Sesi&oacute;n</td> 
  </tr> 
 </tbody>
</table>


[Context]: HelpStartConceptsContexts
[HTTP Sessions .]: HelpStartConceptsHttpsessions