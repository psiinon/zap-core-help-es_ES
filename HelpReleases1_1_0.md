# Release 1.1.0 #

Se hicieron los siguientes cambios en esta versión:

## Cambios significativos: ##

### OWASP rebranding ###

ZAP has been accepted as an OWASP project.
Its homepage is now: https://www.owasp.org/index.php/OWASP\_Zed\_Attack\_Proxy\_Project

### Fuerza Bruta ###

La capacidad de fuerza bruta archivos y directorios basados en el código del proyecto OWASP DirBuster.
La nueva ficha de fuerza bruta muestra los archivos y directorios encontrados.

### Escaneo de puertos ###

La capacidad de sitios de escaneo de puertos.
La nueva ficha de análisis de puertos muestra los puertos que se encuentran.

### Pestaña de Escaneo Activo ###

La nueva [Pestaña de Escaneo Activo][Pesta_a de Escaneo Activo] muestra las peticiones y respuestas como resultado de la exploración activamente un sitio.

### Pestaña araña ###

Se mostrará la [Spider tab][] ahora le permite seguir utilizando ZAP mientras spidering un sitio.
También puede pausar y reanudar el spider.

### Soporte de tarjeta inteligente ###

C/o proyecto Andiparos ha añadido soporte de tarjeta inteligente.
Han probado los siguientes dispositivos de tarjeta inteligente en Windows:

<table> 
 <tbody>
  <tr>
   <td>&nbsp;&nbsp;&nbsp;&nbsp;</td>
   <td>Salvaguardia</td>
   <td>Aladdin eToken</td>
  </tr> 
  <tr>
   <td>&nbsp;&nbsp;&nbsp;&nbsp;</td>
   <td></td>
   <td>Aladdin eToken Pro</td>
  </tr> 
  <tr>
   <td>&nbsp;&nbsp;&nbsp;&nbsp;</td>
   <td>Omnikey</td>
   <td>Omnikey 3121</td>
  </tr> 
  <tr>
   <td>&nbsp;&nbsp;&nbsp;&nbsp;</td>
   <td></td>
   <td>CardMan 6121</td>
  </tr> 
  <tr>
   <td>&nbsp;&nbsp;&nbsp;&nbsp;</td>
   <td>Gemalto</td>
   <td>Reflex 20 V2</td>
  </tr> 
  <tr>
   <td>&nbsp;&nbsp;&nbsp;&nbsp;</td>
   <td></td>
   <td>Swiss Stick</td>
  </tr> 
 </tbody>
</table>

Han probado los siguientes dispositivos de tarjeta inteligente en Windows:

<table> 
 <tbody>
  <tr>
   <td>&nbsp;&nbsp;&nbsp;&nbsp;</td>
   <td>Omnikey</td>
   <td>CardMan 4040</td>
  </tr> 
 </tbody>
</table>

### Menú de ataque ###

El nuevo [Pestaña Sitios][Pesta_a Sitios] menú de clic derecho 'Attack' le permite iniciar varias exploraciones.

### Internacionalización más ###

Todas las fichas principales y elementos de menú ahora se ha internacionalizado.

### Localización ###

Soporte para los siguientes idiomas están incorporadas en esta versión:

<table> 
 <tbody>
  <tr>
   <td>&nbsp;&nbsp;&nbsp;&nbsp;</td>
   <td>Ingl&eacute;s</td>
   <td>Idioma predeterminado</td>
  </tr> 
  <tr>
   <td>&nbsp;&nbsp;&nbsp;&nbsp;</td>
   <td>Portugu&eacute;s Brasile&ntilde;o</td>
   <td></td>
  </tr> 
  <tr>
   <td>&nbsp;&nbsp;&nbsp;&nbsp;</td>
   <td>Alem&aacute;n</td>
   <td></td>
  </tr> 
  <tr>
   <td>&nbsp;&nbsp;&nbsp;&nbsp;</td>
   <td>Polaco</td>
   <td></td>
  </tr> 
  <tr>
   <td>&nbsp;&nbsp;&nbsp;&nbsp;</td>
   <td>Espa&ntilde;ol</td>
   <td></td>
  </tr> 
 </tbody>
</table>

### Selección de idioma: ###

En la puesta en marcha se pedirá que elija el idioma a utilizar.
Nuevos lenguajes son automáticamente detectados por la presencia de archivos con nombres de la forma Messages\_ <locale>.properties en el directorio ZAP.

## Cambios menores: ##

### Desactivar plugins 'default file' ###

Los plugins que detecta archivos predeterminados son despedidos con eficacia por el bruto nueva fuerza escáner.
Estos por lo tanto que se haya desactivado.

### Resúmenes de escáner ###

Cuenta del número y tipos de los análisis actuales se muestra ahora en la [footer][].

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
   <td> <a href="HelpCredits" rel="nofollow">Credits</a></td>
   <td>las personas y grupos que han hecho posible esta versi&oacute;n</td>
  </tr> 
 </tbody>
</table>


[Pesta_a de Escaneo Activo]: HelpUiTabsAscan
[Spider tab]: HelpUiTabsSpider
[Pesta_a Sitios]: HelpUiTabsSites
[footer]: HelpUiFooter