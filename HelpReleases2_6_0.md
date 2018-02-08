# Release 2.6.0 #

Esta versión contiene un gran número de cambios, en particular a la API de ZAP.
Hemos añadido un número significativo de nuevos endpoints API, trabajando hacia nuestro objetivo de hacer totalmente controlable mediante la API de ZAP. También hemos cambiado algunos de los puntos finales existentes y en todos los casos estos cambios son compatibles.

El lanzamiento también incluye un nuevo complemento de JxBrowser así como webdrivers específicos de plataforma para que sea aún más fácil interactuar con ZAP a través de una amplia variedad de navegadores.

## Cambios de seguridad API ##

Hemos cambiado la seguridad de la API en respuesta a los problemas registrados a nosotros a través de nuestro [programa de recompensas de error][]. Detalles de las vulnerabilidades se indican a continuación.
Los cambios de seguridad son por necesidad no compatible, aunque hemos incluimos opciones para deshabilitarlos Si utilizas ZAP en un entorno seguro.

Por defecto todas las llamadas API requieren ahora la API key o un valor nonce. Estos pueden ser suministrados a través de parámetros de URL, parámetros POST o encabezados. Los clientes de ZAP API soportados (incluyendo Java y Python) se han actualizado para suministrar la clave de la API a través de una rúbrica. Nonces son generados por ZAP y están destinados a ser utilizados por complementos ZAP que necesitan tener acceso a la API de ZAP. Para más detalles ver la [pantalla de opciones de API][].

Hay un conjunto de nuevas opciones de API relacionadas con seguridad:

 *  Interfaz de usuario habilitado - si habilita la interfaz del API está disponible para todas las máquinas que son capaces de usar el ZAP como proxy. Esta opción está activada por defecto.
 *  Direcciones IP permiten utilizar la API - por defecto sólo la máquina ZAP está ejecutando es capaz de acceder a la API de ZAP. Puede permitir a otro acceso de máquinas a la API añadiendo patrones regex adecuado. Sólo debe agregar las direcciones IP que usted confía.
 *  No requieren una clave de API para las operaciones de seguras - si está habilitado, entonces la clave de la API no es necesaria para vistas u otras operaciones que se consideran 'seguros', en otras palabras las operaciones que no hacen cambios a ZAP. Este tipo de operaciones sin embargo acceso a datos ZAP como alertas, mensajes y rutas de sistema de archivos. También puede ser utilizados por aplicaciones web para detectar la presencia de ZAP.
 *  Informe de errores de permiso vía API - si habilitado entonces ZAP informe de errores de permiso a través de la API, que puede ser utilizado por aplicaciones web para detectar la presencia de ZAP. Esto no es un problema serio en un ambiente seguro pero si usas ZAP contra sitios potencialmente dañinos entonces usted debe no habilitarla.

Todas las opciones de ZAP pueden ser especificado a través de la línea de comandos al iniciar ZAP - ver la [API Key FAQ][] Mostrar más detalles
También hemos añadido aún más cabeceras de seguridad a la API, incluyendo una política de seguridad de contenido fuerte.

