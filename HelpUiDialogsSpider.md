# Cuadro de diálogo Rastreador #

Este cuadro de diálogo abre el [rastreador][].


## Ámbito ##

La primera pestaña permite seleccionar o cambiar el punto de partida.
Si el punto de partida está es uno o mas [Contextos][] será capaz de seleccionar uno de ellos.
Si el contexto tiene cualquier [Usuario][] definido será capaz de seleccionar uno de ellos.
Si se selecciona uno de los usuarios, el rastreador se realizará como ese usuario, con ZAP reautenticando como ese usuario siempre que sea necesario.

Si se selecciona "recurse" todos los nodos debajo del seleccionado serán también utilizados para esparcir el rastreador.

Si se selecciona "Solo subárbol del Rastreador" el rastreador solo accederá a los recursos que estén bajo el punto de partida (URI). Cuando se evalúa si un recurso se encuentra dentro del subárbol, el rastreador considera solo los componentes esquema, host, port y ruta del URI.

Si se selecciona "Mostrar opciones avanzadas" la siguiente pestaña se mostrará, la cual proporciona un control detallado sobre el proceso del rastreador.

Al hacer clic en el botón "Reiniciar" se reiniciarán todas las opciones a su valor por defecto.

## Avanzado ##

Los parámetros en esta pestaña corresponden a los mismos parámetros en la [pantalla Opciones del Rastreador][].

## Acceso vía ##

<table> 
 <tbody>
  <tr>
   <td>&nbsp;&nbsp;&nbsp;&nbsp;</td>
   <td><a href="HelpUiTabsSpider" rel="nofollow">Spider tab</a></td>
   <td>'New Scan' button</td>
  </tr> 
  <tr>
   <td>&nbsp;&nbsp;&nbsp;&nbsp;</td>
   <td><a href="HelpUiTabsSites" rel="nofollow">Sitios tab</a></td>
   <td>'Attack / Spider...' right click menu item</td>
  </tr> 
  <tr>
   <td>&nbsp;&nbsp;&nbsp;&nbsp;</td>
   <td><a href="HelpUiTabsHistory" rel="nofollow">Pesta&ntilde;a Historia</a></td>
   <td>'Attack / Spider...' right click menu item</td>
  </tr> 
 </tbody>
</table>

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
   <td> <a href="HelpUiDialogsDialogs" rel="nofollow">Cuadros de di&aacute;logo</a></td>
   <td>para detalles de los cuadros de di&aacute;logos o popups </td>
  </tr> 
 </tbody>
</table>


[rastreador]: HelpStartConceptsSpider
[Contextos]: HelpStartConceptsContexts
[Usuario]: HelpStartConceptsUsers
[pantalla Opciones del Rastreador]: HelpUiDialogsOptionsSpider