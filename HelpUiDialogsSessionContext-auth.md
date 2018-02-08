# Pantalla de autenticación de contexto de sesión #

Este es uno de las [Session Context screens][] que permite administrar la manera en que [Authentication][] se hace para el contexto. Tenga en cuenta que cambiar el método de autenticación después de que se hayan definido los Usuarios causará su eliminación, mientras que los tipos de credenciales de usuario necesitan coincidir con el esquema de autentificación. Después de seleccionar el tipo de método de autenticación, las opciones que necesitan ser configurado dependen del método de autenticación.

#### Autenticación manual ####

No se necesita ninguna configuración para este método de autentificación. Leer [más][m_s]...

#### Autenticación basada en formularios ####

Para configurar este método de autenticación, se debe proporcionar la **login url**, al cual que realiza la solicitud de ingreso, el **request body** (POST data), si es necesario, e identificar los **parameters** utilizados para proporcionar el "nombre de usuario" y la "contraseña". Si no se suministra el cuerpo de solicitud, la solicitud de ingreso se realiza como un HTTP GET, de lo contrario un se utilizará HTTP POST. Las credenciales están ellas mismas configuraras en la [Users][] tab. Leer [more][]...

#### Autenticación HTTP/NTLM ####

Para configurar este método de autenticación, se debe proporcionar el **nombre de host** y el **puerto** del servidor con el cual se hace la autenticación y el **dominio** que se aplica a las credenciales. Las credenciales se configuran en la [Users][] tab. Leer [more][more 1]...

#### Autenticación basada en script ####

Para utilizar este método de autenticación, **primero** se necesita escribir (y guardar) un **Script de Autentificación** utilizando la pestaña **Scripts** (ver los ejemplos y plantillas para este tipo de script en la pestaña Scripts). Luego se necesita suministrar el nombre del script en la lista desplegable. Luego de seleccionar el script, se necesita presionar el botón **Load** , cargando todos los requisitos del script. Cualquier parámetro que se especifique como *required* o *optional* en el script, se mostrará en la interfaz para definirse. Sus valores están disponibles para utilizarse en el script, durante la autenticación, como se ha visto en los ejemplos suministrados para Scripts de autentificación. Asegúrese de que después de hacer cualquier cambio en los parámetros requeridos por el script de autenticación vuelva a cargar el script. De lo contrario, los parámetros mostrados en la interfaz puede que no sean los utilizados durante la autenticación y pueden ocurrir errores. Las *credentials* utilizadas por cada usuario durante la proceso de autenticación también puede ser especificada en el Script de autentificación y ser configuradas en la pestaña [Users][] . Leer [más][m_s 1]...

## Acceso a través de ##

<table> 
 <tbody>
  <tr>
   <td>&nbsp;&nbsp;&nbsp;&nbsp;</td>
   <td> <a href="HelpUiTlmenuFile" rel="nofollow">Top level File menu</a></td>
   <td>'Properties...' menu item</td>
  </tr> 
 </tbody>
</table>

## Vease también ##

<table> 
 <tbody>
  <tr>
   <td>&nbsp;&nbsp;&nbsp;&nbsp;</td>
   <td><a href="HelpUiOverview" rel="nofollow">UI Overview</a></td>
   <td>para tener una visi&oacute;n general de la interfaz de usuario</td>
  </tr> 
  <tr>
   <td>&nbsp;&nbsp;&nbsp;&nbsp;</td>
   <td><a href="HelpUiDialogsDialogs" rel="nofollow">Dialogs</a></td>
   <td>para detalles de los cuadros de di&aacute;logos o popups </td>
  </tr> 
  <tr>
   <td>&nbsp;&nbsp;&nbsp;&nbsp;</td>
   <td><a href="HelpUiDialogsSessionContexts" rel="nofollow">Session Context screens</a></td>
   <td>para m&aacute;s detalles de las otras pantallas de contexto</td>
  </tr> 
  <tr>
   <td>&nbsp;&nbsp;&nbsp;&nbsp;</td>
   <td><a href="HelpStartConceptsAuthentication" rel="nofollow">Authentication</a></td>
   <td>para informaci&oacute;n general de la autenticaci&oacute;n </td>
  </tr> 
 </tbody>
</table>


[Session Context screens]: HelpUiDialogsSessionContexts
[Authentication]: HelpStartConceptsAuthentication
[m_s]: HelpStartConceptsAuthentication#manual
[Users]: HelpUiDialogsSessionContexts#users
[more]: HelpStartConceptsAuthentication#formBased
[more 1]: HelpStartConceptsAuthentication#httpAuth
[m_s 1]: HelpStartConceptsAuthentication#scriptBased