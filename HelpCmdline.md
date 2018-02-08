# Línea de comando #

Para ejecutar Zap a través la línea de comando, se necesita ubicar el script de inicio de ZAP.
**Windows:**


``````````
C:\Program Files (x86)\OWASP\Zed Attack Proxy\zap.bat
``````````

**Mac:**


``````````
/Applications/OWASP\ ZAP.app/Contents/Java/zap.sh
``````````

**Linux:**
`zap.sh` estará debajo del directorio donde se instaló ZAP.

Como alternativa, se puede ejecutar el archivo JAR directamente:


``````````
java -jar zap.jar
``````````

Todas las opciones de abajo se pueden pasar a cualquiera de estos.

## Opciones ##

ZAP soporta las siguientes opciones de línea de comando:

<table> 
 <tbody>
  <tr>
   <td>&nbsp;&nbsp;&nbsp;&nbsp;</td>
   <td>-version</td>
   <td>Informa la versi&oacute;n de ZAP</td>
  </tr> 
  <tr>
   <td>&nbsp;&nbsp;&nbsp;&nbsp;</td>
   <td>-cmd</td>
   <td>Ejecuci&oacute;n en l&iacute;nea (sale cuando se completa las opciones de la l&iacute;nea de comando)</td>
  </tr> 
  <tr>
   <td>&nbsp;&nbsp;&nbsp;&nbsp;</td>
   <td>-daemon</td>
   <td>Inicia ZAP en modo daemon, por ejemplo sin IU</td>
  </tr> 
  <tr>
   <td>&nbsp;&nbsp;&nbsp;&nbsp;</td>
   <td>-config &lt;kvpair&gt;</td>
   <td>Anula el par espec&iacute;fico clave=valor en el archivo de configuraci&oacute;n. Las opciones de l&iacute;nea de comando <code>-config</code> se aplican en el orden especificado.</td>
  </tr> 
  <tr>
   <td>&nbsp;&nbsp;&nbsp;&nbsp;</td>
   <td>-configfile &lt;path&gt;</td>
   <td>Anula los pares key=value con esos en el archivo de propiedades especificado</td>
  </tr> 
  <tr>
   <td>&nbsp;&nbsp;&nbsp;&nbsp;</td>
   <td>-dir &lt;dir&gt;</td>
   <td>Utiliza el directorio especificado en lugar del predeterminado</td>
  </tr> 
  <tr>
   <td>&nbsp;&nbsp;&nbsp;&nbsp;</td>
   <td>-installdir &lt;dir&gt;</td>
   <td>Anula el c&oacute;digo que detecta donde ZAP ha sido instalado con el directorio especificado</td>
  </tr> 
  <tr>
   <td>&nbsp;&nbsp;&nbsp;&nbsp;</td>
   <td>-h</td>
   <td>Muestra todas las opciones de l&iacute;nea de comando disponibles, incluyendo los agregados por los complementos</td>
  </tr> 
  <tr>
   <td>&nbsp;&nbsp;&nbsp;&nbsp;</td>
   <td>-help</td>
   <td>Lo mismo que -h</td>
  </tr> 
  <tr>
   <td>&nbsp;&nbsp;&nbsp;&nbsp;</td>
   <td>-newsession &lt;path&gt;</td>
   <td>Crea una nueva sesi&oacute;n en la ubicaci&oacute;n especificada</td>
  </tr> 
  <tr>
   <td>&nbsp;&nbsp;&nbsp;&nbsp;</td>
   <td>-session &lt;path&gt;</td>
   <td>Abre la sesi&oacute;n determinada luego de iniciar ZAP</td>
  </tr> 
  <tr>
   <td>&nbsp;&nbsp;&nbsp;&nbsp;</td>
   <td>-host &lt;host&gt;</td>
   <td>Anula el host usado para el proxy especificado en el archivo de configuraci&oacute;n</td>
  </tr> 
  <tr>
   <td>&nbsp;&nbsp;&nbsp;&nbsp;</td>
   <td>-port &lt;port&gt;</td>
   <td>Anula el puerto utilizado para el proxy especificado en el archivo de configuraci&oacute;n</td>
  </tr> 
  <tr>
   <td>&nbsp;&nbsp;&nbsp;&nbsp;</td>
   <td>-lowmem</td>
   <td>Utiliza la base de datos en lugar de la memoria tanto como sea posible. Esto es experimental</td>
  </tr> 
  <tr>
   <td>&nbsp;&nbsp;&nbsp;&nbsp;</td>
   <td>-experimentaldb</td>
   <td>Usa el c&oacute;digo gen&eacute;rico de la base de datos experimental. Este tambi&eacute;n es experimental</td>
  </tr> 
  <tr>
   <td>&nbsp;&nbsp;&nbsp;&nbsp;</td>
   <td>-addoninstall &lt;addon&gt;</td>
   <td>Instala el complemento especificado desde el Marketplace de ZAP</td>
  </tr> 
  <tr>
   <td>&nbsp;&nbsp;&nbsp;&nbsp;</td>
   <td>-addoninstallall</td>
   <td>Instala todos los complementos disponibles desde el Marketplace de ZAP</td>
  </tr> 
  <tr>
   <td>&nbsp;&nbsp;&nbsp;&nbsp;</td>
   <td>-addonuninstall &lt;addon&gt;</td>
   <td>Desinstala el complemento especificado</td>
  </tr> 
  <tr>
   <td>&nbsp;&nbsp;&nbsp;&nbsp;</td>
   <td>-addonupdate</td>
   <td>Actualiza todos los complementos cambiados desde el Marketplace de ZAP</td>
  </tr> 
  <tr>
   <td>&nbsp;&nbsp;&nbsp;&nbsp;</td>
   <td>-addonlist</td>
   <td>Elabora una lista de los complementos instalados</td>
  </tr> 
  <tr>
   <td>&nbsp;&nbsp;&nbsp;&nbsp;</td>
   <td>-script &lt;script&gt;</td>
   <td>Ejecuta un script especificado (ruta del sistema de archivo) si la l&iacute;nea de comand o dameon, o simplemente cargarlo si GUI</td>
  </tr> 
  <tr>
   <td>&nbsp;&nbsp;&nbsp;&nbsp;</td>
   <td>-last_scan_report &lt;path&gt;</td>
   <td>Genera el &quot;&Uacute;ltimo informe del An&aacute;lisis&quot; dentro de la ruta especificada</td>
  </tr> 
  <tr>
   <td>&nbsp;&nbsp;&nbsp;&nbsp;</td>
   <td>-suppinfo</td>
   <td>Detalles relevantes de salidas para soporte y soluci&oacute;n de problemas (a la consola o salida est&aacute;ndar). Como: versi&oacute;n de ZAP, versi&oacute;n Java, complementos instalados y su versi&oacute;n, informaci&oacute;n local, sistema operativo, etc.</td>
  </tr> 
 </tbody>
