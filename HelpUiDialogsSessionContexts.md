# Pantallas de Contexto de Sesión #

Estas pantallas le permiten controlar [contextos][].

Hay un conjunto de pantallas para cada contexto que defina.

### Pantalla superior ###

Esto te permite escoger el nombre y descripción de contexto.

### Incluir en el contexto ###

Esto le permite administrar las direcciones URL que serán incluidas en el contexto.
Las direcciones URL que no coincidan con ninguna de las expresiones regulares, no serán incluidas en el contexto.

### Excluir del contexto ###

Esto te permite manejar las direcciones URL que serán excluidas del contexto.
Sólo necesitará especificar regexs para direcciones URL que no desea incluir pero que coinciden con una o más de los regexes 'incluir'.

### Estructura ###

See the [Session Context Structure screen][].

### Tecnología ###

Esto te permite especificar las tecnologías usadas en el contexto, en caso de que se conozcan.
Por defecto, todas las tecnologías están incluidas.
Si excluye tecnologías que sabe que no se utilizan, entonces esto puede acelerar [el escaneo activo][] como normas específicas para las tecnologías excluidas pueden ser saltadas.

### Autenticación ###

Ver la [Session Context Authentication screen][].

### Manejo de sesiones ###

Esto te permite administrar la manera en la que el Control de Sesiones se está haciendo para el Contexto. Luego de seleccionar el tipo de Método de Control de Sesión, las opciones que necesitan ser configuradas dependen del Método de Manejo de Sesión.

#### Administración de sesiones basada en cookies ####

No se necesita ninguna configuración para este método de control de sesión. Read [more][]...

#### Control de Sesión de Autenticación de HTTP ####

No se necesita ninguna configuración para este método de control de sesión. Read [more][more 1]...

### Usuarios ###

Esto te permite configurar un conjunto de Usuarios que pueden ser utilizados para diversas acciones a lo largo de la aplicación.

La sección de credenciales del Usuario depende del Método de Autenticación configurado para el Contexto.

## URL regexs ##

En el *Incluir en \**, *Excluir de \** panels and the *Indicadores de inicio/cierre de sesión* of the *Autenticación* panel, you can enter regular expressions to define excluded URLs. While you can escape a single meta-character with a backslash, you can also use the **\\Q...\\E** escape sequence. All the characters between the **\\Q** y el **\\E** se interpretan como caracteres literales. Por ejemplo, \\Q\*\\d+\*\\E es asignado al texto literal \*\\d+\*. Esta secuencia de escape se utiliza en ZAP cuando excludes URLs a través de algunos menús de contexto.
**Nota:** Si tu URL contiene un "\\E" entonces debes seguir los siguientes pasos al utilizar la **\\Q...\\E** secuencia de escape:

 *  Abre la secuencia de escape
 *  Cierra la secuencia de escape antes del "caracter" \\E
 *  Escape the backslash
 *  Open after the "\\E" another escape sequence;
 *  Cierra la secuencia de escape como normalmente lo harías.


Por ejemplo: subdomain.example.com/path?a=**\\E**&moredata=2 debe aparecer como *\\Qsubdomain.example.com/path?a=\\E***\\\\E***\\Q&moredata=2\\E*

## Acceso vía ##

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
   <td> <a href="HelpUiOverview" rel="nofollow">UI Overview</a></td>
   <td>Para una vista general sobre la interfaz de usuario</td>
  </tr> 
  <tr>
   <td>&nbsp;&nbsp;&nbsp;&nbsp;</td>
   <td> <a href="HelpUiDialogsDialogs" rel="nofollow">Cuadros de di&aacute;logo</a></td>
   <td>para detalles de los cuadros de di&aacute;logos o popups </td>
  </tr> 
  <tr>
   <td>&nbsp;&nbsp;&nbsp;&nbsp;</td>
   <td> <a href="HelpStartConceptsAuthentication" rel="nofollow">Autenticaci&oacute;n</a></td>
   <td>para un resumen de Autenticaci&oacute;n </td>
  </tr> 
  <tr>
   <td>&nbsp;&nbsp;&nbsp;&nbsp;</td>
   <td> <a href="HelpStartConceptsSessionManagement" rel="nofollow">Control de Sesiones</a></td>
   <td>for an overview of Session Management </td>
  </tr> 
 </tbody>
</table>


[contextos]: HelpStartConceptsContexts
[Session Context Structure screen]: HelpUiDialogsSessionContext-struct
[el escaneo activo]: HelpStartConceptsAscan
[Session Context Authentication screen]: HelpUiDialogsSessionContext-auth
[more]: HelpStartConceptsSessionManagement#cbsm
[more 1]: HelpStartConceptsSessionManagement#hasm