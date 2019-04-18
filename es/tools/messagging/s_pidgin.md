---
index: 13
title: Pidgin
---
# GUÍA DE HERRAMIENTAS PIDGIN

## Guía de Herramientas Pidgin
Mensajería instantánea encriptada para Windows

**Lección para leer:
- [Enviando un mensaje](umbrella://communications/sending-a-message)**
**Ubicación de descarga:**
- [https://pidgin.im/download/](https://pidgin.im/download/) 
- [https://otr.cypherpunks.ca/](https://otr.cypherpunks.ca/)  
**Requisitos de la computadora:** Una conexión a Internet, una computadora con Windows XP o superior y una cuenta XMPP (Jabber).
_(Pidgin puede trabajar con muchos sistemas de chat, pero aquí nos centraremos en XMPP, anteriormente conocido como Jabber)_
**Versión utilizada en esta guía:**
- Windows 7 Ultimate
- Pidgin 2.10.9, pidgin-otr 4.0.0-1
**Licencia:** Software libre; mezcla de licencias de software libre
**Nivel:** Principiante
**Otra lectura:** [https://pidgin.im/cgi-bin/mailman/listinfo/support](https://pidgin.im/cgi-bin/mailman/listinfo/support)
**Tiempo requerido:** 20 minutos.

**Usar OTR con Pidgin le dará:**
- La capacidad de organizar y administrar algunos de los servicios de mensajería instantánea más populares a través de un solo programa.
- La capacidad de tener chats encriptados en mensajería instantánea, sin que el servidor registre esos chats.
- La capacidad de asegurarse de que la persona con la que está chateando realmente es esa persona.

### 1.0 Antes de Comenzar

Pidgin es un cliente de mensajería instantánea fácil de usar para Windows que utiliza un protocolo llamado OTR (Off-the-record), que permite a los usuarios tener conversaciones confidenciales.

- Nota: OTR no debe confundirse con "Off the record" de Google, que simplemente desactiva el registro de chat y no tiene capacidades de encriptación o verificación.
- Pidgin es compatible con los siguientes servicios de IM: AIM, Bonjour, Gadu-Gadu, Google Hangouts, Groupwise, ICQ, IRC, SILC, SIMPLE, Sametime, Zephyr y cualquier cliente de IM que ejecute el protocolo de mensajería XMPP.
- Pidgin no permite la comunicación entre diferentes servicios de mensajería instantánea. Por ejemplo, si está utilizando Pidgin para acceder a su cuenta de Google Hangouts, no podrá chatear con un amigo usando una cuenta de ICQ.
- Sin embargo, Pidgin se puede configurar para administrar varias cuentas basados en cualquiera de los protocolos de mensajería compatibles. Es decir, puede utilizar simultáneamente cuentas de Gmail e ICQ, y chatear con corresponsales utilizando cualquiera de esos servicios específicos (que son compatibles con Pidgin).
- Pidgin, registra automáticamente las conversaciones de forma predeterminada, sin embargo, tiene la capacidad de deshabilitar esta función. Dicho esto, usted no tiene control sobre la persona con la que está chateando; podría estar registrando o tomando capturas de pantalla de su conversación, incluso si usted mismo ha inhabilitado el registro.

**¿Por qué debería usar Pidgin + OTR?**
Cuando tiene una conversación de chat con Google Hangouts en el sitio web de Google, ese chat se cifra mediante HTTPS, lo que significa que el contenido de tu chat está protegido contra hackers y otros terceros mientras está en tránsito. Sin embargo, no está protegido de Google, que tiene las claves de sus conversaciones y puede entregarlas a las autoridades.

Una vez que haya instalado Pidgin, puede iniciar sesión con varias cuentas al mismo tiempo. Por ejemplo, podría usar Google Hangouts, Facebook y XMPP simultáneamente. Pidgin también te permite chatear usando estas herramientas sin OTR. Dado que OTR solo funciona si ambas personas lo están usando, esto significa que incluso si la otra persona no lo tiene instalado, aún puede chatear con ellos usando Pidgin.

Pidgin también le permite realizar una verificación fuera de banda para asegurarse de que está hablando con la persona con la que cree que está hablando. Para cada conversación, hay una opción que le mostrará las huellas digitales clave que tiene para usted y la persona con la que está chateando. Una "huella digital clave" es una cadena de caracteres como "342e 2309 bd20 0912 ff10 6c63 2192 1928", que se usa para verificar una clave pública más larga. Intercambie sus huellas digitales a través de otro canal de comunicaciones, como MD de Twitter o correo electrónico, para asegurarse de que nadie interfiera con su conversación.

**Limitaciones: ¿Cuándo no debo usar Pidgin + OTR?**

Pidgin es un programa complejo, que no se ha escrito con la seguridad como una prioridad máxima. Es casi seguro que tiene errores, algunos de los cuales pueden ser utilizados por los gobiernos o incluso por las grandes empresas para acceder a las computadoras que lo utilizan. Usar Pidgin para cifrar tus conversaciones es una gran defensa contra el tipo de vigilancia no dirigida que se usa para espiar las conversaciones de Internet de todos, pero si crees que será atacado personalmente por un atacante con muchos recursos (como un estado-nación), debe considerar precauciones más estrictas, como el correo electrónico encriptado con PGP.

### 2 Descargando e instalando

### 2.1 Obteniendo Pidgin

Puede obtener Pidgin en Windows descargando el instalador desde la página de descargas de Pidgin.
! [imagen] (tool_pidgin1.png)

Haga clic en la pestaña _púrpura_ DESCARGAR. _ **No** haga clic en el botón verde Descargar ahora porque querrá elegir un archivo de instalación diferente.
Serás llevado a la página de descarga.
![image](tool_pidgin2.png)

_De nuevo, **no** haga clic en el botón verde Descargar ahora porque queremos elegir un archivo de instalación diferente.
El instalador predeterminado para Pidgin es pequeño porque no contiene toda la información y descarga los archivos por ti. Esto a veces falla, por lo que tendrá una mejor experiencia con el "instalador offline" que contiene todo el material de instalación necesario.

Haga clic en el enlace "**instalador offline**". Se lo llevará a una nueva página titulada "Sourceforge" y después de unos segundos, una pequeña ventana emergente le preguntará si desea guardar un archivo.

- Nota: aunque la página de descarga de Pidgin usa "HTTPS" y, por lo tanto, está relativamente a salvo de manipulación, el sitio web al que lo dirige a descargar la versión de Windows de Pidgin es actualmente Sourceforge, que usa "HTTP" no cifrado y, por lo tanto, no ofrece protección. Eso significa que el software que descarga puede ser manipulado antes de descargarlo. La mayoría de estos riesgos provendrían de alguien con acceso a la infraestructura de Internet local que intente realizar una vigilancia dirigida contra usted personalmente (por ejemplo, un proveedor malicioso de puntos calientes) o un plan estatal o gubernamental para distribuir software comprometido a muchos usuarios. La extensión [HTTPS Everywhere] (https://www.eff.org/https-everywhere) puede reescribir las URL de descarga de Sourceforge en HTTPS, por lo que se recomienda que instale HTTPS Everywhere antes de descargar cualquier otro software. Además, según nuestra experiencia, Sourceforge a menudo tiene anuncios confusos de página completa en sus páginas de descarga que pueden engañar a las personas para que instalen algo que quizás no quieran. Puede instalar un bloqueador de anuncios antes de cualquier otro software para evitar estos anuncios confusos.

Muchos navegadores le pedirán que confirme si desea descargar este archivo. Internet Explorer 11 muestra una barra en la parte inferior de la ventana del navegador con un borde naranja.
![image](tool_pidgin3.png)

Para cualquier navegador, es mejor guardar primero el archivo antes de continuar, así que haga clic en el botón "Guardar". De forma predeterminada, la mayoría de los navegadores guardan los archivos descargados en la carpeta Descargas.

### 2.2 Obteniendo OTR

Puede obtener pidgin-otr, el complemento OTR para Pidgin, descargando el instalador desde la [página de descarga OTR](https://otr.cypherpunks.ca/).![image](tool_pidgin4.png)

Haga clic en la pestaña "Descargas" para acceder a la sección "Descargas" de la página. Haga clic en el enlace "Win32 installer for pidgin".
![image](tool_pidgin5.png)

Muchos navegadores le pedirán que confirme si desea descargar este archivo. Internet Explorer 11 muestra una barra en la parte inferior de la ventana del navegador con un borde naranja.
![image](tool_pidgin6.png)

Para cualquier navegador, es mejor guardar primero el archivo antes de continuar, así que haga clic en el botón "Guardar". De forma predeterminada, la mayoría de los navegadores guardan los archivos descargados en la carpeta Descargas.

Después de descargar Pidgin y pidgin-otr, debe tener dos archivos nuevos en su

carpeta de descargas:
![image](tool_pidgin7.png)

### 2.3 Instalando Pidgin

Mantenga la ventana del Explorador de Windows abierta y haga doble clic en pidgin-2.10.9-offline.exe. Se le preguntará si desea permitir la instalación de este programa. Haga clic en el botón "Sí".
![image](tool_pidgin8.png)

Se abre una pequeña ventana que le pide que seleccione un idioma. Haga clic en el botón "Aceptar".
![image](tool_pidgin9.png)

Se abre una ventana que le proporciona una visión general rápida del proceso de instalación. Haga clic en el botón "Siguiente".
![image](tool_pidgin10.png)

Ahora obtiene una descripción general de la licencia. Haga clic en el botón "Siguiente".
![image](tool_pidgin11.png)

Ahora podrá ver qué componentes diferentes están instalados. No cambie la configuración. Haga clic en el botón "Siguiente".
![image](tool_pidgin12.png)

Ahora puede ver dónde se instalará Pidgin. No cambie esta información. Haga clic en el botón "Siguiente".
![image](tool_pidgin13.png)

Ahora verá una ventana con texto de desplazamiento hasta que diga "Instalación completa". Haga clic en el botón "Siguiente".
![image](tool_pidgin14.png)

Finalmente, verá la última ventana del instalador de Pidgin. Haga clic en el botón "Finalizar".
![image](tool_pidgin15.png)

### 2.4 Instalación de pidgin-otr

Regrese a la ventana del Explorador de Windows y abra y haga doble clic en pidgin-otr-4.0.0-1.exe. Se le preguntará si desea permitir la instalación de este programa. Haga clic en el botón "Sí".
![image](tool_pidgin16.png)

Se abre una ventana que le proporciona una visión general rápida del proceso de instalación. Haga clic en el botón "Siguiente".
![image](tool_pidgin17.png)

Ahora obtiene una descripción general de la licencia. Haga clic en el botón "Acepto".
![image](tool_pidgin18.png)

Verá dónde se instalará pidgin-otr. No cambie esta información. Haga clic en el botón "Instalar".
![image](tool_pidgin19.png)

Finalmente, verá la última ventana del instalador pidgin-otr. Haga clic en el botón "Finalizar".
![image](tool_pidgin20.png)

### 3 Configuracion

### 3.1 Configurando Pidgin

Vaya al menú Inicio, haga clic en el ícono de Windows y seleccione Pidgin en el menú.
![image](tool_pidgin21.png)

### 3.2 Añadiendo una cuenta

Cuando se inicie Pidgin por primera vez, verá esta ventana de bienvenida que le brinda la opción de agregar una cuenta. Como todavía no tiene una cuenta configurada, haga clic en el botón "Agregar".
![image](tool_pidgin22.png)

Ahora verá la ventana "Agregar cuenta".

**_Pidgin puede trabajar con muchos sistemas de chat, pero aquí nos centraremos en XMPP, anteriormente conocido como Jabber._**

En la entrada del Protocolo, seleccione la opción "XMPP".

En la entrada del Nombre de Usuario, ingrese su nombre de usuario de XMPP.

En la entrada del dominio, ingrese el dominio de su cuenta de XMPP.

En la entrada de Contraseña, ingrese su contraseña de XMPP.

Marcar la casilla con la entrada "Recordar contraseña" facilitará el acceso a su cuenta. Tenga en cuenta que al hacer clic en "Recordar contraseña", su contraseña se guardará en la computadora, haciéndola accesible a cualquier persona que pueda acceder a su computadora. Si esto es una preocupación, no marque esta casilla. A continuación, se le solicitará que introduzca la contraseña de su cuenta de XMPP cada vez que inicie Pidgin.
![image](tool_pidgin23.png)

### 3.3 Añadiendo un Amigo

Ahora querrá agregar a alguien con quien chatear. Haga clic en el menú "Amigos" y seleccione "Agregar amigo". Se abrirá una ventana "Agregar amigo".
![image](tool_pidgin24.png)

En la "Ventana Agregar", puede ingresar el nombre de usuario de la persona con la que desea chatear. Este otro usuario no tiene que ser del mismo servidor, pero tiene que usar el mismo protocolo, como XMPP.

En la entrada "Nombre de usuario de Amigo", ingrese el nombre de usuario de su amigo con el nombre de dominio. Esto se verá como una dirección de correo electrónico.

En la entrada "Alias (Opcional)", puede ingresar el nombre que elija para su amigo. Esto es completamente opcional, pero puede ayudar si la cuenta XMPP de la persona con la que está conversando es difícil de recordar.

Haga clic en el botón "Agregar".
![image](tool_pidgin25.png)

Una vez que haya hecho clic en el botón "Agregar", Boris recibirá un mensaje preguntándole si le autoriza para que lo agregue. Una vez que Boris lo haga, agrega su cuenta y usted obtendrá la misma solicitud.

Haga clic en el botón "Autorizar".
![image](tool_pidgin26.png)

### 3.4 Configurando el plugin OTR

Ahora configurará el complemento OTR para que pueda chatear de forma segura. Haga clic en el menú "Herramientas" y seleccione la opción "Complementos".
![image](tool_pidgin27.png)

Desplácese hacia abajo hasta la opción "Mensajería Off-the-Record" y marque la casilla.

Haga clic en la entrada "Mensajes off-the-record" y haga clic en el botón "Configurar complemento".
![image](tool_pidgin28.png)

Ahora verá la ventana de configuración "Mensajería". Fíjese que dice "No hay clave presente".

Haga clic en el botón "Generar".
[image](tool_pidgin29.png)

Ahora una pequeña ventana se abrirá y generará una clave. Cuando haya terminado, haga clic en el botón "Aceptar".
![image](tool_pidgin30.png)

Verá nueva información: una cadena de texto de 40 caracteres, dividida en 5 grupos de ocho caracteres. Esta es su huella dactilar OTR. Haga clic en el botón "Cerrar".
![image](tool_pidgin31.png)

Ahora haga clic en el botón "Cerrar" en la ventana de complementos.

### 4.0 Chateando de forma segura

Ahora puede chatear con Boris. Ustedes dos pueden enviar mensajes de ida y vuelta. Sin embargo, todavía no estamos chateando de forma segura. Incluso si se está conectando al servidor XMPP, es posible que la conexión entre usted y Boris no esté protegida contra el espionaje.

Si observa la ventana de chat, observe que dice "No privado" en rojo en la parte inferior derecha. Haga clic en el botón "No privado".
![image](tool_pidgin32.png)

Se abrirá un menú, seleccione "Autenticar amigo".
![image](tool_pidgin33.png)

Se abrirá una ventana. Se le pregunta: "¿Cómo le gustaría autenticar a su amigo?"

La lista desplegable tiene tres opciones:

**Opción 1: secreto compartido**

Un secreto compartido es una línea de texto que usted y la persona con la que desea conversar han acordado usarla antes de tiempo. Debería haber compartido esto en persona y nunca haberlo intercambiado por canales inseguros como el correo electrónico o Skype.

Usted y su amigo deben ingresar este texto juntos. Haga clic en el botón "Autenticar".
![image](tool_pidgin34.png)

La verificación de secreto compartido es útil si usted y su amigo ya han hecho arreglos para conversar en el futuro pero aún no han creado las huellas digitales OTR en la computadora que está usando.

**Opción 2: Verificación manual de huellas digitales**

La verificación manual de huellas digitales es útil si ya le dieron la huella digital de su amigo y ahora se está conectando con Pidgin. Esto no será útil si su amigo cambió de computadora o tuvo que crear nuevas huellas digitales.

Si la huella digital que recibió y la huella digital en la pantalla coinciden, seleccione "La Tengo" y haga clic en el botón "Autenticar".
![image](tool_pidgin35.png)

**Opción 3: Pregunta y respuesta**

La verificación de preguntas y respuestas es útil si conoce a su amigo pero no ha establecido un secreto compartido ni tuvo la oportunidad de compartir huellas digitales. Este método es útil para establecer una verificación basada en algo que ambos saben, como un evento compartido o una memoria.

Ingrese la pregunta que quiere hacer. No la haga tan simple que alguien pueda adivinarlo fácilmente, pero no la haga imposible. Un ejemplo de una buena pregunta sería "¿Dónde fuimos a cenar en Minneapolis?" Y el ejemplo de una mala pregunta sería "¿Puedes comprar manzanas en Tokio?"

**Las respuestas deben coincidir exactamente; así que téngalo en cuenta al elegir una respuesta a tu pregunta. La capitalización es importante, por lo que podría considerar incluir una nota como (por ejemplo: usar mayúsculas, minúsculas).**

Ingrese la pregunta y la respuesta, luego haga clic en el botón "Autenticar".
![image](tool_pidgin36.png)

Su amigo tendrá una ventana abierta con la pregunta mostrada que solicita la respuesta. Tendrán que responder y hacer clic en el botón "Autenticar". Luego recibirán un mensaje informándoles si la autenticación fue exitosa.
![image](tool_pidgin37.png)![image](tool_pidgin38.png)

Una vez que tu amigo haya completado el procedimiento de autenticación, aparecerá una ventana que te permitirá saber si la autenticación se realizó correctamente.
![image](tool_pidgin39.png)

Su amigo también debe verificar su cuenta para que ambos puedan estar seguros de que la comunicación es segura. Esto es lo que le gustaría a Akiko y Boris. Observe los iconos verdes "Privados" en la esquina inferior derecha de la ventana de chat.
![image](tool_pidgin40.png)

### 5 Trabajando con otro software

Los mecanismos para verificar la autenticidad deberían funcionar entre diferentes programas de chat como Pidgin y Adium. No es necesario que use el mismo software de chat para usar el chat sobre XMPP y OTR, pero a veces hay errores en el software. Adium, un software de chat para OS X, tiene un error al recibir la verificación de Preguntas y Respuestas. Si encuentra que está fallando la verificación de otros cuando está usando la verificación de Preguntas y Respuestas, verifique si están usando Adium y vea si puede usar otro método de verificación.