# Release 2.4.0 #

Se hicieron los siguientes cambios en esta versión:

## Cambios significativos: ##

### Menú de ataque ###

Un nuevo 'ATAQUE' [Modo][] ha sido agregado - nuevos nodos que están en [Ámbito][mbito] son [escaneo activo][] tan pronto como son descubiertos.

### Configuración avanzada ###

Se ha introducido un diálogo de fuzz completamente nuevo que permite atacar múltiples puntos de inyección al mismo tiempo.
Esto admite nuevas cargas útiles de ataque, incluida la opción de utilizar scripts para generar las cargas útiles, así como la manipulación y el análisis antes y después del ataque.

### Escanear diálogos con opciones avanzadas ###

Nuevo [Escaneo Activo][], [Spider(Araña)][Spider_Ara_a] y los diálogos AJAX Spider han reemplazado el creciente número de opciones de 'Ataque' con el botón derecho.
Estos proporcionan un acceso fácil a todas las opciones más comunes y, opcionalmente, a una amplia gama de opciones avanzadas.

### Reglas de escaneo... ###

Un nuevo [Diálogo del administrador de política de escaneo][Di_logo del administrador de pol_tica de escaneo] te permite crear tantos [Reglas de escaneo...][] como necesites.
Las políticas de escaneo definen exactamente qué reglas se ejecutan como parte de un [Escaneo Activo][escaneo activo].
También definen cómo se ejecutan estas reglas, lo que influye en la cantidad de solicitudes que se realizan y en la probabilidad de que se marquen los posibles problemas.


### Pestañas no utilizadas ocultas ###

De forma predeterminada, solo se muestran las pestañas esenciales cuando se inicia ZAP.
Las pestañas restantes se revelan cuando se usan (por ejemplo, para la araña y el escáner activo) o cuando las muestras a través de la pestaña especial en el extremo derecho de cada ventana con el ícono verde "+". Esta pestaña especial desaparece si no hay pestañas ocultas.
Las pestañas se pueden cerrar mediante un pequeño ícono 'x' que se muestra cuando se selecciona la pestaña.
Las pestañas también se pueden 'fijar' usando un pequeño ícono 'pin' que también se muestra cuando se selecciona la pestaña: se mostrarán pestañas fijas cuando se inicie ZAP.

### Habilitadores para el complemento de escaneo de secuencia ###

Un nuevo complemento opcional de calidad 'alfa' agrega la capacidad de escanear 'secuencias' de páginas web, en otras palabras, páginas que deben visitarse en un orden estricto para funcionar correctamente.

### Habilitadores para el complemento de prueba de control de acceso ###

Un nuevo complemento opcional de calidad 'alpha' agrega la capacidad de automatizar muchos aspectos de las pruebas de control de acceso.

### Nota para los usuarios de la API ###

Tenga en cuenta que el identificador del Plugin para el explorador redirección externa ha cambiado de 30000 a 20019.

