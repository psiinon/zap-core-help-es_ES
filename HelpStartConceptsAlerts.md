# Alertas #

Una alerta es una vulnerabilidad potencial y se asocia con una petición específica.
Una solicitud puede tener más de una alerta.


Alertas se muestran en la interfaz de usuario con una bandera que indica el riesgo:

<table> 
 <tbody>
  <tr>
   <td>&nbsp;&nbsp;&nbsp;&nbsp;</td>
   <td><img src="https://github.com/zaproxy/zap-core-help/wiki/images/16/071.png" align="bottom" width="16" height="16" />&nbsp; Alto</td>
   <td></td>
  </tr> 
  <tr>
   <td>&nbsp;&nbsp;&nbsp;&nbsp;</td>
   <td><img src="https://github.com/zaproxy/zap-core-help/wiki/images/16/076.png" align="bottom" width="16" height="16" />&nbsp; Medio</td>
   <td></td>
  </tr> 
  <tr>
   <td>&nbsp;&nbsp;&nbsp;&nbsp;</td>
   <td><img src="https://github.com/zaproxy/zap-core-help/wiki/images/16/074.png" align="bottom" width="16" height="16" />&nbsp; Bajo</td>
   <td></td>
  </tr> 
  <tr>
   <td>&nbsp;&nbsp;&nbsp;&nbsp;</td>
   <td><img src="https://github.com/zaproxy/zap-core-help/wiki/images/16/073.png" align="bottom" width="16" height="16" />&nbsp; Informativo</td>
   <td></td>
  </tr> 
  <tr>
   <td>&nbsp;&nbsp;&nbsp;&nbsp;</td>
   <td><img src="https://github.com/zaproxy/zap-core-help/wiki/images/16/072.png" align="bottom" width="16" height="16" />&nbsp; Falso positivo</td>
   <td></td>
  </tr> 
 </tbody>
</table>

Alertas pueden ser levantados por varios componentes ZAP, incluyendo pero no limitado a: [exploración activa][exploraci_n activa], [escaneo pasivo][], scripts, addons (extensiones), o manualmente usando el [cuadro de diálogo Agregar alerta][cuadro de di_logo Agregar alerta] (que también le permite actualizar o cambiar los datos de alerta / información).

Alertas están marcados en la [ficha historial][] con una bandera que indica que la alerta máxima de riesgo.
Todas las alertas aparecen en la [pestaña de alertas][pesta_a de alertas] y en el [pie de página][pie de p_gina] se muestra un recuento del número total de alertas por riesgo.

## Alerta de sobreescritura ##

Alertas por ZAP incluyen información genérica y específica sobre las alertas levantado. La información específica se relaciona directamente con el posible problema encontrado, tal como el URL y el parámetro afectado. La información genérica incluye cosas como una descripción y vínculos a recursos en línea relacionados.

Puede reemplazar o agregar información genérica utilizando un archivo de configuración de "anulación de alerta". Esto le permite incluir información específica a las políticas de la empresa tales como el mandato, enlaces internos o Consejo para tecnologías específicas que utilizas.

Un archivo de configuración de alerta de la anulación es un archivo de propiedades de UTF-8 que contiene sólo la información que le gustaría cambiar. Líneas que comienzan con '\#' son tratadas como comentarios y no hizo caso.

El formato es:

``````````
<alertid>.<property> = [ + | - ] <your information>
``````````

Están compatible con las siguientes propiedades:

 *  nombre
 *  Descripción
 *  Solución
 *  otherInfo
 *  Referencia

Por ejemplo

``````````
# 40012 = XSS reflejado
40012.solution = Sigue las directrices específicas de nuestra compañía en http://internet.example.com/xss.html
``````````

Si el valor comienza con un '+' entonces se agrega a la información existente.
Si el valor comienza con un '+' entonces se agrega a la información existente.
Si no se inicia con un '+' o '-' entonces reemplaza la información existente.

El archivo de configuración de alerta de anulación puede ser especificado a través de la [API][], [Pantalla de alerta de opciones][] o el uso de la [línea de comando][l_nea de comando] opciones:

``````````
-config alert.overridesFilename=<filename>
``````````

## Véase también ##

<table> 
 <tbody>
  <tr>
   <td>&nbsp;&nbsp;&nbsp;&nbsp;</td>
   <td> <a href="HelpUiOverview" rel="nofollow">Resumen de IU</a></td>
   <td>para tener una visi&oacute;n general de la interfaz de usuario</td>
  </tr> 
  <tr>
   <td>&nbsp;&nbsp;&nbsp;&nbsp;</td>
   <td> <a href="HelpStartConceptsConcepts" rel="nofollow">Caracteristicas</a></td>
   <td>proporcionado por ZAP</td>
  </tr> 
 </tbody>
</table>


[exploraci_n activa]: HelpStartConceptsAscan
[escaneo pasivo]: HelpStartConceptsPscan
[cuadro de di_logo Agregar alerta]: HelpUiDialogsAddalert
[ficha historial]: HelpUiTabsHistory
[pesta_a de alertas]: HelpUiTabsAlerts
[pie de p_gina]: HelpUiFooter
[API]: HelpStartConceptsApi
[Pantalla de alerta de opciones]: HelpUiDialogsOptionsAlert
[l_nea de comando]: HelpCmdline