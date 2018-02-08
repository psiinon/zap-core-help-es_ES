# Pantalla de opciones de vectores de entrada de escaneo activo #

Esta pantalla permite configurar las [escaneo activo][] vectores de entrada.
Estos son los elementos que el escaner activo atacará.
Escanear todos los elementos soportados tomará más tiempo, pero no escanear alguno de los elementos puede ocasionar que se ignoren algunas vulnerabilidades.

### Objetivos incorporables ###

Estos son los elementos que el escaner activo atacará.

#### Secuencia de Consulta URL y Data Driven Nodes ####

Claves pares de valor de la consulta de la URL de petición, es decir después de la `?`.
Si no hay parámetros de consulta se probarán una arbitraria. If [Data Driven Nodes][] se definen dentro de un contexto que se probará.

#### Datos POST ####

Key de valores clave en la solicitud de datos POST.

#### Ruta de URL ####

Elementos de la ruta en la URL de petición, es decir los elementos separados por `/`.

#### Encabezados de HTTP ####

Solicitar encabezados de HTTP.

##### Todas las Solicitudes #####

Permite escanear las Cabeceras HTTP de todas las solicitudes. No solo las solicitudes que envíen parámetros, a través de la consulta o el cuerpo de la solicitud.

#### Datos de Cookie ####

Solicitar cookies.

### Build-in Input Vector Handlers ###

The data formats that the active scanner will target:

<table> 
 <tbody>
  <tr>
   <td>&nbsp;&nbsp;&nbsp;&nbsp;</td>
   <td>Multipart Form Data</td>
   <td></td>
  </tr> 
  <tr>
   <td>&nbsp;&nbsp;&nbsp;&nbsp;</td>
   <td>XML tag/attribute</td>
   <td></td>
  </tr> 
  <tr>
   <td>&nbsp;&nbsp;&nbsp;&nbsp;</td>
   <td>JSON</td>
   <td></td>
  </tr> 
  <tr>
   <td>&nbsp;&nbsp;&nbsp;&nbsp;</td>
   <td>Google Web Toolkit</td>
   <td></td>
  </tr> 
  <tr>
   <td>&nbsp;&nbsp;&nbsp;&nbsp;</td>
   <td>OData id/filter</td>
   <td></td>
  </tr> 
 </tbody>
</table>

### Actirvar Script Input Vectors ###

Si se selecciona esta opción el explorador activo utilizará cualquier vectores de entrada de escritura habilitada.
Vectores de entrada de secuencia de comandos son scripts que han escrito o importados en ZAP y permiten a los elementos objetivos que no son compatibles por defecto.

Esta pantalla también te permite configurar los parámetros que serán ignorados por el escaner activo.

## Vease también ##

<table> 
 <tbody>
  <tr>
   <td>&nbsp;&nbsp;&nbsp;&nbsp;</td>
   <td><a href="HelpUiOverview" rel="nofollow">UI Overview</a></td>
   <td>Para una vista general sobre la interfaz de usuario</td>
  </tr> 
  <tr>
   <td>&nbsp;&nbsp;&nbsp;&nbsp;</td>
   <td><a href="HelpUiDialogsOptionsOptions" rel="nofollow">Di&aacute;logos de opciones</a></td>
   <td>for details of the other Options dialog screens</td>
  </tr> 
  <tr>
   <td>&nbsp;&nbsp;&nbsp;&nbsp;</td>
   <td><a href="HelpUiDialogsOptionsAscaninput" rel="nofollow">Active Scan Input Vectors</a></td>
   <td></td>
  </tr> 
 </tbody>
</table>


[escaneo activo]: HelpStartConceptsAscan
[Data Driven Nodes]: HelpStartConceptsDdc