# Ficha de sesiones HTTP #

Esta ficha muestra el conjunto de sesiones HTTP identificadas para cada sitio, según lo detectado por la [extensión de sesiones HTTP][extensi_n de sesiones HTTP].

El sitio actual de a que la información se refiere puede ser seleccionado mediante la barra de herramientas o la [Sites tab][].

La barra de herramientas proporciona un botón ("New Session") que le permite iniciar una nueva sesión, obligando a todos los mensajes de solicitud saliente para estar sin el conjunto de tokens de sesión, el servidor considera que es una nueva sesión. Esto permite la creación de una nueva sesión, sin destruir la anterior.

Cada una de las entradas en la tabla de sesiones (each session) tiene inicialmente un nombre generado, pero se puede cambiar seleccionando la celda de 'Name' y editarlo.

Cada una de las entradas en la tabla de sesiones puede ser derecha clic, que activa el menú emergente, con las siguientes opciones:

 *  Remove Session - deletes the session
 *  Establecer como activo (disponible sólo en las sesiones inactivas) - marca esta sesión como activo. Si cualquier período de sesiones fue establecida previamente como activos, será desactivada como activa y, si no especifica ningún valor simbólico, se eliminará.
 *  Marca (disponible sólo en la sesión activa) - como activo esta sesión por no ser activo ya. Si la sesión no especifica ningún valor simbólico, se eliminará.

*Con respecto a la sesión activa, se pueden leer más detalles en la página de ayuda de conceptos generales de la [Sesions extension HTTP][extensi_n de sesiones HTTP]*

Para cada sesión se puede ver:

 *  Activa - ya sea la sesión activa o no
 *  Name - El nombre de la sesion
 *  Valores de Tokens de sesión: la lista de valores asociados a cada uno de los tokens de sesión. Las entradas están separadas por el ';' símbolo.
 *  Mensajes Matched: el número de mensajes HTTP que la extensión ha igualado con esta sesión

## Vease también ##

<table> 
 <tbody>
  <tr> 
   <td>&nbsp;&nbsp;&nbsp;&nbsp;</td> 
   <td><a href="HelpUiOverview" rel="nofollow">UI Overview</a></td> 
   <td>Para una vista general del IU</td> 
  </tr> 
  <tr> 
   <td>&nbsp;&nbsp;&nbsp;&nbsp;</td> 
   <td><a href="HelpStartConceptsHttpsessions" rel="nofollow">HTTP Sessions Extension</a></td> 
   <td>para una vista general de la herramienta</td> 
  </tr> 
  <tr> 
   <td>&nbsp;&nbsp;&nbsp;&nbsp;</td> 
   <td><a href="HelpUiDialogsOptionsHttpsessions" rel="nofollow">HTTP Sessions Options screen</a></td> 
   <td>para una vista general de las opciones de la herramienta</td> 
  </tr> 
 </tbody>
</table>


[extensi_n de sesiones HTTP]: HelpStartConceptsHttpsessions
[Sites tab]: HelpUiTabsSites