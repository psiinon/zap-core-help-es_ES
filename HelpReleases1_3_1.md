# Versión 1.3.1 #

Se hicieron los siguientes cambios en esta versión:

## Corrección de error: ##

### Problema 97: Directorio de trabajo para aplicaciones ###

### Problema 98: No es posible cancelar el control de actualizaciones ###

### Problema 100: Solapa alertas tiene 2 'enviar...' a la derecha haga clic en ventanas emergentes ###

### Problema 104: cuadro de diálogo de advertencia de pantalla, cuando no existe ningún certificado de CA raíz ###

### Problema 110: elegir el idioma del usuario de forma predeterminada, al iniciar la primera vez ###

### Problema 112: Proporcione una forma de aplicar paquetes de idioma en Mac OS ###

### Problema 121: Reporte de comparación de sesión javascript dañado en Firefox 3 ###

### Tema 123: Cant https seleccionadas sitio de ventana escaneo activo si hay un equivalente http ###

### Problema 127: la característica de token de CSRF no funciona en fuzz: explicación de ayuda adicional para la reparación parcial ###

### Problema 140: las opciones de visualización no deberían incluir las opciones avanzadas o de administrador de Windows ###

### Error SSL que impidió establecer conexiones SSL en cualquier navegador ###

## Problemas conocidos: ##

### Mac OS X: SSL dinámico y Google Chrome ###

Actualmente Dynamic SSL no funciona cuando se usa Google Chrome. Esto se debe a un problema conocido no resuelto con Google Chrome y Mac OS X Keychain. Al importar la CA raíz de OWASP ZAP al llavero y solicitar un sitio web SSL, se muestra un mensaje de error de "Certificado no válido".

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