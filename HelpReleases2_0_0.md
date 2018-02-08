# Versión 2.0.0 #

Se hicieron los siguientes cambios en esta versión:

## Cambios significativos: ##

### Un mercado integrado de add-ons ###

ZAP puede ampliarse con complementos que tengan pleno acceso a todos los componentes internos ZAP. Cualquiera puede escribir complementos y subir en el mercado de Add-on ZAP (OK, así que es un proyecto de código de Google llamado zap-extensiones, pero usted consigue la idea).
Lo más importante puede ahora navegar, descargar e instalar los add-ons de dentro de ZAP. Más complementos pueden dinámicamente instalar (y desinstalar) así que wont incluso necesario un reinicio.
Usted puede ser notificado de actualizaciones e incluso se actualiza automáticamente. Y como las normas de exploración se implementan ahora como add-ons puede obtener las últimas normas tan pronto como son publicados.

### Un reemplazo para la Spider 'estándar' ###

La ‘old’ Spider estaba mostrando su edad, por lo que su estado completamente reescrita y es mucho más rápida y más completa que la anterior. Esto sigue siendo una spider 'tradicional' que analiza el código HTML para los enlaces que puede encontrar.

### Una nueva spider 'Ajax' ###

Además de la 'traditional' spider hemos añadido una araña de Ajax que es más eficaz con las aplicaciones que hacen un uso intensivo de JavaScript. Esto utiliza el proyecto Crawljax, que controla un navegador (utilizando Selenium) y, por lo tanto, puede descubrir los enlaces que genera una aplicación, incluso los generados por el lado del cliente.

### Soporte de Web Socket ###

ZAP ahora admite WebSockets, ZAP ahora puede ver todos los mensajes de WebSocket enviado a y desde tu navegador. Como mensajes HTTP basado, ZAP también puede interceptar los mensajes de WebSocket y permite cambiar sobre la marcha.
También puede pelusa WebSockets mensajes así todas las cargas fuzzing incluidas en ZAP de proyectos como JBroFuzz y fuzzdb. Y por supuesto usted puede añadir fácilmente sus propios archivos de fuzzing.

### Inicio Rápido ###

El primer principal ficha que verá es un 'Quick Start' que le permite al tipo solo en una dirección URL y escanear con un solo clic.
Este es un punto de partida ideal para las personas nuevas a la seguridad de la aplicación, pero expertos fácilmente pueden eliminar si encuentra distracción.

### Conciencia social ###

ZAP es ahora mantener conciencia de sesión, por lo que puede reconocer ZAP vía de múltiples sesiones. Le permite crear nuevas sesiones, alternar entre ellos y se aplica a todos los otros componentes, como la araña y el explorador activo.

### Contextos definidos por el usuario ###

Ahora puede definir cualquier número de 'contextos' - relacionados con conjuntos de direcciones URL que componen una aplicación. Entonces pueden dirigirse todas las URLs en un contexto, por ejemplo usando la araña o el explorador activo. También puede añadir los contextos en el ámbito de aplicación y asociar otros datos, como los datos de autenticación.

### Sesión detenida ###

El alcance de sesión le permite especificar qué contextos está interesado en cualquier momento. Puede restringir lo que ves en varias pestañas a sólo las URL en alcance y evitar que accidentalmente ataca las URLs no en alcance usando el modo protegido.

### Diferentes modos de ###

ZAP ahora soporta 3 modos:

 *  Caja de seguridad, en los que no hay operaciones potencialmente peligrosas permite
 *  Protegidas, en el que puede realizar cualquier acción en las URLs en el ámbito
 *  Estándar, en la que usted puede hacer cualquier cosa para cualquier URL

### Error de autentificación ###

Ahora puede asociar datos de autenticación en cualquier contexto, que permite ZAP hacer cosas como detectar si está conectado y automáticamente usted nuevamente en registro. Esto es especialmente útil cuando se utiliza mediante la API de seguridad pruebas de regresión.

### Más apoyo de la API ###

La API de REST se ha ampliado significativamente, dándole mucho más acceso a la funcionalidad ZAP proporciona.

### Controles de exploración granos finos ###

Las normas de exploración activo ahora pueden ser afinadas para ajustar su fuerza (el número de ataques que realizan) y el umbral en el cual reportan problemas potenciales.

### Nuevo y mejorado de activo y pasivo análisis de las normas ###

Hemos subido los resultados de la ejecución de ZAP 2.0.0 contra wavsep (el más completa evaluación proyecto de código abierto que conocemos) a la wiki de ZAP: https://github.com/zaproxy/zaproxy/wiki/Testing TODO ;)

## Lista completa de cambios: ##

### Problema 43: Opción para el filtrado del alcance ###

### Número 163: Explorador activo falta contra DVWA \[altos falsos positivos/verdaderos negativos tasa\] ###

### Tema 175: Lista de palabras de fuerza bruta mejor ###

### Número 240: SocketException mientras fuzzing no maneja correctamente. ###

### Edición de 278: Certificado de CA raíz dinámica SSL no válido en algunas plataformas debido a la extensión ExtendeKeyUsage ###

### Edición 281: Clase alerta dependencia JSON ###

### Emisión 299: Solicitud característica: Mostrar conteo de URIs encontrados durante la araña ###

### Número 305: Regla de escáner pasivo comentarios sospechosos como TODO y FIXME ###