## Lista completa de cambios: ##

 *  Problema 117: Mejora: comparar sesiones arrastran problemas de autenticación
 *  Número 234: Soporte para fuzzing múltiples partes
 *  Edición 329: Mejora: Añadir soporte de sitemap.xml
 *  Edición 389: Habilitar posibilidades de la tecnología de escáneres
 *  Edición 414: API: apoyo de secuencias de comandos
 *  Número 445: SSLContextManager.isProviderAvailable() devuelve true por defecto
 *  Edición 557: Falsos negativos SQL inyección
 *  Edición 642: Ficha salida necesita marcas de tiempo
 *  Edición 653: Mango actualizaciones mejor en Kali Linux
 *  Tema 704: ZAP Error: alerta de apretón de manos: unrecognized\_name
 *  Edición 722: ZAP UI no maneja múltiples escaneos activos bien
 *  Número 883: Apoyar múltiples exploraciones en la API
 *  Número 949: Araña (sitio) no sigue los hipervínculos en documentos JSON
 *  Número 959: actualización Add-on puede ignorar cambios de proxy saliente
 *  Cuestión 984: Mejorar la ascan API para permitir el método para especificar
 *  Número 990: Permiten para eliminar alertas a través de la API
 *  Número 1151: Exploración activa en el ámbito de aplicación termina antes de escanear todos los mensajes de alcance si múltiples dominios disponibles
 *  Número 1154: Herramienta de punta de texto "Mostrar la ficha nombres y los iconos de la pestaña" IdealFirstBug
 *  Número 1175: Apoyar un árbol de contextos
 *  Número 1176: Diálogo de exploración avanzada spider
 *  Problema de 1180: Proxy corrompe URL cuando hay múltiples signos de interrogación
 *  Número 1184: Mejorado el soporte para IBM JDK
 *  Problema de 1207: AScan API - cambiar la vista de "exploradores" para incluir las dependencias
 *  Problema 1208: Clases y recursos de búsqueda de complementos declarado como dependencias
 *  Número 1209: Fiabilidad adicional valores y opciones y fiabilidad de renombrar a la confianza en la interfaz de usuario
 *  Número 1214: Clasificación en la política de exploración de cuadros de diálogo de usabilidad
 *  Número 1215: Árbol alerta ordenar/clasificar tema usabilidad
 *  Problema de 1216: Error en la ficha secuencias de comandos
 *  Número 1217: Formato de la tabla no muestra información al conjunto de caracteres está presente en el encabezado Content-Type
 *  Número 1224: Mostrar la calidad, estado en exploración usabilidad de diálogos de política
 *  Número 1226: Scanner activo excluidos regexes del parámetro no validado
 *  Número 1227: Scanner activo envía solicitudes GET con contenido en el cuerpo de la solicitud
 *  Número 1238: NullPointerException si un escáner activo plantea una alerta con ataque null
 *  Número 1239: Permite que la spider se extiende desde extensiones
 *  Número 1241: Scanner activo podría no indicar Estado terminado al utilizar escáneres de host
 *  Problema de 1242: Scanner activo puede utilizar configuración política anticuada
 *  Número 1243: NullPointerException si un tipo de secuencia de comandos no tiene núcleo incluye plantillas de scripts
 *  Número 1244: Secuencias de comandos activa escáner debería ser categoría Misc no inyección de usabilidad
 *  Número 1252: Excepción de conexión durante el apagado mientras se está ejecutando exploraciones a través de la API
 *  Número 1256: Revisar falta nivel del explorador X-Frame-Options
 *  Problema de 1257: Crear una regla de pasiva que detecta gran redirecciones
 *  Número 1261: NPE en "Configuración de Plug-n-Hack" actualización del mercado
 *  Edición 1262: Dirección "Pasivo reglas – riesgo – confiabilidad" \[usuario controlable HTML elemento atributo (potencial XSS) y Timestamp revelación - Unix\]
 *  Problema de 1263: Generar informe anula archivos existentes sin preguntar al usuario
 *  Número 1264: Autenticación Manual - desajuste de galleta debido a mal manejo de dominio y ruta de acceso
 *  Edición 1265: Contexto de importación y exportación
 *  Problema 1272: API ZAP: Core.MessagesHAR () falla si una solicitud HTTP contiene encabezado (s) de cookie no válido
 *  Problema 1274: Error de ZAP \[javax.net.ssl.SSLException\]: versión de registro no compatible SSLv2Hello
 *  Problema 1275: SpiderODataAtomParser debe devolver verdadero de "parseResource"
 *  Problema 1278: Elementos de menú seguros no disponibles en modos protegidos y seguros
 *  Problema 1279: los parámetros excluidos del escáner activo no funcionan cuando "Where" is "Any"
 *  Número 1280: Accesos directos de la API que no se quitan cuando se quita el ApiImplementor
 *  Número 1281: QuickStart - permite generar el informe cuando la vista está inicializada
 *  Número 1282: Extension\#stop() no se llama nunca antes destroy()
 *  Problema de 1283: SQLDataException: excepción de datos: datos de cadena, truncamiento derecho escribiendo una alerta a DB
 *  Número 1286: Fuzzer parece lento
 *  Número 1290: "Exploración de puertos host" del menú activado incluso si una exploración de puerto ya está en marcha
 *  1291:407 autenticación de Proxy necesaria de emitir durante el escaneo activo
 *  Número 1292: NullPointerException cuando trataban de retirar un ManualRequestEditorDialog no registrado
 *  Problema de 1294: Trivial\_UI\_Issue: de la palabra - 'será' aparece dos veces bajo el indicador de 'Propiedades de la sesión'.
 *  Número 1295: Petición de mejora - nueva regla de exploración activa para comprobar el acceso HTTP a HTTPS contenido
 *  Problema de 1300: Complementos Mostrar idioma incorrecto cuando inglés es seleccionado en configuración regional de inglés no
 *  Número 1301: Fuga de AbstractPanel a través de TabbedPanel2
 *  Número 1302: Acción de elemento del menú de contexto podría no se ejecutan
 *  Número 1303: Fuga de HttpPanel\[SyntaxHighlight\]TextArea a través de HighlighterManager
 *  Número 1304: Fuga de ZapMenuItem a través de ExtensionKeyboard
 *  Número 1305: Proxy saliente está deshabilitado durante la actualización de versiones antiguas
 *  Número 1307: Build Ant OS X de zip obtiene espacios de nombre de archivo confundido
 *  Problema 1308: resolución de icns de ZAP demasiado baja
 *  Problema 1308: resolución de icns de ZAP demasiado baja
 *  Edición 1310: Permite establecer tipos de historia como temporal
 *  Número 1311: Diferenciar los mensajes internos temporales de los mensajes de escáner temporal
 *  Número 1312: Engañoso mensaje de error cuando no se puede enlazar el proxy local a la dirección especificada
 *  Número 1319: Añadir soporte de API para la configuración de detección de un contexto autorización
 *  Número 1322: Quitar deprecated API Auth
 *  Número 1324: Incluyen complemento que llama a api en el API generado
 *  Número 1325: Opción eliminar contextos
 *  Número 1326: Movimiento araña Ajax extensión de Beta al estado de liberación
 *  Número 1333: ExtensionAntiCSRF ConcurrentModificationException
 *  Problema de 1334: ZAP no maneja solicitudes de API en reutilizadas conexiones hacia UnknownHostException: www.zap.com
 *  Número 1335: NullPointerException mientras selecciona un nodo en la pestaña de "Alertas" después de excluir sitios de proxy
 *  Número 1339: Introducir un bus de eventos simple
 *  Problema de 1343: Usabilidad de internacionalización de XContentTypeOptionsScanner
 *  Número 1345: Modo de ataque de apoyo
 *  Edición 1346: Romper las respuestas gziped falla en el navegador
 *  Cuestión 1348: Cliente Java api no esperen las tareas Ant
 *  Problema de 1353: Opción de descanso más simple
 *  Número 1355: Generación de informes Html a través de la API
 *  Edición 1356: Corregir errores tipográficos de CacheControlScanner
 *  Número 1357: Ocultar pestañas sin usar
 *  Problema de 1359: Restablecer pantalla de inicio
 *  Número 1360: Nuevo Add-on-consejos y trucos
 *  Edición 1361: No hay datos aparecen en panel 'Spider' y 'Escaneo activo' spidering o exploración por API
 *  Edición 1362: Se permite añadir duplica fichas Anti CSRF solamente por API
 *  Edición 1363: Falta API para obtener contextId
 *  Edición 1367: No puede detectar "Xpath Injection" en un determinado ambiente.
 *  Edición 1377: "Divulgación del código de fuente – SVN" falta escape regex
 *  Edición 1378: Renovar el panel de exploración activa
 *  Número 1379: Oyentes de la extensión no todos están enganchados durante la instalación de Add-on
 *  Edición 1381: Limpiamente cerrar cuadro de diálogo de agregar/editar punto de interrupción en cancelar
 *  Número 1383: NullPointerException si un token CSRF anti no tiene un valor
 *  Problema de 1384: HttpSessions API no acepta a URIs con componente de trazado
 *  Edición 1385: Informe XML no se genera a través de la API si ZAP no se ejecuta desde el directorio de instalación predeterminado
 *  Número 1386: PScan API - permite cambiar y ver los umbrales de alerta
 *  Problema de 1387: No pueden cambiar de dirección/puerto del proxy si se especifica la dirección del puerto a través de la línea de comandos
 *  Número 1388: No todos los archivos de traducción se actualizan cuando se importa el paquete "zaplang"
 *  Problema de 1389: NullPointerException durante el inicio si no se encuentra el núcleo ayuda jar
 *  Número 1390: Fuerza https en UFC llamada
 *  Problema de 1391: Exploración activa enviar carga mal de tipo multipart/formularios de datos
 *  Edición 1394: Importar archivos de vulnerabilities.xml durante la actualización de los recursos traducidos
 *  Número 1395: datos de vulnerabilidades en la memoria incluso si no utiliza
 *  Problema 1397: mueva archivos de ayuda a complementos
 *  Problema 1399: mejora la ayuda para abrir enlaces 'externos' en el navegador predeterminado de los usuarios
 *  Problema 1404: SpiderODataAtomParser debe devolver verdadero solo si se detectan enlaces
 *  Problema 1406: mueva los elementos del menú en línea a un complemento
 *  Problema 1409: acelere el inicio de ZAP
 *  Problema 1415: Carga de archivos fijos> 128k
 *  Problema 1412: Administrar políticas de escaneo
 *  Issue 1416 : Allow spider to be restricted by the number of children
 *  Problema 1418: Opción para que ZAP permanezca en la parte superior cuando golpee el punto de ruptura
 *  Problema 1419: incluir evidencia de alerta en el informe HTML
 *  Problema 1420: cambie el URLCanonicalizer de araña para omitir URI sin autorización
 *  Problema 1427: Estandarizar en el orden de los botones \[Cancelar\] \[Aceptar\]
 *  Problema 1433: Spider Select target no seleccionado automáticamente
 *  Problema 1439: botón para mostrar / ocultar solo el contexto / sitios con ámbito en la pestaña del sitio
 *  Problema 1445: Propiedades de sesión muestra el ID de contexto no el nombre de contexto
 *  Problema 1446: la falla de complementos descargados no se manejó correctamente.
 *  Problema 1447: actualización de la biblioteca RSyntaxTextArea
 *  Problema 1449: Reenviar / Manual Solicitar ayuda desactualizada
 *  Problema 1458: Cambiar las rutas del directorio de inicio / instalación para que sean siempre absolutas
 *  Problema 1460: los tipos de script no se muestran en el árbol "Script" cuando se agrega el tipo de script durante la instalación de un add-on
 *  Problema 1461: API principal: permite obtener un mensaje por ID en formato de archivo HTTP
 *  Problema 1461: API principal: permite obtener un mensaje por ID en formato de archivo HTTP
 *  Problema 1463: permitir que las secuencias de comandos accedan a clases de complementos
 *  Problema 1464: Permitir enviar encabezado "Referer" en solicitudes de spider
 *  Problema 1465: los archivos traducidos no se copian en el directorio correcto si ZAP no se ejecuta desde el directorio de instalación predeterminado
 *  Problema 1466: opción de configuración para el tamaño de 'pantalla grande'
 *  Problema 1467: AuthenticationApiExample no funciona
 *  Problema 1468: las plantillas de scripts no están disponibles cuando se agregan nuevos tipos de scripts durante la instalación de un add-on
 *  Problema 1469: agregue automáticamente un usuario si la autenticación basada en formulario se ha especificado en función de una solicitud
 *  Problema 1472: Permitir que las extensiones especifiquen un nombre para los componentes de la interfaz de usuario
 *  Problema 1475: Es posible que las alertas con un nombre diferente del mismo escáner no se muestren en el informe
 *  Problema 1475: Es posible que las alertas con un nombre diferente del mismo escáner no se muestren en el informe
 *  Problema 1483: MissingResourceException después de desinstalar un complemento con escáneres pasivos
 *  Problema 1484: NullPointerException durante la desinstalación de un complemento con escáneres activos
 *  Problema 1485: no permitir volver a seleccionar un complemento si la desinstalación no fue correcta
 *  Problema 1486: pérdida de componentes de complementos
 *  Problema 1489: Número de versión en el título de la ventana
 *  Problema 1489: Número de versión en el título de la ventana
 *  Problema de 1491: Añadir versión AbstractParam
 *  Edición 1492: Actualizar biblioteca commons-csv
 *  Edición 1493: Eliminar obsoletas las clases de autenticación
 *  Problema de 1494: Directorios de secuencia de comandos de apoyo
 *  Edición 1502: Permiten para quitar contenedores de motor de secuencia de comandos
 *  Problema de 1503: No todos los motores se muestran al crear una secuencia de comandos de tipo
 *  Edición 1504: Excepción de cuando un motor de secuencias de comandos no está instalado/encontrado
 *  Edición 1505: "Obligado examinar" no todos los componentes estén completamente vacíos durante la desinstalación
 *  Número 1507: No todos los componentes de "Consola de comandos" se descarguen durante la desinstalación
 *  Edición 1508: Alertas añadidos a la vista en modo demonio
 *  Edición 1510: Nuevo método de Extension.postInit() que se llamará una vez todas las extensiones cargadas
 *  Edición 1511: Agregar la opción Permitir sólo conexiones seguras a la API
 *  Número 1514: Certificado de CA raíz no generada en modo demonio
 *  Problema de 1515: No todos los componentes "Ralladura" son descargados durante la desinstalación
 *  Edición 1520: Añadir icono de bloqueo a sitios https en el árbol de sitios
 *  Edición 1521: Throwable errores como StackOverflowError no atrapado por escáner pasivo
 *  Problema de 1524: Cuadro de diálogo nuevo sesión persiste
 *  Problema de 1525: Introducir una capa de interfaz de base de datos para permitir implementaciones alternativas
 *  Edición 1528: Tamaño de fuente definido por el usuario de apoyo
 *  Edición 1530: Por defecto fuerza de ataque y umbral de alerta, en 'La exploración política', no por exploradores
 *  Tema 1534: Cambiar complemento de "la spider del Ajax" dependen de complemento "Selenio"
 *  : 1535 actualización Crawljax biblioteca y dependencias (complemento de "la spider del Ajax")
 *  Problema de 1536: Cambio "Zest" Add-on depender de complemento "Selenio"
 *  Número 1537: ZAP debe permitir importar certificados de CA
 *  Edición 1540: Permitir secuencias de comandos de proxy simular las respuestas
 *  Edición 1541: Permitir secuencias de comandos de exploración activa escanear a una dirección URL en lugar de cada parámetro
 *  Edición 1544: Apoyar las variables de script persistente
 *  Edición de 1551: ZAP no detecta confusión de ruta de acceso relativa (aka "relativa camino sobrescribir" / "Importar ruta relativa hoja de estilos")
 *  Edición 1552: ZAP no detectar hacia adelante / reversa Proxies
 *  Edición de 1553: ZAP no detecta la capacidad de almacenamiento / almacenamiento en caché de una respuesta
 *  Número 1557: Bloqueo solicitud manual

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


[Modo]: HelpStartConceptsModes
[mbito]: HelpStartConceptsScope
[escaneo activo]: HelpStartConceptsAscan
[Escaneo Activo]: HelpUiDialogsAdvascan
[Spider_Ara_a]: HelpUiDialogsSpider
[Di_logo del administrador de pol_tica de escaneo]: HelpUiDialogsScanpolicymgr
[Reglas de escaneo...]: HelpStartConceptsScanpolicy