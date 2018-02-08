# Activar Diálogos de Escaneos #

Este cuadro de diálogo presenta la [active scanner][].


### Scope ###

La primera pestaña le permite seleccionar o cambiar el punto de partida.
Si usted tiene más que una [scan policies][] entonces, usted podrá seleccionar para utilizarlo.
Si el punto de partida es de uno o más [Contexts][] Luego podrás elegir uno de ellos.
Si ese contexto tiene alguna [Users][] definirá a continuación. Usted podrá seleccionar uno de ellos.
Si selecciona uno de los usuarios la exploración activa se realizará como ese usuario, con ZAP (re) autenticar como usuario siempre que sea necesario.

Si selecciona 'recurse', todos los nodos debajo de un seleccionado también se explorará.
Vectores de entrada personalizados sólo se admiten si esta opción no está seleccionada.

Si selecciona "Show advanced options" luego las siguientes fichas se mostrará que proporcionan control de grano fino sobre el proceso de escaneo activo.

Haciendo clic en el botón 'Reset' se restablecerán todas las opciones a sus valores predeterminados.

### Input Vectors ###

Los Input Vectors permiten reemplazar los vectores de entrada por defecto que están definidos en las [Options Active Scan Input Vectors screen][].
Haciendo click en el botón 'Reset', usted reinicia los input vectores que estén predeterminados por defecto.

### Custom Vectors ###

La pestaña Custom Vectors permite especificar ubicaciones definidas en la solicitud de ataque.
Los Custom Vectors solo están disponibles si no se selecciona la opción 'recurse' en la primera pestaña.
Para agregar input vectors, resalte los caracteres que desea atacar en la solicitud y haga clic en el botón 'Add'.
Puede agregar tantos vectores de entrada personalizados como quieras.
Para eliminar los custom input vectors destacan cualquiera de los caracteres seleccionados y haga clic en el botón 'Remove'.
Marca la casilla 'Disable non custom input vectors' deshabilita todos los vectores de entrada excepto los que defines manualmente en esta ficha.

### Tecnología ###

La tecnología ficha le permite especificar qué tipos de tecnologías para la exploración.
Las tecnologías sin selección que usted sabe que no están presentes en el destino de la aplicación, pueden acelerar la exploración como reglas que tienen como objetivo que la tecnología pueda omitir esas pruebas.

### Policy ###

La ficha Policy permite reemplazar cualquiera de la configuración especificada en la [scan policy][scan policies].



## Acceder a través de ##

<table> 
 <tbody>
  <tr>
   <td>&nbsp;&nbsp;&nbsp;&nbsp;</td>
   <td><a href="HelpUiTabsAscan" rel="nofollow">Active Scan tab</a></td>
   <td>'New Scan' button</td>
  </tr> 
  <tr>
   <td>&nbsp;&nbsp;&nbsp;&nbsp;</td>
   <td><a href="HelpUiTlmenuTools" rel="nofollow">Top level Tools menu</a></td>
   <td>'Active Scan...' menu item</td>
  </tr> 
  <tr>
   <td>&nbsp;&nbsp;&nbsp;&nbsp;</td>
   <td><a href="HelpUiTabsSites" rel="nofollow">Sites tab</a></td>
   <td>'Attack / Active Scan... right click menu item</td>
  </tr> 
  <tr>
   <td>&nbsp;&nbsp;&nbsp;&nbsp;</td>
   <td><a href="HelpUiTabsHistory" rel="nofollow">History tab</a></td>
   <td>'Attack / Active Scan...' right click menu item</td>
  </tr> 
 </tbody>
</table>

## Vease también ##

<table> 
 <tbody>
  <tr>
   <td>&nbsp;&nbsp;&nbsp;&nbsp;</td>
   <td> <a href="HelpUiOverview" rel="nofollow">UI Overview</a></td>
   <td>Para tener una visi&oacute;n general del IU</td>
  </tr> 
  <tr>
   <td>&nbsp;&nbsp;&nbsp;&nbsp;</td>
   <td> <a href="HelpUiDialogsDialogs" rel="nofollow">Dialogos</a></td>
   <td>Para m&aacute;s detalles de los cuadros de di&aacute;logo o pop-ups </td>
  </tr> 
 </tbody>
</table>


[active scanner]: HelpStartConceptsAscan
[scan policies]: HelpStartConceptsScanpolicy
[Contexts]: HelpStartConceptsContexts
[Users]: HelpStartConceptsUsers
[Options Active Scan Input Vectors screen]: HelpUiDialogsOptionsAscaninput