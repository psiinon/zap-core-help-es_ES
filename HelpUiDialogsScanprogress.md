# Exploración De Diálogo De Progreso #

Esto muestra el estado de un [active scan][].


### Progress tab ###

This shows which scan rules are running for each host being scanned, as well as other details such as the elapsed time they have been running and the number of requests made per rule.
También le permite saltarse la regla de que, actualmente, se ejecuta haciendo clic sobre el 'Saltar actual se ejecuta active scan' botón ![137.png][] in the Status column.

### Response Chart tab ###

Esto muestra el número de respuestas por segundo recibidos por ZAP, mientras que activa el escaneo de un sitio.
Las respuestas están en los mapas por 'estado de respuesta HTTP de código de grupo":

 *  1xx Informational
 *  2xx Success
 *  3xx Redirection
 *  4xx Client Error
 *  5xx Server Error

Se puede acercar al seleccionar una zona de la gráfica con el ratón.
También puedes hacer clic derecho en el gráfico para obtener más opciones.
Las barras verticales indican aproximadamente cuando cada escaneo regla se inicia (es muy difícil, para ser exactos).
El gráfico sólo se actualizan al mismo tiempo abierto, si cierra y vuelve a abrir el gráfico a continuación, los datos anteriores se perderán.
Por defecto, el tiempo máximo de la carta de cubierta es de 10 minutos, usted puede cambiar esto a través de la [Opciones de la Exploración Activa de la pantalla][Opciones de la Exploraci_n Activa de la pantalla].

## Accessed via ##

<table> 
 <tbody>
  <tr>
   <td>&nbsp;&nbsp;&nbsp;&nbsp;</td>
   <td><a href="HelpUiTabsAscan" rel="nofollow">Active Scan tab</a></td>
   <td></td>
  </tr> 
 </tbody>
</table>

## See also ##

<table> 
 <tbody>
  <tr>
   <td>&nbsp;&nbsp;&nbsp;&nbsp;</td>
   <td> <a href="HelpUiOverview" rel="nofollow">UI Overview</a></td>
   <td>para una visi&oacute;n general de la interfaz de usuario</td>
  </tr> 
  <tr>
   <td>&nbsp;&nbsp;&nbsp;&nbsp;</td>
   <td> <a href="HelpUiDialogsDialogs" rel="nofollow">Dialogs</a></td>
   <td>for details of the dialogs or popups </td>
  </tr> 
 </tbody>
</table>

## External Links ##

<table> 
 <tbody>
  <tr>
   <td>&nbsp;&nbsp;&nbsp;&nbsp;</td>
   <td><a href="https://en.wikipedia.org/wiki/List_of_HTTP_status_codes" rel="nofollow">https://en.wikipedia.org/wiki/List_of_HTTP_status_codes</a></td>
   <td></td>
  </tr> 
 </tbody>
</table>


[active scan]: HelpStartConceptsAscan
[137.png]: https://github.com/zaproxy/zap-core-help/wiki/images/10/137.png
[Opciones de la Exploraci_n Activa de la pantalla]: HelpUiDialogsOptionsAscan