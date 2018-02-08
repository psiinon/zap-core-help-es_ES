# Release 2.3.0 #

Se hicieron los siguientes cambios en esta versión:

## Cambios significativos: ##

### Versión ZAP 'lite' ###

Para este lanzamiento estamos ofreciendo un *'lite'* versión de ZAP además la *‘full’* versión: Contiene exactamente el mismo código de base, pero sólo incluye menos complementos por defecto. Por supuesto, puede descargar todos los complementos 'desaparecidos' desde el marketplace ZAP ' actualizar ' la versión lite a un completo.
Se mostrará la *‘lite’* versión está dirigida a personas nuevas a la seguridad que necesitan menos funcionalidad inicial que se espera que sea más fácil empezar con. También será conveniente para gente que busca una descarga de menor tamaño o aquellos que deseen personalizar exactamente qué complementos instale.

### Apoyo a eventos del lado del cliente (navegador) ###

Ahora puede ver, interceptar, manipular, reenviar y difuminar **client-side events**. Esto incluye postMessages, por lo que ahora puede detectar vulnerabilidades XSS basadas en DOM en postMessages. Se trata de la primera fase de una serie de cambios planificados para la prueba de aplicaciones AJAX y HTML5 aún más eficaz.

### Soporte de autenticación mejorado ###

El soporte de ZAP para la autenticación ha sido completamente renovado para manejar fácilmente tipos complejos de **authentication methods and scenarios**. También se ha agregado soporte para scripts definidos por el usuario que le permiten manejar esquemas de autenticación personalizados. Además, ahora ZAP entiende y le permite configurar **web applications' Users** por lo que desde el punto de vista de los usuarios definidos se pueden realizar varias acciones a lo largo de ZAP. Para empezar, echa un vistazo al nuevo *Autenticación* y en la *Users* paneles en las propiedades de sesión para cada uno de los contextos definidos.

### Soporte para aplicaciones no estándar ###

Esta versión incluye soporte para **‘single page’ applications** y en la **non standard key-value separators**. Ahora puede controlar esta configuración a través de la nueva *Structure* panel en las propiedades de la sesión.

### Nuevos vectores de entrada incluyendo secuencias de comandos definida por el usuario ###

ZAP admite nuevas opciones para definir la **input vectors** es decir, los elementos de una solicitud que ZAP atacará. Las nuevas opciones están disponibles en la *Active Scan Input Vectors* panel de las Opciones. También se ha agregado soporte para definir scripts personalizados que definen nuevos vectores de entrada.

### Análisis de políticas - control de grano fino ###

La política de exploración ahora tiene un **fine grained control**, lo que le permite ajustar las reglas individuales del escáner. También puede definir, cargar y guardar políticas de análisis, lo que le permite mantener un conjunto de políticas que funcionan bien en diferentes circunstancias.
Además, por defecto ZAP no ahora analizará parámetros de servicio bien conocido (e.g. \_\_VIEWSTATE) acelerar el proceso general de análisis. Esto es totalmente usuario configurable, lo que le permite especificar exactamente qué parámetros ZAP debe pasar por alto.

### Diálogo activo exploración avanzada ###

Un nuevo *Diálogo activo exploración avanzada* cuadro de diálogo permite especificar exactamente cómo desea que el explorador activo para funcionar. Permite especificar **‘custom vectors’** definir explícitamente que cadenas quieres atacar. También soporta la opción de escanear como cualquiera de los usuarios ha definido para la aplicación sometida a prueba. Iniciar un *Advanced Active Scan* via the *Herramientas* menu or via the *Atacar* sección de la derecha Haz clic en el menú emergente.

### Opciones de línea de comando extendido ###

Ahora puede ejecutar ZAP 'inline' es decir **without starting the ZAP UI or a daemon**. En este modo, puede ejecutar ataques simples o ejecutar scripts que pueden acceder a todas las funciones de ZAP. Ahora también puede reemplazar cualquiera de las opciones definidas en el archivo de configuración a través de parámetros de línea de comandos.

### Más apoyo de la API ###

La API se ha ampliado para apoyar aún más la funcionalidad de ZAP.

### Archivo de ayuda internacionalizado ###

