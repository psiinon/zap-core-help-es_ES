# Params tab #

Esto muestra un resumen de los parámetros y los campos de respuestas de cabecera que utiliza un sitio.

Los sitios pueden seleccionarse a través de la barra de herramientas o de la [Sitios tab][].

Por cada parámetro se puede ver:

<table> 
 <tbody>
  <tr>
   <td>&nbsp;&nbsp;&nbsp;&nbsp;</td> 
   <td>El tipo - cookie, form, URL, o encabezado</td>
  </tr> 
  <tr>
   <td>&nbsp;&nbsp;&nbsp;&nbsp;</td> 
   <td>El nombre del par&aacute;metro (o encabezado de respuesta)</td>
  </tr> 
  <tr>
   <td>&nbsp;&nbsp;&nbsp;&nbsp;</td> 
   <td>El n&uacute;mero de veces que ha sido utilizado</td>
  </tr> 
  <tr>
   <td>&nbsp;&nbsp;&nbsp;&nbsp;</td> 
   <td>El n&uacute;mero de valores &uacute;nicos</td>
  </tr> 
  <tr>
   <td>&nbsp;&nbsp;&nbsp;&nbsp;</td> 
   <td>El cambio de porcentaje, donde 0 significa solo un valor ha sido utilizado y 100 significa que todos los valores son &uacute;nicos</td>
  </tr> 
  <tr>
   <td>&nbsp;&nbsp;&nbsp;&nbsp;</td> 
   <td>Los indicadores - incluyen indicadores de cookies y anticsrf y sesi&oacute;n</td>
  </tr> 
  <tr>
   <td>&nbsp;&nbsp;&nbsp;&nbsp;</td> 
   <td>Alguno de los valores - el conjunto completo de valores puede no ser visible del todo</td>
  </tr> 
 </tbody>
</table>

## Menú de botón derecho ##

Al hacer click derecho sobre un nodo se abrirá un menú que le permitirá:

### Buscar ###

Esto mostrará todos los ejemplos del parámetro seleccionado en la [pestaña Buscar][pesta_a Buscar].

### Flag as Anti CSRF token ###

Esto indicará el parámetro como un [Anti CSRF token][].

### Unflag as Anti CSRF token ###

Esto eliminará el indicador Anti CSRF token del parámetro.


### Flag as Session token ###

Esto marcará el parámetro como un token de sesión para el sito actual y notificará a la herramienta [Sesiones HTTP][] correspondiente.


### Unflag as Session token ###

Esto desmarcará el parámetro como un token de sesión para el sitio actual y notificará la herramienta [Sesiones HTTP][] correspondiente.


## Vease también ##

<table> 
 <tbody>
  <tr>
   <td>&nbsp;&nbsp;&nbsp;&nbsp;</td>
   <td> <a href="HelpUiOverview" rel="nofollow">UI Overview</a></td>
   <td>Para una vista general sobre la interfaz de usuario</td>
  </tr> 
 </tbody>
</table>


[Sitios tab]: HelpUiTabsSites
[pesta_a Buscar]: HelpUiTabsSearch
[Anti CSRF token]: HelpStartConceptsAnticsrf
[Sesiones HTTP]: HelpStartConceptsHttpsessions