## Mejoras: ##

 *  Problema 368: API: URL de informe que acaba de encontrar Spider
 *  Problema 689: mejorar la gestión del alcance
 *  Problema 958: identificación de la versión de Java cuando se exporta una variable de entorno para Java
 *  Problema 1853: Permitir el análisis activo de un contexto a través de la API de ZAP
 *  Problema 1952: No permita contextos con el mismo nombre
 *  Problema 2117: establecer / actualizar el umbral y la fuerza predeterminados para una política de escaneo
 *  Problema 2334: Habilite la búsqueda en los complementos ZAP.
 *  Número 2415: Mostrar la razón por qué se saltó un escáner activo
 *  Problema 2559: No limpie sesiones no guardadas (basadas en archivos)
 *  Problema 2570: opción de cambio de proxy para eliminar la codificación no compatible
 *  Problema 2592: diferenciar la fuente de alertas
 *  Problema 2611: Cambiar los diálogos de puntos de interrupción HTTP a modal
 *  Problema 2633: Mejora del selector de archivos certificados por el cliente
 *  Issue 2647 : Support a/pscan rule configuration
 *  Problema 2655: proporcione un motivo de omisión para las reglas de exploración activa de scripts
 *  Problema 2682: ordenar (principal) ayuda add-on TOC entradas
 *  Problema 2690: Soporte para ignorar formularios especificados cuando se buscan vulnerabilidades de CSRF
 *  Emisión 2699: Solicitud mejora: mejorar el manejo de errores de falta de negociación de SSL
 *  Emisión 2701: Solicitud mejora: de fábrica
 *  Número 2723: Apoyar las solicitudes POST de acciones de la API
 *  Número 2728: Permiten para quitar filtros y analizadores de spider
 *  Número 2742: Permiten la anulación/personalización del valor de "networkaddress.cache.ttl" de Java
 *  Problema de 2750: Añadir un CSP razonablemente fuerte a la API
 *  Número 2773: Uso UTF-8 para leer/escribir scripts ZAP
 *  Número 2782: Apoyo el parámetro de línea de comandos - archivo de configuración
 *  Número 2825: Comentario adicional para las plantillas de JS
 *  Problema 2853: Información alerta anulación
 *  Número 2855: Funcionalidad de pausa apoyo en la API
 *  Número 2865: Normalizar paneles de contexto de inclusión/exclusión
 *  Número 2886: Opción para generar reportes en formato Markdown
 *  Número 2891: Mostrar a la causa por qué no se cargó una secuencia de comandos
 *  Número 2936: Siempre ponga mem Java 1/4 disponible (más de 512Mb)
 *  Tema 2937: Cambio ZAP API para lectura y uso del cuerpo de la solicitud
 *  Número 2939: Uso no absoluta URI base elemento HTML de spider
 *  Número 2951: Apoyo activo exploración exploración y regla máximo duración
 *  Número 2954: Permite exportar un contexto a través del menú de contexto
 *  Número 2966: Uso L & F especificado mediante args JVM
 *  Número 2970: Permiten para configurar, por el tipo de secuencia de comandos, el estado habilitado de nuevo/cargado de scripts
 *  Número 2982: Permite para desactivar el registro de salida estándar por defecto
 *  Número 2994: Mostrar columna 'Tamaño o cuerpo' de la historia en bytes
 *  Número 3004: Permiten la exploración pasiva sólo mensajes HTTP en el ámbito
 *  Número 3028: Generador de valor (previamente formulario de manejo)
 *  Problema de 3038: Volver tipo de solicitud a través de la API de ZAP
 *  Número 3042: Permiten para seleccionar varios parámetros en la ficha parámetros
 *  Número 3050: Devolver marca de hora/RTT de las solicitudes a través de la API de ZAP
 *  Número 3058: Permite configurar los dominios siempre en el ámbito de la araña (Spider API)
 *  Número 3061: Permiten para descartar extremos de API
 *  Número 3069: Parámetro estructural contexto sólo acepta gráficos alfanuméricos
 *  Número 3079: Cookie agregado ignorar lista regla y inc sueño por defecto a 20 para reducir FPs
 *  Edición : 3081 cambiar tiempo por defecto para 15 y hacer accesibles al público
 *  Número : 3090 ser más Clemente en formato de nombre de archivo de agregar-en el
 *  Número 3098: Registro presentar aunque ZAP se ejecuta 'inline'
 *  Problema de 3118: incluir extensión subjectAlternativeName en certificados generados
 *  Número 3123: Anotaciones mayor seguridad para formas que no necesitan anti token CSRF
 *  Número 3130: Agregado autoupdate API llamadas
 *  Número 3149: Línea de base: problemas en curso y archivo de contexto de la ayuda
 *  Número 3159: Permitir esc cerrar el diálogo de mercado
 *  Problema de 3163: Selección automática importado certificado
 *  Número 3176: Permite mostrar más datos de la solicitud en la pestaña historial
 *  Número 3195: Agregar solución al proxy local para emulador de Android
 *  Número 3226: Opción API key o nonces mediante Rúbrica
 *  Número 3227: Direcciones de IP de acceso límite API a lista blanca
 *  Tema 3229: Usar la Directiva de referente en ZAP API
 *  Tema 3232: Active Scan API - permite iniciar el análisis con nodos no hoja
 *  Número 3238: Agregar controlador entradas para Smartcards virtuales CSPid
 *  Problema de 3261: Cliente certificado PKCS \#11 - interfaz de usuario de excepciones
 *  Número 3285: Editar alerta mejoras
 *  Número 3290: Mostrar las peticiones con errores I/O en ficha de araña
 *  Número 3296: Crear directorios de secuencia de comandos al inicializar el directorio de inicio
 *  Número 3297: Start proxy local después de procesar los argumentos de línea de comandos en modo daemon

