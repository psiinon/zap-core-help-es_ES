# Opción: Certificados SSL Dinámicos #

OWASP ZAP le permite descifrar las conexiones SSL de forma transparente. Para hacerlo, ZAP tiene que cifrar cada solicitud antes de enviar al servidor y descifrar cada respuesta, que viene detrás. Pero, esto ya lo hace el navegador. Por eso, la única forma de descifrar o interceptar la transmisión es hacer un enfoque de "man in the middle".

## Resumen ##

![man in the middle][]

En palabras resumidas, cada dato enviado y recibido del servidor se encripta/desencripta utilizando el certificado original del servidor dentro de ZAP. De esta manera, ZAP conoce el texto plano. Para establecer una sesión protegida por SSL para ti (tu navegador), ZAP utiliza su propio certificado. Este es el que puedes crear. Cada certificado creado por ZAP será firmado por el mismo nombre del servidor. En el ejemplo superior, ZAP creará un certificado para el nombre de servidor "www.example.com". De esta manera, tu navegador realizará la encriptación SSL normal.

## Certificado ZAP Root CA ##

Imagina que estás visitando varios sitios SSL protegido. Cada vez que tu navegador conecta a dicho sitio, se crea un nuevo certificado SSL. Sin embargo, estos certificados son de confianza no cualquiera (porque uno mismo creado por ZAP). En otras palabras, tu navegador no aceptará estos certificados en el primer lugar. Usted puede familiarizarse con estas situaciones, cuando su navegador queja de error de certificado, pero usted puede crear manualmente una regla de excepción para ese servidor.

Cada certificado creado por ZAP se encuentra en la cadena de confianza del certificado "ZAP Root CA". (Para más detalles sobre la cadena de confianza, utiliza tu motor de búsqueda favorito ;-) ) Esto significa, tú (tu navegador) solo debes confiar en el certificado ZAP Root CA una vez, y cualquier otro certificado será aceptado automáticamente. En otras palabras, una vez hayas agregado el certificado ZAP Root CA a tu lista de Root CAs de confianza, tu navegador no reconoce un ataque intermediario.

### Generar ###

Si estás ejecutando ZAP por primera vez, debes generar un certificado Root CA primero. Una vez hayas generado uno, debes instalarlo en tu navegador o aplicación de cliente HTTP. Ve la sección de [instalación][instalaci_n] para más detalles.

Cada certificado Root CA generado es válido por un año. Después de este periodo debes crear uno nuevo.
Cada certificado Root CA generado tiene fortaleza de 2048 bit (RSA con SHA1).
Cada certificado Root CA generado inicia con número de serial "1". Every generated Root CA certificate consists of the following identifiers:

`CN = OWASP Zed Attack Proxy Root CA L = 87b77fe834b0a301 O = OWASP Root CA OU = OWASP ZAP Root CA C = XX`

Como se puede ver, hay un identificador de localización (L) que es sólo un número hexadecimal. Este número se construye fuera de dos códigos de hash de 32 bits: nombre de usuario y directorio home del usuario. De esta manera puede identificar su propio certificado al utilizar múltiples instalaciones. Pero no hay manera de que alguien pueda encontrar tu nombre de este código de hash.

### Importar ###

Cuando está utilizando la instalación múltiple de ZAP y desea usar el mismo certificado de CA raíz, para que pueda importarlo. Simply use one installation of OWASP ZAP to generate one Root CA certificate.
Copy the file 'OWASP ZAP/config.xml' from your users home directory to the PC, where you want to use the same certificate and press 'import' to import it.

