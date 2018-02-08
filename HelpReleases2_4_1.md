# Release 2.4.1 #

Esta versión incluye arreglos de seguridad importantes - los usuarios son instados a actualizar cuanto antes.

Uno de los cambios quiere decir que un API key se crea por defecto, lo que significa que todas las aplicaciones utilizando la API de ZAP fallará a menos que se actualizan para usar esa clave.
La clave API se puede encontrar en el [API Options screen][]
También se puede definir la línea de comandos utilizando una opción como:

``````````
-config api.key=change-me-9203935709
``````````


Mostrar más detalles https://github.com/zaproxy/zaproxy/wiki/FAQapikey


Se hicieron los siguientes cambios en esta versión:

## Mejoras: ##

 *  Número 321: Soporte de múltiples bases de datos
 *  Número 1459: Añadir una secuencia de comandos del agente de escucha HTTP remitente
 *  Tema 1500: Bibliotecas de actualización Bouncy Castle
 *  Número 1566: Mejorar progreso reportado activo de exploración
 *  Problema de 1573: Se agrega opción para inyectar plugin ID en cabecera para todas las solicitudes de ascan
 *  Problema de 1607: No se puede guardar la sesión de prueba a través de API
 *  Problema de 1621: AScan API - permiten analizar como usuario
 *  Edición 1625: Soporte múltiples parámetros estructurales y sobre los nodos de nivel superior
 *  Edición 1653: Tecla de menú de contexto soporte para árboles
 *  Problema de 1655: Copia sesión Token ficha sesiones Http en el portapapeles
 *  Problema de 1662: Agregar el parámetro token por defecto carriles anti CSRF
 *  Problema de 1664: Clientes ficha desplazamiento automático
 *  Edición 1684: No se puede establecer la tecnología a través de API
 *  Edición 1688: Actualización owasp/zap2docker imagen con la API de cliente de Python
 *  Edición 1690: Bump tamaño par de claves de 2048 para todos certificados en cadena de la (del proxy) de confianza
 *  Tema 1695: Cambiar algoritmo de firma de certificado SSL a "SHA-256 con cifrado RSA"
 *  Edición 1699: Permite ApiImplementor agregar encabezados personalizados
 *  Problema de 1715: Incapaz de pasar argumentos al lanzar el ZAP de la línea de comandos en Mac OS X
 *  Problema de 1728: Actualización JRE a 1.7u79 (CPU) para MacOS

## Corrección de error: ##

 *  Número 444: Garantizado NPE en AliasCertificate.getName() si getCN () == null
 *  Edición 1442: Arriba/abajo teclas de flecha en los resultados de dejar de trabajar si "refleja"
 *  Edición 1473: spider no maneja URLs extraídas de etiquetas meta correctamente
 *  Número 1497: spider es extraer y reportando enlaces desde comentarios - evento cuando se le indique no hacerlo
 *  Edición 1598: script de arranque carece de soporte para FreeBSD
 *  Problema de 1615: Busca la opción "Todos" no funciona
 *  Número 1617: ZAP 2.4.0 lanza HeadlessExceptions cuando se ejecuta en modo demonio en máquina sin cabeza
 *  Problema de 1618: Tecnología de destino no
 *  Edición 1619: Regex búsqueda no puede ser validado
 *  Problema de 1624: Error al cargar el ZAP 2.4.0
 *  Edición 1626: Parámetros estructurales no guardan cuando contexto exportado y no disponible a través de la API
 *  Número 1636: Usuarios (auth) y no cargado de sesión de usuario forzado
 *  Problema de 1647: Mal referencia Zest resultado
 *  Edición 1674: Araña de Ajax no teniendo en cuenta parámetros get
 *  Edición 1677: Fuzzers no se puede ampliar en OS X
 *  Edición 1694: "Error: el archivo de configuración. Programa voluntad salida."incluso si el archivo existe
 *  Edición 1698: Excepciones de API escapar
 *  Edición 1700: Listas de navegación forzada falta de Drop-Down en 2.4.0
 *  Edición 1706: Añadir opciones de seguridad de API
 *  Problema de 1708: Árbol de tecnología de contexto puede conseguir fuera de sincronización
 *  Número 1709: Las aplicaciones no son (inmediatamente) se muestra después de comienzo
 *  Número 1714: PNH no reflejara API key a menos que el usuario provee
 *  Edición 1716: Restringir el uso de la Rúbrica CORS en pnh
 *  Número 1720: Añadir más opciones de seguridad de API de JSONP
 *  Número 1724: Asegurar el componente API nombres se escapan en la salida HTML
 *  Edición 1735: Tecnologías de contexto no escaneo activo a menos que se reemplaza

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


[API Options screen]: HelpUiDialogsOptionsApi