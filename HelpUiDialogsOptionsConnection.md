# Pantalla de Opciones de Conexión #

La pantalla de Opciones de Conexión te permite configurar las opciones de conexión de ZAP:

### Tiempo de espera (segundos) ###

Esto hace que es más fácil de probar aplicaciones lentas.

### Agente de usuario predeterminado: ###

El agente de usuario que ZAP debe utilizar al crear mensajes de HTTP (por ejemplo, mensajes de araña o Conecte las peticiones al proxy saliente).

### Encabezado de solicitud única Cookie ###

Controla si el ZAP de administrado (cookies[Habilitar seguimiento de la sesión (Cookie)][Habilitar seguimiento de la sesi_n _Cookie]) se debe colocar en un encabezado de solicitud "Cookie" único o varios encabezados de la petición de "Cookie", al enviar una petición HTTP al servidor.

### DNS ###

#### Consultas exitosas TTL ####

Define por cuánto tiempo deben en caché las consultas DNS exitosas:

 *  Negativo número, caché para siempre;
 *  Cero, desactiva la caché;
 *  Número positivo, el número de segundos que se almacenará en caché las consultas.

**Nota:** Cambios se aplican después de un reinicio.

También se puede definir la opción mediante el `-config` argumento de línea de comandos con la key `connection.dnsTtlSuccessfulQueries`.

### Protocolos de seguridad ###

Permite para elegir las versiones SSL/TLS para las conexiones salientes (por ejemplo, a los servidores). Debe habilitar al menos una versión, versiones no el JRE no seleccionadas y desactivadas.
Debe seleccionar la opción SSLv2Hello en conjunto con al menos una versión SSL/TLS.

### Utilice la cadena de Proxy ###

Esta sección le permite conectarse a otro proxy para las conexiones salientes.
Esto a menudo es necesaria en un entorno corporativo.

### Autenticación Proxy ###

Esta sección le permite configurar la autenticación de proxy saliente.

## Véase también ##

<table> 
 <tbody>
  <tr>
   <td>&nbsp;&nbsp;&nbsp;&nbsp;</td>
   <td> <a href="HelpUiOverview" rel="nofollow">UI Overview</a></td>
   <td>para tener una visi&oacute;n general de la interfaz de usuario</td>
  </tr> 
  <tr>
   <td>&nbsp;&nbsp;&nbsp;&nbsp;</td>
   <td> <a href="HelpUiDialogsOptionsOptions" rel="nofollow">Options dialogs</a></td>
   <td>para m&aacute;s detalles de las otras Opciones de di&aacute;logo de las pantallas</td>
  </tr> 
  <tr>
   <td>&nbsp;&nbsp;&nbsp;&nbsp;</td>
   <td> <a href="HelpCmdline" rel="nofollow">Command Line</a></td>
   <td>para obtener m&aacute;s informaci&oacute;n de la l&iacute;nea de comandos</td>
  </tr> 
 </tbody>
</table>


[Habilitar seguimiento de la sesi_n _Cookie]: HelpUiTlmenuEdit