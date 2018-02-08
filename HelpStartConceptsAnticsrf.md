# Tokens anti CSRF #

Los tokens anti CSRF son parámetros (pseudo) aleatorios utilizados para proteger contra ataques de Falsificación de Peticiónes en sitios cruzados.
Sin embargo, dificultan el trabajo de los testers de penetración, especialmente si las fichas son regeneradas cada ves que se pide un formulario.


ZAP detecta anti token CSRF puramente por los nombres de atributos - la lista de nombres de atributos considerados anti token CSRF se configura utilizando la [pantalla de opciones Anti CSRF][].
Cuando ZAP detecta estas fichas registra el valor simbólico y que URL genera el token de.
Otros exploradores, como el [Explorador activo][], con opciones que ZAP regenerar automáticamente las fichas cuando se requiera.

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
   <td> <a href="HelpStartConceptsConcepts" rel="nofollow">Caracteristicas</a></td>
   <td>proporcionado por ZAP</td>
  </tr> 
 </tbody>
</table>


[pantalla de opciones Anti CSRF]: HelpUiDialogsOptionsAnticsrf
[Explorador activo]: HelpStartConceptsAscan