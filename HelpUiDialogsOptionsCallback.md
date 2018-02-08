# Options Callback Address screen #

The Callback Address screen le permite configurar la dirección utilizada para detectar vulnerabilidades que permiten a un atacante llamar a URL remotas.
En versiones anteriores, la API de ZAP se usaba para este propósito, pero a partir de la 2.6.0 se usa un punto final separado para que los sistemas de destino no ya no es necesario tener acceso a la API.

### Dirección local (por ejemplo, 0.0.0.0): ###

La dirección local en la que ZAP escuchará las conexiones entrantes. El valor predeterminado de '0.0.0.0' significa que ZAP escuchará en todas las direcciones locales disponibles.

### Dirección remota: ###

La dirección que se especificará en los ataques relevantes. Esta dirección debe ser accesible desde el sistema de destino. Puede usar la URL de prueba para verificar que este sea el caso.

### Puerto aleatrorio: ###

Por defecto, ZAP usará un puerto diferente cada vez que se ejecute. Si necesita usar el mismo puerto (por ejemplo, para permitir el acceso a través de firewalls), desmarque esta opción.

### Puerto especifico: ###

Si la opción Puerto aleatorio está desmarcada, este es el puerto en el que ZAP escuchará. Debe ser diferente a los otros puertos que usa ZAP, por ejemplo, el puerto que usa para las conexiones de proxy.

### URL de prueba: ###

Esta es la URL de prueba a la que puede intentar acceder desde sistemas remotos. Todos los accesos a la URL de prueba se registrarán en el archivo de registro de ZAP en el nivel INFO. Si está utilizando la interfaz de usuario de ZAP, los accesos también se mostrarán en [Output tab][].

## Vease también ##

<table> 
 <tbody>
  <tr>
   <td>&nbsp;&nbsp;&nbsp;&nbsp;</td>
   <td> <a href="HelpUiOverview" rel="nofollow">UI Overview</a></td>
   <td>para una vista general de la interfaz de usuario</td>
  </tr> 
  <tr>
   <td>&nbsp;&nbsp;&nbsp;&nbsp;</td>
   <td> <a href="HelpUiDialogsOptionsOptions" rel="nofollow">Opciones de dialogo</a></td>
   <td>para detalles de otras pantallas de opciones de di&aacute;logos</td>
  </tr> 
 </tbody>
</table>


[Output tab]: HelpUiTabsOutput