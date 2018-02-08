# Release 2.4.3 #

Se hicieron los siguientes cambios en esta versión:

## Mejoras: ##

 *  Problema de 1576: Definir elementos de ruta de acceso de dirección URL como 'no estructural'
 *  Emisión 1711: Solicitud característica: opción para especificar el número de símbolo (token) que se generen.
 *  Edición 1768: Actualización utilizar un agente de usuario más reciente
 *  Problema de 1894: ZAP sólo analiza "User-Agent", "Referencia" y "Host" cabeceras de petición
 *  Problema 1911: Buscar solicitudes AJAX de araña
 *  Problema 1913: Pase todos los parámetros a zap.sh - paquete Debian
 *  Edición de 1914: Varios directorios de Add-on
 *  Edición 1920: Informe el host: Puerto ZAP está escuchando en modo daemon o salida si no
 *  Edición 1927: Realce de: rotura solamente para direcciones URL incluidas en el alcance.
 *  Edición 1944: Tabla de respuestas por segundo en curso de ascan
 *  Edición 1953: Permiten a la spider un contexto a través de la API de ZAP
 *  Edición 1962: Instalar y actualizar complementos de la línea de comandos
 *  Edición 1975: Suite de cifrado de RC4-SHA SSL no admitida
 *  Edición 1980: Añadir CLI ZAP a imágenes de Docker
 *  Edición 1985: Abrir el cuadro de diálogo modificar si el usuario se duplica en una fila en un AbstractMultipleOptionsBaseTablePanel
 *  Edición 2009: Añadir enlaces en línea a las páginas de FAQ y Boletín
 *  Problema 2084: Advierten a los usuarios si probablemente están utilizando versiones fuera de fecha
 *  Problema 2086: recuentos de solicitudes de informes por complemento
 *  Problema 2088: admite un botón "actualizar todo" para instalar todos los complementos actualizados
 *  Problema 2094: Ayuda un '-addoninstallall' opción de línea de comandos
 *  Edición 2102: Permiten a spider ajax opciones a través de la API

## Corrección de error: ##

 *  Problema 1070: no funciona la ruptura de una URL personalizada con parámetros de consulta.
 *  Problema 1555: SAXParseException al generar el informe
 *  Número 1617: ZAP 2.4.0 lanza HeadlessExceptions cuando se ejecuta en modo demonio en máquina sin cabeza
 *  Problema 1877: corregir ruta a .ZAP\_JVM.properties en zap.sh
 *  Problema 1893: Regresión: no se puede deshabilitar y habilitar escáneres específicos a través de la API
 *  Problema 1910: API no devuelve contenido en la codificación esperada, en errores
 *  Problema 1917: las pestañas Solicitud y Respuesta no escalan el texto
 *  Problema 1939: Scripts - Problema de habilitación de botón de guardado
 *  Problema 1949: el script con el tipo faltante impide que se carguen scripts y plantillas
 *  Problema de 1950: Conexión cerrada sin respuesta, con una secuencia de comandos de autenticación con errores
 *  Edición 1951: Excepción al intentar agregar usuarios antes de cargar un script de autenticación
 *  Problema 1960: el diálogo de Active Scan podría usar una política de escaneo obsoleta
 *  Edición 1969: Problemas con la instalación de escáneres
 *  Edición 1970: Instalar complemento dependencias podrían no tomarse en cuenta al instalar add-ons
 *  Edición 1973: Lista de HAR devuelta no contiene mensajes de redirección correcta
 *  Edición 1981: Spider podría no indicar que el número correcto de URI
 *  Edición 2005: Exploración activa incorrectamente realizado en nodos relacionados
 *  Problema de 2044: Problemas en la implementación del algoritmo de Hirschberg
 *  Número 2045: No copiar configuraciones viejo si utiliza la opción - dir
 *  Problema 2052: los cambios de autenticación realizados a través de la API no se guardaron en la sesión

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