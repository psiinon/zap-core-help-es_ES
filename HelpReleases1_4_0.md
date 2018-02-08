# Versión 1.4.0 #

Se hicieron los siguientes cambios en esta versión:

## Cambios significativos: ##

### Tema 133: Añade resaltado de sintaxis para Panel de respuesta ###

Los paneles HTML ahora soportan resaltado de sintaxis conmutable.

### Número 153: integración de fuzzdb ###

El fuzzer incluye fuzzdb (https://github.com/fuzzdb-project/fuzzdb) archivos de fuzzing.
Tenga en cuenta que algunos archivos de fuzzdb han quedado ya que común anti antivirus a bandera que contienen virus.
Usted puede sustituir (y fuzzdb) por descargar la versión más reciente de fuzzdb y expansión en la biblioteca 'fuzzers'.

### Número 212: Análisis del parámetro ###

Una nueva pestaña de parámetros muestra un resumen de todos los parámetros que se ha utilizado un sitio.

### Número 228: Escáner XSS mayor ###

El escáner de Cross Site Scripting activo ha sido reescrito desde cero para encontrar más posibles problemas de XSS e informe menos falsos positivos.

### Número 244: Puerto el vigilante pasivo comprueba ###

Las siguientes comprobaciones han sido portadas de vigilante (gracias a Chris Weber por oking esto):

<table> 
 <tbody>
  <tr>
   <td>&nbsp;&nbsp;&nbsp;&nbsp;</td>
   <td>Check.Pasv.CrossDomain.ScriptReference.cs</td>
   <td>verifica la inclusi&oacute;n de archivos javascript entre dominios.</td>
  </tr> 
  <tr>
   <td>&nbsp;&nbsp;&nbsp;&nbsp;</td>
   <td>Check.Pasv.Header.CacheControl.cs</td>
   <td>verifica el encabezado de control de cach&eacute; HTTP en p&aacute;ginas SSL.</td>
  </tr> 
  <tr>
   <td>&nbsp;&nbsp;&nbsp;&nbsp;</td>
   <td>Check.Pasv.Header.ContentTypeMissing.cs</td>
   <td>checks that the Content-Type HTTP header is not missing.</td>
  </tr> 
  <tr>
   <td>&nbsp;&nbsp;&nbsp;&nbsp;</td>
   <td>Check.Pasv.Header.FrameOptions.cs</td>
   <td>checks that the X-FRAME-OPTIONS is not missing or insecurely set.</td>
  </tr> 
  <tr>
   <td>&nbsp;&nbsp;&nbsp;&nbsp;</td>
   <td>Check.Pasv.Header.IeXssProtection.cs</td>
   <td>checks that the X-XSS-Protection has not been set to disable IE's XSS protection.</td>
  </tr> 
  <tr>
   <td>&nbsp;&nbsp;&nbsp;&nbsp;</td>
   <td>Check.Pasv.Header.MimeSniff.cs</td>
   <td>checks that the X-CONTENT-TYPE-OPTIONS has been set.</td>
  </tr> 
  <tr>
   <td>&nbsp;&nbsp;&nbsp;&nbsp;</td>
   <td>Check.Pasv.InformationDisclosure.DatabaseErrors.cs</td>
   <td>checks for database error messages.</td>
  </tr> 
  <tr>
   <td>&nbsp;&nbsp;&nbsp;&nbsp;</td>
   <td>Check.Pasv.InformationDisclosure.DebugErrors.cs</td>
   <td>checks for debugging error messages.</td>
  </tr> 
  <tr>
   <td>&nbsp;&nbsp;&nbsp;&nbsp;</td>
   <td>Check.Pasv.InformationDisclosure.InUrl.cs</td>
   <td>checks for information disclosure in URL parameters.</td>
  </tr> 
  <tr>
   <td>&nbsp;&nbsp;&nbsp;&nbsp;</td>
   <td>Check.Pasv.InformationDisclosure.ReferrerLeak.cs</td>
   <td>checks HTTP Referer header for information disclosure.</td>
  </tr> 
 </tbody>
</table>

### Número 253: Extensiones de tarjetas ###

Toda su extensión puede ahora conectarse a ZAP dinámicamente con acceso completo a todas las características del ZAPs.

## Cambios menores: ##

### Tema 54: Cierre correcto ###

### Problema 90: Agregar soporte GUI para la renegociación de SSL/TLS insegura ###

### Problema 102: Guardar la solicitud y la respuesta cruda y guardar el cuerpo de la respuesta y solicitud ###

### Número 126: Permiten trabajar archivo directorio y configuración a través de línea de cmd ###

### Número 154: Incluir param id en informes ###

### Edición 164: Botón de configuración de barra de herramientas ###

### Edición 168: Revelan campos ocultos en páginas web ###

### Número 192: Puntos de interrupción activar/desactivar ###

### Edición 193: Detectar vulnerabilidad de directory traversal ###

### Edición 194: Mejora: Mostrar ID de petición en el panel de búsqueda ###

### Número 200: Detectar las vulnerabilidades CSRF ###

### Número 230: Mejorar zap.sh para hacer frente con enlaces simbólicos ###

### Número 236: Opción para activar URLencoding ###

### Número 242: Nodo de exportación / req/resp via click derecho ###

### Número 248: Eliminar alertas / vuelva a probar la petición de característica ###

### Número 251: Reestructurar el código de alertas ###

### Número 253: Permitir extensiones definir dependencias ###

### Edición 270: Icono cambia ###

### Número 277: Racionalizar los elementos de menú de clic derecho ###

### Número 253: Extensiones de tarjetas ###

### Edición 282: Añadir autor, Descripción y URL para extensiones ###

## Corrección de error: ##

### Tema 42: Redirección arbitraria ###

### Problema 94: PKCS \#11 controlador ###

### Tema 107: La última petición/respuesta interceptada permanece en la ventana con rotura de ###

### Tema 135: Roto las URL en el Panel sitios ###

### Problema 148: El nuevo panel HTTP rompió el administrador de deshacer / rehacer ###

### Problema 180: vista tabular para la solicitud GET ###

### Problema 187: Problemas de codificación ###

### Edición 197: Decodificador no puede procesar entrada base64 sin saltos de línea ###

### Problema 198: el informe no se genera cuando existe una alerta de "alteración de parámetros" con carácter "NULO" ###

### Número 210: Al usar la opción "Path Traversal" en la exploración activa de la excepción ###

### Número 223: Excepción en pestaña de "Sites" la hora de elegir una opción emergente, "Delete (from view)" o "Purge (from DB)", cuando no se ha seleccionado ningún árbol de nodo ###

### Número 224: toma demasiado tiempo para recuperarse de un número de puerto de proxy fuera de intervalo válido ###

### Número 225: ZAP salidas al inicio si un valor de opción contiene caracteres extendidos como å, ä, ö ###

### Edición 226: cuadro de edición número puerto proxy no debe permitir millones de caracteres ###

### Número 227: Herramientas, opciones de deben ir a la pestaña mismo como la última vez ###

### Número 237: Error: problemas con los paneles de HTTP ###

### Número 238: Excepción cuando se utiliza un archivo personalizado de pelusa ###

### Número 241: zap.sh valor de Xmx para funcionamiento estable ###

### Número 243: El DynamicLoader las cargas del tarro de local, no tienen en cuenta el nombre del paquete ###

### Número 246: Cabecera Pragma requiere encabezado Cache-Control para las solicitudes de HTTP/1.1 ###

### Número 255: Excepción de API cuando debido al carácter ilegal en contexto XML ###

### Número 256: Llamar HttpMessage.setGetParams pierde el puerto ###

### Número 260: Excepción al eliminar las entradas de pestaña ("Purge (from DB) "History" ###

### Número 261: Lengua parcial partido no funciona ###

### Número 262: Alertas de "Autenticación débil" no aparece con araña ###

### Número 262: Alertas de "Cookie without secure flag" no aparece con araña ###

### Número 264: Excepción en el "Manual Request Editor"/"Resend" diálogos ###

### Número 268: Cambiar ZAP Informe XML ###

### Edición 269: Parámetro de profundidad araña ###

### Tema 274: Orden delete / opciones de purga ###

### Número 280: Escape URL en árbol de sitios ###

### Número 283: RFE: suavizado de fuente no activado por defecto en la solicitud y respuesta ###

### Edición 284: Paneles de cabecera etcetera de solicitud/respuesta demasiado pequeños ###

### Número 286: Cadena de búsqueda no destacada resultados de pelusa ###

### Número 287: Escáner pasivo no recoge nuevas fichas de anticsrf ###

### Número 289: archivos de fuzzdb causan alertas de virus ###

### Número 291: Path Traversal tiene 'param' vacía pero puso el nombre de param 'attack' ###

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