# Añadir Alerta, #

Este diálogo te permite agregar o cambiar manualmente una [Alerta][] asociada a una solicitud específica.


## Campos ##

El diálogo tiene los siguientes campos:

### Tipo ###

El tipo de alerta es un campo desplegable que te permite seleccionar un tipo de problema de un conjunto precompletado.
También puedes introducir tu propio texto o cambiar el texto de alguno de los artículos que has seleccionado.
Si seleccionas uno de los tipos existentes los campos de la Descripción, Solución y Otra Información se rellenarán con el texto asociado al elemento que seleccionaste.

### Riesgo ###

Un campo desplegable que te permite especificar qué tan grave consideras que es el riesgo:

<table> 
 <tbody>
  <tr>
   <td>&nbsp;&nbsp;&nbsp;&nbsp;</td>
   <td>Informativo</td>
   <td></td>
  </tr> 
  <tr>
   <td>&nbsp;&nbsp;&nbsp;&nbsp;</td>
   <td>Bajo</td>
   <td></td>
  </tr> 
  <tr>
   <td>&nbsp;&nbsp;&nbsp;&nbsp;</td>
   <td>Medio</td>
   <td></td>
  </tr> 
  <tr>
   <td>&nbsp;&nbsp;&nbsp;&nbsp;</td>
   <td>Alto</td>
   <td></td>
  </tr> 
 </tbody>
</table>

### Confianza ###

Un campo desplegable que te permite especificar qué tanto confías en la validez del hallazgo:

<table> 
 <tbody>
  <tr>
   <td>&nbsp;&nbsp;&nbsp;&nbsp;</td>
   <td>Falso Positivo</td>
   <td>para problemas potenciales que luego resultan no ser explotables</td>
  </tr> 
  <tr>
   <td>&nbsp;&nbsp;&nbsp;&nbsp;</td>
   <td>Bajo</td>
   <td>para problemas no confirmados</td>
  </tr> 
  <tr>
   <td>&nbsp;&nbsp;&nbsp;&nbsp;</td>
   <td>Medio</td>
   <td>para problemas que son un poco confiables</td>
  </tr> 
  <tr>
   <td>&nbsp;&nbsp;&nbsp;&nbsp;</td>
   <td>Alto</td>
   <td>for findings you are highly confident in</td>
  </tr> 
  <tr>
   <td>&nbsp;&nbsp;&nbsp;&nbsp;</td>
   <td>Confirmado</td>
   <td>para problemas confirmados</td>
  </tr> 
 </tbody>
</table>

### Parámetro ###

Un campo desplegable que te permite especificar a qué parámetro se asocia el problema.
Este campo es prepopulado con los parámetros URL y FORM encontrados, pero también puedes ingresar tu propio nombre para el parámetro.
Los parámetros del arreglo (en el componente de consulta de URL y `el cuerpo de solicitud x-www-form-urlencoded` ) se identifican con su índice. Por ejemplo, para una solicitud que contenga `choices[]=ChoiceA&choices[]=ChoiceB` el primer parámetro sería identificado como `choices[0]` y el segundo como `choices[1]`.

### Descripción ###

Una descripción general del tipo de problema encontrado.
Se rellena cuando se selecciona uno de los tipos predefinidos, pero también se puede cambiar según sea necesario.
Ten en cuenta que cualquier cambio que hagas se perderá si seleccionas otro tipo.

### Otra Información ###

La información específica a un problema particular que se haya encontrado.
Este campo no se rellena previamente.

### Recomendación ###

Las recomendaciones sobre cómo arreglar el problema.
Se rellena cuando se selecciona uno de los tipos predefinidos, pero también se puede cambiar según sea necesario.
Tenga en cuenta que cualquier cambio que se haga se perderá si se selecciona otro tipo.

### Referencia ###

Uno o mas URLs que apunten a mayor informacion en internet sobre el tipo de alerta seleccionado.
Se rellena cuando se selecciona uno de los tipos predefinidos, pero también se puede cambiar según sea necesario.
Ten en cuenta que cualquier cambio que hagas se perderá si seleccionas otro tipo.

## Acceso vía ##

<table> 
 <tbody>
  <tr>
   <td>&nbsp;&nbsp;&nbsp;&nbsp;</td>
   <td> <a href="HelpUiTabsHistory" rel="nofollow">Pesta&ntilde;a Historia</a></td>
   <td>'New Alert...' right click menu item</td>
  </tr> 
  <tr>
   <td>&nbsp;&nbsp;&nbsp;&nbsp;</td>
   <td> <a href="HelpUiTabsAlerts" rel="nofollow">Alerts tab</a></td>
   <td>double clicking on an existing alert</td>
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


[Alerta]: HelpStartConceptsAlerts