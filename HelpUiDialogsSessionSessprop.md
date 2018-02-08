# Session Properties dialog #

This allows you to set the session properties and is made up of the following screens:

### General ###

This allows you to set the session name and description.

### Excluir del Proxy ###

Esto te permite administrar las URLs que se ignorarán por los proxies locales.

### Excluir del Escáner ###

Est ote permite administrar las URLs que se ignorarán por el escáner.

### Exclude from Spider ###

This allows you to manage the URLs which will be ignored by the spiders (standard and AJAX).

### Contextos ###

Un conjunto de pantallas para administrar [contexts][]

## URL regexs ##

In the *Exclude from \** dialogs, you can enter regular expressions to define excluded URLs. While you can escape a single meta-character with a backslash, you can also use the **\\Q...\\E** escape sequence. All the characters between the **\\Q** and the **\\E** are interpreted as literal characters. E.g. \\Q\*\\d+\*\\E matches the literal text \*\\d+\*. This escape sequence is used in ZAP when you exclude URLs via some context menus.
**Note:** If your URL contains a "\\E", then you have to do the following steps when using the **\\Q...\\E** escape sequence:

 *  Open the escape sequence
 *  Close the escape sequence before the "character" \\E
 *  Escape the backslash
 *  Open after the "\\E" another escape sequence;
 *  Close the escape sequence as normally would.


Example: subdomain.example.com/path?a=**\\E**&moredata=2 should appear as *\\Qsubdomain.example.com/path?a=\\E***\\\\E***\\Q&moredata=2\\E*

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
 </tbody>
</table>


[contexts]: HelpStartConceptsContexts