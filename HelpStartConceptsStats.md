# Estadísticas #

ZAP mantiene estadísticas que pueden ayudarlo a comprender lo que realmente está sucediendo al interactuar con aplicaciones grandes.

Las estadísticas están disponibles a través de [API][] y también se puede enviar a un servidor de Statsd cuando configurado a través de [Options Statistics screen][].

### Estadísticas basadas en el sitio ###

Estadísticas en base al sitio incluyen:

 *  códigos de respuesta, ej:
    
     *  stats.code.200
     *  stats.code.302
 *  tiempos de respuesta en ms (usando una escala logarítmica), ej:
    
     *  stats.responseTime.1
     *  stats.responseTime.2
     *  stats.responseTime.4
     *  stats.responseTime.8
     *  stats.responseTime.16
 *  tipos de contenido, ej:
    
     *  stats.contentType.text/css
     *  stats.contentType.text/html;charset=utf-8
 *  [etiquetas][], ej:
    
     *  stats.tag.Password
     *  stats.tag.Hidden
 *  piezas anticsrf generadas:
    
     *  stats.acsrf.anticsrf
 *  información de autenticación:
    
     *  stats.auth.success (number of authentication successes)
     *  stats.auth.failure (number of authentication failures)
     *  stats.auth.state.loggedin (number of responses that appear to be logged in)
     *  stats.auth.state.loggedout (number of responses that appear to be logged out)
     *  stats.auth.state.noindicator (number of responses where no logged in or out indicators have been set)
     *  stats.auth.state.unknown (number of responses which don't contain either logged in or out indicators)

## Véase también ##

<table> 
 <tbody>
  <tr>
   <td>&nbsp;&nbsp;&nbsp;&nbsp;</td>
   <td><a href="HelpUiOverview" rel="nofollow">Resumen del UI</a></td>
   <td>Para una vista general sobre la interfaz de usuario</td>
  </tr> 
  <tr>
   <td>&nbsp;&nbsp;&nbsp;&nbsp;</td>
   <td><a href="HelpStartConceptsConcepts" rel="nofollow">Caracteristicas</a></td>
   <td>proporcionado por ZAP</td>
  </tr> 
 </tbody>
</table>


[API]: HelpStartConceptsApi
[Options Statistics screen]: HelpUiDialogsOptionsStats
[etiquetas]: HelpStartConceptsTags