# Opciones de control para pantalla de actualizaciones #

Esta pantalla te permite configurar si ZAP debe comprobar para ver si estás ejecutando la última versión cuando se inicie, y en este caso qué debe hacer.

### Comprobar actualizacones al inicio ###

Si se selecciona, entonces ZAP comprobará automáticamente la existencia de actualizaciones de la aplicación por completo y de todos los complementos al inicio.
Se recomienda encarecidamente que esta opción se marque.
Si por alguna razón escoges no hacerlo, entonces debes comprobar manualmente si hay actualizaciones con frecuencia.
ZAP solo hará una solicitud, y la única información incluida será la versión actual que utilizas.

### Descargar automáticamente nuevas versiones de ZAP ###

Si se selecciona, entonces ZAP descargará automáticamente nuevas versiones de ZAP cuando estén disponibles y pedirá la instalación.

### Instalar automáticamente actualizaciones a los complementos que han sido instalados ###

Si se selecciona, entonce ZAP automáticamente descargará e instalará cualquier actualización a los complementos que tienes instalados.

### Instalar automáticamente actualizaciones a las reglas de escaneo que has instalado ###

Si se selecciona, entonces ZAP automáticamente descargará e instalará cualquier actualización a las reglas de escaneo que has instalado.
Estos son un subconjunto del conjunto completo de complmenetos instalados.

### Informar sobre el lanzamiento de nuevos complementos de calidad ###

Si se selecciona entonces ZAP te informará si y cuando cualquier complemento sea promovido a la categoría de calidad.
Estos complementos habrán sido probados rigurosamente y revisados, y puedes estar seguro de que son de la más alta calidad.

### Report new beta quality add-ons ###

If selected then ZAP will inform you if and when any add-ons are promoted to 'beta' quality.
These add-ons will have been tested and reviewed, and are considered to be of a reasonable quality and mostly fit for purpose.
Sin embargo pueden estar incompletos o necesitar mayores pruebas.
Algunos de los complementos incluidos en ZAP por defecto todavía se encuentran en nivel beta.

### Report new alpha quality add-ons ###

If selected then ZAP will inform you if and when any new add-ons are added at 'alpha' quality.
These add-ons will have been reviewed but they are typically at an early stage of development.
They may be incomplete, contain significant issues or cause stability problems.

### Directorios de complementos ###

ZAP cargará todos los complementos del [default `plugin` directories][default _plugin_ directories].
También puedes agregar tantos directorios adicionales de complementos como lo necesites agregándolos aquí.
Esto puede ser muy útil al ejecutar múltiples instancias de ZAP en una máquina, por ejemplo en un entono de CI.
Puedes descargar complementos nuevos o actualizados una vez e inmediatamente compartirlos entre múltiples instancias.
Los complementos descargados a los directorios compartidos solo serán agregados a nuevas instancias de ZAP, no a aquellas que ya están ejecutándose, con la excepción de la instancia que descargó el complemento.

### Directorio de descargas ###

Este es el directorio en el que ZAP descargará complementos nuevos o actualizados.
Por defecto será el directorio local, pero también puedes escoger uno de los directorios compartidos siempre y cuando esta instancia de ZAP pueda escribir en él.
ZAP solo moverá complementos a un directorio compartido una vez que estén descargados por completo, para que otras instancias de ZAP no intente cargar un complemento incompleto.

## Vease también ##

<table> 
 <tbody>
  <tr>
   <td>&nbsp;&nbsp;&nbsp;&nbsp;</td>
   <td> <a href="HelpUiOverview" rel="nofollow">UI Overview</a></td>
   <td>Para una vista general sobre la interfaz de usuario</td>
  </tr> 
  <tr>
   <td>&nbsp;&nbsp;&nbsp;&nbsp;</td>
   <td> <a href="HelpUiDialogsOptionsOptions" rel="nofollow">Cuadros de di&aacute;logos de opciones</a></td>
   <td>for details of the other Options dialog screens</td>
  </tr> 
 </tbody>
</table>


[default _plugin_ directories]: HelpStartConceptsAddons