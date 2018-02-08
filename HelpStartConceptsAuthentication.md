# Autenticación #

ZAP maneja varios tipos de autenticación (llamados **Métodos de autenticación**) que puede ser utilizado para sitios web / webapps. Cada **[contexto][]** posee un Método de Autenticación definido el cual dicta cómo se maneja la autenticación. La autenticación se utiliza para crear sesiones Web que corresponden a la aplicación web autenticado [usuarios][].

Con el fin de detectar mensajes de respuesta de servidores web corresponden a autenticar las solicitudes, se puede configurar un conjunto de indicadores. **Conectado en el indicador**, cuando se presenta en un mensaje de respuesta (el encabezado o el cuerpo), significa que el mensaje de respuesta corresponde a una solicitud autenticada (por ejemplo, la presencia de un enlace de' cerrar sesión' o de 'Bienvenido de nuevo, usuario X'). Del mismo modo, **conectado a indicador** indica una solicitud sin autenticar (p. ej. presencia de un 'enlace de inicio de sesión'). Si ZAP detecta la sesión un indicador de que se vuelva a autenticar, de lo contrario se supone que ya está autenticado y continuará como de costumbre. Sólo uno (1) de los indicadores de dos 2 es necesario para un funcionamiento correcto. En el caso que ninguno de los indicadores se ha especificado, se consideran todos los mensajes, por defecto, autenticado.

Para establecer una **sesión iniciada indicadores de entrada/salida**, ya sea tipo regex directamente en el *cuadro de diálogo de [Propiedades de sesión][Propiedades de sesi_n]\-> panel de autenticación-> conectado in/out indicador del campo*, ya sea encontrar un mensaje autenticado en el árbol de sitios, seleccionarlo, abierta la Ver respuesta y seleccione el texto que desea definir como el indicador de uso del ratón y seleccionar la *bandera como contexto... Sesión de entrada/salida indicador de* opción de menú de botón derecho.

Para realizar la autenticación de un usuario de un sitio web o en una aplicación Web, el método de autenticación define cómo realiza la autentificación (el proceso), mientras que las credenciales necesarias (los identificadores exactas) dependen del usuario, así, en ZAP, que son el config medido en los usuarios.

El modelo genérico **pasos principales** se necesitan para configurar la autenticación para una aplicación web son los siguientes:

1.  configurar correctamente un ZAP [contexto][] de la aplicación web
2.  configurar el [método de administración de sesión][m_todo de administraci_n de sesi_n] para el contexto al que se utiliza en su aplicación
3.  configurar el método de autenticación para el contexto:
    
    1.  configurar al menos uno de la *Sesión en indicador* o la *sesión iniciada por indicador*, como se describió anteriormente
    2.  configurar el método de autenticación de la aplicación, especificar todos los requisitos (como se ve abajo)
4.  configurar un conjunto de [usuarios][] para el contexto que se corresponden directamente con el método de autenticación para el contexto

Métodos de autenticación pueden utilizarse en varios lugares alrededor de ZAP. Algunos ejemplos incluyen:

 *  definición de usuarios y login automático
 *  detección de Estados autenticado/no autenticado
 *  realizar autenticación automática

Se han implementado varios métodos de autenticación y fácil adición de nuevos métodos, es compatible con el sistema según las necesidades del usuario. Lo principal que se describen a continuación.

### Autenticación manual ###

Este método permite que los usuarios realicen la autenticación manualmente (por ejemplo, autenticación en el navegador mientras proxy-ing a través de ZAP) y seleccione la correspondiente sesión HTTP. Como la autenticación actual se está realizando por usted, este método no permite autenticación en caso de que la aplicación cierra la sesión un usuario.

Cuando se utiliza este método de autenticación, configurar un usuario para el contexto requieren elegir una sesión HTTP autenticada.

### Autenticación basada en formularios ###

Este método se utiliza para sitios web / webapps donde se realiza la autenticación por enviar un formulario o realizar una obtener la petición a un 'url de inicio de sesión' con un par de 'contraseña' de credenciales de autenticación. Autenticación es posible. Configuración se puede hacer usando el [Diálogo de contextos de sesión][Propiedades de sesi_n] o utilizando PopupMenu contextual: *bandera como... Solicitud de autenticación por formulario de inicio de sesión*.

Cuando utilizando este método de autenticación, configurar un usuario para el contexto requiere establecer el par de *contraseña* de las credenciales que se utilizan para el formulario de autenticación basada en.

### Autenticación HTTP/NTLM ###

Este método se utiliza para sitios web webapps donde se aplique la autenticación utilizando los mecanismos HTTP o la autenticación NTLM con encabezados de los mensajes HTTP. Se admiten tres esquemas de autenticación: Basic, Digest y NTLM. Autenticación es posible, como los encabezados de autenticación se enviaron con cada solicitud autenticada. Configuración se puede hacer usando el [Diálogo de contextos de sesión][Propiedades de sesi_n].

Cuando se utiliza este método de autenticación, configurar un usuario para el contexto requiere configurar el par *usuario/contraseña* de credenciales que se utilizan para la autenticación de HTTP/NTLM.

### Autenticación basada en script ###

Este método es útil para sitios web / webapps donde la autenticación es un más complejo uno y algunos scripts personalizados que manejan el proceso de autenticación son beneficiosos. Para utilizar este método, primero es necesario definir una secuencia de comandos de autenticación que envía mensajes o realiza otras acciones como necesarias para la aplicación web. Este script es seleccionado para el uso de un determinado contexto y se llama cuando se realiza una autenticación. Autenticación es posible. Configuración se puede hacer usando la [Sesión contextos de diálogo][Propiedades de sesi_n] y requiere tener el Addon Scripts consola ZAP instalado desde el Marketplace.

