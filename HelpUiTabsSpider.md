# Spider tab #

La Araña ficha muestra el conjunto de la única Uri encontrado por la [Araña][Ara_a] durante el análisis.

El Nuevo 'Scan' botón, se abre la [Araña de diálogo][Ara_a de di_logo], que permite para especificar exactamente lo que deben ser analizados.
La Araña se puede ejecutar en varios Sitios en paralelo y los resultados de cada análisis son se muestra mediante la selección de la exploración a través de la 'Progreso' pull-down.

La barra de herramientas muestra información acerca de un análisis y permite el control del mismo. Proporciona un conjunto de botones que permiten:

 *  ![botón de pausa][bot_n de pausa] Pausa (y ![botón de reanudar][bot_n de reanudar] reanudar) la seleccionado araña de exploración;
 *  ![botón de parar][bot_n de parar] Parada el seleccionado de la araña de exploración;
 *  ![borrar botón de escaneo][borrar bot_n de escaneo] Borrar escaneos completados;
 *  ![mostrar mensajes de botón][mostrar mensajes de bot_n] Mostrar/Ocultar Mensajes - muestra/oculta una ficha (llamados Mensajes) que muestra todos los HTTP los mensajes enviados por el seleccionado de la araña de exploración;
 *  ![araña botón de opciones][ara_a bot_n de opciones] Open the [Spider Options screen][].

La barra de progreso muestra el seleccionado de araña de escaneo ha progresado. También se muestra el número de activos de la araña exploraciones y el número de URIs encontrado para el escaneo seleccionada.

Para cada URI encontrado se puede ver:

 *  Procesado - Si la URI a la que fue procesado por la Araña o se ha omitido de recuperación debido a una regla (por ejemplo, estaba fuera de ámbito de aplicación)
 *  Método - El método HTTP, ejemplo. OBTENER o POSTEAR, a través del cual el debe accederse al recurso
 *  URI - el recurso encontrado
 *  Banderas - cualquier información acerca de la URI (por ejemplo, si es una semilla o por qué no fue procesado)

Para cada araña mensaje, que se muestra en la ficha Mensajes, usted puede ver los detalles de la solicitud y de respuesta recibió, además, es el indicado, en la columna `Procesado`, ya sea o no que el mensaje fue procesado (es decir, la respuesta fue recibida con éxito y se analiza).

## Véase también ##

<table> 
 <tbody>
  <tr> 
   <td>&nbsp;&nbsp;&nbsp;&nbsp;</td> 
   <td><a href="HelpUiOverview" rel="nofollow">Resumen de UI</a></td> 
   <td>para una visi&oacute;n general de la interfaz de usuario</td> 
  </tr> 
  <tr> 
   <td>&nbsp;&nbsp;&nbsp;&nbsp;</td> 
   <td><a href="HelpStartConceptsSpider" rel="nofollow">Spider</a></td> 
   <td>para una visi&oacute;n general de la Ara&ntilde;a</td> 
  </tr> 
  <tr> 
   <td>&nbsp;&nbsp;&nbsp;&nbsp;</td> 
   <td><a href="HelpUiDialogsOptionsSpider" rel="nofollow">Pantalla de opciones de spider</a></td> 
   <td>para una vista general de las opciones de spider</td> 
  </tr> 
 </tbody>
</table>


[Ara_a]: HelpStartConceptsSpider
[Ara_a de di_logo]: HelpUiDialogsSpider
[bot_n de pausa]: https://github.com/zaproxy/zap-core-help/wiki/images/16/141.png
[bot_n de reanudar]: https://github.com/zaproxy/zap-core-help/wiki/images/16/131.png
[bot_n de parar]: https://github.com/zaproxy/zap-core-help/wiki/images/16/142.png
[borrar bot_n de escaneo]: https://github.com/zaproxy/zap-core-help/wiki/images/fugue/broom.png
[mostrar mensajes de bot_n]: https://github.com/zaproxy/zap-core-help/wiki/images/16/178.png
[ara_a bot_n de opciones]: https://github.com/zaproxy/zap-core-help/wiki/images/16/041.png
[Spider Options screen]: HelpUiDialogsOptionsSpider