## Corrección de error: ##

 *  Edición 1107: Comentario adicional necesario para Script plantillas/ejemplos
 *  Edición 1152: Pasivo CSRF Sensor informes falta CSRF fichas para todas las formas, no sólo POST pide falta Anti CSRF Tokens
 *  Número 1212: Falsos positivos en pruebas de SQLi
 *  Número 2176: Sean durante zapbot WAVSEP analiza
 *  Problema 2218: Sesiones persistentes no guardar sin configurar el contexto por defecto
 *  Problema de 2546: ZAP acceder a URLs que están fuera de alcance
 *  Número 2550: GUI se congela al abrir el diálogo de progreso de la exploración
 *  Número 2561: Uso UTF-8 para escribir el informe HTML
 *  Edición 2578: Menor problema de usabilidad: debe hacer clic en texto en la columna de opciones para seleccionar fila
 *  Número 2585: Eliminar solicitudes de secuencia temporales en sesión de limpieza
 *  Número 2586: Usa todas las peticiones de diálogo Active Scan
 *  Número 2605: Evitar caída del GUI al agregar mensajes a la historia
 *  Número 2608: Quitar un DDN desde un contexto no parecen desencadenar una actualización de la ficha de sitios
 *  Número 2637: Evitar que UI API se carguen en un marco
 *  Número 2642: Rueda de ratón lento desplazamiento en árbol de sitio
 *  Número 2657: Persistencia correcta de extensiones con discapacidad
 *  Número 2674: Automatizar las solicitudes de autenticación se muestra en la pestaña de sesiones HTTP
 *  Problema 2681: corrección de excepción al agregar script a través de la API
 *  Problema 2694: Posibilidad de establecer los parámetros excluidos de la API
 *  Problema 2696: habilite el elemento del menú emergente Copiar URL para todos los mensajes
 *  Problema 2707: la instalación manual de complementos necesita mensajes de diálogo más significativos
 *  Número 2735: Wiki: ModesAndScope no cubre a modo de ataque
 *  Edición 2736: Error: no se puede generar informes de datos de sesión guardados
 *  Número 2737: API correcta mensaje de error faltan parámetros de script
 *  Número 2745: Spider excepción cuando sitemap.xml no encontrado
 *  Número 2748: ZAP Spidering HTML formularios con múltiples botones de envío
 *  Número 2757: Alertas con el método de petición se consideran el mismo
 *  Número 2774: Valor incorrecto que se muestra en la ubicación de la pelusa para cuerpo del texto cuando se selecciona a través de la vista combinada
 *  Problema de 2792: Capaz de superponer lugares pelusa (HTTP)
 *  Número 2793: Mal destacar en vista combinada con la última parte del encabezado de solicitud
 *  Número 2810: Alertas activa escáneres persistieron dos veces cuando con GUI
 *  Número 2836: ZAP hsqldb OutOfMemoryError al eliminar registros de limpieza
 *  Número 2862: XSS en url de la página sin parámetros que no se encuentran
 *  Tema 2874: Cálculo offset correcto vistas de cabecera de texto
 *  Número 2898: Analizador de spider un Tweak faja omitir paréntesis emparejados en URLs
 *  Número 2935: Charset incorrecto utilizado en el cuerpo de la respuesta si ningún conjunto de conjunto de caracteres
 *  Tema 2977: HTTP500 de JSON/httpSessions/vista/sesiones /? sitio = FOO
 *  Número 3002: Representar correctamente todos los nodos en el árbol de la casilla de verificación
 *  Número 3041: Solucionar problemas de concurrencia cuando se publican eventos ZAP
 *  Número 3052: Corregir la carga de estado habilitado de extensiones
 *  Número 3054: Claro viejo contextos, siempre, cuando se carga una sesión de
 *  Número 3073: Skip procesar mensajes automatizados para la pestaña de sesiones HTTP
 *  Número 3100: Contexto en cambio alcance podría no aplicarse
 *  Número 3142: Mostrar correctamente parámetros excluidos a través de API de ZAP
 *  Número 3157: Sesión comparación excepción
 *  Número 3175: Cancelar/Guardar StandardFieldsDialog en la tecla escape
 *  Número 3192: Direcciones URL incluidas en contexto son ignoradas por la araña
 *  Número 3211: No se encuentra. ZAP\_JVM.properties con %HOMEPATH% cuando se utiliza zap.bat en windows
 *  Cuestión 3215: Diálogo de filtro de la historia no puede ser escalado
 *  Número 3221: Algunos iconos que no se escala correctamente
 *  Número 3224: Inyección de HTML en la pestaña de "Alert"
 *  Número 3275: Global excluir URL (beta) - después de cerrar y volver a abrir no recoge añadido regex para excluir URLs
 *  Tema 3278: Reset proxy excluir URLs en nueva sesión
 *  Número 3309: Mejorar la enumeración de nodos en la fase de pre-exploración del
 *  Número 3320: Creación correcta de las semillas de spider Git/SVN
 *  Problema de 3330: Aplicar configuración argumentos en el orden especificado

