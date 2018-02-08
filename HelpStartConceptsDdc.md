# Contenido manejado por datos #

El contenido dirigido por datos es tipo de [ Modificador estructural que identifica rutas de URL que representan datos.
][Modificador estructural que identifica rutas de URL que representan datos.]

[ En las aplicaciones web 'tradicionales', la estructura de la aplicación se define típicamente por las rutas URL y los datos están contenidos en los parámetros URL y datos POST.
URLs como: ][Modificador estructural que identifica rutas de URL que representan datos.]

 *  https://www.example.com/app/aaa?ddd=eee
    
    https://www.example.com/app/aaa?ddd=fff
    
    https://www.example.com/app/bbb?ddd=eee

[ están representados en el ][Modificador estructural que identifica rutas de URL que representan datos.][Sites tab][] como dos 'nodos' en el árbol:

 *  Sitios
    
     *  https://www.example.com
        
         *  app
            
             *  GET:aaa(ddd)
             *  GET:bbb(ddd)

El árbol de Sitios es muy importante ya que refleja la comprensión de ZAP de la estructura de la aplicación.
Si no es una buena representación de la estructura, entonces ZAP no podrá atacar la aplicación de manera efectiva.

Algunas aplicaciones incluyen datos en rutas URL.
Por ejemplo:

 *  https://www.example.com/app/company1/aaa?ddd=eee
 *  https://www.example.com/app/company2/aaa?ddd=fff
 *  https://www.example.com/app/company3/aaa?ddd=ggg

Estas 3 URL representan la misma página pero con datos diferentes, pero por defecto ZAP las representará como tres nodos separados:

 *  Sitios
    
     *  https://www.example.com
        
         *  app
            
             *  company1
                
                 *  GET:aaa(ddd)
             *  company2
                
                 *  GET:aaa(ddd)
             *  company3
                
                 *  GET:aaa(ddd)

Esto es un problema porque ZAP ahora atacará las 3 páginas cuando solo necesite atacar a una de ellas.
En este caso atacar la misma página 3 veces no es un gran problema, pero si tiene cientos o miles de páginas como esta aumentarán significativamente el tiempo que lleva escanear la aplicación.

En términos de ZAP, los nodos de "empresa" son "contenido dirigido por datos": elementos de ruta de URL que contienen datos en lugar de representar parte de la estructura de la aplicación.
Puede definir contenido dirigido por datos agregando la aplicación a un [Contexto][] y luego configurarlos a través de la [Pestaña del sitio][Sites tab] 'Marcar como Contexto -> *Nombre del Contexto* Nodo manejado por datos' click derecho en ítem de menú
Una vez que haya hecho esto, las páginas se representarán correctamente como 1 nodo:

 *  Sitios
    
     *  https://www.example.com
        
         *  app
            
             *  «company»
                
                 *  GET:aaa(ddd)

Los personajes & \# x00AB; y & \# x00BB; se utilizan para indicar que este es un nodo "especial" y usted puede establecer el nombre del nodo (en este caso, "empresa") para indicar qué representa ese nodo.

## Accedido mediante ##

<table> 
 <tbody>
  <tr>
   <td>&nbsp;&nbsp;&nbsp;&nbsp;</td>
   <td><a href="HelpUiTabsSites" rel="nofollow">Pesta&ntilde;a Sitios</a></td>
   <td>'Marcar como Contexto -&gt;<i>Nombre del Contexto</i> Nodo manejado por datos' click derecho en &iacute;tem de men&uacute;</td>
  </tr> 
  <tr>
   <td>&nbsp;&nbsp;&nbsp;&nbsp;</td>
   <td><a href="HelpUiTabsHistory" rel="nofollow">Pesta&ntilde;a Historia</a></td>
   <td>'Flag as Context -&gt; <i>Context Name</i> Data driven node' right click menu item</td>
  </tr> 
 </tbody>
</table>

## Véase también ##

<table> 
 <tbody>
  <tr>
   <td>&nbsp;&nbsp;&nbsp;&nbsp;</td>
   <td><a href="HelpUiOverview" rel="nofollow">Resumen de IU</a></td>
   <td>para tener una visi&oacute;n general de la interfaz de usuario</td>
  </tr> 
  <tr>
   <td>&nbsp;&nbsp;&nbsp;&nbsp;</td>
   <td><a href="HelpStartConceptsConcepts" rel="nofollow">Caracteristicas</a></td>
   <td>proporcionado por ZAP</td>
  </tr> 
  <tr>
   <td>&nbsp;&nbsp;&nbsp;&nbsp;</td>
   <td><a href="HelpStartConceptsStructparams" rel="nofollow">Par&aacute;metros estructurales</a></td>
   <td>que identifica los par&aacute;metros que representan la estructura de la aplicaci&oacute;n en lugar de los datos del usuario</td>
  </tr> 
  <tr>
   <td>&nbsp;&nbsp;&nbsp;&nbsp;</td>
   <td><a href="HelpUiDialogsSessionContext-struct" rel="nofollow">Pantalla de estructura de contexto de sesi&oacute;n</a></td>
  </tr> 
 </tbody>
</table>


[Modificador estructural que identifica rutas de URL que representan datos.]: HelpStartConceptsStructmods
[Sites tab]: HelpUiTabsSites
[Contexto]: HelpStartConceptsContexts