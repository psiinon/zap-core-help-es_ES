# Versión 2.1.0 #

Se hicieron los siguientes cambios en esta versión:

## Cambios menores: ##

### Número 355: Permiten Fuzzing posicional ###

### Emisión 475: Valor sesiones Http cookies personalizadas ###

### 484 del problema: Compruebe la versión del java en zap.sh ###

### Edición 496: Permite ver la solicitud y respuesta al mismo tiempo en la ventana principal ###

### Issue 505: Http Session API Implementation ###

### Edición 515: Cambiar add-ons para hacer uso de carga automática de mensajes ###

### Número 516: Cambiar complementos mensajes claves que prefijo único ###

### Edición 518: Agregar compatibilidad con OData ###

### Edición 537: Opción a fuerza de buscar archivos y recursos con las extensiones definidas por el usuario ###

### Problema 538: Permitir que se seleccionen líneas no secuenciales en el registro de historial ###

### Número 542: ver api - ventana pronto para permitir ###

### Edición 551: Añadir csrfmiddlewaretoken a la lista de tokens de predeterminados Anti csrf ###

### Problema 552: haga ZapPortNumberSpinner una subclase de ZapNumberSpinner ###

### Problema 553: opción Agregar para filtrar alertas por alcance ###

### Edición 561: Opción de copiar los enlaces con el clic ###

### Edición 566: Clase abstracta para crear popups genéricos ###

### Problema 568: Permitir que las extensiones se ejecuten desde la línea de comando ###

### Problema 569: permitir que Spider Scan comience sin una visita previa ###

### Problema 587: Actualice a JBroFuzz ​​2.5 ###

### Problema 592: No mostrar el menú emergente principal si no tiene elementos visibles del menú emergente ###

### Problema 597: se muestra el campo "Autor" en los complementos disponibles (pestaña "Mercado") ###

### Problema 602: Permitir (explícitamente) elegir el tipo de archivo al exportar URLs al archivo ###

### Issue 605: Force intercepts via header ###

### Problema 621: maneja las solicitudes al proxy URL (y genera un archivo PAC) ###

### Problema 638: Sesiones persistentes e instantáneas en lugar de guardarlas ###

## Corrección de error: ##

### Problema 150: java.io.IOException en org.owasp.jbrofuzz.system.Logger.checkOrCreateDirs ###

### Problema 205: una opción previamente guardada (Barra de herramientas) no está configurada en el inicio cuando está marcado "Solicitar credenciales de proxy al iniciar". ###

### Problema 317: Mueva (o proteja) el botón 'Bin' ###

### Problema 452: API: cierre asíncrono ###

### Problema 488: categorías de Fuzz disponibles para la categoría predeterminada no actualizadas después de instalar / desinstalar un complemento (con archivos fuzz) ###

### Problema 490: la nueva autenticación solo funciona con el escáner activo ###

### Problema 499: NullPointerException al desinstalar un complemento con un editor de solicitud manual ###

### Problema 500: NullPointerException al desinstalar manualmente un complemento instalado ###

### Problema 501: ExtensionFactory conserva referencias a complementos desinstalados (con extensiones) ###

### Problema 502: los complementos instalados manualmente no permanecen instalados ###

### Problema 504: la tabla de complementos instalados puede no actualizarse después de instalar manualmente un complemento ###

### Problema 507: la pestaña Inicio rápido no tiene un panel de desplazamiento ###

### Número 508: Algunos complementos no descarga todos sus componentes al desinstalar ###

### Edición 509: Quitar complemento ResourceBundle al desinstala un complemento ###

### Edición 509: Quitar complemento ResourceBundle al desinstala un complemento ###

### Edición 511: Permitir complementos quitar etiquetas de estado de pie de página ###

### Problema de 512: Permiten para quitar la etiqueta de estado de pie de página añadida por la ScanPanel ###

### Edición 513: Etiquetas de estado de pie de página no inmediatamente se muestra cuando un Add-on está instalado ###

### Edición 514: Etiqueta de estado de pie de página navegación forzada todavía utiliza icono de llave inglesa ###

### Número 517: Add-ons se añaden al cargador de clases "principales" cuando se instala ###

### Edición 520: MissingResourceException al generar "Alertas" Informe ###

### Edición 524: Autenticación de Host se utiliza incluso cuando deshabilita ###

### Edición 525: Falla "Informe / exportar todas las direcciones URL a archivo..." ###

### Número 528: Diálogo de progreso de la exploración puede mostrar tiempos de progreso negativo ###

### Edición 533: Por defecto los puertos 80 y 443 se añaden a los sitios en el árbol de sitio ###

### Edición 540: Fichas de trabajo maximizados ocultados cuando respuesta ficha cambiadas de posición ###

### Número 548: Mensajes de Diff se anexan al diálogo "Diff" ###

### Edición 549: Diff del menú cuando se seleccionaron el nodo de raíz de árbol de "Sitios" y un nodo secundario ###

### Edición 550: Fuzzer - paradas de desbordamiento de búfer debido a java.sql.SQLDataException: excepción de datos: datos de cadena, truncamiento derecho ###

### Edición 558: Auto Etiquetado roto ###

### Edición 564: Scanner activo puede colgar si utilizan las dependencias ###

### Edición 565: Mercado: descargas no usan configuración Proxy ascendente ###

### Número 567: Error de ortografía ###

### Número 574: Spider falla cuando se invoca mediante la API ###

### Edición 579: Algunos objetivos (estructura) incorrectamente se basan en la codificación predeterminada de plataforma ###

### Edición 582: NullPointerException al abrir una sesión en modo demonio ###

### Edición 583: NullPointerException al mismo tiempo, una sesión en modo demonio con «WebSockets» complemento instalado ###

### Edición 588: ExtensionHistory.historyIdToRef debe ser despejó al cambiar sesión ###

### Edición 593: Inicio rápido puede comenzar la exploración activa sin esperar a que la spider terminar ###

### Edición 614: Etiquetas de SessionFixation mal ###

### Edición 616: Manijas de spider forman incorrectamente acciones que contengan fragmentos (\#) ###

### Edición 617: NullPointerException cuando spidering un contexto ###

### Edición 622: Pide proxy Local no puede detectar correctamente a sí mismo ###

### : 626 barra de desplazamiento de áreas de texto de alerta se trata siempre en la parte inferior ###

### Edición 627: Permitir complementos quitar botones/separadores de barra de herramienta principal ###

### Edición 628: Permitir complementos quitar la API registrada ###

### Edición 632: Manual Editor de pedir diálogo (HTTP) las configuraciones que no se guardan correctamente ###

### Edición 633: Escáneres de etiqueta automática se muestran en tabla de escáneres pasivos ###

### Edición 633: Escáneres de etiqueta automática se muestran en tabla de escáneres pasivos ###

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