### : 326 tiempo de respuesta y longitud total de solicitud manual ###

### Problema de 330: robots.txt análisis ###

### Número 332: Soporte para los modos ###

### Número 333: Spider - se agrega opción para rastrear todo en el ámbito ###

### Edición 335: Web Sockets - añadido soporte para los modos y alcances ###

### Número 342: Añadir un HttpSenderListener ###

### Número 350: Administración de autenticación ###

### Número 354: Cadenas de ataque Fuzzer no se muestra ###

### Número 356: Generar formulario de test de CSRF ###

### Número 358: Error en la solución de 'XFO encabezado no Set' ###

### Tema 360: directorios de sub fuerza bruta ###

### Número 361: getHostPort en HttpRequestHeader solicitudes HTTPS conexión devuelve el puerto mal ###

### Número 370: API - guardar sesión, mejor manejo de errores ###

### Problema 374: API: guarde la sesión sincrónica o proporcione el estado ###

### Número 376: Enmascarar las contraseñas para la autenticación ###

### Número 385: Contextos de apoyo ###

### Número 386: API Web interfaz de usuario - ayuda de parámetros con vistas ###

### Edición 388: Que el usuario pueda especificar qué tecnologías aplicarán a un contexto ###

### Edición 390: Spider - añadir opción a araña todo en el contexto ###

### Número 391: ZAP mejoras en el rendimiento ###

### Número 393: Más enlaces en línea del menú ###

### Edición 397: Apoyo semanal construye ###

### Número 400: Generar nuevos CA certificado producirá siempre certificado con el mismo número de serie ###

### Número 401: Excepción cuando la Spider (nueva) se inicia a través de la API ###

### Número 402: GUI se muestran etiquetas de no correctamente en Linux (cuando idioma polaco) ###

### Problema 403: Definir las opciones mediante la API utilizando la reflexión ###

### Problema 404: Etiquetas no aparece cuando se elige la lengua persa ###

### Número 406: Spider - se agrega opción para controlar el efecto de los parámetros de las URL visitadas ###

### Problema 410: conjunto de caracteres en Comillas ###

### Número 411: Permitir puerto de proxy para especificar en la línea de comandos ###

### Número 417: IndexOutOfBoundsException de ExtensionHttpSessions en modo demonio ###

### Edición 419: Reestructurar jarra código de carga ###

### Número 420: API - apoyo absoluto sesión caminos ###

### Edición 421: Cerrar limpiamente cualquier subprocesos de análisis activa en paro ###

### Número 422: Utilizar exec en zap.sh para que un nuevo proceso no es bifurcado ###

### Edición 423: Araña y explorador activo pueden interbloqueo si ZAP está apagado mientras se están ejecutando ###

### Edición 424: Excepciones en Web Sockets cuando abrió sesión ###

### Número 425: Añadir pestaña Inicio rápido ###

### Edición 428: ZAP apoyo mercado ###

### Número 429: Enlace activo exploración mediante API explora más que la dirección URL especificada ###

### Número 433: API: introducir parámetros obligatorios y descripciones opcionales ###

### Edición 435: Exploración activa alertas pueden ser "lost" después de guardar la sesión ###

### Edición 436: Bloqueo en sesión guardar o apagado mediante la API ###

### Número 438: Mejoras de la API ###

### Edición 441: Vista iniciada incorrectamente en muchos lugares estando en "daemon mode" ###

### Edición 443: "No Anti-CSRF tokens were found in a HTML submission form" como "None. Warning only." ###

### Edición 446: Claves de un proveedor registrado de PKCS \#11 no se recuperan si ya se ha registrado un proveedor de PKCS \#11 ###

### Número 447: Destacar ataque al mostrar alertas ###

### Problema 448: Cambie el nombre de Brute Force ext a Forced Browse y agregue URL al árbol ###

### Problema 449: Falta la página de ayuda para el panel "Extensiones" en el diálogo "Opciones" ###

### Problema 451: la comprobación manual de actualizaciones no funciona correctamente en las versiones semanales más recientes ###

### Problema 453: carga y descarga dinámica de complementos ###

### Problema 455: dividir fuzzbd en un nuevo complemento ###

### Problema 456: sesión de Spider manejando tweeks ###

### Problema 457: Soporte de la tecla de flecha de la pestaña de búsqueda ###

### Problema 459: bloqueo activo del escáner ###

### Problema 460: agregue un diálogo de progreso de escaneo ###

### Problema 461: Agregue el archivo de ayuda para el complemento de Inicio rápido ###

### Problema 462: Revisión: revisión / revisión: SSLSocketFactory con TLS habilitado y opciones de cifrado predeterminadas ###

### Problema 466: Mueva la extensión Port Scan al proyecto de extensiones ZAP ###

### Problema 468: Actualice la regla de inyección SQL para 'release' ###

### Problema 469: permitir que se agregue y elimine el token anti csrf a través de la API ###

### Problema 466: Mueva la extensión Port Scan al proyecto de extensiones ZAP ###

### Problema 472: Spider accede al panel de la interfaz de usuario en modo daemon ###

### Problema 473: Permitir complementos para eliminar vistas / componentes agregados a los paneles de mensajes ###

### Problema 474: Promueva un inicio rápido para liberar el estado ###

### Problema 478: Permitir elegir enviar las cookies administradas de ZAP en un solo encabezado de solicitud de Cookie y establecerlo como el predeterminado ###

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