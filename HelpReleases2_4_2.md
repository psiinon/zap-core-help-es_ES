# Release 2.4.2 #

Se hicieron los siguientes cambios en esta versión:

## Mejoras: ##

 *  Tema 1306: Bandera de línea de comandos PermSize Java en Java 8
 *  Problema de 1593: Desplazamiento automático en la Spider tab
 *  Problema de 1600: No informe alerta X-Frame-Options en las páginas 403 y 404
 *  Problema de 1654: httpSessions/createEmptySession debe inicializar un sitio que no fue visitado anteriormente
 *  Número 1702: Añadir "efectuar recursividad" opción a la spider API
 *  Problema de 1715: Incapaz de pasar argumentos al lanzar el ZAP de la línea de comandos en Mac OS X
 *  Edición 1766: Quitar de contexto mediante la API
 *  Edición 1768: Actualización utilizar un agente de usuario más reciente
 *  Edición 1778: Exploración pasiva AJAX spider peticiones
 *  Problema de 1790: Movimiento búfer desbordamiento analizador de Beta lanzamiento
 *  Edición 1793: Permitir secuencias de comandos de exploración activa comprobar si la exploración se detuvo
 *  Problema de 1795: Permite opciones JVM para ser configurado vía GUI
 *  Número 1799: Solicitud de prestación menor: URL permite a pegar en iniciar diálogo de spider.
 *  Edición 1802: Leve mejora: cambiar botón de pausa activa para un botón de Play
 *  Edición 1849: Opción combinar temas relacionados en los informes
 *  Edición 1857: Bibliotecas que fueron actualizadas
 *  Edición 1865: Aumentar el tamaño del db máxima

## Corrección de error: ##

 *  Problema de 1760: No se puede inicializar el directorio de inicio! XML/config.XML (No existe el fichero o directorio)
 *  Problema de 1763: Comprobación automática de actualizaciones no informe nuevas versiones
 *  Edición de 1770: Excepciones cuando se llama a (algunos) acciones de contexto API en modo daemon
 *  Edición 1771: Para el zap.sh en el núcleo OSX descargar duro y la ubicación relativa de java
 *  Problema de 1772: En OS X, versión de Java encuentra se encuentra
 *  Problema de 1777: "no puede encontrar configuración fuente null.policy" después de abrir el diálogo "Análisis activo"
 *  Edición 1781: Errores ZAP con "Unsupported opción '-psn\_x\_xxxxxxx'" en OS X
 *  Problema de 1784: NullPointerException cuando se activa la exploración a través de la API con un objetivo sin esquema
 *  Edición 1785: Plugin activado incluso si las dependencias no lo son, "hangs" la exploración activa
 *  Edición 1787: Contexto no utilizado por la spider aunque seleccionado
 *  Edición 1788: Exploración panel progreso clasificación necesita cambio
 *  Número 1789: Mensajes de forzoso examinar/AJAX spider no restaurados a ficha sitios
 *  Edición : 1792 informe generado no en modo daemon
 *  Edición 1798: Parada ataque característica encierra ZAP?
 *  Problema de 1804: Deshabilitar procesamiento de entidades externas XML por defecto
 *  Edición 1805: ZAP API puede no devolver la respuesta en el formato solicitado en errores
 *  Edición de 1858: Spider puede informar mal progreso después de terminar
 *  Edición de 1872: EDT en modo daemon

## Véase también ##

<table> 
 <tbody>
  <tr>
   <td>&nbsp;&nbsp;&nbsp;&nbsp;</td>
   <td><a href="HelpIntro" rel="nofollow">Introducci&oacute;n</a></td>
   <td>introducci&oacute;n a ZAP</td>
  </tr> 
  <tr>
   <td>&nbsp;&nbsp;&nbsp;&nbsp;</td>
   <td><a href="HelpReleasesReleases" rel="nofollow">Lanzamientos</a></td>
   <td>el conjunto completo de lanzamientos</td>
  </tr> 
  <tr>
   <td>&nbsp;&nbsp;&nbsp;&nbsp;</td>
   <td><a href="HelpCredits" rel="nofollow">Cr&eacute;ditos</a></td>
   <td>las personas y grupos que han hecho posible esta versi&oacute;n</td>
  </tr> 
 </tbody>
</table>