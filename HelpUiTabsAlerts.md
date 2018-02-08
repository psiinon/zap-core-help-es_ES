# Alerts tab #

La pestaña de Alertas muestra las [Alertas][] que se han generado en esta sesión. Las alertas se muestran en un árbol según el orden de riesgos en el panel izquierdo, y cada nodo del árbol muestra el número total de alertas debajo de él.

Seleccionar una alerta con un click la mostrará en el panel derecho. Al hacer doble clic en una alerta aparecerá el cuadro de diálogo [Agregar Alerta][], el cual permite cambiar los detalles de la alerta.

## Filtrando alertas ##

Los botones de filtro, mostrados inmediatamente encima del árbol, te permiten restringir qué alertas se muestran:

### ![target.png][] /  ![target-grey.png][]  Show only URLs in Scope / Show all URLs ###

Permite mostrar solo las alertas de las URLS que se encuentran en el [ámbito][mbito].

### ![094.png][] /  ![earth-grey.png][]  Link / Unlink with Sites selection ###

Permite mostrar solo las alertas del [Sitios tab][] nodo del árbol seleccionado.

**Nota:** Seleccionar un filtro deshabilitará el otro ya que son mutuamente excluyentes.

### ![018.png][]  Editar Alerta ###

Mostrará el cuadro de diálogo [Agregar Alerta][] , el cual permite cambiar los detalles de la alerta, para la alerta seleccionada.

**Nota:** Si se seleccionan múltiples alertas en el árbol, se edita el elemento seleccionado más recientemente.

## Menú de botón derecho ##

Al hacer clic derecho en un nodo abrirá un menú que permite:

### Reenviar... ###

Esto abrirá el [cuadro de diálogo Reenviar][cuadro de di_logo Reenviar] que permite reenviar las solicitudes asociadas con la alerta después de hacerle cualquier cambio deseado.

## Vease también ##

<table> 
 <tbody>
  <tr>
   <td>&nbsp;&nbsp;&nbsp;&nbsp;</td>
   <td> <a href="HelpUiOverview" rel="nofollow">UI Overview</a></td>
   <td>Para una vista general sobre la interfaz de usuario</td>
  </tr> 
 </tbody>
</table>


[Alertas]: HelpStartConceptsAlerts
[Agregar Alerta]: HelpUiDialogsAddalert
[target.png]: https://github.com/zaproxy/zap-core-help/wiki/images/fugue/target.png
[target-grey.png]: https://github.com/zaproxy/zap-core-help/wiki/images/fugue/target-grey.png
[mbito]: HelpStartConceptsScope
[094.png]: https://github.com/zaproxy/zap-core-help/wiki/images/16/094.png
[earth-grey.png]: https://github.com/zaproxy/zap-core-help/wiki/images/16/earth-grey.png
[Sitios tab]: HelpUiTabsSites
[018.png]: https://github.com/zaproxy/zap-core-help/wiki/images/16/018.png
[cuadro de di_logo Reenviar]: HelpUiDialogsResend