## ZAP API cambia criterios de valoración: ##

### Ascan de acción de la exploración ###

El parámetro de url ahora es opcional y se ha añadido un parámetro opcional contextId. Debe suministrar uno de estos.

### ACCIÓN ascan / scanAsUser ###

Los parámetros url y contextId ahora son opcionales. Debe suministrar uno de estos.

### ACCIÓN ascan / addScanPolicy ###

Agregado alertThreshold y attackStrength los parámetros opcionales.

## ZAP API nuevas terminales: ##

### Ver ascan / optionMaxRuleDurationInMins ###

Devuelve el tiempo máximo en minutos que una regla de exploración puede funcionar para, cero es ilimitado.

### Ver ascan / optionMaxScanDurationInMins ###

Devuelve el tiempo máximo en minutos que puede ejecutar un análisis completo para, cero es ilimitado.

### ACCIÓN ascan / setOptionMaxRuleDurationInMins ###

Establece el tiempo máximo en minutos que una regla de exploración puede funcionar para, cero es ilimitado.

### ACCIÓN ascan / setOptionMaxScanDurationInMins ###

Establece el tiempo máximo en minutos que puede ejecutar un análisis completo para, cero es ilimitado.

### ACCIÓN ascan / updateScanPolicy ###

Se actualiza la política de exploración especificado con el alertThreshold especificado o attackStrength.

### Rotura de vista / isBreakAll ###

Devuelve True si ZAP se romperá en solicitudes y respuestas.

### Rotura de vista / isBreakRequest ###

Devuelve True si ZAP se romperá en las peticiones.

### Rotura de vista / isBreakResponse ###

Devuelve True si ZAP se romperá en las peticiones.

### Rotura de vista / httpMessage ###

Devuelve el mensaje HTTP actualmente interceptado (si existe).

### Rotura de acción / romper ###

Controla la funcionalidad de rotura global. El tipo puede ser uno de: http-all, solicitud http o http de respuesta. El estado puede ser verdadero (para encender el descanso para el tipo especificado) o false (para desactivación de rotura). Ámbito de aplicación no se utiliza actualmente.

### Rotura de acción / setHttpMessage ###

Sobrescribe el mensaje actualmente interceptado con los datos suministrados.

### Rotura de acción / continuar ###

Envía el mensaje actualmente interceptado y unsets los puntos de rotura de petición/respuesta.

### Rotura de acción / paso ###

Envía que el mensaje actualmente interceptado, la siguiente solicitud o respuesta automáticamente ser interceptada.

### Rotura de la acción / de la gota ###

Cae el mensaje actualmente interceptado.

### Núcleo de vista / optionDnsTtlSuccessfulQueries ###

Obtiene el TTL (en segundos) de éxito consultas DNS.

### Núcleo de acción / sendRequest ###

Envía la solicitud HTTP, opcionalmente después de redirecciones. Devuelve la solicitud y la respuesta recibieron y seguido de redirecciones, si cualquier. El modo se aplica al enviar la solicitud (y después de redirecciones), solicitudes manual personalizadas no se permitieron en modo 'Seguro' ni modo 'Protegido' si está fuera de alcance.

### Núcleo de acción / setOptionDnsTtlSuccessfulQueries ###

Establece el TTL (en segundos) de éxito consultas DNS (se aplica después de reiniciar de ZAP).

### OTRO núcleo / mdreport ###

Genera un informe en formato Markdown.

### HttpSessions vista / centros ###

Obtiene todos los sitios que tienen sesiones.

### Pscan vista / scanOnlyInScope ###

Dice si o no la exploración pasiva debe realizarse sólo en los mensajes que están en el ámbito.

### Pscan acción / setScanOnlyInScope ###

Establece o no la exploración pasiva debe realizarse sólo en los mensajes que están en el ámbito.

### Vista Spider / allUrls ###

Devuelve una lista de URL únicas de la tabla de historia basada en HTTP mensajes añadidos por el spider

### Vista Spider / optionMaxChildren ###

No obtiene al número máximo de nodos secundarios (por nodo) que puede ser rastreado, 0 significa límite.

### Acción spider / setOptionMaxChildren ###

No establece al número máximo de nodos secundarios (por nodo) que puede ser rastreado, 0 significa límite.

## Detalles de la vulnerabilidad ##

