# Release 2.2.0 #

Se hicieron los siguientes cambios en esta versión:

## Cambios menores: ##

### Problema 717: Scripts: admite varios scripts e incrustaciones en los componentes de ZAP ###

### Soporte para Mozilla Zest: https://developer.mozilla.org/en-US/docs/Zest ###

### Soporte para Mozilla Zest: https://developer.mozilla.org/en-US/docs/Zest ###

### Soporte para escanear encabezados, así como formatos JSON y XML ###

## Cambios menores: ##

### Problema 711: Soporte de escaneo de solicitudes XML ###

### Problema 713: Agregue números CWE y WASC a problemas ###

### Problema 719: puntos de interrupción de http personalizados con más opciones ###

### Problema 738: Opciones para ocultar pestañas / ventanas ###

### Problema 750: consola de script de actualización para admitir lenguajes de scripting no basados ​​en texto ###

### Problema 752: cree una nueva CA raíz cuando ejecute por primera vez ###

### Problema 775: permitir que el host se configure a través de la línea de comando ###

## Corrección de error: ##

### Problema 555: paneles Http predeterminados a vista hexadecimal ###

### Problema 599: la api de guardar sesión no permite sobrescribir la sesión que ya tiene el mismo nombre ###

### Problema 630: URLCanonicalizer.getCanonicalURL produce decodificadores "mitad" de URI decodificados ###

### Problema 631: URLCanonicalizer.buildCleanedParametersURIRepresentation devuelve URI en forma de porcentaje codificado y decodificado ###

### Problema 652: el apagado después de un análisis grande lleva demasiado tiempo (borrar registros de ascan) ###

### Problema 655: problemas de codificación de API ###

### Issue 665 : NullPointerException while proxying with a URI with an empty path component ###

### Problema 666: JSONException al llamar a una acción API sin los parámetros necesarios ###

### Problema 669: restricciones de algoritmo de certificado en Java 1.7 ###

### Problema 674: agregue HttpSessionAPI a ApiGeneratorUtils ###

### Problema 685: Agregue el archivo ficticio al directorio "fuzzers" ###

### Problema 686: Log HttpException (como error) en ProxyThread ###

### Problema 687: Cambiar el analizador de encabezado de respuesta HTTP para que sea menos estricto ###

### Problema 690: las URL de autenticación de contexto no fallan la sobrescritura manual. ###

### Problema 691: gestionar complementos antiguos ###

### Problema 692: informa la versión de java encontrada por zap.sh ###

### Problema 693: la línea de comando debería mostrar todas las opciones ###

### Problema 694: API UI falla en IE ###

### Problema 695: El árbol de sitios no borra la nueva sesión creada por la API ###

### Problema 696: cambie las opciones de complemento "Ajax Spider" para usar ZapNumberSpinner ###

### Issue 697 : API action "proxy.pac" might return wrong domain/port ###

### Problema 698: La vista de la API del analizador pasivo "recordsToScan" devuelve -1 después de terminar de escanear los mensajes ###

### Problema 699: corregir errores HTML en las páginas de ayuda ###

### Problema 702: No cargue versiones de complemento más nuevas si no están destinadas a la versión ZAP en ejecución. ###

### Problema 703: Add-on ZAP restricciones "not-before-version" y "not-from-version" no son respetados por complementos ya "instalados" ###

### Número 706: ZAP API no analizar correctamente los parámetros de la consulta con "&" caracteres ###

### Problema 710: URLCanonicalizer.getCanonicalURL no puede analizar correctamente los parámetros de consulta con "& amp;" y "=" caracteres ###

### Problema 712: La acción de la API de HttpSessions "setSessionTokenValue" debe agregar el nombre del token de sesión a los tokens de sesión del sitio ###

### Problema 720: No se pueden enviar métodos http no estándar ###

### Edición 721: Solicitudes POST no y poner reciban un 504 al servidor espera un cuerpo de la solicitud ###

### Número 724: No clonar mensaje de alerta que aparecerá en los paneles de mensaje ###

### Número 725: Limpiar los campos de panel de alarma ###

### Número 726: Captura excepciones de variantes scanner activo ###

### : 727 nombre de sesiones HTTP creadas automáticamente se trata siempre en inglés ###

### Edición 728: Permite crear una sesión con un nombre dado a través de la API de HttpSessions ###

### Edición 729: Actualizar código de autenticación de NTLM ###

### Edición 730: MissingResourceException al seleccionar una extensión de movilidad (de un Add-on) en el panel de opciones de "Extensiones" ###

### Edición 731: MissingResourceException con ExtensionFuzz activado y desactivado ExtensionBruteForce ###

### Edición 736: Cambiar clase de complemento carga estrategia para padres-último ###

### Edición 737: Restaurar las dependencias de Add-on de "Ajax spider" ###

### Número 756: Permite intercomunicación contexto paneles ###

### : 763 XML informe vacía cuando se usa en modo demonio ###

### Edición 764: HTTP fuzz resultados no admiten menús de clic derecho ###

### Edición 766: Busca resultados de pelusa no incluye el encabezado ###

### Problema de 767: Sesión HTTP API podría ser menos estricto ###

### Número 772: Reestructuración de los datos de contexto de ahorro/carga ###

### Número 774: Construcción no incluye el directorio de secuencias de comandos ###

### Número 776: Permitir complementos a usuario si estás cerrando ZAP con abierto sin guardar recursos ###

### Problema de 777: No se puede cancelar los cambios cuando usando Include en excluir del contexto ###

### Número 782: NoSuchMethodError al excluir a un enlace de canal de WebSocket de contexto ###

### Número 785: Cambiar zap.sh para hacer frente a Java 1.8 ###

### Número 786: Instantánea menú de sesión no funciona ###

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