# API #

ZAP proporciona una interfaz de programación de aplicaciones (API) que le permite interactuar mediante programación con ZAP.

La API está disponible en formatos JSON, HTML y XML.
Una web simple que permite explorar y utilizar la API de interfaz de usuario está disponible a través de la URL http://zap/ cuando estés proxy vía ZAP, o mediante el host y el puerto ZAP está escuchando, por ejemplo, [http://localhost: 8080 /][http_localhost_ 8080].


Por defecto sólo la máquina que Zap está ejecutando es capaz de acceder a la API. Puede permitir a otras máquinas, que son capaces de usar el ZAP como un proxy, el acceso a la API. La API está configurada utilizando la [pantalla de opciones de API][].

La API proporciona acceso a la mayoría de la base ZAP características tales como el [Explorador activo][] y [araña][ara_a].
Las versiones futuras de ZAP aumentará la funcionalidad disponible a través de la APi.

## Vease también ##

<table> 
 <tbody>
  <tr>
   <td>&nbsp;&nbsp;&nbsp;&nbsp;</td>
   <td> <a href="HelpUiOverview" rel="nofollow">Resumen de IU</a></td>
   <td>Para una vista general sobre la interfaz de usuario</td>
  </tr> 
  <tr>
   <td>&nbsp;&nbsp;&nbsp;&nbsp;</td>
   <td> <a href="HelpStartConceptsConcepts" rel="nofollow">Caracteristicas</a></td>
   <td>proporcionado por ZAP</td>
  </tr> 
 </tbody>
</table>


[http_localhost_ 8080]: http://localhost:8080/
[pantalla de opciones de API]: HelpUiDialogsOptionsApi
[Explorador activo]: HelpStartConceptsAscan
[ara_a]: HelpStartConceptsSpider