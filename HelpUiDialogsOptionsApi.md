# Pantalla de opciones de la API #

Esta pantalla permite configurar las [API][] opciones:

### Habilitado ###

Si habilita luego el API está disponible para todas las máquinas que son capaces de usar el ZAP como proxy.


### UI Enabled ###

Si entonces habilitada la interfaz de la API está disponible para todas las máquinas que son capaces de usar el ZAP como proxy. Para acceder a la interfaz de usuario de Web API punto tu navegador en el host y el puerto que escucha ZAP en.


### Secure Only ###

Si está habilitado, entonces la API sólo estará disponible a través de HTTPS. De lo contrario estará disponible a través de HTTP y HTTPS.


### Clave API ###

Una clave que debe especificarse en los API 'actions' y algunas operaciones de 'other'.
La clave API se utiliza para evitar que sitios maliciosos tengan acceso a la API de ZAP.
Se recomienda que establezca una clave a menos que utilice ZAP en un entorno completamente aislado.


### Direcciones permitidas utilizar para usar la API ###

Por defecto sólo la máquina que Zap está ejecutando es capaz de acceder a la API de ZAP.
Puedes permitir el acceso de otras máquinas a la API al agregar patrones de regex adecuados.
Sólo debe agregar las direcciones IP que usted confía.
Tenga en cuenta que la API ZAP también ahora revisa el encabezado de host, por lo también debe ser una de las direcciones permitidas.

### Desactivar API key ###

Al seleccionar esta opción deshabilita el API key.
No es recomendable salvo que utilice ZAP en un ambiente totalmente aislado, ya que permite sitios maliciosos acceder a la API de ZAP.

### No requieren una clave de API para operaciones seguras ###

Si habilita la clave de la API no es necesaria para vistas u otras operaciones que se consideran 'safe', en otras palabras las operaciones que no hacen cambios a ZAP. Este tipo de operaciones da acceso a datos de ZAP como alertas, mensajes y rutas de archivos de sistema. También puede ser utilizados por aplicaciones web para detectar la presencia de ZAP.

### Informe de errores de permiso vía API ###

Si está habilitado, entonces ZAP informe de errores de permiso a través de la API, que puede ser utilizado por aplicaciones web para detectar la presencia de ZAP. Esto no es un problema serio en un ambiente seguro pero si usas ZAP contra sitios potencialmente dañinos entonces usted debe no habilitarla.

### Detalles del informe de error a través de API ###

Si se selecciona esta opción más detalles del error se devuelven mediante la API.
No es recomendable excepto para propósitos de depuración como estos mensajes de error pueden tener fugas de información a sitios maliciosos.
Tenga en cuenta que los detalles del error completo siempre se escriben en el archivo de registro ZAP.

### Autorrelleno API key en el UI API ###

Si se selecciona esta opción el API key automáticamente está incluido en la API de interfaz de usuario.
No es recomendable salvo que utilice ZAP en un ambiente totalmente aislado, ya que permite sitios maliciosos acceder a la API Key de ZAP.


### Activar JSONP ###

Al seleccionar esta opción permite el formato JSONP.
Esto puede ser útil para algunos usos, pero generalmente no se recomienda ya que incrementa el área de superficie de ataque ZAP, es decir las características que un sitio malintencionado puede abusar.
Si está activado JSONP todas las operaciones de la API usando JSONP (incluidas las vistas) requerirá el API key para evitar que sitios maliciosos tengan acceso a información confidencial mantenida por ZAP, como claves de sesión.

## Vease también ##

<table> 
 <tbody>
  <tr>
   <td>&nbsp;&nbsp;&nbsp;&nbsp;</td>
   <td> <a href="HelpUiOverview" rel="nofollow">UI Overview</a></td>
   <td>Para una vista general sobre la interfaz de usuario</td>
  </tr> 
  <tr>
   <td>&nbsp;&nbsp;&nbsp;&nbsp;</td>
   <td> <a href="HelpUiDialogsOptionsOptions" rel="nofollow">Cuadros de di&aacute;logo de opciones</a></td>
   <td>para m&aacute;s detalles de las otras pantallas de di&aacute;logo de opciones</td>
  </tr> 
 </tbody>
</table>


[API]: HelpStartConceptsApi