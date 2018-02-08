# Parámetros estructurales #

Los parámetros estructurales son un tipo de [Structural Modifier][] que identifican los parámetros que representan la estructura de la aplicación en lugar de los datos del usuario.


En las aplicaciones web 'traditional', la estructura de la aplicación se define típicamente por las rutas URL y los datos están contenidos en los parámetros URL y datos POST.
URLs like:

 *  https://www.example.com/app/aaa?ddd=eee
 *  https://www.example.com/app/aaa?ddd=fff
 *  https://www.example.com/app/aaa?ddd=ggg

estan representados en el [Sites tab][] es un 'node' es los tree:

 *  Sitios
    
     *  https://www.example.com
        
         *  app
            
             *  GET:aaa(ddd)

El árbol de Sitios es muy importante ya que refleja la comprensión de ZAP de la estructura de la aplicación.
Si no es una buena representación de la estructura, entonces ZAP no podrá atacar la aplicación de manera efectiva.

En las aplicaciones de página 'single', un parámetro se usa para indicar la 'page' lógica:

 *  https://www.example.com/app/aaa?page=p1&ddd=eee
 *  https://www.example.com/app/aaa?page=p2&ddd=fff
 *  https://www.example.com/app/aaa?page=p3&ddd=ggg

these 3 URLs represent different logical pages, but by default ZAP will still represent them as one node:

 *  Sites
    
     *  https://www.example.com
        
         *  app
            
             *  GET:aaa(ddd,page)

Esto es un problema porque ZAP ahora no atacará todas las funcionalidades de la aplicación.

En términos de ZAP, el parámetro URL de 'page' es un 'structural parameter', un parámetro que define parte de la estructura de la aplicación.
Puede definir contenido dirigido por datos agregando la aplicación a un [Context][] y luego configurarlos a través de la [Session Context Structure screen][].
Una vez que haya hecho esto, las páginas se representarán correctamente como 3 nodos:

 *  Sites
    
     *  https://www.example.com
        
         *  app
            
             *  aaa
                
                 *  GET:p1(ddd,page)
                 *  GET:p2(ddd,page)
                 *  GET:p3(ddd,page)

## Accedido mediante ##

<table> 
 <tbody>
  <tr>
   <td>&nbsp;&nbsp;&nbsp;&nbsp;</td>
   <td><a href="HelpUiDialogsSessionContext-struct" rel="nofollow">Session Context Structure screen</a></td>
  </tr> 
 </tbody>
</table>

## Véase también ##

<table> 
 <tbody>
  <tr>
   <td>&nbsp;&nbsp;&nbsp;&nbsp;</td>
   <td><a href="HelpUiOverview" rel="nofollow">UI Overview</a></td>
   <td>para tener una visi&oacute;n general de la interfaz de usuario</td>
  </tr> 
  <tr>
   <td>&nbsp;&nbsp;&nbsp;&nbsp;</td>
   <td><a href="HelpStartConceptsConcepts" rel="nofollow">Caracteristicas</a></td>
   <td>proporcionado por ZAP</td>
  </tr> 
  <tr>
   <td>&nbsp;&nbsp;&nbsp;&nbsp;</td>
   <td><a href="HelpStartConceptsStructmods" rel="nofollow">Modificadores estructurales</a></td>
   <td>controles que cambian c&oacute;mo ZAP representa la estructura de la aplicaci&oacute;n</td>
  </tr> 
  <tr>
   <td>&nbsp;&nbsp;&nbsp;&nbsp;</td>
   <td><a href="HelpStartConceptsDdc" rel="nofollow">Contenido manejado por datos</a></td>
   <td>que identifican rutas de URL que representan datos</td>
  </tr> 
 </tbody>
</table>


[Structural Modifier]: HelpStartConceptsStructmods
[Sites tab]: HelpUiTabsSites
[Context]: HelpStartConceptsContexts
[Session Context Structure screen]: HelpUiDialogsSessionContext-struct