</table>


Las opciones `-session` and `-newsession` son mutuamente excluyentes. Se mostrará un error y se saldrá de ZAP (si no está en GUI) cuando se configuren ambas opciones.
Las rutas relativas al archivo de la sesión se solucionan por el directorio "sesión" ubicado en el directorio principal de ZAP (predeterminado o especificado con la opción `-dir` ).
Las claves de configuración deben especificarse utilizando la notación de puntos basada en su ubicación el el XML del archivo de configuración, por ejemplo:


``````````
<zap-script> -config api.key=12345 -config connection.timeoutInSecs=60
``````````

Tenga en cuenta que los complementos pueden agregar opciones adicionales de línea de comandos.

Ejemplos:

 *  Iniciar ZAP en modo "daemon" con una nueva sesión creada en una ruta determinada:
    
    ``````````
    <zap-script> -daemon -newsession session
    ``````````
 *  Crea un informe del último análisis de una sesión existente y sale de ZAP una vez terminada:
    
    ``````````
    <zap-script> -last_scan_report /full/path/to/save/report.xml -session /full/path/to/existing/session -cmd
    ``````````

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
   <td> <a href="HelpStartConceptsApi" rel="nofollow">API</a></td>
   <td>para controlar mediante programaci&oacute;n el ZAP</td>
  </tr> 
 </tbody>
</table>