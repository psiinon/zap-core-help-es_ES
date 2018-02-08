# Versión 2.6.0 #

Se trata de una corrección de errores y mejora liberación, que requiere un mínimo de Java 8.

Algunas de las mejoras más significativas incluyen:

 *  Lanzamiento del navegador incluido por defecto - esto le permite lanzar navegadores de ZAP que están preconfigurados para proxy a través de ZAP e ignoran las advertencias de certificado por el certificado de raíz ZAP.
 *  Permiten ZAP escuchar en múltiples direcciones o puertos
 *  Indicación de nombre de servidor de soporte
 *  Actualizada aplicación de motor NTLM - Esto soluciona los casos donde el dominio está siendo validado y mejora la interoperabilidad con otras implementaciones de NTLM (servidor)
 *  Un montón de nuevas terminales de API - ver abajo para más detalles

Tenga en cuenta que si usted tiene cualquier problema con esta versión también hay un nuevo elemento de menú ' Ayuda/Info...' que proporciona la información necesaria sobre la instalación de ZAP, que debe incluir cualquier temas que subes.

## Mejoras: ##

 *  Número 1015: Indicación de nombre del servidor de la ayuda
 *  Número 1313: Spider - permite configurar el límite de tamaño de las respuestas de un
 *  Problema 1604: Importar archivo de directivas mediante API
 *  Número 1620: Añadir punto final para obtener el número de avisos agrupados por nivel de riesgo
 *  Tema 1681: Cambio 'Active Scan' para mostrar las solicitudes números pasadas en lugar de los primeros
 *  Número 2411: Advertir si esta caducado dinámico certificado de CA raíz SSL
 *  Número 2615: Filtrado informes ZAP para mostrar los elementos de alto riesgo
 *  Problema de 3040: Exportar contenido de pestaña param
 *  Número 3101: Permitir complementos para utilizar versiones semántica
 *  Número 3156: Uso G1 como recolector de basura por defecto
 *  Número 3253: Exportar URLs por contexto
 *  Número 3365: Mejora: patrones por defecto de excluir Global adicional
 *  Número 3367: Exponer la ruta de acceso de inicio dir de ZAP a través de la API de ZAP
 *  Número 3374: Ajustar al más ancho de las columnas favorables usuario
 *  Número 3381: i18n núcleo extensión nombres
 *  Número 3387: Permitir esc cerrar AbstractFormDialog
 *  Problema 3392: muestra todos los mensajes enviados por la araña
 *  Número 3395: Añadir opción a spider de forma anónima con una sesión de
 *  Número 3398: Aumentar el límite del valor de las variables de la escritura global
 *  Número 3404: Agregar nuevo Default CSRF Token de OWASP CSRF Guard
 *  Número 3408: Mejorar el manejo de errores cuando restablecer las opciones de
 *  Problema 3443: Opciones de alertas de exponer a través de la API de ZAP
 *  Número 3446: Mejora: Añadir capacidad de exportar un mapa del sitio mediante el menú contextual
 *  Número 3457: Permite para filtrar base vista "URL" por la URL base
 *  Número 3460: Mejora: ofrecer ayuda para encontrar el directorio de registro en la interfaz de usuario
 *  Número 3461: Mejora: ver API no funciona al navegador no usa ZAP como proxy
 *  Número 3476: Permitir que las reglas pasivas elegir el tipo de mensajes
 *  Número 3481: Tablas de exportación a través de la interfaz de usuario
 *  Problema de 3498: Leve mejora: soporte mismas columnas en los resultados como historial
 *  Problema de 3500: Permiten para administrar etiquetas de mensajes en varias pestañas
 *  Cuestión 3508: Utilizar más reciente ECMAScript motor si está disponible
 *  Número 3514: Permiten para obtener varios mensajes por ID
 *  Emisión 3521: Solicitud mejora: agregar filtro a Panel de opciones de las reglas de exploración pasiva
 *  Número 3527: Actualizar script base para python 3
 *  Problema de 3529: Permite añadir reglas pasivas
 *  Número 3533: Botones de exportación tabla adicional
 *  Tema 3539: Mejora: recoger mensajes para analizar antes de la exploración activa
 *  3552 edición: Exponer etiquetas del mensaje mediante la API de ZAP
 *  Número 3559: ZAP opción API para emitir informe en formato JSON
 *  Problema 3574: Mostrar el nombre del Add-on en el panel de extensiones
 *  Tema 3587: Permite utilizar la configuración regional del sistema para el formato de
 *  Número 3594: ZAP API permite especificar dominios/direcciones que API se servirá de
 *  Número 3595: Imprimir msg args y error cuando no pudo analizar args
 *  Número 3599: Siempre atacar nodos de datos impulsada por
 *  Número 3619: Mostrar plugin como OFF, en los paneles de la política, si
 *  Número 3626: Permite borrar los mensajes con atajo de teclado
 *  Edición 3676: Mejora: eliminar alerta solo usando el api
 *  Problema de 3681: Utilizar número spinner para tiempo de espera de conexión
 *  Número 3686: Permiten para seleccionar IDs CWE/WASC y fuente de alerta
 *  Número 3688: Mostrar ID/nombre del escáner en la Alert tab
 *  Número 3691: Modernizado y refinados informes HTML
 *  Número 3700: Asegurar el panel con errores de validación es visible
 *  Número 3714: Spider - informe \# de nuevas terminales de descubierto
 *  Número 3727: Sitios árbol alfa tipo debe ignorar el método HTTP
 *  Problema de 3733: Ascan API - retorno cuenta alerta para cada escáner
 *  Número 3739: Permite saltar espera de escáneres
 *  Problema de 3765: Mostrar conteo de alerta en el diálogo de progreso de la exploración
 *  Tema 3769: Añadir control de botón de barra de herramientas de versiones
 *  Problema de 3770: Claro dockerfiles
 *  Número 3782: Añadir msg y cuenta alerta a la tarea de análisis activa API vista
 *  Asunto 3787: Escaneo pasivo añadido tiempo de espera
 *  Problema de 3793: Permite filtrar el panel de opciones de teclado
 *  Número 3808: añadido archivo de imagen de desnudo docker
 *  Número 3810: Añadir soporte de salida JSON a zap-completo-scan.py
 *  Cuestión 3818: Cambio haga clic en "Enviar..." para "Enviar a Manual solicitar Editor de"
 *  Tema 3836: Permiten la dirección de bucle invertido de IPv6 acceder a la API por defecto
 *  Problema de 3837: Añadir anoncsrf como nombre token anticsrf
 *  Número 3851: Spider nuevo analizar consistencia de la interfaz de usuario
 *  Cuestión 3871: Forma predeterminada, comprobación de actualizaciones en Inicio
 *  Número 3878: Ayuda conexiones persistentes en la API
 *  Problema de 3910: Permite saltar escáneres a través de la API
 *  Número 3918: archivo de docker mejora
 *  Problema de 3922: Refactorizar acceso objetivo en secuencias de comandos de docker
 *  Número 3931: Menor realce al mensaje de cuerpo muy grande respuesta
 *  Número 3977: Incluir mensajes de araña al comparar las sesiones
 *  Edición 3983: Permiten ZAP escuchar en múltiples direcciones o puertos
 *  Número 3992: Permite para habilitar código plegable en vistas de texto de cuerpo
 *  Problema de 3993: Agregado casilla de verificación seguro al diálogo de la opción de devolución de llamada.
 *  Número 4001: Permite borrar un contexto con atajo de teclado
 *  Edición 4049: Permiten para eliminar alertas con atajo de teclado
 *  Número 4053: Envoltura de línea AlertViewPanel
 *  Número 4055: Nueva pantalla de bienvenida
 *  Edición 4061: Actualización aplicación del motor NTLM
 *  Edición 4063: Validar que cmd - y - daemon no establecen
 *  Problema de 4066: Mejorar el mensaje de error en la secuencia de comandos API