You can also import certificates stored in pem files as long as they include both the certificate and the unencrypted private key in the following format:
`-----BEGIN CERTIFICATE----- MIIC9TCCAl6gAwIBAgIJANL8E4epRNznMA0GCSqGSIb3DQEBBQUAMFsxGDAWBgNV BAoTD1N1cGVyZmlzaCwgSW5jLjELMAkGA1UEBxMCU0YxCzAJBgNVBAgTAkNBMQsw CQYDVQQGEwJVUzEYMBYGA1UEAxMPU3VwZXJmaXNoLCBJbmMuMB4XDTE0MDUxMjE2 MjUyNloXDTM0MDUwNzE2MjUyNlowWzEYMBYGA1UEChMPU3VwZXJmaXNoLCBJbmMu MQswCQYDVQQHEwJTRjELMAkGA1UECBMCQ0ExCzAJBgNVBAYTAlVTMRgwFgYDVQQD Ew9TdXBlcmZpc2gsIEluYy4wgZ8wDQYJKoZIhvcNAQEBBQADgY0AMIGJAoGBAOjz Shh2Xxk/sc9Y6X9DBwmVgDXFD/5xMSeBmRImIKXfj2r8QlU57gk4idngNsSsAYJb 1Tnm+Y8HiN/+7vahFM6pdEXY/fAXVyqC4XouEpNarIrXFWPRt5tVgA9YvBxJ7SBi 3bZMpTrrHD2g/3pxptMQeDOuS8Ic/ZJKocPnQaQtAgMBAAGjgcAwgb0wDAYDVR0T BAUwAwEB/zAdBgNVHQ4EFgQU+5izU38URC7o7tUJml4OVoaoNYgwgY0GA1UdIwSB hTCBgoAU+5izU38URC7o7tUJml4OVoaoNYihX6RdMFsxGDAWBgNVBAoTD1N1cGVy ZmlzaCwgSW5jLjELMAkGA1UEBxMCU0YxCzAJBgNVBAgTAkNBMQswCQYDVQQGEwJV UzEYMBYGA1UEAxMPU3VwZXJmaXNoLCBJbmMuggkA0vwTh6lE3OcwDQYJKoZIhvcN AQEFBQADgYEApHyg7ApKx3DEcWjzOyLi3JyN0JL+c35yK1VEmxu0Qusfr76645Oj 1IsYwpTws6a9ZTRMzST4GQvFFQra81eLqYbPbMPuhC+FCxkUF5i0DNSWi+kczJXJ TtCqSwGl9t9JEoFqvtW+znZ9TqyLiOMw7TGEUI+88VAqW0qmXnwPcfo= -----END CERTIFICATE----- -----BEGIN PRIVATE KEY----- MIICXgIBAAKBgQDo80oYdl8ZP7HPWOl/QwcJlYA1xQ/+cTEngZkSJiCl349q/EJV Oe4JOInZ4DbErAGCW9U55vmPB4jf/u72oRTOqXRF2P3wF1cqguF6LhKTWqyK1xVj 0bebVYAPWLwcSe0gYt22TKU66xw9oP96cabTEHgzrkvCHP2SSqHD50GkLQIDAQAB AoGBAKepW14J7F5e0ppa8wvOcUU7neCVafKHA4rcoxBF8t+P7UhiMVfn7uQiFk2D K8gXyKpLcEdRb7K7CI+3i8RkoXTRDEZU5XPMJnZsE5LWgNQ+pi3HwMEdR0vD2Iyv vIH3tq6mNKgDu+vozm8DWsEP96jrhVbo1U1rzyEtX46afo79AkEA/VXanGaqj4ua EsqfY6n/7+MTm4iPOM7qfoyI4EppJXZklc/FbcV2lAjY2Jl9U6X7WnqCPn+/zg44 6lKWTnhAawJBAOtmi6nw8WjY6uyXZosE/0r4SkSSo20EJbBCJcgdofKT+VCGB4hp h6XwGdls0ca+qa5ZE1a196dpwwVre0hm88cCQQDrUm3QbHmw/39uRzOJs6dfYPKc vlwz69jdFpQqrFRBjVlf4/FDx3IfjpxHj0RgiEUUxcnoXmh/8qwh1fdzCrbjAkB4 afg/chTLQUrKw5ecvW2p9+Blu20Fsv1kcDHLb/0LjU4XNrhbuz+8TlmqstOMCrPZ j48o5+RLKvqrpxNlMeS5AkEA6qIdW/yp5N8b1j2OxYZ9u5O//BvspwRITGM60Cps yemZE/ua8wm34SKvDHf5uxcmofShW17PLICrsLJ7P35y/A== -----END PRIVATE KEY-----`
And yes, that example will work - its the Superfish certificate!

### Ver ###

En el cuadro de diálogo de opciones de ZAP, está viendo los bytes sin formato (hexadecimales codificados) del certificado. La opción "view" intenta usar la herramienta de visualización predeterminada de su sistema para los archivos ".CER". En Windows, esto suele ser el mismo, al exportar el certificado y hacer doble clic en él.

### Guardar/Exportar ###

En el cuadro de diálogo de opciones de ZAP, está viendo los bytes sin formato (hexadecimales codificados) del certificado. Muchos programas usan este formato simple para funciones de importación / exportación. Al hacer clic en "export", estos bytes se guardan en el disco. Esto es igual a seleccionar todo y hacer CTRL + C (copiar al portapapeles) y guardarlo en un nuevo archivo .CER (que es texto simple como se ve en el cuadro de diálogo).

## Certificados SSL Dinámicos ##

