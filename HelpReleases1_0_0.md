# Release 1.0.0 #

Se hicieron los siguientes cambios en esta versión:

## Cambios significativos: ##

### Pantallas de ayuda ###

Ayuda se han agregado pantallas para todas las funciones proporcionadas por ZAP.
Ayuda sensible al contexto también se ha implementado para que al presionar la tecla F1 se muestre la pantalla de ayuda de la tab seleccionada.

### Break Points ###

La implementacion de [Puntos de interrupción][Puntos de interrupci_n] se ha cambiado para estar más cerca a aquella proporcionada por entornos integrados de desarrollo de software.
Los controles del punto de interrupción se han movido a la nueva [La barra de herramientas de nivel superior][].
Break points can now also be set by right clicking nodes in the [Sitios][] y en la [Pestaña Historia][Pesta_a Historia].

### Menú de reporte ###

Se mostrará la [Report Menu][] ha cambiado significativamente y ahora incluye los siguientes elementos del menú:

<table> 
 <tbody>
  <tr>
   <td>&nbsp;&nbsp;&nbsp;&nbsp;</td>
   <td>Generar informe XML...</td>
   <td>Que genera informes en el demanda</td>
  </tr> 
  <tr>
   <td>&nbsp;&nbsp;&nbsp;&nbsp;</td>
   <td>Exportar mensajes a fichero...</td>
   <td>Desde el <a href="HelpUiTlmenuFile" rel="nofollow">men&uacute; Archivo</a></td>
  </tr> 
  <tr>
   <td>&nbsp;&nbsp;&nbsp;&nbsp;</td>
   <td>Exportar respuesta a fichero...</td>
   <td>Desde el <a href="HelpUiTlmenuFile" rel="nofollow">men&uacute; Archivo</a></td>
  </tr> 
  <tr>
   <td>&nbsp;&nbsp;&nbsp;&nbsp;</td>
   <td>Exportar Todas las URLs a un fichero...</td>
   <td>Nueva funcionalidad</td>
  </tr> 
  <tr>
   <td>&nbsp;&nbsp;&nbsp;&nbsp;</td>
   <td>Comparar con otra Sesi&oacute;n...</td>
   <td>Nueva funcionalidad</td>
  </tr> 
 </tbody>
</table>

### Búsqueda de la mejor historia ###

El nuevo [Buscar en pestañas][Buscar en pesta_as] le permite buscar expresiones regulares en todas las URLs, las solicitudes y respuestas.
Botones anteriores y siguiente te permiten ver los términos de búsqueda encontrado en la [Petición][Petici_n] y en la [Response tabs][].


### Filtro de historial ###

[La barra de herramientas filtro de historia][Pesta_a Historia] ha añadido que le permite restringir las solicitudes de que se muestran.
Las solicitudes pueden ser filtradas en base a los métodos HTTP, los códigos de resultado HTTP y cualquier [etiquetas][], [alertas][], o [notas][] se han aplicado.

### Notas ###

You can now associate [notas][] con cualquier petición.

### Múltiples etiquetas ###

Ahora puede asociar múltiples [etiquetas][] con cualquier petición.

### Más control sobre las alertas ###

Se mostrará la [Añadir Alerta,][A_adir Alerta] permite manualmente agregar o cambiar una alerta.

### Nuevo codificador/decodificador ###

Un nuevo [Encode/Decode/Hash dialog][Encode_Decode_Hash dialog] ha sustituido el codificador/el decodificador anterior.

### Escaneo pasivo ###

[Escaneo pasivo][] se ha agregado
En esta versión de ZAP utilizará sólo escaneo pasivo para agregar automáticamente [etiquetas][].
Comunicados en el futuro también puede aumentar [alertas][] para posibles problemas.

## Cambios menores: ##

### La barra de herramientas de nivel superior ###

[La barra de herramientas de nivel superior][] ha sido agregado y proporciona botones de configuración para la funcionalidad comúnmente utilizada.

### Resúmenes de pie alerta ###

Cuentas de alta, media, baja e informativo [alertas][] ahora se muestran en el [pie][].

### Ver y sentir ###

Se utiliza un nuevo aspecto 'Nimbus'.

### Manejo de contraseña de proxy ###

[La pantalla de opciones de conexión][La pantalla de opciones de conexi_n] tiene una nueva opción para 'Pedir credenciales de proxy en la puesta en marcha'.
Si se selecciona esta opción entonces la contraseña de proxy no se almacenará en el disco duro.

### Enviar la ficha de sitios ###

Se mostrará la [Pestaña de sitios][Sitios] que le permite enviar la solicitud después de hacer los cambios que desee.

### Directorio de usuario entre sesiones ###

El último directorio utilizado por el usuario ahora se almacena en el archivo de configuración para que se mantenga entre sesiones.

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
 </tbody>
</table>


[Puntos de interrupci_n]: HelpStartConceptsBreakpoints
[La barra de herramientas de nivel superior]: HelpUiTltoolbar
[Sitios]: HelpUiTabsSites
[Pesta_a Historia]: HelpUiTabsHistory
[Report Menu]: HelpUiTlmenuReport
[Buscar en pesta_as]: HelpUiTabsSearch
[Petici_n]: HelpUiTabsRequest
[Response tabs]: HelpUiTabsResponse
[etiquetas]: HelpStartConceptsTags
[alertas]: HelpStartConceptsAlerts
[notas]: HelpStartConceptsNotes
[A_adir Alerta]: HelpUiDialogsAddalert
[Encode_Decode_Hash dialog]: HelpUiDialogsEnc_dec
[Escaneo pasivo]: HelpStartConceptsPscan
[pie]: HelpUiFooter
[La pantalla de opciones de conexi_n]: HelpUiDialogsOptionsConnection