El archivo de ayuda se ha internacionalizado y está en proceso de traducción a muchos otros idiomas a través de https://crowdin.net/project/owasp-zap-help. Si usa ZAP en uno de los muchos idiomas que admitimos, los archivos de ayuda incluirán todas las traducciones disponibles para ese idioma, y ​​volverán al inglés de forma predeterminada para las frases que aún no se hayan traducido.
Los idiomas con una cantidad significativa de páginas de ayuda traducidas incluyen:

 *  Bosnio
 *  Francés
 *  Japonés
 *  Español

### Accesos directos del teclado ###

Todos los elementos del menú ahora se pueden invocar mediante atajos de teclado. Los valores predeterminados se definen para prácticamente todos los casos, pero puede configurar sus propias preferencias en *Teclado* panel de las Opciones.

### Opciones de noticias ###

Hay una nueva opción para cambiar la pantalla de modo que la pestaña seleccionada ocupe el **full screen**. Esto es útil cuando se usa ZAP en pantallas pequeñas. También hay una opción para **alternar la visibilidad de los nombres de las pestañas** en un apagado para ahorrar aún más espacio.

La mayoría de las listas de IU también se han convertido en tablas, lo que le permite cambiar el ancho de las columnas y definir exactamente qué columnas se muestran y cómo se ordenan las tablas.

### Mayor funcionalidad movida a complementos ###

La mayor parte de la funcionalidad básica se ha trasladado a complementos que nos permiten entregar actualizaciones dinámicamente a través del ZAP Marketplace en lugar de requerir nuevas versiones completas.
Esto incluye los paquetes de idiomas, por lo que las traducciones realizadas a la interfaz de usuario de ZAP a través de https://crowdin.net/project/owasp-zap pueden descargarse dentro de ZAP o incluso instalarse automáticamente.

### Nuevo y mejorado de activo y pasivo análisis de las normas ###

Muchas de las reglas de escaneo activo y pasivo de calidad de lanzamiento se han mejorado. Hay nuevas reglas de calidad alfa y beta y se han promovido muchas reglas de alfa a beta y de beta a calidad de lanzamiento.