## Corrección de error: ##

 *  Número 765: No funciona tecla Ctrl-F en reenviar / Manual de solicitud de cuadros de diálogo de Editor
 *  Número 1222: Falsos positivos: exploración de XSS
 *  Edición 1984: Siempre deben devolver alertas API 'evidencia' (y todas las otras teclas)
 *  Número 2375: No pueden cambiar de modo sin barra de herramientas principal
 *  Número 2496: ZAP sólo informe de la primera alerta de matriz
 *  Número 2744: No se puede activar/desactivar el modo de usuario forzado sin barra de herramientas principal
 *  Número 2756: Bloqueo de carga de clase al cargar script de httpsender de spidering y llamada a la API
 *  Problema de 2989: Historial de redirección no registrado cuando enviar solicitud
 *  Número 3154: Orden de ejecución de Plugins en exploración progreso detalles, ficha progreso
 *  Número 3207: Historial borra cuando sesión persistió
 *  Número 3284: Aceptar guiones bajos en nombres de host
 *  Tema 3289: Proxy excluir URLs todavía procesadas por ZAP
 *  Problema de 3350: wrong comparación de mensajes HTTP en queryEquals() método de clase HttpMessage
 *  Número 3351: la url desaparecen cuando yo haga clic en
 *  Número 3353: ZAP API ver: contextList método devuelve una cadena en lugar de la lista JSON
 *  Edición 3359: Falta pantalla de opciones de conexión de datos ayuda
 *  Número 3363: Spider mensajes vista incluye columna de etiquetas infrautilizadas
 *  Número 3377: ZAP ya no puede cargar scripts no UTF8
 *  Número 3382: Arreglar "error interno" en ScriptAPI
 *  Número 3394: Opción Habilitar seguimiento de sesión (cookies) no persistieron
 *  Número 3397: Desinstalar un archivo si no existe
 *  Número 3411: Borrar caché certs al establecer certificado de CA raíz
 *  Problema de 3440: Registro excepción cuando no pudo analizar el archivo de configuración proporcionado
 *  Número 3456: Bug: pausa explora limpió hacia fuera cuando persiste una sesión
 *  Número 3459: Mejora: previsualización de salida es confuso. Por favor aclarar.
 *  Número 3490: Representación de fuentes pobres en linux
 *  Problema de 3531: Scripts de Docker podrían atascarse en "Registros de exploración pasiva" aparentemente indefinidamente
 *  Número 3555: Cambio de nombre de la sesión, no se actualiza el nombre de la ventana
 *  Tema 3571: Requieren dependencias de extensión durante la extensión de carga
 *  Tema 3590: Establecer estado de instalación complementos de mercado
 *  Cuestión 3591: Correctamente comprobar si hay actualizaciones de Add-on en calc dep
 *  Tema 3620: Devolver error correcto en faltan parámetros de autenticación
 *  Edición 3621: Caché sincronización HistoryReference en ExtensionHistory
 *  Número 3632: No cerrar sesión al cambiar sus propiedades
 *  Cuestión 3633: "generar Anti CSRF prueba Form" no funciona
 *  Número 3648: Correcto estado de opción adv en diálogo de araña
 *  Número 3667: Problema de formato descuento Informe partida
 *  Problema 3673: API: sendHarRequest produce un error si los redireccionamientos son verdaderos
 *  Problema 3675: opción del árbol de sitios Mostrar solo las URL en el ámbito que no funciona
 *  Problema 3692: manejo camino correcto zap-api-scan.py
 *  Problema 3696: respuesta correcta de API para cambios de proxy salientes
 *  Problema 3703: org.parosproxy.paros.db.DatabaseException: java.sql.SQLException: no puede emitir executeUpdate() o executeLargeUpdate() para selecciona
 *  Número 3711: Instantáneas de la sesión podrían "romper" ejecutando exploraciones
 *  Número 3723: Restablecer correctamente panel de opciones de base de datos
 *  Número 3748: Saltar automáticamente analizadores dependiente
 *  Número 3759: Actualización versión llegadas zap.sh script de Java 9
 *  Tema 3771: Archivos de complemento que no se actualizan cuando se ejecuta la versión más reciente de ZAP/core
 *  Tema 3779: No puede abrir la ventana de reenvío falta fuente
 *  Problema de 3799: Declarar ExtensionDynSSL mem bajo apoyo
 *  Número 3825: Error de mostrar si no se activa el certificado
 *  Tema 3827: valor NULL mysql en donde en la cláusula
 *  Número 3832: Errores en las plantillas de vectores de entrada
 *  Número 3849: Pscanrule contenido tipo Missing no funciona con mensajes de spider
 *  Problema de 3854: Error durante el uso de Api - ERROR ExtensionUserManagement - a los usuarios
 *  Tema 3889: Inicializar el origen de la alerta siempre
 *  Número 3895: JSON entrada Vector error si string ha citado caracteres
 *  Problema de 3907: Normalizar validación de URL basado en formularios de login, uso
 *  Número 3912: VariantDirectWebRemotingQuery podría colgar en bucle infinito
 *  Tema 3914: Archivo de uso ZapVersions.xml en imágenes de Docker
 *  Número 3927: zap-full-scan en docker intenta llegar a la red externa
 *  Problema 3955: Base de datos demasiado pequeño para manejar cuerpos de solicitud de login grande
 *  Problema 3965: Encabezado Cookie vacía provoca errores
 *  Número 3969: Iniciar sesión/indicadores no persistió cuando
 *  Número 4004: zap.bat debe usar %USERPROFILE% en lugar de %HOMEDRIVE%%HOMEPATH%
 *  Tema 4013: Enviar hasta el punto final de devolución de llamada mientras que proxy a través de ZAP registra un error
 *  Número 4014: Problema al intentar ignorar todas las reglas para una dirección URL
 *  Tema 4028: Advertir cuando busque actualizaciones falla
 *  Edición 4056: Utilizar el dominio como dominio para la autenticación NTLM
 *  Edición 4065: Borrar una URL de padre en el historial no debe eliminar todas las URLs de niño

