# Fuzzer tab #

The Fuzzer tab shows you the requests and responses performed when you [fuzz][] a string.
Selecting a row see the full requests and responses. You can also search for strings in the fuzz results using the [Search tab][].


## HTTP Fuzzer results ##

The results have to be manually assessed to know if any vulnerability was found.
Meaning of values of the "State" column:

 *  "Successful" - the message was successfully sent/received;
 *  "Error" - an error occurred while creating or sending/receiving the message (for example: malformed HTTP message, time out while reading the response);
 *  "Reflected" - the injected fuzz string (value of "Fuzz" column) was found in the response body.

## Menú de botón derecho ##

Right clicking on a row will bring up a menu which will allow you to:

### Excluir de ###

Este menú tiene los siguientes submenús:

#### Proxy ####

Esto excluirá los nodos seleccionados desde el proxy. Aunque seguirán siendo procesadas vía ZAP no aparecerán en ninguna de las pestañas.
Esto puede usarse para ignorar las URLs que no son relevantes para el sistema que actualmente está probando.
Los nodos pueden ser incluidos a través del cuadro de dialogo [Propiedades de la Sesión][Propiedades de la Sesi_n] .

#### Escáner ####

Esto evitará que los nodos seleccionados sean escaneados activamente.
Los nodos pueden ser incluidos a través del cuadro de dialogo [Propiedades de la Sesión][Propiedades de la Sesi_n] .

#### Spider(Araña) ####

This will prevent the selected nodes from being spidered.
Los nodos pueden ser incluidos a través del cuadro de dialogo [Propiedades de la Sesión][Propiedades de la Sesi_n] .

### Reenviar... ###

Esto hará que aparezca el cuadro de dialogo [Reenviar][] que le permite enviar la solicitud después de hacer los cambios que desee.

### Nueva alerta... ###

Esto hará que aparezca el cuadro de dialogo [Añadir Alerta,][A_adir Alerta] el que le permitirá agregar una nueva [alerta][] de forma automática en la petición.

### Ver en el navegador ###

La dirección URL del nodo seleccionado se abrirá en el navegador por defecto.

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
   <td> <a href="HelpUiDialogsOptionsFuzz" rel="nofollow">Options Fuzz screen</a></td>
   <td>for details of the fuzz configuration</td>
  </tr> 
 </tbody>
</table>


[fuzz]: HelpStartConceptsFuzz
[Search tab]: HelpUiTabsSearch
[Propiedades de la Sesi_n]: HelpUiDialogsSessionSessprop
[Reenviar]: HelpUiDialogsResend
[A_adir Alerta]: HelpUiDialogsAddalert
[alerta]: HelpStartConceptsAlerts