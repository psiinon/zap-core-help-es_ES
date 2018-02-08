# Release 2.5.0 #

Se hicieron los siguientes cambios en esta versión:

## ZAP cambios en la API: ##

### Ver autorización / getAuthorizationDetectionMethod ###

Ahora devuelve datos envueltos en un objeto llamado authorizationDetectionMethod Por ejemplo:

``````````
{"authorizationDetectionMethod":{"statusCode":"-1"..."headerRegex":""}}
``````````

En lugar de

``````````
{"statusCode":"-1"..."headerRegex":""}
``````````

### Contexto vista / contexto + technologyList ###

Both now return data wrapped in an object called "context" For example:

``````````
{"context":{"id":"1", ..., "inScope":"true","loggedOutPattern":""}}
``````````

instead of:

``````````
{"id":"1", ..., "inScope":"true","loggedOutPattern":""}
``````````

### Spider de acción / scan + scanAsUser ###

Ahora soportan un nuevo parámetro opcional 'subtreeOnly' que limita la spider para el subárbol especificado. El parámetro 'enlace' también ahora es opcional, siempre y cuando se suministra un parámetro válido 'contexto'

### Nuevo componente de 'estadísticas' ###

El nuevo componente de 'estadísticas' API proporciona acceso a la [stats][] now maintained by ZAP.

Nota que algunos componentes existentes también tendrá nuevas operaciones, véase el [API Web UI][] Mostrar más detalles

## Mejoras: ##

 *  Número 266: Añadir auto marcado para el establecimiento de cookies, json
 *  Edición 646: Contraseña saliente proxy en formato de texto en pantalla
 *  Problema 1171: Árbol sitios para levantar ' nuevo sitio / nuevo nodo ' eventos
 *  Problema de 1229: Actualización extensiones/Plugins para tomar ventaja de la nueva escala de confianza
 *  Número 1341: Actualización alertas XML schema para eliminar colisiones de nombre de nivel de elemento
 *  Edición 1590: Modo aplicar cuando se ejecuta como un demonio
 *  Problema de 1713: Revelación de código fuente SVN arroja falsos positivos
 *  Edición 1864: Progreso de la exploración de copia como texto en el portapapeles
 *  Edición 1958: Permite para desactivar el registro de base de datos (HSQLDB)
 *  Edición 1959: Permitir encabezados de exploración activa de todas las solicitudes de
 *  Edición 1980: Añadir CLI ZAP a imágenes de Docker
 *  Número 2068: LoggedIn LoggedOut los indicadores y dentro de secuencias de comandos de autenticación
 *  Número 2070: Debería ser posible para las secuencias de comandos de autenticación configurar cómo se envían los mensajes
 *  Número 2121: Desactivar Req/Resp pestañas Coloque opciones cuando esté en disposición "Expandir todo"
 *  Edición 2127: Advertir si la generación de informes de error
 *  Número 2162: agregar-mercado-clasificación
 *  Número 2171: Complementos administran vía api, cli
 *  Número 2174: ExpressionLanguageInjectionPlugin - necesita registro fijar
 *  Número 2177: SourceCodeDisclosureSVN - no se puede escribir a temp DB
 *  Número 2183: API: incluye calidad en la respuesta de ascan/progreso
 *  Problema 2237: Permiten mem máximo java para ser anulado en la línea de comandos
 *  Número 2238: spider: suplencia a analizar HTML comentarios como texto si no hay URL encuentra
 *  Número 2272: SQLInjectionHypersonic (Beta) - excepciones
 *  Problema de 2273: Apoyar estadísticas de nivel de sitio
 *  Número 2274: Permitir a spider sólo subárbol de un sitio
 *  Número 2275: spider: no requieren de una dirección URL, a través de la API, si el contexto tiene semillas
 *  Edición 2277: spider: conservar los parámetros de la consulta con el mismo nombre cuando canonicalising URL
 *  Número 2289: Sitio de registro basado en las estadísticas de tiempo de respuesta
 *  Problema 2324: Incluir la calidad de los escáneres en las vistas de los escáneres API
 *  Problema 2330: Agregar estadísticas de autenticación
 *  Número 2335: Añadir saliente máxima de contraseña de Proxy
 *  Problema 2342: Capacidad de administrar sitios en ZAP a través de API
 *  Número 2347: Permite eliminar fábricas de contexto de vista/modelo
 *  Número 2361: Renombrar barra de herramientas opción ampliar completo diseño completo
 *  Número 2362: Permite seleccionar todos los resultados de spider
 *  Número 2367: Rotura de cambio botones ubicación sin reiniciar ZAP
 *  Número 2368: No requieren un reinicio para mostrar/ocultar la barra de herramientas principal
 *  Número 2381: No permiten para guardar y escritura a archivos de sólo lectura
 *  Número 2400: Mostrar un mensaje más informativo en tiempos de espera de lectura a través del proxy
 *  Número 2410: Mensajes HTTP Mostrar en la pestaña de spider
 *  Número 2413: Desactivar "Mostrar en la ficha historial" si el mensaje no es válido
 *  Número 2418: spider: duración máxima de la ayuda en minutos opción
 *  Problema de 2420: Permiten escáneres activos comunicar un mensaje
 *  Edicion 2422 : apoyo Statsd y estadísticas se movió a nueva ext
 *  Número 2465: Permiten para esperar ZAP iniciar con ClientApi
 *  Número 2466: Permite para acceder a una dirección URL mediante la API de ZAP
 *  Número 2479: Guía del usuario Mostrar incluso si una perspectiva de investigación tiene errores
 *  Número 2481: Establecer nombre de la aplicación correcta en Linux
 *  Número 2482: Normalizar mesas de diálogo de sesión "Exclude from"
 *  Número 2484: Redirecciones de Circular
 *  Número 2486: Claro ScriptVars en la sesión de cambio
 *  Número 2494: ZAP Proxy no aparece la solicitud HTTP CONNECT en la ficha historial.
 *  Número 2504: Agregar explícitamente manual peticiones HTTP al árbol de sitios
 *  Número 2506: Deseche la sesión para la base de datos de archivo
 *  Problema de 2512: Actualizar biblioteca HSQLDB versión 2.3.4
 *  Número 2519: Activar botón de menú cuando se instala el complemento de ayuda

