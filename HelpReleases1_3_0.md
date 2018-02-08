# Versión 1.3.0 #

Se hicieron los siguientes cambios en esta versión:

## Cambios significativos: ##

### Fuzzing ###

Cadenas en una respuesta pueden ser fuzzed ahora para tratar de encontrar vulnerabilidades.
Anti CRSF fichas pueden ser detectadas y regenera automáticamente cuando fuzzing.
Esta funcionalidad se basa en código del proyecto OWASP JBroFuzz.

### Certificados SSL Dinámicos ###

El soporte para conexiones SSL fue mejorado y simplificado.
Usuario ahora puede crear su propio certificado raíz y distribuir esto en sus clientes HTTP.
Véase [Opción: Certificados SSL Dinámicos][Opci_n_ Certificados SSL Din_micos] Mostrar más detalles

### Modo daemon y API ###

A partir de ZAP con el "-daemon" opción de línea de comando hará que se ejecute en segundo plano en el modo 'headless', lo que significa que no se muestra ninguna interfaz de usuario.
Una API inicial ha sido implementada en XML, JSON y HTML.
Si ZAP se ejecuta como un daemon entonces la API se activa automáticamente, de lo contrario la API debe habilitarse a través de la pantalla de opciones API.
La API se puede navegar con la apertura de http://zap/ en tu navegador cuando proxy vía ZAP.

### Integración de BeanShell ###

Se mostrará la [BeanShell][] es un shell interactivo de Java que se puede utilizar para ejecutar secuencias de comandos de BeanShell.
Estos scripts son una forma simplificada de Java que utilizan muchos elementos de la sintaxis de Java, pero en un formato de secuencias de comandos más simple.
Todo el código Java también es código válido de BeanShell.
BeanShell integración en OWASP ZAP le permite escribir scripts utilizando las funciones ZAP y el conjunto de datos.
Esto puede ser una característica muy potente para el análisis de aplicaciones web.


### Mas internacionalización ###

Toda cadena de presentación ahora son plenamente internacionalizado.

### Localización ###

Soporte de caja para los siguientes idiomas:

<table> 
 <tbody>
  <tr>
   <td>&nbsp;&nbsp;&nbsp;&nbsp;</td>
   <td>Ingl&eacute;s</td>
  </tr> 
  <tr>
   <td>&nbsp;&nbsp;&nbsp;&nbsp;</td>
   <td>Portugu&eacute;s Brasile&ntilde;o</td>
  </tr> 
  <tr>
   <td>&nbsp;&nbsp;&nbsp;&nbsp;</td>
   <td>Chino</td>
  </tr> 
  <tr>
   <td>&nbsp;&nbsp;&nbsp;&nbsp;</td>
   <td>Franc&eacute;s</td>
  </tr> 
  <tr>
   <td>&nbsp;&nbsp;&nbsp;&nbsp;</td>
   <td>Alem&aacute;n</td>
  </tr> 
  <tr>
   <td>&nbsp;&nbsp;&nbsp;&nbsp;</td>
   <td>Griego</td>
  </tr> 
  <tr>
   <td>&nbsp;&nbsp;&nbsp;&nbsp;</td>
   <td>Indonesio</td>
  </tr> 
  <tr>
   <td>&nbsp;&nbsp;&nbsp;&nbsp;</td>
   <td>Japon&eacute;s</td>
  </tr> 
  <tr>
   <td>&nbsp;&nbsp;&nbsp;&nbsp;</td>
   <td>Polaco</td>
  </tr> 
  <tr>
   <td>&nbsp;&nbsp;&nbsp;&nbsp;</td>
   <td>Espa&ntilde;ol</td>
  </tr> 
 </tbody>
</table>

## Cambios menores: ##

### Ver hexagonal ###

Se mostrará la [Petición][Petici_n], [Respuesta][] las pestañas ahora proporcionan una ' Hex Vew ' opción que muestra los cuerpos de respuesta y de solicitud en formato hexadecimal.

### Resultados de la búsqueda ###

Se mostrará la [Pestaña de búsquedas ][Pesta_a de b_squedas] ahora muestra todas las instancias de una cadena que se encuentra en lugar de sólo la primera instancia en cada petición o respuesta.