## ZAP romper cambios de API: ##

### Autenticación de acción / setAuthenticationMethod ###

El tipo de autenticación "formBasedAuthentication" ahora requiere la URL de inicio de sesión siempre en forma codificada. El cambio garantiza el inicio de sesión que se que utiliza/Enviar URL como fue especificado. Anteriormente aceptaría URL codificadas parcialmente pero se a codificado cuando se usa, conduce potencialmente a un URL diferente se utiliza/se envía.

### Contexto vista / contextList ###

Este cambio rompe a los consumidores que manualmente analizar/extraían los nombres de la cadena. Se cambió la estructura de los datos devueltos para separar correctamente cada nombre:

> ``````````
> {"contextList":["Context 1","Context 2"]}
> ``````````

y en la

> ``````````
> <contextList type="list">
>     <contextName>Context 1</contextName>
>     <contextName>Context 2</contextName>
> </contextList>
> ``````````

En lugar de

> ``````````
> {"contextList":"[Context 1, Context 2]"}
> ``````````

y en la

> ``````````
> <contextList>[Context 1, Context 2]</contextList>
> ``````````

### Núcleo de vista / setOptionUseProxyChain ###

Cambiado para volver `FAIL` Si el proxy saliente no fue habilitado (porque la necesaria dirección/nombre de host no se ha establecido anteriormente), antes de que volvería siempre `OK`.