Cada instancia de ZAP está usando su propio certificado raíz. Por supuesto, puede importar certificados raíz para usarlos en varias máquinas. Cuando se ejecuta, habrá sub-certificado creado, cada vez que un HTTPS recurso solicitado Eso significa que el certificado de CA raíz se usa como emisor.

Cada certificado generado dinámicamente es válido por 1000 días.
Cada certificado generado dinámicamente tiene una potencia de 2048 bits (RSA con SHA1).
Cada certificado generado dinámicamente tiene un número de serie aleatorio. Cada certificado generado dinámicamente consta de los siguientes identificadores:

`CN = www.example.com E = owasp-zed-attack-proxy@lists.owasp.org C = XX O = OWASP OU = Zed Attack Proxy Project`

 *Nota al margen: Cada vez que inicia ZAP, internamente se genera un desplazamiento de número de serie aleatorio. Cada certificado generado dinámicamente usará este desplazamiento más un aumentar el contador. Por ejemplo, primero se ha certificado dinámicamente número de serie 2314, el segundo 2315, el tercero 2316 y así sucesivamente. La razón de esto es simple: los navegadores también están almacenando certificados en caché. Cuando reinicie ZAP pero no reinicie su navegador, podría suceder, el navegador ve el mismo certificado pero con un número de serie diferente. Al final, el navegador se quejaría y rechazaría el certificado. Al usar el desplazamiento aleatorio (número aleatorio interno de 48 bits), las posibilidades son 1 a 281.474.976.710.656 que al reiniciar ZAP, el número de serie el desplazamiento es diferente.
En el raro caso, está descubriendo que su navegador se queja de un número de serie roto dentro del certificado, solo reinicie su navegador ;-) .* 

## Install ZAP Root CA certificate ##

Cualquier cliente HTTPS para utilizar, tiene que saber el certificado CA raíz de la OWASP como 'certificado raíz de confianza'. Por lo general usted tiene que instalar manualmente el certificado ZAP en lista del explorador de certificados raíz de confianza.

### Windows / Internet Explorer ###

La manera más fácil es hacer click en [ver][] y escoger 'Instalar certificado'. Alternativamente, puedes guardar/exportar tu certificado generado (copiarlo a tu computadora destino) y hacer doble click en el archivo .CER. Al hacer esto, el asistente usual de Windows para la asistencia en instalación de certficados se mostrará. En este asistente selecciona manualmente la tienda de certificado. NO permitas que Windows seleccione la tienda de certificado automáticamente. Elija 'Trusted Root Certificates' como almacen y finalice el asistente.

Después de una instalación satisfactoria, puedes revisar el certificado.

1.  Ir a opciones de Internet
2.  Contenido de la Pestaña
3.  Haz click en certificados
4.  Haz click en la pestaña de certificados de raíz de confianza
5.  The OWASP ZAP Root CA should be there

### Mozilla Firefox ###

Firefox usa su propia tienda de certificados. Es por esto que debes importarlo dos veces, cuando utilices ambos navegadores en Windows. La instalación y validación tardía se realiza en el mismo cuadro de diálogo de preferencia:

1.  Ir a Preferencias
2.  Pestaña Avanzados
3.  Pestaña Criptografía/Certificados
4.  Haz click en Ver Certificados
5.  Haz click en la pestaña de Autoridades
6.  Haz click en Importar y selecciona el archivo owasp\_zap\_root\_ca.cer guardado
7.  En el asistente escoge confiar en este certificado para identificar sitios web (marca las casillas)
8.  Concluye con el asistente

## Riesgos ##

**Atención, ¡hay riesgos!**
Cuando se agregan certificados Root CA autogenerados a la lista de certificados de raíz de confianza, toda persona con el certificado raíz puede introducir datos a tu sistema (navegador). En otras palabras cuando no estás realizando pruebas en un entorno seguro, sino en máquinas en producción, ten en cuenta que estás abriendo un vector de ataque adicional a tu sistema.

## Vease también ##

<table> 
 <tbody>
  <tr>
   <td>&nbsp;&nbsp;&nbsp;&nbsp;</td>
   <td> <a href="HelpUiDialogsOptionsCertificate" rel="nofollow">Certificados</a></td>
   <td>para certificados de clientes SSL</td>
  </tr> 
 </tbody>
</table>


[man in the middle]: https://github.com/zaproxy/zap-core-help/wiki/images/maninthemiddle.png
[instalaci_n]: HelpUiDialogsOptionsDynsslcert#install
[ver]: HelpUiDialogsOptionsDynsslcert#view