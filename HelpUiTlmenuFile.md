# El menú Archivo #

Este menú se encarga de la sesión actual. Por defecto los siguientes elementos del menú estarán presentes:


### Nueva sesión ###

Esto crea una nueva sesión.
Si no has guardado la sesión actual se mostrará una advertencia.
Iniciar una nueva sesión sin guardar la actual se perderá toda la información de la sesión actual.

### Abrir sesión ###

Esto abre una sesión que ha sido previamente guardada.
Abrir nueva sesión sin guardar la actual se perderá toda la información de la sesión actual.

### Mantener sesión... ###

Esto mantiene la sesión actual.
Mientras que la sesión siembre se almacena en una base de datos en el disco, se perderá cuando ZAP se detenga a menos que haya sido mantenida.
Solo se necesita mantener una vez, luego se guardarán todos los cambios.

### Fotos instantánea de sesión como... ###

Esto guarda una instantánea de una sesión que ya se ha mantenido.
Sugiere que el mismo nombre del archivo sea el mismo de la sesión mantenida con una cadena de fecha anexado a él, y permite al usuario establecer cualquier nombre que el elija.


### Propiedades de la sesión... ###

Esto muestra el cuadro de diálogo [Propiedades de la Sesión][Propiedades de la Sesi_n] .
Esto permite escoger el nombre de la sesión y la descripción.

### Importar contexto... ###

Permite importar un [Contexto][].

### Exportar contexto... ###

Permite exportar un Contexto.

### Cargar archivo de complemento... ###

Carga un archivo local de [complemento][] .
Los complementos generalmente se instalan a través del cuadro de diálogo [Administrar Complementos][] , pero esta opción solo es útil si se ha descargado manualmente un complemento o si se está poniendo a prueba uno que haya desarrollado uno mismo.
Los complementos se mantienen instalados hasta que se desinstalen manualmente.

### Salir y Eliminar Sesión... ###

Esto sale de ZAP y elimina la sesión, incluso si ha sido previamente mantenida.
La sesión ya no será accesible cuando se reinicie ZAP, aunque cualquier foto instantánea tomada todavía estará disponible.
Un cuadro de diálogo de advertencia se mostrará para asegurar si realmente se quiere elegir esta opción.

### Salir ###

Esto saldrá de ZAP.
Si no has guardado la sesión actual entonces se le dará la opción de hacerlo.

Tenga en cuenta que [ add-ons ][complemento] puede agregar elementos de menú adicionales.

## Vease también ##

<table> 
 <tbody>
  <tr>
   <td>&nbsp;&nbsp;&nbsp;&nbsp;</td>
   <td> <a href="HelpUiTlmenuTlmenu" rel="nofollow">Men&uacute; de nivel superior</a></td>
   <td></td>
  </tr> 
  <tr>
   <td>&nbsp;&nbsp;&nbsp;&nbsp;</td>
   <td> <a href="HelpUiOverview" rel="nofollow">UI Overview</a></td>
   <td>Para una vista general sobre la interfaz de usuario</td>
  </tr> 
 </tbody>
</table>


[Propiedades de la Sesi_n]: HelpUiDialogsSessionSessprop
[Contexto]: HelpStartConceptsContexts
[complemento]: HelpStartConceptsAddons
[Administrar Complementos]: HelpUiDialogsManageaddons