### Excluir direcciones URL ###

Las direcciones URL pueden ser explícitamente excluidas del explorador activo, araña y desde el proxy.

### Soporte de copia ###

La mayoría de los paneles proporciona ahora una 'clic derecho' 'Copiar' opción de menú, incluyendo los paneles de análisis de puertos y fuerza bruta.

### Deshacer/rehacer apoyo ###

Todos los campos de entrada ahora apoyan acciones de deshacer/rehacer usando los aceleradores de deshacer/rehacer de sistemas operativos por defecto:

 *  Windows/Linux: Ctrl+Z / Ctrl+Y
 *  Mac OS X: Cmd + Z / Cmd + Shift + Z

### Opción de apoyo y tiempo de espera de proxy scanner puerto ###

El Port Scanner ahora puede utilizar al servidor proxy saliente (si está configurada) y también ahora se puede establecer el tiempo de espera en milisegundos.

### Botones de rotura de solicitud y respuesta ###

Ahora hay 2 botones 'Set Break' para permitir descansos para establecerse independientemente en todas las solicitudes y todas las respuestas.

### Ampliar información y sitios pestaña botones ###

Ahora hay 2 botones que permiten cambiar entre tener la información y sitios de pestañas ampliadas.

### Rotura ficha icono cambios color cuando punto de quiebre ###

Si bien la pestaña Descanso no está en uso, su ícono es una cruz gris: & nbsp; ![101grey.png][] .
Mientras un [punto de interrupción][punto de interrupci_n] se presiona el ícono de la pestaña se cambia a una cruz roja: & nbsp; ![101.png][] .


### Tiempo de espera ajustable ###

Se mostrará la [Opción: Conexión][Opci_n_ Conexi_n] pantalla le permite configurar el tiempo de espera en segundos para que sea más fácil probar aplicaciones lentas.

### Actualizaciones de la biblioteca ###

La mayoría de las bibliotecas utilizadas por ZAP se han actualizado a las últimas versiones.

### Un nuevo icono :) ###

Gracias a Simon Egli y a todos los demás por enviar interesantes sugerencias de iconos.

## Problemas conocidos: ##

### Mac OS X: SSL dinámico y Google Chrome ###

Actualmente Dynamic SSL no funciona cuando se usa Google Chrome. Esto se debe a un problema conocido no resuelto con Google Chrome y Mac OS X Keychain. Al importar la CA raíz de OWASP ZAP al llavero y solicitar un sitio web SSL, se muestra un mensaje de error de "Certificado no válido".

## Vease también ##

<table> 
 <tbody>
  <tr>
   <td>&nbsp;&nbsp;&nbsp;&nbsp;</td>
   <td> <a href="HelpIntro" rel="nofollow">Introducci&oacute;n</a></td>
   <td>Introducci&oacute;n a ZAP</td>
  </tr> 
  <tr>
   <td>&nbsp;&nbsp;&nbsp;&nbsp;</td>
   <td> <a href="HelpReleasesReleases" rel="nofollow">Lanzamientos</a></td>
   <td>el conjunto completo de los comunicados de</td>
  </tr> 
  <tr>
   <td>&nbsp;&nbsp;&nbsp;&nbsp;</td>
   <td> <a href="HelpCredits" rel="nofollow">Cr&eacute;ditos</a></td>
   <td>las personas y grupos que han hecho posible esta versi&oacute;n</td>
  </tr> 
 </tbody>
</table>


[Opci_n_ Certificados SSL Din_micos]: HelpUiDialogsOptionsDynsslcert
[BeanShell]: http://www.beanshell.org/
[Petici_n]: HelpUiTabsRequest
[Respuesta]: HelpUiTabsResponse
[Pesta_a de b_squedas]: HelpUiTabsSearch
[101grey.png]: https://github.com/zaproxy/zap-core-help/wiki/images/16/101grey.png
[punto de interrupci_n]: HelpStartConceptsBreakpoints
[101.png]: https://github.com/zaproxy/zap-core-help/wiki/images/16/101.png
[Opci_n_ Conexi_n]: HelpUiDialogsOptionsConnection