## ZAP API cambia criterios de valoración: ##

### Núcleo de vista / alertas ###

Parámetro riskId opcional añadido para facilitar el riesgo de filtración. Donde riskId está en el rango 0 para informativo y 3 de alto.

### VER núcleo / número de Alertas ###

Parámetro riskId opcional añadido para facilitar el riesgo de filtración. Donde riskId está en el rango 0 para informativo y 3 de alto.

### Núcleo de vista / alertas ###

Añadido opcional `baseurl` parámetro, para filtrar las URL que se devuelven.

### VER AScan / escaneos ###

Modificado para devolver también la cantidad total de alertas generadas y los mensajes enviados durante cada exploración.

### VER AScan / escaneos ###

Modificado para devolver también la cantidad de alertas generadas por cada escáner.

## ZAP API Nuevos puntos finales: ##

### Núcleo de vista / alertas ###

Una nueva vista de Resumen de alertas que muestra cuentas de alertas por el nivel de riesgo. Opcionalmente, filtrados por un valor de baseurl.

> ``````````
> {"High":0,"Low":132,"Medium":39,"Informational":153}
> ``````````

### Núcleo de vista / messagesById ###

Gets the HTTP messages with the given IDs.

### Núcleo de vista / messagesHarById ###

Obtiene los mensajes HTTP con el ID dado, en formato HAR.

