# Pantalla de opciones de Proxies locales #

La pantalla de opciones de conexión le permite configurar las direcciones y puertos que ZAP acepta conexiones entrantes.


## Proxy local ##

Por defecto ZAP escuchará en un puerto y dirección local, y estas son la dirección y el puerto que debe configurar su navegador para usar como proxy.

### Dirección ###

La dirección local que ZAP va a utilizar. Todas las direcciones disponibles se identifican automáticamente.

### Puerto ###

El puerto en el que ZAP va a escuchar.

### Detrás de NAT ###

Indica que el Proxy Local (ZAP) está detrás de NAT. Cuando se selecciona ZAP intentará determinar la dirección IP pública, para detectar y controlar las solicitudes con el público Dirección IP (por ejemplo, para ser atendidos por el ZAP de la API).

**Nota:** Esta opción sólo se admite cuando ZAP se ejecutan en AWS instancia de EC2. ZAP obtendrá la dirección IP pública de [AWS EC2 de la instancia de metadatos][].
ZAP se debe de empezar con esta opción habilitada, si el acceso a la API, a través de la dirección IP pública, es necesario:

> zap.sh -daemon -puerto 8080 -host 0.0.0.0 configuración de proxy.behindnat=true

Also, the [API][] necesita ser configurado para aceptar direcciones IP externas (es decir, la IP dirección desde donde ZAP es la que se accede).

### Quitar Incompatible Codificaciones ###

Permite que el proxy para quitar incompatible codificaciones de la "Accept-Encoding" solicitud de encabezado de campo, por lo que no (no admitida) en la codificación de las transformaciones se realizan para la respuesta.
Esta opción debe estar activada siempre, salvo cuando las pruebas de la codificación de las transformaciones.
Los mensajes codificados incompatible con las codificaciones de no ser correctamente analizado (ya sea por activa y pasiva de los escáneres).

### Protocolos De Seguridad ###

Permite escoger el SSL/TLS versiones habilitado para conexiones entrantes (por ejemplo, de los navegadores). Al menos una versión debe estar habilitado, las versiones no soportadas por el JRE, será seleccionado y movilidad.
La opción SSLv2Hello deben ser seleccionados junto con al menos uno de SSL/TLS versión.
Las opciones de seguridad se aplican a la principal y todos los apoderados adicionales.

## Los Servidores Proxy Adicionales ##

Puede añadir tantas direcciones y puertos para ZAP para escuchar como te gusta.
Esto puede ser útil cuando las pruebas de aplicaciones móviles - puede proxy de la aplicación móvil a través de una conexión Wi-Fi gratuita interfaz al mismo tiempo como usar el backend del sitio directamente a través de un navegador proxy a través de ZAP emulando un agente de usuario móvil.

## Véase también ##

<table> 
 <tbody>
  <tr>
   <td>&nbsp;&nbsp;&nbsp;&nbsp;</td>
   <td> <a href="HelpUiOverview" rel="nofollow">Resumen de la IU</a></td>
   <td>para una visi&oacute;n general de la interfaz de usuario</td>
  </tr> 
  <tr>
   <td>&nbsp;&nbsp;&nbsp;&nbsp;</td>
   <td> <a href="HelpUiDialogsOptionsOptions" rel="nofollow">Cuadros de di&aacute;logo de opciones</a></td>
   <td>para m&aacute;s detalles de las otras Opciones de di&aacute;logo de las pantallas</td>
  </tr> 
 </tbody>
</table>


[AWS EC2 de la instancia de metadatos]: https://docs.aws.amazon.com/AWSEC2/latest/UserGuide/using-instance-addressing.html#working-with-ip-addresses
[API]: HelpUiDialogsOptionsApi