Las siguientes vulnerabilidades se han divulgado en las versiones anteriores de ZAP. Otros problemas menos graves han sido también fijo como una obviedad.
Muchas gracias a todos los investigadores que éticamente nos han comunicado estos problemas a través de nuestro [Programa de recompensas de error][programa de recompensas de error]. Si usted necesita más detalles acerca de cualquiera de estas vulnerabilidades entonces póngase en contacto con nosotros.

### RCE vía formulario de Test de CSRF y divulgación del API Key ###

Si el usuario utiliza el formulario de prueba Anti CSRF contra una página HTML especialmente diseñada se filtró el API key para ese sitio. El sitio podría entonces acceder a la API de ZAP y realizar cualquier acción, incluyendo cargar scripts ZAP. Secuencias de comandos sólo pueden cargarse de filesystems 'locales' pero si el usuario ejecuta ZAP en Windows entonces el atacante puede hacer un script malicioso disponible a través de una participación pública de SMB. Esto parece ZAP a ser un archivo local y el guión por lo tanto está cargado y se puede ejecutar mediante la API.
El requisito para la API key o nonce en todas las operaciones de la API son el resultado directo de esta vulnerabilidad, como están cambiando complementos para utilizar nonces para reducir el riesgo de escaparse el API key.

**Crédito: Artemy Bogdanov (@Abr1k0s)**
Artemy recibió una recompensa de $1000 errores como resultado de esta presentación. Este es el primer bounty bug que hemos pagado hacia fuera - Felicidades la Artemy!

### Windows Installer Vulnerable a DLL Hijacking ###

El instalador de Windows ZAP para todas las versiones incluyendo la 2.5.0 son vulnerables al secuestro de DLL en Windows 7 (y versiones anteriores). Se trata de una vulnerabilidad en el 3 º en instalador InnoSetup de partido. La 2.6.0 que instaladores (en todas las plataformas) ahora se generan usando Install4J.

Si por alguna razón usted necesita instalar las versiones anteriores de ZAP en Windows 7 o versiones anteriores, entonces recomendamos que mueva al instalador en un directorio limpio antes de ejecutarlo.

Nota Burp Suite también utilizar Install4J así futuras vulnerabilidades en instaladores de Install4j generado pueden ser elegibles para el programa de recompensas de error Burp Suite: https://hackerone.com/portswigger

**Fotografía: James Kettle (Burp Suite)**

### Ejecución de código arbitrario a través de invocar aplicaciones parámetro inyección ###

Los parámetros de HTML podrían elaborarse específicamente para provocar la ejecución de código arbitrario, si el usuario elige invocar la aplicación de destino con una solicitud que contenga ese parámetro desde dentro de ZAP.
El complemento Aplicaciones de Invocar se ha actualizado para solucionar este problema: todos los usuarios de ZAP deben instalar esta nueva versión antes de continuar utilizando el complemento.

**Crédito: Artemy Bogdanov (@Abr1k0s)**

### XSS via Anti CSRF Test Form ###

El formulario de prueba de Anti CSRF era vulnerable a los ataques XSS si se ejecutaba contra una página HTML específicamente diseñada.
La API ahora usa una sólida Política de seguridad de contenido para evitar tales problemas

**Credit: g\_sato - [https://bugcrowd.com/g\_sato][https_bugcrowd.com_g_sato]**

### API Vulnerable a DNS Rebinding ###

La API era vulnerable a los ataques de reenlace de DNS. Ahora comprueba el encabezado del host y rechaza cualquier solicitud de hosts inesperados.

**Credit: Artemy Bogdanov (@Abr1k0s)**

## Véase también ##

<table> 
 <tbody>
  <tr>
   <td>&nbsp;&nbsp;&nbsp;&nbsp;</td>
   <td><a href="HelpIntro" rel="nofollow">Introducci&oacute;n</a></td>
   <td>Introducci&oacute;n a ZAP</td>
  </tr> 
  <tr>
   <td>&nbsp;&nbsp;&nbsp;&nbsp;</td>
   <td><a href="HelpReleasesReleases" rel="nofollow">Lanzamientos</a></td>
   <td>el conjunto completo de los comunicados de</td>
  </tr> 
  <tr>
   <td>&nbsp;&nbsp;&nbsp;&nbsp;</td>
   <td><a href="HelpCredits" rel="nofollow">Cr&eacute;ditos</a></td>
   <td>las personas y grupos que han hecho posible esta versi&oacute;n</td>
  </tr> 
 </tbody>
</table>


[programa de recompensas de error]: https://bugcrowd.com/owaspzap
[pantalla de opciones de API]: HelpUiDialogsOptionsApi
[API Key FAQ]: https://github.com/zaproxy/zaproxy/wiki/FAQapikey
[https_bugcrowd.com_g_sato]: https://bugcrowd.com/g_sato