# Pantalla de opciones de Spider #

Esta pantalla le permite configurar ls opciones de [Spider][] .

Cabe señalar que la modificación de la mayoría de estas opciones también afecta a el funcionamiento de Spider.

### Máxima profundidad para rastrear ###

El parámetro define la profundidad máxima en el proceso de rastreo donde un la página debe estar en orden para que sea procesada. Los recursos que se encuentran más profundo que este nivel no se recopila y analiza la Spider.

la profundidad es calculada partiendo de las seeds, así, si una exploración de spider empieza con una única URL (ejemplo: Spider URL), la profundidad es calculado a partir de este. Sin embargo, si el análisis se inicia con múltiples las seeds (por ejemplo. Spider site), un recurso es procesada si la profundidad de en relación a *cualquier* de las seeds es menor que el definido uno.

### Número de threads usados ###

La spider es multi-threaded y este es el número que define la número máximo de subprocesos de trabajo utilizado en el proceso de rastreo. El cambio de este el parámetro no tiene ningún efecto en cualquier rastreo en progreso.

### Máxima duración ###

La longitud máxima de tiempo que la spider se deben ejecutar para, medido en minutos. Cero (por defecto) significa que la spider se va a ejecutar hasta que se ha encontrado a todos los enlaces de que es capaz.

### Máximo de children a rastrear ###

Este parámetro limita el número de children que puede ser rastreado en cada nodo en el árbol.
Esto es útil para aplicaciones conducidas por datos, que tienen un gran número de páginas, las cuales son de hecho el mismo código, pero contienen datos diferentes, por ejemplo, una base de datos.
Por defecto se establece a cero, lo que significa que no hay límites al número de nodos secundarios rastreado.

### Máximo tamaño de análisis ###

Define el máximo tamaño, en bytes, de una respuesta que puede tener que ser analizada. Esto permite a la spider saltar respuestas o archivos grandes.

### Dominios siempre en el alcance ###

Permite administrar los dominios, cadena de literales o expresiones regulares, que están en el alcance de la spider. El comportamiento normal de la spider es el único en seguir los enlaces de recursos encontrados en el mismo dominio que la página donde comenzó la exploración. Sin embargo, esta opción permite definir adicionalmente dominios que son considerados en la mira durante el proces de crawling ". Las páginas en éste dominio son procesadas durante la exploración.

### Manejo de parámetros de computadora ###

Cuando se arrastraba, la spider tiene un sistema mecánico interno que marca las páginas que nosotros visitamos. para que no sean procesadas nuevamente. Cuando el check está marcado, el sentido en que las ULR son manejadas según ésta opción. exísten 3 tipos de opciones disponilbles:

 *   **Ignore los parámetros por completo** si www.example.org/?bar=?456, entonces, el ejemplo www.example.org/?foo=123 no será visitado
 *  **Considere sólo el nombre del parámetro**(ignore valor del parámetro) - si www.example.org/?foo=123 es visitada, entonces www.example.org/?foo=456 no será visitado, pero www.example.org/?bar=789 o www.example.org/?foo=456&bar=123 serán visitados
 *  **Considere ambos parámetros nombre y valor** si www.example.org/?123 es visitado, cualquier otra Url que sea diferente ( incluyendo, por ejmplo, www.example.org/?foo=456 o www.example.org/?bar=abc) serán visitados

### Enviar encabezado "Referencia" ###

Si las solicitudes de spider deben ser enviadas con el encabezado "Referencia".

### Cookies aceptadas ###

Si los escaneos de spider deben aceptar cookies mientras son llevados a cabo. Si se encuentra activa ésta opción la spider manejará correctamente cualquier cookie recibida desde el servidor y las enviará de vuelta en consecuencia. Si la opción se encuentra deshabilitada, la spider no enviará ninguna cookie en sus solicitudes. Por ejemplo, esto podría controlar si la spider usa o nó la misma sesión a través de un escaneo de spider.
Al aceptar las cookies, ellas no son compartidas entre escaneos de spider, cada escaneo tiene su propia jarra para estas.
Esta opción tiene una baja prioridad, la araña respetará las otras opciones (globales) relacionadas al estado de HTTP. Esta opción es ignorada si, por ejemplo, la opción [Habilitar rastreo de sesión (Cookie)][Habilitar rastreo de sesi_n _Cookie] se ecncuentra habilitada, mientras de hace el escaneo de spider como un [Usuario][] o cuando una [Sesión HTTP][Sesi_n HTTP] este activa.

### Formas de Procesos ###

Durante el proceso de arrastre, el comportamiento de la spider cuando se encuentra con formas HTML queda definido por esta opción. Si se encuentra desactivado, los formularios HTML no serán procesados en lo absoluto. De encontrarse habilitado, las formas HTML con los métodos definidos como HTTP GET serán presentados con algunos valores generados. El comportamiento al encontrarse formas con el método definido como HTTP POST es configurado mediante la siguiente opción.

### Formas POST ###

Descrito brevemente en el párrafo anterior (Formas de Procesos), ésta opción configura el comportamiento de la spider cuando *Formas de Procesos* se encuentra habilitado y cuando de encuentre con formas HTML que debden ser publicadas.

### Analizar gramaticalmente comentarios HTML ###

Esta opción define si la spider debe también realizar escaneos de araña en los comentarios HTML, buscando enlaces de recursos. Sólo los recursos encontrados en etiquetas de comentarios HTML válidas serán procesados.

### Analizar gramaticalmente archivos 'robots.txt' ###

Esta opción define si la spider debe también realizar escaneos de spider en los archivos robots.txt encontrados en páginas web, buscando enlaces de recursos. Esta opción no define si la spider debe seguir las reglas impuestas por los archivos tipo robots.txt.

### Manejo de los parámetros específicos de OData ###

Esta opción define si la araña debería intentar detectar parámetros específicos de OData (es decir, identificadores de recursos) para procesarlas correctamente de acuerdo a la regla definida por la opción de "manejo de parámetros de consulta".

## Vease también ##

<table> 
 <tbody>
  <tr> 
   <td>&nbsp;&nbsp;&nbsp;&nbsp;</td> 
   <td><a href="HelpUiOverview" rel="nofollow">UI Overview</a></td> 
   <td>Para una vista general sobre la interfaz de usuario</td> 
  </tr> 
  <tr> 
   <td>&nbsp;&nbsp;&nbsp;&nbsp;</td> 
   <td><a href="HelpStartConceptsSpider" rel="nofollow">Spider(Ara&ntilde;a)</a></td> 
   <td>para una vista general sobre la ara&ntilde;a</td> 
  </tr> 
  <tr> 
   <td>&nbsp;&nbsp;&nbsp;&nbsp;</td> 
   <td><a href="HelpUiTabsSpider" rel="nofollow">Etiqueta de ara&ntilde;a</a></td> 
   <td>para una vista general sobre la etiqueta de ara&ntilde;a</td> 
  </tr> 
 </tbody>
</table>


[Spider]: HelpStartConceptsSpider
[Habilitar rastreo de sesi_n _Cookie]: HelpUiTlmenuEdit
[Usuario]: HelpStartConceptsUsers
[Sesi_n HTTP]: HelpStartConceptsHttpsessions