### Otros cambios y adiciones varios ###

 *  Una nueva opción para detener las reglas de escaneo individuales sin detener todo el escaneo
 *  Un nuevo botón en la barra de herramientas que le permite grabar rápida y fácilmente las secuencias de comandos de Zest.
 *  Se ha creado un nuevo grupo para compartir scripts ZAP ([ https://groups.google.com/group/zaproxy-scripts ).][https_groups.google.com_group_zaproxy-scripts _.]
 *  La capacidad de arañar aplicaciones basadas en metadatos de control de origen (SVN y Git) expuestos a través de un servidor web
    
    La capacidad de forzar saltos desde las secuencias de comandos Proxy

[Lista completa de cambios:

Problema 122: lecturas de tiempo de espera de registro ProxyThread con mensaje incorrecto (URL)

Problema 207: Mejora: Teclas de acceso rápido

Problema 362: Permitir que las listas de Alertas se filtren por selección en el panel Sitios

Problema 399: manejo del directorio zap.sh

Problema 412: habilitar la opción de renegociación SSL / TLS insegura no guardada

Problema 416: normalice cómo se administran múltiples opciones relacionadas a través de ZAP y mejore la usabilidad de algunas opciones

Problema 485: hacer paquetes de idiomas en complementos

Problema 503: Cambie las pestañas del pie de página para mostrar los datos con tablas en lugar de listas.

Problema 572: Cambie la propiedad generate\_root\_ca a una función en la API de Python

Problema 575: devuelva la lista de alertas en la API de Python en lugar de un diccionario con una entrada

Problema 585: Proxy - los errores "502 Bad Gateway" respondieron como "504 Gateway Timeout"

Problema 589: Extensión Move Reveal para el proyecto de extensiones ZAP

Problema 590: exploración forzada utiliza un esquema incorrecto al "atacar" un sitio al que se accede a través de una conexión segura (HTTPS) en un puerto no predeterminado

Problema 590: exploración forzada uso de un esquema incorrecto en "atacar" un sitio en el que se accede a través de una conexión segura (HTTPS) en un puerto no predeterminado

Problema 595: Spider no se puede iniciar (panel de pie de página) con un sitio al que se accede a través de una conexión segura (HTTPS) en un puerto no predeterminado

Problema 606: deshabilite el botón de escaneo "Inicio" cuando se selecciona la opción "--Seleccionar sitio--"

Problema 607: sitios solicitados manualmente que se muestran escaneados en los paneles del pie de página cuando se seleccionan en la pestaña "Sitios"

Problema 609: Proporcione una interfaz común para consultar el estado y acceder a los datos (HttpMessage e HistoryReference) que se muestran en las pestañas

Problema 613: Mueva la extensión Save Raw HttpMessage al proyecto de extensiones ZAP

Problema 613: Mueva la extensión Save Raw HttpMessage al proyecto de extensiones ZAP

Problema 613: Mueva la extensión Save Raw HttpMessage al proyecto de extensiones ZAP

Problema 783: el apagado debería ser un método en la aplicación python zap.core

Problema 788: actualización de la versión de Java para Mac

Problema 788: actualización de la versión de Java para Mac

Problema 799: Agregar HttpAuthentication como método de autenticación

Problema 803: revisión para /trunk/src/help/zaphelp/zaphelp/credits.html

Problema 804: agregue compatibilidad para varios tipos de autenticación para un contexto

Problema 804: agregue compatibilidad para varios tipos de autenticación para un contexto

Problema 806: Agregar soporte para usuarios de webapp

Problema 807: Error al cargar ZAP cuando se cierra la pestaña Inicio rápido

Problema 816: Agregar con el botón derecho Copiar / Pegar & amp; Encuentra opciones en el cuadro de diálogo Encode / Decode / Hash

Problema 817: Python API no maneja las "otras" operaciones correctamente

Problema 822: API de Java: ApiResponseSet.getAttributes () no funciona

Problema 825: versión anterior de Rhino incluida en el directorio lib

Problema 827: los tokens de sesión predeterminados no se envuelven con menor frecuencia cuando se agregan a través del diálogo de opciones

Problema 828: NullPointerException al acceder a la API HttpSessions ver "sessionTokens" cuando un sitio no existe o no tiene tokens

Problema 666: JSONException al llamar a una acción API sin los parámetros necesarios

Problema 830: API de cliente Java no codifica parámetros de consulta al enviar solicitudes a la API de ZAP

Problema 832: la pestaña Http Sessions debe borrarse cuando se crea una nueva sesión

Edición 837: Actualización, siempre, la solicitud HTTP enviada/adelante por proxy de ZAP

Tema 838: Búsqueda API - agregar vistas de búsqueda que devuelven mensajes HTTP

Número 839: Búsqueda API - agregar vistas de búsqueda que devuelven mensajes en formato de archivo HTTP

Número 840: Núcleo API - permiten para obtener los mensajes en formato de archivo HTTP

Número 841: NullPointerException después de enviar una solicitud HTTP manual con ExtensionHistory con discapacidad

Número 842: NullPointerException mientras escaneo activo con ExtensionAntiCSRF personas con discapacidad

Número 841: NullPointerException después de enviar una solicitud HTTP manual con ExtensionHistory con discapacidad

Número 844: NullPointerException al invocar el diálogo "Análisis política" con ExtensionPassiveScan con discapacidad

Número 845: AbstractPanel añadido dos veces para TabbedPanel2 en ExtensionLoader \#addTabPanel

Número 846: NullPointerException mientras escaneo activo con ExtensionScript personas con discapacidad

Número 846: NullPointerException mientras escaneo activo con ExtensionScript personas con discapacidad

Problema de 852: API de búsqueda - vistas de URL volver la misma URL varias veces

Número 853: Núcleo API - permite obtener el número de alertas

Número 853: Núcleo API - permite obtener el número de alertas

Número 855: Núcleo API - permite obtener un mensaje de ID

Número 856: Núcleo API - permite obtener una alerta por ID

Número 857: Núcleo API - vista "alertas" podría devolver alertas inesperados cuando se utiliza paginación

Número 857: Núcleo API - vista "alertas" podría devolver alertas inesperados cuando se utiliza paginación

Número 859: PScan API - permite para activar/desactivar la exploración pasiva

Problema de 860: PScan API - permiten para lista o conseguir los escáneres pasivos

Número 859: PScan API - permite para activar/desactivar la exploración pasiva

Número 862: PScan API - permite para activar/desactivar un escáner pasivo determinado

Problema de 860: PScan API - permiten para lista o conseguir los escáneres pasivos

Número 859: PScan API - permite para activar/desactivar la exploración pasiva

Número 859: PScan API - permite para activar/desactivar la exploración pasiva

Número 866: Alerta mantiene más de lo necesario cuando HistoryReference set/HttpMessage

Número 867: HttpMessage \#getFormParams debe devolver un TreeSet vacía si el cuerpo de la solicitud no es "x--www-form-urlencoded"

Número 868: Núcleo API - ver "mensajes" no devuelve mensajes de interna temporal

Número 869: Distinguir las solicitudes de proxy de las solicitudes de usuario (ZAP)

Problema de 870: Cambio el MainToolbarPanel de expandir botones ButtonGroup y acción

Tema 871: Título que no se actualiza cuando se cambia de nombre de la sesión mediante el botón de la barra de herramienta principal "Sesión propiedades..."

Número 872: Núcleo API - permite enviar una solicitud manual

Edición 873: Núcleo API - permite enviar una solicitud de manual en formato HAR

Número 874: BreakPanelToolbarFactory de cambio con acciones

Número 875: Eliminar directorio i18n

Número 876: Descartan FuzzerPanel \#PANEL\_NAME

Número 877: ExtensionPopupMenuItem \#isEnableForComponent llamado dos veces en algunos pop-up menús cada vez se muestra con el MainPopupMenu

Problema de 878: ExtensionPopupMenuItem\#getMenuIndex() como no hay efecto en MainPopupMenu

Problema de 879: Pop-up menú "Spider contexto..." está habilitada incluso si ExtensionSpider está inhabilitada

Problema de 880: Recordar último directorio seleccionado al agregar archivos personalizados pelusa

Número 881: Error inmediatamente si no se encuentra archivo zapdb.script

Número 882: Eliminar "Copia" surge del menú mostrado en la pestaña "Browse forzado"

Edición 884: Fase Plug-n-Hack 2

Tema 885: API - respuesta de acciones no se muestra utilizando el formato HTML

Problema 886: Principal pop-up menú invocada dos veces en algunos de los componentes

Problema 887: botón de pausa del escáner con selección incoherente / estado habilitado

Número 857: Núcleo API - vista "alertas" podría devolver alertas inesperados cuando se utiliza paginación

Issue 889 : JSONException while calling an API "other" without the required parameter(s)

Problema 890: Permitir borrar la pestaña "Salida"

Problema 891: la generación de destino "generar-javadocs" debería aplicar la propiedad SVN mime-type a todos los archivos generados

Problema 892: La memoria caché de la longitud del cuerpo de respuesta en HistoryReference podría no ser correcta

Problema 896: PnH: bandera de cualquier ataque de fuzz que el oráculo de DOM XSS

Problema 897: Agregue un JToggleButton que permita establecer un texto de punta de herramienta basado en el estado del botón

Número 898: Reemplazar todos los botones de alternar que un texto de sugerencia de herramienta basado en estado de botón con ZapToggleButton

Número 899: Quitar actualización "manual" del icono conmutar botones basado en estado de botón

Número 900: IllegalArgumentException al invocar el menú con menús o super con índice alto del menú emergente principal

Número 901: Separador de "éxito" del menú emergente no se agrega cuando se utiliza el menú en MainPopupMenu

Número 902: Cambiar todos los métodos de reemplazo ExtensionAdaptor\#hook(ExtensionHook) para llamar a la implementación base

Número 903: Modificar las opciones deslizadores para utilizar el mismo componente del hilo de rosca

Problema 904: agregue un grupo de botones que permita anular la selección del botón seleccionado

Número 905: Enlace incorrecto en páginas de ayuda de la "Ficha de rotura"

Tema 910: Usuario forzado no se puede cambiar

Tema 911: AScan API - cambiar la vista de "exploradores" para incluir el estado del escáner activo

Número 912: PScan API - cambiar la vista de "exploradores" para incluir el estado del escáner pasivo

Número 913: AScan API - permiten para lista o conseguir las políticas activa escáner

Número 914: AScan API - permite establecer las políticas de activo explorador habilitadas

Número 915: Filtrar dinámicamente historia basada en la selección en la ventana de sitios

Número 919: Permite vulnerabilities.xml ser localizado IdealFirstBug

Tema 920: Añadir incluir/excluir patrones de url, filtro de la historia

Número 921: PnH2: abierto como url monitoreados

Número 923: Permite los umbrales de la regla individual y fortalezas a través GUI

Problema de 925: HTML Informe temas

Número 929: AScan API - permite para fijar el umbral de fuerza y alerta de ataque de políticas activa escáner y escáneres activos

Número 930: AScan API - permiten para lista o conseguir los escáneres activos por identificación política

Número 931: Permite extensiones a recoger args de línea de comandos en modo gráfico

Número 932: Permitir scripts a especificarse en la línea de comandos

Número 933: Determinar automáticamente el directorio de instalación

Número 934: Administrar los archivos en la línea de comandos a través de la extensión

Número 935: Mejorar la identificación de la versión de Java

Edición 939: ZAP debe aceptar conexiones SSL en puertos no estándar automáticamente

Número 947: Araña falla las URL con caracteres ilegales

Número 950: Lidiar con Add-ons que contiene los archivos copiados directamente en el directorio de plugins

Edición 951: Versiones de TLS 1.1 y 1.2 no activado por defecto

Número 954: Cambios en ciertos campos en la interfaz gráfica no se guardan después de hacer clic en OK/Proceed

Número 955: foco de teclado perdió al cuerpo grande encontrado

Número 956: Copia las direcciones URL no copiar múltiples

Número 957: Referencia alerta "opciones de tipo X-contenido encabezado faltante"

Número 963: Complemento añadido a lista de bloques si no se puede eliminar en actualización

Número 965: Soporte aplicaciones 'sola página' y separadores de parámetro no estándar

Edición 966: Opción de línea de comandos Inicio rápido

Número 967: InvalidParameterException al actualizar el complemento de "Consola de comandos"

Número 968: Permite elegir el habilitado protocolos SSL/TLS

Edición 969: Proxy - no incluyen el cuerpo de la respuesta al responder a peticiones de cabeza sin éxito

Cuestión 970: Cuerpo de solicitudes de cancelación debe ser enviada/adelante

Número 974: Analizar elementos de ruta de acceso URL

Emisión 975: Búsqueda inversa pelusa resultados Buggy

Problema 976: Araña contexto ataque provoca spidering fuera de contexto

Edición 979: Árboles alertas y sitios pueden conseguir dañados

Edición 981: Internacionalizar ayuda archivo

Número 982: Clave de API

Número 986: ScanProgress nuevo diálogo implementación y omitiendo la funcionalidad del plugin

Número 987: Permitir configuración arbitraria valores de archivo a través de la línea de comandos

Número 988: Ayuda ZAP se bloquea antes de iniciar

Número 989: Añadir una opción de clic derecho "Agregar usuario" en una sesión HTTP

Número 991: solicitud de revisión regla de Add-on/Scan - XSS persistente

Edición 996: Asegurar que todos los diálogos cierran cuando se presiona la tecla de escape

Número 997: Session.open se queja por uso inadecuado de addPath

Problema de 998: Búsqueda regexp tonto mata ZAP

Número 999: Historia cargado en orden incorrecto

Número 1002: Añadido soporte para autenticación a través de secuencias de comandos

Problema 1003: Complemento de prueba de vulnerabilidad XXE

Problema 1004: divulgación del código fuente con metadatos de Git

Issue 1005 : Source Code disclosure using Subversion meta-data

Número 1006: Spidering de aplicaciones web utilizando metadatos de Git

Número 1007: Spidering de aplicaciones web utilizando los metadatos de Subversion (SVN)

Problema 1010: Permitir ordenar los resultados de fuzz

Problema 1012: cuadro de diálogo Encode / Decode: admite codificación HTML y JavaScript IdealFirstBug

Problema 1016: problema de visualización de codificación HTML en credits.html

Problema 1017: Proxy establecido en 0.0.0.0 provoca que se genere un archivo PAC incorrecto

Número 1018: Acceso AbstractAppParamPlugin implementaciones para el tipo de parámetro

Edición 1019: ZAP inicio con mala JAVA\_HOME muestra mensaje de error confuso

Edición 1020: Duplicar vista capaz de enchufe ": tabla de cuerpo" de fichas de solicitud/rotura

Número 1021: OutOutOfMemoryError mientras se ejecuta el explorador activo

Edición 1022: Proxy - permite reemplazar un mensaje proxy

Número 1023: Consola de Script - marcha/parada de botones con estado incoherente

Problema de 1024: Ver respuesta grande se muestra incluso si no existe un cuerpo de la respuesta

Problema 1025: NullPointerException mientras presiona una tecla con las áreas de texto de la "Consola de comandos" seleccionadas

Número 1030: Cargar y guardar las políticas de exploración

Edición 1031: Agregar funcionalidades de parámetro de exclusión para el explorador activo

Edición 1032: Añadir soporte de API para autenticación basada en Script

Edición 1033: org.zaproxy.clientapi.core.Alert no sobrescribir el método equals()

Edición 1037: Parámetros de JSON RPC no se configuran correctamente

Edición 1039: Mejorar el plugin redireccionar externo exactitud

Edición 1041: Exploración activa plugins no se inician si el sitio es local 127.0.0.1

Número 1042: Tiene problemas significativos de abrir una sesión anterior

Número 1043: Cuadro de diálogo active scan personalizado

Edición 1044: Modo usuario forzado no persiste a través de sesiones guarda/carga

Edición 1046: El método getHttpCookies() en el HttpResponseHeader no correctamente establece el dominio

Número 1047: Archivos de copia de seguridad no detectados por Zap

Número 1049: Patrón múltiple búsqueda rápida componente

Número 1050: Secuencias de comandos basado en vectores de entrada

Edición 1051: Zap puede limitados servicios a todas las interfaces de red

Número 1052: Devolución de llamada API para plugins de escaneo activo

Problema: 1053 similitud de secuencia y componente del algoritmo de LCS

Edición 1055: Cargar extensiones antes de plugins

Edición 1057: Agregar un método Extension.postInstall() para el post instalar acciones

Número 1059: Añadir apoyo Jython para autenticación basada en Script

Número 1060: Añadir soporte de JRuby para autenticación basada en Script

Edición 1061: Seleccionar adecuada escritura tipo, motor y plantilla al crear nuevo script

Edición 1063: Opción para decodificar agregar contenido comprimido con gzip (era la compresión de la manija para secuencias de comandos)

Edición 1065: Renombrar ExtensionScripts a ExtensionScriptsConsole mantenimiento

Edición 1066: Añadido soporte para rápidamente establecer autenticación basada en secuencias de comandos de secuencias de comandos de interfaz de usuario

Número 1068: Zap no detecta código fuente en las respuestas

Edición 1069: Apoyo.-: en nombres de variables de ralladura

Número 1071: Script de Zest "Reemplazar en el cuerpo de la respuesta" entrega mal encabezado Content-Length.

Número 1072: SQLDataException: excepción de datos: datos de cadena, truncamiento derecho

Edición 1074: Se agrega opción para mostrar sólo la salida de la secuencia de comandos muestra

Número 1075: Cambio TableHistory para borrar los archivos por lotes rendimiento

Número 1076: Explorador activo cambio para no borrar los mensajes de temporales genera rendimiento

Número 1077: Fuzzer de cambio (HTTP) para no borrar los mensajes de temporales genera rendimiento

Número 1078: Cambio ExtensionBreak de respaldo a base de implementación de Gerente de punto de interrupción de tipo de mensaje

Número 1079: Quitar separadores de menú emergente principal de fuera de lugar

Problema de 1080: Usuario guía HTML páginas incorrectamente depender la codificación predeterminada de plataforma

Edición 1081: ExtensionPopupMenu deberá "notificar" niño ExtensionPopupMenu (y ExtensionPopupMenuItem) cuando el pop up se invoca

Número 1082: URL de búsqueda coincide con resaltado en posición incorrecta

Número 1083: Descartar el método ExtensionPopupMenuItem\#isSuperMenu()

Número 1084: NullPointerException mientras selecciona un nodo en la pestaña de "Sitios"

Número 1085: No agregar o quitar elementos del menú emergente a través del método View\#getPopupMenu()

Número 1086: Permite para agregar o quitar dinámicamente escáneres pasivos

Número 1087: Cambiar extensiones para agregar dinámicamente escáneres pasivos

Número 1088: Descartar el método ExtensionPopupMenu \#prepareShow

Problema de 1089: Cambio ExtensionPopupMenu en honor a la pop-up métodos de extensión

Número 1090: No agregar pop-up menús si no está habilitada la extensión de destino

Número 1091: CoreAPI - no obtengo el ID de registro de historia temporal

Número 1092: SearchThread - no permita que los ID de los mensajes descartados

Número 1093: Añadir un HTTP solicitud vista del cuerpo que avisa de cuerpo grande

Número 1094: ExtensionManualRequestEditor de cambio sólo añadir componentes de la vista en modo gráfico

Edición 1095: Reemplazar principal pop-up menús de sub con ExtensionPopupMenu cuando sea apropiado

Tema 1096: AddOnLoader llamadas incorrecta notificación método después de desinstalar archivos Add-on

Edición 1097: Movimiento "Ejecute aplicaciones" (invocar) extensión a proyecto de zap-extensiones

Edición 1098: Movimiento AJAX araña ayuda páginas para complemento de "la araña del Ajax" (y actualizarlos)

Problema de 1099: Permite para anotar métodos de opción como ignorado por API ZAP

Edición 1100: Anotar métodos de opción que no deben ser expuestos en la API de ZAP

Edición 1101: Cambiar escáneres pasivos para exponer sus identificadores

Número 1102: Ajax Spider - proxy de araña reemplazar ajax con proxy de núcleo

Número 1103: De la escritura consola - permite limpiar salida incluso si "claro en funcionamiento" está habilitada

Issue 1104 : Replace all toggle buttons that set a tool tip text based on button's state with ZapToggleButton (add-ons)

Edición 1105: Quitar actualización "manual" del icono conmutar botones basado en estado de botón (complementos)

Número 1106: Asignación de historia de historia ID a índices de la lista no se actualiza cuando se elimina la entrada de la historia

Problema 1110: API de Spider: no se puede establecer cómo se manejan los parámetros mediante API

Problema 1111: Buscar actualizaciones al inicio se desactiva (automáticamente) al acceder al diálogo "Opciones"

Problema 1112: Cambie ZAP (núcleo) para admitir la nueva estructura de directorio agregado

Problema 1113: cambiar la estructura de directorios de complementos (ayuda y recursos)

Número 1118: Tab alertas puede conseguir fuera de sincronización

Problema 1119: Spider no detecta formularios múltiples en la misma URL

Problema 1120: el complemento de desinstalación falla si las reglas usan el paquete de mensajes en la desinstalación

Issue 1121 : Scan progress dialog can cause UI freezes

Problema 1122: Información adicional del complemento

Problema 1125: No se puede volver a importar la secuencia de comandos jython como una secuencia de comandos proxy

Problema 1126: Errores en los filtros de punto de interrupción

Problema 1127: Solicitud de características: Permitir que los scripts generen rupturas

Problema 1131: Acciones de intercepción de Zest de soporte en complemento

Problema 1132: HttpSender ignora la opción "Enviar encabezado de solicitud de cookie única"

Problema 1134: expresiones regulares de la Regla de exploración pasiva no validadas

Problema 1135: la pestaña Marketplace no se puede actualizar si cfu se ejecuta al iniciar

Problema 1137: ZAP se bloquea al eliminar nodos

Problema 1138: cambios en la Regla de exploración pasiva no guardados

Problema 1145: error de análisis de cookies si se usa una coma

Vease también

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
</table>][https_groups.google.com_group_zaproxy-scripts _.]


[https_groups.google.com_group_zaproxy-scripts _.]: https://groups.google.com/group/zaproxy-scripts