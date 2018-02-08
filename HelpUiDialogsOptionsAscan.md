# Pantalla de opciones de escaneo activo #

Esta pantalla permite configurar las [escaneo activo][] opciones:

### Número de hosts escaneados simultáneamente ###

El número máximo de hosts que se analizará al mismo tiempo. Este aumento puede poner tensión extra en el equipo de en que Zap se ejecuta.

### Hilos de análisis concurrentes por host ###

El número de subprocesos que utiliza el escáner por host.
Aumentando el número de subprocesos que acelerará el análisis pero pueden poner tensión extra en el equipo de ZAP se ejecuta en y el host de destino.

### Resultados de Max a la lista de ###

El número de resultados que se mostrarán en la ficha de exploración activa.
Mostrando un gran número de resultados puede aumentar significativamente el tiempo que toma una exploración.

### Duración de la regla máxima (min, 0 es ilimitado) ###

El tiempo máximo de cualquier regla individual puede funcionar por minutos. Cero no significa límite. Esto puede usarse para evitar que las reglas que están tomando una cantidad excesiva de tiempo.

### Duración máximo de análisis (min, 0 es ilimitado) ###

El tiempo máximo que el análisis entero puede funcionar por minutos. Cero no significa límite. Esto puede usarse para asegurar que se realice una exploración alrededor de una hora.

### Demora al escanear en milisegundos ###

El retardo en milisegundos entre cada solicitud.
El parámetro a un valor cero será aumentar el tiempo de una exploración activa toma, pero pondrá menos de una tensión en el host de destino.

### Inyectar el plugin ID en cabecera para todas las solicitudes de exploración activa ###

Si se selecciona esta opción el lector activo inyectará el encabezado de solicitud `X-ZAP-Scan-ID` con el identificador del explorador que está enviando el HTTP solicita.

### Handle anti CSRF tokens ###

Si se selecciona esta opción entonces el explorador activo intentará solicitar automáticamente [anti CSRF][] fichas cuando sea necesario.
Tenga en cuenta que esto es una funcionalidad experimental y ralentizará el proceso de digitalización como sólo un subproceso se utilizará para asegurar que anti CSRF token pide no salir de paso.

### En el indicador de modo de ataque a analizar nodos cuando alcance ###

Si se selecciona esta opción entonces al seleccionar ataque [modo][] se le pedirá elegir entre volver a analizar los nodos de ámbito.
Si la opción no está seleccionada la opción siguiente se controla si los nodos se volverán a explorar.

### En el modo de Ataque siempre se examinan de nuevo los nodos cuando cambia el alcnace ###

Si esta opción está seleccionada entonces al ejecutarse en Ataque [modo][] todos los nodos en el ámbito serán examinados nuevamente si el ámbito cambia.
Esto no se recomienda para sitios grandes ya que podría tomar mucho tiempo.

### Política predeterminada de escaneo activo ###

El [Política de escaneo][Pol_tica de escaneo] se utiliza de forma predeterminada al iniciar una exploración activa.

### Política de exploración de modo de Attack ###

La [Política de Escaneo][Pol_tica de escaneo] that is used for scanning in Attack [mode][modo].

### Diagrama de progreso máximo en minutos ###

El tiempo máximo en minutos para el cual los códigos de respuesta serán diagramados en el [Scan Progress dialog][].
Para deshabilitar el gráfico la opción debe establecerse en cero minutos.

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
   <td><a href="HelpUiDialogsOptionsOptions" rel="nofollow">Cuadros de di&aacute;logo de opciones</a></td>
   <td>for details of the other Options dialog screens</td>
  </tr> 
  <tr>
   <td>&nbsp;&nbsp;&nbsp;&nbsp;</td>
   <td><a href="HelpUiDialogsOptionsAscan" rel="nofollow">Active Scan options</a></td>
   <td></td>
  </tr> 
 </tbody>
</table>


[escaneo activo]: HelpStartConceptsAscan
[anti CSRF]: HelpStartConceptsAnticsrf
[modo]: HelpStartConceptsModes
[Pol_tica de escaneo]: HelpStartConceptsScanpolicy
[Scan Progress dialog]: HelpUiDialogsScanprogress