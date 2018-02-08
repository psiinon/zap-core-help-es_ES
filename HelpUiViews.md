# Vistas #

ZAP proporciona un conjunto de vistas que se conectan que permite mostrar las solicitudes y respuestas de diferente manera.
Las siguientes vistas se incluyen por defecto:

<table> 
 <tbody>
  <tr>
   <td>&nbsp;&nbsp;&nbsp;&nbsp;</td>
   <td>Texto</td>
   <td>La informaci&oacute;n en formato de texto</td>
  </tr> 
  <tr>
   <td>&nbsp;&nbsp;&nbsp;&nbsp;</td>
   <td>Hex</td>
   <td>Una tabla que muestra la representaci&oacute;n hex de todos los caracteres en el encabezado y el cuerpo. <br />Esto permite para pantallas editables a&ntilde;adir caracteres de control mediante sus c&oacute;digos hex.<br /> No se puede a&ntilde;adir o eliminar caracteres en esta vista. Para hacerlo, cambie a otra vista y luego vuelva a la vista hex para continuar.</td>
  </tr> 
  <tr>
   <td>&nbsp;&nbsp;&nbsp;&nbsp;</td>
   <td>Imagen</td>
   <td>La imagen, solo disponible para cuerpos que contienen im&aacute;genes</td>
  </tr> 
  <tr>
   <td>&nbsp;&nbsp;&nbsp;&nbsp;</td>
   <td>Tabla</td>
   <td>Una tabla con una fila por atributo y valor.<br /> Para pantallas editables todos los valores se codificar&aacute;n en URL autom&aacute;ticamente cuando se env&iacute;en. </td>
  </tr> 
  <tr>
   <td>&nbsp;&nbsp;&nbsp;&nbsp;</td>
   <td>Tabla (adv)</td>
   <td>Una tabla con una fila por atributo y valor m&aacute;s las funciones adicionales.<br /> Para pantallas editables los valores no se codificar&aacute;n autom&aacute;ticamente en URL cuando se env&iacute;en, pero esto se puede hacer &quot;manualmente&quot; a trav&eacute;s de la funci&oacute;n &quot;URLEncode&quot;. </td>
  </tr> 
  <tr>
   <td>&nbsp;&nbsp;&nbsp;&nbsp;</td>
   <td>Solicitud Grande</td>
   <td>Una vista de marcador de posici&oacute;n se utiliza para evitar que la IU intente cargar un cuerpo de solicitud muy grande.<br /> Se necesita cambiar a una vista diferente para mostrar los contenidos actuales.<br /> El umbral para la vista puede cambiarse a trav&eacute;s de la <a href="HelpUiDialogsOptionsView" rel="nofollow">pantalla Mostrar Opciones</a></td>
  </tr> 
  <tr>
   <td>&nbsp;&nbsp;&nbsp;&nbsp;</td>
   <td>Respuesta Grande</td>
   <td>Una vista de marcador de posici&oacute;n se utiliza para evitar que la IU intente cargar un cuerpo de respuesta muy grande.<br /> Se necesita cambiar a una vista diferente para mostrar los contenidos actuales.<br /> El umbral para la vista puede cambiarse a trav&eacute;s de la <a href="HelpUiDialogsOptionsView" rel="nofollow">pantalla Mostrar Opciones</a></td>
  </tr> 
 </tbody>
</table>

Tome en cuenta que [add-ons][] puede agregar vistas adicionales.

## Utilizado en ##

<table> 
 <tbody>
  <tr>
   <td>&nbsp;&nbsp;&nbsp;&nbsp;</td>
   <td><a href="HelpUiTabsBreak" rel="nofollow">Pesta&ntilde;a de interrupci&oacute;n</a></td>
   <td></td>
  </tr> 
  <tr>
   <td>&nbsp;&nbsp;&nbsp;&nbsp;</td>
   <td><a href="HelpUiTabsRequest" rel="nofollow">Pesta&ntilde;a de solicitud</a></td>
   <td></td>
  </tr> 
  <tr>
   <td>&nbsp;&nbsp;&nbsp;&nbsp;</td>
   <td><a href="HelpUiTabsResponse" rel="nofollow">Pesta&ntilde;a Respuesta</a></td>
   <td></td>
  </tr> 
  <tr>
   <td>&nbsp;&nbsp;&nbsp;&nbsp;</td>
   <td><a href="HelpUiDialogsMan_req" rel="nofollow">Manual Request dialog</a></td>
   <td></td>
  </tr> 
  <tr>
   <td>&nbsp;&nbsp;&nbsp;&nbsp;</td>
   <td><a href="HelpUiDialogsResend" rel="nofollow">Cuadro de di&aacute;logo Reenviar</a></td>
   <td></td>
  </tr> 
 </tbody>
</table>

## Véase también ##

<table> 
 <tbody>
  <tr>
   <td>&nbsp;&nbsp;&nbsp;&nbsp;</td>
   <td><a href="HelpUiOverview" rel="nofollow">UI Overview</a></td>
   <td>for an overview of the user interface</td>
  </tr> 
 </tbody>
</table>


[add-ons]: HelpStartConceptsAddons