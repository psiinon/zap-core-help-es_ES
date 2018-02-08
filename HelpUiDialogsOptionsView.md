# Pantalla de monitor de opciones #

El la pantalla de monitor te permite configurar:

### Imágenes ###

Si ZAP procesa imágenes.

### Mostrar solicitidues (locales) de CONNECT ###

Si la solicitud de CONNECT HTTP recibida por los [Proxies locales][] debe persistir en la [sesión][sesi_n] actual y mostrada en la [pestaña de historia][pesta_a de historia]. la configuración predeterminada es no mostrar esas de las solicitudes, estas suceden frecuentemente (en preparación para TLS/SSL, conecciones WebSocket ) y, a menos que al inspeccionar el comportamiento de la aplicación del cliente, no son (usualmente) de mucho interés.

### Monitor ###

El diseño de los 3 paneles principales.
Las siguientes opciones se encuentran disponibles:

 *  Maximizar la pestaña izquierda (sitio) - el panel de 'árbol' que contiene las pestañas de los sitios se extiende a través de toda la longitud del lado izquierdo. Esto reducirá la cantidad de espacio disponible en el panel de 'información'.
 *  Maximizar pestañas inferiores (Historia, etcetera) - El panel de 'información' se extiende aa traves de toda la longitud de la parte inferior. Esto reduce la cantidad de espacio disponible en el panel de 'árbol'.
 *  Diseño completo - La pestaña seleccionada ocupa la pantalla completa. Esto es de ultilidad cuando se usa ZAP en pantallas pequeñas.

### Posición del panel de respuesta ###

Permite configurar la posición de la pestaña de respuesta con respecto a la pestaña de solicitud.
Las siguientes opciones se encuentran disponibles:

 *  Pestañas lado a lado - Las pestañas de solicitud y respuesta se encuentran una al lado de la otra. Esto incrementa la información que puede ser mostrada, pero significa que no podrás ver las pantallas de solicitud y de respuesta al mismo tiempo.
 *  Paneles lado a lado - El panel de solicitud es mostrado a la izquierda del panel de respuesta. Esto decrece la información que puede ser mostrada, pero significa que puedes ver a la vez las pestañas de solicitud y respuesta.
 *  Solicitud mostrada arriba de la respuesta - El panel de solicitud es mostrado arriba del panel de respuesta. Esto decrece la información que puede ser mostrada, pero significa que puedes ver ambas, la respuesta y solicitud a la vez.

La opción de posición del panel de respuesta no se aplica cuando la opción de visualización se establece para pantalla completa.

### Mostrar botones de interrupción ###

La ubicación de los botones de interrupción.

### Mínimo tamaño de la solicitud de vista agrandada ###

El tamaño mínimo de un cuerpo de la solicitud en bytes a partir del punto en el que un mensaje de 'solicitud de cuerpo agrandado' aparecerá en vez del cuerpo actual.
Esto es para prevenir que cuerpos realmente grandes reduzcan la velocidad de la interfaz de usuario.
Configurando este valor a -1 resultará en que la solicitud siempre se muestre, sin importar cuan larga sea.

### Mínimo tamaño de la vista agrandada de respuesta ###

El tamaño mínimo del cuerpo de respuesta en bytes a partir del punto en el que un mensaje de 'cuerpo de respuesta larga' será mostrado en lugar del cuerpo actual.
Esto es para prevenir que cuerpos realmente grandes reduzcan la velocidad de la interfaz de usuario.
Configurando este valor a -1 resultará en que la respuesta siempre se muestre, sin importar cuan larga sea.

### Output Tabs Time Stamp Options ###

Una vez que hayas habilitado firmas de tiempo en la pestaña de resultado puedes configurar el formato en el que prefieres que estas firmas de tiempo aparezcan. Selecciona o bien un formato pre-definido de la lista desplegable o ingresa uno de tu preferencia. El formato está basado en la clase SimpleDateFormat de Java. Después de escoger o ingresar un formato de firma de tiempo si presionas enter el ejemplo en la derecha se actualizará para reflejar tu preferencia. Si ZAP no puede utilizar un formato que hayas ingresado entonces el ejemplo se mostrará con base en el formato Predeterminado.

<table> 
 <tbody>
  <tr> 
   <td> Long &amp; Default </td> 
   <td> yyyy-MM-dd HH:mm:ss </td> 
  </tr> 
  <tr> 
   <td> ISO8601 </td> 
   <td> yyyy-MM-dd'T'HH:mm:ssZ </td> 
  </tr> 
  <tr> 
   <td> Solo Tiempo </td> 
   <td> HH:mm:ss </td> 
  </tr> 
 </tbody>
</table>

### Tamaño de Fuente ###

El tamaño de fuente predeterminado utilizado para visualizar ZAP. Si fijas esto en -1 entonces se utilizará el tamaño predeterminado del sistema.
El campo 'Ejemplo de fuente' te mostrará qué tan grande se mostrará el texto por defecto.
La configuración solo tomará efecto cuando ZAP se reinicie.

## Véase también ##

<table> 
 <tbody>
  <tr>
   <td>&nbsp;&nbsp;&nbsp;&nbsp;</td>
   <td> <a href="HelpUiOverview" rel="nofollow">UI Overview</a></td>
   <td>for an overview of the user interface.</td>
  </tr> 
  <tr>
   <td>&nbsp;&nbsp;&nbsp;&nbsp;</td>
   <td> <a href="HelpUiDialogsOptionsOptions" rel="nofollow">Options dialogs</a></td>
   <td>for details of the other Options dialog screens.</td>
  </tr> 
 </tbody>
</table>

## Enlaces externos ##

<table> 
 <tbody>
  <tr>
   <td>&nbsp;&nbsp;&nbsp;&nbsp;</td>
   <td> <a href="https://docs.oracle.com/javase/8/docs/api/java/text/SimpleDateFormat.html" rel="nofollow">Detalles de SimpleDateFormat de Java</a></td>
  </tr> 
 </tbody>
</table>


[Proxies locales]: HelpUiDialogsOptionsLocalproxy
[sesi_n]: HelpUiTlmenuFile
[pesta_a de historia]: HelpUiTabsHistory