Al usar este método de autenticación, configurar un Usuario para el contexto requiere configurar un conjunto de parámetros definidos en el script. Para más detalles, ve los ejemplos que aparecen en el Script de Autenticación.

## Ejemplo de configuración ##

Un ejemplo de configuración que muestra cómo configurar completamente una aplicación web que utiliza *autenticación basada en formularios* y en la *Administración de sesiones basadas en cookies* se ve a continuación:

1.  establecer un contexto para la aplicación web
2.  configurar el método de administración de sesión gestión de *sesión basada en cookies*
3.  Asegúrese de que sus proxies de navegador todo por ZAP e inicie sesión en su aplicación utilizando el navegador
4.  ir a ZAP e identificar la solicitud que se hizo para el inicio de sesión (de más generalmente es un HTTP POST solicitar que contiene el nombre de usuario y la contraseña y posiblemente otros elementos)
5.  click derecho sobre la solicitud y la bandera como contexto... Petición de Login de autenticación basada en formularios
6.  se abrirá una ventana que ya contiene la URL de solicitud y los parámetros (si los hay). Utilice las opciones del menú desplegable para seleccionar cuál de los parámetros corresponden con el nombre de usuario y la contraseña
7.  entonces usted necesita decirle a ZAP cómo identificar si una autenticación tuvo éxito o no. Para ello fijando logueado o registrado hacia fuera de los indicadores. Estos son patrones de expresión regular que, si se encuentra en una respuesta, Dile ZAP si está autenticado o no (por ejemplo, la presencia de un enlace de http://example.com/logout o la presencia de un 'Bienvenido, usuario X'). Sólo uno de ellos es necesario. Para definir uno de ellos, ya sea tipo la regex directamente en las propiedades de sesión-> autenticación-> registrado en indicador, ya sea encontrar un mensaje autenticado en el árbol de sitios, seleccione, abra la vista de la respuesta y seleccione el texto que desea definir como indicador utilizando el ratón y seleccionar la bandera como contexto... Iniciar sesión en la opción de menú de clic derecho de indicador.
8.  definir tantos usuarios como necesite en las propiedades de sesión-> sección usuarios.
9.  después de este paso, varias acciones están disponibles en ZAP. Por ejemplo, ahora puede seleccionar el usuario en el [diálogo de spider][di_logo de spider]. O, usando el modo de usuario obligado, puede forzar todas las interacciones que atraviesan ZAP para un contexto dado que desde la perspectiva de un usuario. El modo de forzado de usuario se activa mediante la tecla anterior a la última en la barra de herramientas (el uno con el usuario y el bloqueo) y se configura a través de propiedades de la sesión-> obligado modo de usuario.

La mayoría de los pasos anteriores se aplica también para otros métodos de autenticación. Lo único que cambia cuando se trata de configurar la autenticación utilizando un método diferente es los pasos 3, 4, 5 y 6. En vez de éstos, seleccione el método de autenticación de la lista desplegable y configurar según sea necesario. Más detalles sobre la configuración de cada tipo de autenticación pueden estar por encima y [aquí][aqu].

## Configura a través ##

<table> 
 <tbody>
  <tr> 
   <td>&nbsp;&nbsp;&nbsp;&nbsp;</td> 
   <td><a href="HelpUiDialogsSessionContexts#auth" rel="nofollow">Di&aacute;logo de propiedades de sesi&oacute;n</a></td> 
   <td></td> 
  </tr> 
 </tbody>
</table>

## Vease también ##

<table> 
 <tbody>
  <tr> 
   <td>&nbsp;&nbsp;&nbsp;&nbsp;</td> 
   <td><a href="https://youtu.be/cR4gw-cPZOA" rel="nofollow">YouTube tutorial</a></td> 
   <td>de las caracter&iacute;sticas de autenticaci&oacute;n, manejo de sesiones y de gesti&oacute;n de usuarios de ZAP [enlace externo a https://youtu.be/cR4gw-cPZOA].</td> 
  </tr> 
  <tr> 
   <td>&nbsp;&nbsp;&nbsp;&nbsp;</td> 
   <td><a href="HelpUiOverview" rel="nofollow">Resumen de la interfaz de usuario</a></td> 
   <td>para tener una visi&oacute;n general de la interfaz de usuario</td> 
  </tr> 
  <tr> 
   <td>&nbsp;&nbsp;&nbsp;&nbsp;</td> 
   <td><a href="HelpStartConceptsConcepts" rel="nofollow">Caracteristicas</a></td> 
   <td>proporcionado por ZAP</td> 
  </tr> 
  <tr> 
   <td>&nbsp;&nbsp;&nbsp;&nbsp;</td> 
   <td><a href="HelpUiDialogsSessionContexts" rel="nofollow">Di&aacute;logo de contextos de sesi&oacute;n</a></td> 
   <td>para una descripci&oacute;n general de las Propiedades de sesi&oacute;n</td> 
  </tr> 
  <tr> 
   <td>&nbsp;&nbsp;&nbsp;&nbsp;</td> 
   <td><a href="HelpStartConceptsUsers" rel="nofollow">Usuarios</a></td> 
   <td>para una descripci&oacute;n general de los usuarios</td> 
  </tr> 
 </tbody>
</table>


[contexto]: HelpStartConceptsContexts
[usuarios]: HelpStartConceptsUsers
[Propiedades de sesi_n]: HelpUiDialogsSessionContexts#auth
[m_todo de administraci_n de sesi_n]: HelpStartConceptsSessionManagement
[di_logo de spider]: HelpUiDialogsSpider
[aqu]: HelpUiDialogsSessionContexts