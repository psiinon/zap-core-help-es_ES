# Escaneo Pasivo #

ZAP pasivamente por defecto escanea los mensajes HTTP (solicitudes y respuestas) enviados a la aplicación web están probada.
Exploración pasiva no cambie las solicitudes ni las respuestas de ninguna manera y por lo tanto es segura de usar.
La exploración se realiza en un subproceso en segundo plano para asegurar que no demorar la exploración de una aplicación.

El comportamiento (principal) del escáner pasivo puede configurarse utilizando la [Pantalla de escáner pasivo opciones][Pantalla de esc_ner pasivo opciones].

Exploración pasiva también puede utilizarse para automáticamente agregar [etiquetas][] y levantar [alertas][] de problemas potenciales.
Un conjunto de reglas para el etiquetado automático se proporcionan por defecto. Estos pueden ser cambiados, eliminados o añadidos a través de la [pantalla de opciones de etiquetas de exploración pasiva][pantalla de opciones de etiquetas de exploraci_n pasiva].

Las alertas por escáneres pasivos pueden configurarse utilizando la [pantalla de opciones pasivo analizar las reglas de][].


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
  <tr>
   <td>&nbsp;&nbsp;&nbsp;&nbsp;</td>
   <td> <a href="HelpStartConceptsAscan" rel="nofollow">Escaneo activo</a></td>
   <td></td>
  </tr> 
  <tr>
   <td>&nbsp;&nbsp;&nbsp;&nbsp;</td>
   <td> <a href="HelpStartChecks" rel="nofollow">Reglas de escaneo</a></td>
   <td>soportadas por omisi&oacute;n</td>
  </tr> 
 </tbody>
</table>


[Pantalla de esc_ner pasivo opciones]: HelpUiDialogsOptionsPscanner
[etiquetas]: HelpStartConceptsTags
[alertas]: HelpStartConceptsAlerts
[pantalla de opciones de etiquetas de exploraci_n pasiva]: HelpUiDialogsOptionsPscan
[pantalla de opciones pasivo analizar las reglas de]: HelpUiDialogsOptionsPscanrules