### Núcleo de vista / optionAlertOverridesFilePath ###

Obtiene la ruta del archivo con anulaciones alerta.

### Núcleo de vista / optionMaximumAlertInstances ###

Obtiene el número máximo de instancias alerta para incluir en un informe.

### Núcleo de vista / optionMergeRelatedAlerts ###

Obtiene o no alertas relacionadas se combinarán en los informes generados.

### Núcleo de vista / zapHomePath ###

Obtiene la ruta al directorio de ZAP.

### Ver localProxies / additionalProxies ###

Obtiene todos los servidores proxy adicionales que se han configurado.

### Vista spider / optionAcceptCookies ###

Obtiene o no un proceso de araña debe aceptar las cookies mientras spidering.

### Núcleo de acción / deleteAlert ###

Borra la alerta con el identificador dado.

### Núcleo de acción / setOptionAlertOverridesFilePath ###

Establece (o elimina, si está vacío) reemplaza a la ruta del archivo con la alerta.

### Núcleo de acción / setOptionMaximumAlertInstances ###

Establece el número máximo de instancias alerta para incluir en un informe. Un valor de cero se trata como ilimitado.

### Núcleo de acción / setOptionMergeRelatedAlerts ###

Establece o no alertas relacionadas se combinarán en los informes generados.

### ACCIÓN ascan / importScanPolicy ###

Las importaciones a una política de exploración usando la ruta de sistema de archivo.

### ACCIÓN ascan / skipScanner ###

Salta el explorador utilizando el ID de la exploración y el escáner.

### Ver localProxies / addAdditionalProxy ###

Agrega a un nuevo proxy mediante los datos suministrados. Ver la [Pantalla de opciones de Proxies locales][] para obtener información detallada de los parámetros.

### Ver localProxies / removeAdditionalProxy ###

Quita al proxy adicional con la dirección especificada y el puerto.

### Acción de spider / setOptionAcceptCookies ###

Establece o no un proceso de spider debe aceptar las cookies mientras spidering.

## Detalles de la vulnerabilidad ##

La siguiente vulnerabilidad se ha divulgado en una versión anterior de ZAP.
Muchas gracias a todos los investigadores que éticamente nos han comunicado cuestiones a través de nuestro [bug bounty program][].
Si usted necesita más detalles acerca de esta vulnerabilidad entonces póngase en contacto con nosotros.

### Desinstalador de Windows Vulnerable a DLL Hijacking ###

El desinstalador de Windows ZAP para 2.6.0 es vulnerable a DLL secuestro en Windows. Se trataba de una vulnerabilidad en el instalador de partido 3 º Install4j que ahora se ha solucionado.
Tenga en cuenta que esto sólo puede ocurrir si una DLL maliciosa ya está en el camino.

**Crédito: Sajeeb Lohani (sml555) de ZDS a prueba de balas**

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


[Pantalla de opciones de Proxies locales]: HelpUiDialogsOptionsLocalproxy
[bug bounty program]: https://bugcrowd.com/owaspzap