## Corrección de error: ##

 *  Problema 1529: TestExternalRedirect falta de caso de uso además de rendimiento y mejoras de FP
 *  Problema 1597: Java 8 - Mac OS / X paquete
 *  Problema 1639: XSS falsos negativos en inyecciones de script en la cabecera HTTP Referer
 *  Problema 1786: Activescan Scripts fracaso silencioso
 *  Problema 1801: Enlace StandardParameterParser no funciona correctamente con QueryString
 *  Problema 1848: VariantURLQuery lanzar excepciones en la exploración activa
 *  Edición 1874: Línea dos galletas en el encabezado cuando se agrega una cookie con un guión de httpsender y haciendo una exploración activa
 *  Edición 1875: Historia temp escáner no limpia en cerrar
 *  Problema 2090: Contexto: cambiar el nombre de usuario, puede seleccionar en el Panel de usuario obligado
 *  Número 2110: Inyección SQL consigue saltar
 *  Número 2112: Política equivocada en la exploración activa
 *  Número 2115: context.context("MyContext") Python API está roto
 *  Problema 2119: Descripción del contexto no importada
 *  Número 2122: Cambio SpiderAPI ignorar nombres de vacío contexto al manejar la acción de análisis
 *  Problema : 2125 registrar la excepción al abrir el archivo de sesión e internacionalizar el mensaje
 *  Número 2126: Fix NullPointerException en la falta de secuencia de comandos de contexto autenticación
 *  Problema 2132: Zap Informe contando Bug
 *  Edición 2142: Fuzzer lanzar excepciones
 *  Problema 2144: Java.lang.NullPointerException en "AWT-EventQueue-0"
 *  Problema 2151: AJAX Spider no hace clic en todos los elementos establecidos en las opciones
 *  Número 2153: 2.4.3 no pudo analizar los datos POST contiene bracket(\[\])
 *  Problema 2193: ficha Tecnología de inicialización con contexto seleccionado en el diálogo Active Scan
 *  Problema 2197: instale nuevas versiones de los complementos después de la descarga con -addonupdate
 *  Problema 2199: no permitir Spider escanea cuando ZAP está en modo seguro (o protegido)
 *  Problema 2203: repara avisos de findbugs
 *  Problema 2208: Impedir que el escáner activo informe un progreso superior al 100%
 *  Problema 2226: ZAP debería manejar los errores de cookies de HttpSessionsSite con mayor gracia
 *  Problema 2246: Error en la vista de sesiones con tokens
 *  Problema 2259: reparación de NullPointerException en la implementación de VariantCookie
 *  Problema 2281: filtros params para un sitio específico
 *  Número 2282: spider es un contexto todo a la vez
 *  Número 2292: Mejorar alertFingerPrint
 *  Número 2297: Activación de bloqueador AWT interrumpido - java.lang.InterruptedException
 *  Número 2307: Añadir falta el parámetro opcional "scanPolicyName" a las acciones de API de ascan
 *  Tema 2312: Dar atención al diálogo de "Editar el atajo de teclado"
 *  Número 2313: Convertir correctamente dominios proxy excluidos (viejo)
 *  Número 2314: No puede agregar varias cargas a fuzzer (NullPointerException)
 *  Número 2323: Fix loop de petición de API ZAP (seguro)
 *  Edición 2328: Arreglar problema durante la desinstalación de la extensión de nombre
 *  Problema de 2329: Filtrar las semillas inmediatamente antes de ejecutar la spider
 *  Número 2331: Contexto paneles no muestran en contextos existentes después de la instalación de Add-on
 *  Número 2336: BadLocationException que se produce cuando utiliza comprobador aleatorio
 *  Número 2357: Incoherencias mientras se cambia de un tipo de panel
 *  Número 2363: Botones de rotura mantener en sincronización al cambiar de modo
 *  Problema 2366: se muestran incoherencias en los botones de corte
 *  Número 2373: Ver pestaña no funciona correctamente en el diseño completo para las fichas de información no
 *  Problema 2374: no se puede cambiar la posición de la pestaña de respuesta sin la barra de herramientas principal
 *  Edición 2390: HeadlessException debe ser manejado con más gracia y README necesita detalles sin cabeza
 *  Número 2394: Cambiar API autorización vista para envolver su objeto
 *  Número 2399: Tiempo de espera de solicitudes no se muestra en ZAP
 *  Número 2421: Falta de coincidencia scanner activo solicitud cuenta
 *  Número 2428: Pérdida de memoria sobre creación de sesión, carga
 *  Número 2429: InterruptedExceptions al detener la araña con autenticación de usuario
 *  Número 2435: Limpiar recursos de tarea de araña, cuando no consume
 *  Número 2436: No puede dinámicamente desinstalar complemento de WebSockets
 *  Problema de 2440: Excepción al abrir el diálogo de exploración activa
 *  Número 2451: Sólo un solo nodo impulsado por datos pueden guardarse en un contexto
 *  Número 2463: Websocket no proxy cuando saliente proxy se establece
 *  Número 2469: Devolver siempre el 100% cuando araña
 *  Número 2472: Usar caso de nombre de archivo al cargar las políticas de archivo
 *  Número 2474: Agregar múltiples URL de contexto en / exclusiones a la vez
 *  Número 2475: Página de ayuda correcto opciones de reglas de exploración pasiva
 *  Issue 2487 : Wrong charset used in HTTP body
 *  Issue 2516 : Add auth and spider task types to temporary types

## Véase también ##

<table> 
 <tbody>
  <tr>
   <td>&nbsp;&nbsp;&nbsp;&nbsp;</td>
   <td><a href="HelpIntro" rel="nofollow">Introducci&oacute;n</a></td>
   <td>introducci&oacute;n a ZAP</td>
  </tr> 
  <tr>
   <td>&nbsp;&nbsp;&nbsp;&nbsp;</td>
   <td><a href="HelpReleasesReleases" rel="nofollow">Lanzamientos</a></td>
   <td>el conjunto completo de lanzamientos</td>
  </tr> 
  <tr>
   <td>&nbsp;&nbsp;&nbsp;&nbsp;</td>
   <td><a href="HelpCredits" rel="nofollow">Cr&eacute;ditos</a></td>
   <td>las personas y grupos que han hecho posible esta versi&oacute;n</td>
  </tr> 
 </tbody>
</table>


[stats]: HelpStartConceptsStats
[API Web UI]: HelpStartConceptsApi