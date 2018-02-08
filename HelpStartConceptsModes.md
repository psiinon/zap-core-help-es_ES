# Modos #

ZAP tiene un 'modo' que puede ser:

 *  Caja de seguridad - no operaciones potencialmente peligrosas permitidas
 *  Protegido - sólo puede realizar acciones peligrosas (potencialmente) las URL en el [ámbito][mbito]
 *  Estándar - al igual que en versiones anteriores, se puede hacer nada
 *  ATTACK - nuevos nodos que se encuentran en el [ámbito de aplicación][mbito] son [activamente explorado][] tan pronto como son descubiertos

Se recomienda que utilice el modo protegido para asegurar que sólo atacar sitios que usted quiere.

Puede cambiar el modo de la [barra de herramientas][] (o la API de ZAP) y persiste entre sesiones.

Ejemplos de lo que no será posible en cualquier modo seguro o en modo protegido cuando no actúa en las URLs en el ámbito de aplicación:

 *  Indizado de web
 *  Escaneo activo
 *  Fuzzing
 *  Forzar navegación
 *  Romper (interceptar)
 *  Reenviar solicitudes

Se puede definir la [Política de escaneo][Pol_tica de escaneo] para el modo de ataque la [Pantalla de opciones de escaneo activo][].


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
   <td> <a href="HelpStartConceptsConcepts" rel="nofollow">Caracteristicas</a></td>
   <td>proporcionado por ZAP</td>
  </tr> 
 </tbody>
</table>


[mbito]: HelpStartConceptsScope
[activamente explorado]: HelpStartConceptsAscan
[barra de herramientas]: HelpUiTltoolbar
[Pol_tica de escaneo]: HelpStartConceptsScanpolicy
[Pantalla de opciones de escaneo activo]: HelpUiDialogsOptionsAscan