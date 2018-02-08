# Primeros pasos #

La manera mas rápida de comenzar a utilizar ZAP es ejecutando el suplemento de inicio rápido, el cual está instalado por omisión. Éste permite ingresar una URL a la cual ZAP primero la recorre usando un [spider][] y luego realizará un [escaneo activo][]. Para pruebas con más profundidad, debe explorar la aplicación utilizando su navegador o a través de pruebas de regresión automatizadas utilizando a ZAP como proxy.

En su corazón ZAP es un [man-in-the-middle proxy][].
Para obtener el máximo provecho de ZAP es necesario configurar su navegador o pruebas funcionales para conectarse a la aplicación web queremos comprobar a través de ZAP.
Si es necesario que también puede configurar ZAP conectarse a través de otro proxy - esto a menudo es necesario en un entorno corporativo.


Puede fácilmente lanzar navegadores configuradas previamente a proxy a través de ZAP a través de la pestaña de inicio rápido. Esto puede iniciar cualquiera de los navegadores más comunes que han instalado con nuevos perfiles.
Si desea utilizar cualquiera de sus navegadores con un perfil existente, por ejemplo con otros complementos de navegador instalados, entonces usted tendrá que configurar manualmente el navegador de proxy vía ZAP.
Si sabes como configurar proxy en su navegador web y luego seguir adelante y pruébalo!
Si no está seguro entonces echa un vistazo a la sección de [configuración de proxies][configuraci_n de proxies].

Una vez que haya configurado ZAP como el proxy de su navegador intente conectarse a la aplicación web que estará probando.
Si tiene problemas de conexión, verifique nuevamente la configuración del servidor proxy. Necesitará verificar la configuración del servidor proxy en su navegador así como la configuración del proxy en ZAP.
¡También es recomendable verificar que la aplicación que intenta probar esté corriendo!

Cuando se haya conectado correctamente a la aplicación a través de su navegador, visualice ZAP nuevamente. Debería ver una o más líneas en las pestañas [Sitios][] e [Historia][].
Si es así, está listo para continuar. Si no, deberá verificar nuevamente la configuración del proxy.

El siguiente paso a realizar es comenzar con un [test de penetración básico][test de penetraci_n b_sico].


## Vease también ##

<table> 
 <tbody>
  <tr>
   <td>&nbsp;&nbsp;&nbsp;&nbsp;</td>
   <td> <a href="HelpStartProxies" rel="nofollow">Configurando proxies</a></td>
   <td>para detalles de c&oacute;mo configurar ZAP como proxy en su navegador</td>
  </tr> 
  <tr>
   <td>&nbsp;&nbsp;&nbsp;&nbsp;</td>
   <td> <a href="HelpIntro" rel="nofollow">Introducci&oacute;n</a></td>
   <td>para una introducci&oacute;n a ZAP</td>
  </tr> 
  <tr>
   <td>&nbsp;&nbsp;&nbsp;&nbsp;</td>
   <td> <a href="HelpStartConceptsConcepts" rel="nofollow">Caracteristicas</a></td>
   <td>que son proporcionadas por ZAP</td>
  </tr> 
  <tr>
   <td>&nbsp;&nbsp;&nbsp;&nbsp;</td>
   <td> <a href="HelpStartChecks" rel="nofollow">Reglas de escaneo</a></td>
   <td>que son soportadas por omisi&oacute;n</td>
  </tr> 
 </tbody>
</table>


[spider]: HelpStartConceptsSpider
[escaneo activo]: HelpStartConceptsAscan
[man-in-the-middle proxy]: HelpStartConceptsIntercept
[configuraci_n de proxies]: HelpStartProxies
[Sitios]: HelpUiTabsSites
[Historia]: HelpUiTabsHistory
[test de penetraci_n b_sico]: HelpPentestPentest