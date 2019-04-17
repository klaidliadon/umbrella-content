---
index: 12
title: PGP para Windows
---
# GUÍA DE HERRAMIENTAS DE PGP PARA WINDOWS

Correo cifrado para Windows

**Lección para leer:**
- **[Email](umbrella://communications/email)**
**Ubicación de Descarga:**
- GPG4Win
- Mozilla Thunderbird
- Enigmail
**Requerimientos del equipo:** Una conexión a Internet, una computadora con Windows, una cuenta de correo electrónico
**Versión utilizada en esta guía:**
- Windows: Windows 7 Ultimate
- Mozilla Thunderbird 24.6.0
- Enigmail 1.7
- GPG4Win 2.2.1
**Licencia:** Software libre; combinación de licencias de Software Libre
**Nivel:** Avanzado
**Tiempo requerido:** 30-60 minutos.

**Usar PGP le dará:**
- La capacidad de proteger sus comunicaciones por correo electrónico para que nadie las lea, excepto sus destinatarios.
- La capacidad de demostrar que un correo electrónico provino de una persona en particular, en lugar de ser un mensaje falso enviado por otro remitente (de otra manera es muy fácil que el correo electrónico sea fabricado). Ambas son defensas importantes si se lo busca por vigilancia o información errónea.

**Nota:** Si le preocupa que el correo electrónico encriptado con PGP no sea seguro después de que se informaron las vulnerabilidades en mayo de 2018, lea la sección Efail de nuestra lección avanzada de [correo electrónico] (umbrella://communications/email).

### 1.0 Antes de comenzar

Para usar Pretty Good Privacy (PGP), deberá instalar algún software adicional que funcione con su programa de correo electrónico actual. También deberá crear una clave privada, que mantendrá privada. La clave privada es lo que usará para descifrar los correos electrónicos que se le envíen y para firmar digitalmente los correos electrónicos que envíe para mostrar que realmente provienen de usted. Finalmente, aprenderá cómo distribuir su clave pública, una pequeña porción de información que otros deberán conocer antes de que puedan enviarle correo cifrado y que puedan usar para verificar los correos electrónicos que envíe.

**Tenga en cuenta que ambos extremos de la conversación de correo electrónico deben utilizar un software compatible con PGP para que funcione.**

La gente normalmente usará esto solo en sus dispositivos personales, no en dispositivos compartidos. Afortunadamente, PGP está disponible para la mayoría de las computadoras de escritorio y dispositivos móviles, y puede apuntarlas a estas guías para ayudarles a configurar su propia versión. Esta guía es para usuarios de Windows.

### 1.1 Resumen

Para usar PGP para intercambiar correos electrónicos seguros, debe reunir tres programas: GPG4Win (GNU Privacy Guard para Windows conocido como GnuPG), Mozilla Thunderbird y Enigmail.

- GnuPG es el programa que en realidad cifra y descifra el contenido de su correo.
- Mozilla Thunderbird es un cliente de correo electrónico que te permite leer y escribir correos electrónicos sin usar un navegador.
- Enigmail es un complemento de Mozilla Thunderbird que lo une todo.

¡Nota! Lo que esta guía enseña es cómo usar PGP con Mozilla Thunderbird, un programa cliente de correo electrónico que realiza una función similar a Outlook. Puede tener su propio programa de software de correo electrónico favorito (o usar un servicio de correo web como Google Mail o Outlook.com). Esta guía no le dirá cómo usar PGP con estos programas. Puede elegir instalar Thunderbird y experimentar con PGP con un nuevo cliente de correo electrónico, o puede investigar otras soluciones para usar PGP con su software habitual. Todavía no hemos encontrado una solución satisfactoria para estos otros programas.

**El uso de PGP no encripta completamente su correo electrónico: la información del remitente y del destinatario aún no está encriptada, al igual que la línea de asunto.**

Cifrar la información del remitente y el destinatario no es posible en el sistema de correo electrónico existente. El uso de Mozilla Thunderbird con el complemento Enigmail le brinda una manera fácil de cifrar el contenido de su correo electrónico. Es posible que alguien que espíe sus correos electrónicos aún vea las identidades de las personas con las que se comunica y cuándo las envía por correo electrónico.

Primero descargará todo el software necesario, lo instalará y luego terminará con la configuración y el uso.

### 2 Descargando el software

### 2.1 Obteniendo GPG4Win

Puede obtener GnuPG (también conocido como GPG) en Windows descargando el instalador de la página de descargas de GPG4Win.
![image](tool_pgpwin1.png)

Haga clic en la versión más reciente de GPG4Win con solo el componente GnuPG (Vanilla o Light) para descargar el instalador de GPG.

**Nota: esta versión de GPG está disponible solo en un sitio web que ofrece descargas "http", no descargas seguras "https". Si le preocupa que su organización pueda ser objeto de una vigilancia que pueda alterar su conexión a Internet, es posible que desee investigar soluciones más drásticas, como descargar y ejecutar Tails, un sistema operativo seguro que reemplaza a Windows.**

Muchos navegadores le pedirán que confirme si desea descargar este archivo. Internet Explorer 11 muestra una barra en la parte inferior de la ventana del navegador con un borde naranja.

Para cualquier navegador, es mejor guardar primero el archivo antes de continuar, así que haga clic en el botón "Guardar". De forma predeterminada, la mayoría de los navegadores guardan los archivos descargados en la carpeta Descargas.

### 2.2 Obtener Mozilla Thunderbird

Vaya al sitio web de Mozilla Thunderbird.
![image](tool_pgpwin2.png)

Haga clic en el botón verde con la etiqueta "Descarga gratuita de Thunderbird".

El sitio web de Mozilla Thunderbird habrá detectado su idioma preferido. Si desea utilizar Thunderbird en otro idioma, haga clic en el enlace "Otros Sistemas e Idiomas" y realice su selección desde allí.

Muchos navegadores le pedirán que confirme si desea descargar este archivo. Internet Explorer 11 muestra una barra en la parte inferior de la ventana del navegador con un borde naranja.
![image](tool_pgpwin3.png)

Para cualquier navegador, es mejor guardar primero el archivo antes de continuar, así que haga clic en el botón "Guardar". De forma predeterminada, la mayoría de los navegadores guardan los archivos descargados en la carpeta Descargas.

### 2.3 Obtener Enigmail

Puede obtener Enigmail desde el sitio web de Enigmail.
![image](tool_pgpwin4.png)

Muchos navegadores le pedirán que confirme si desea descargar este archivo. Internet Explorer 11 muestra una barra en la parte inferior de la ventana del navegador con un borde naranja.
![image](tool_pgpwin5.png)
Para cualquier navegador, es mejor guardar primero el archivo antes de continuar, así que haga clic en el botón "Guardar". De forma predeterminada, la mayoría de los navegadores guardan los archivos descargados en la carpeta Descargas.


Después de descargar Enigmail, GPG4Win y Mozilla Thunderbird, debería tener tres nuevos archivos en tu carpeta de descargas:
[image](tool_pgpwin6.png)

### 3 Instalando el software

### 3.1 Instalando GPG4Win

Mantenga la ventana del Explorador de Windows abierta y haga doble clic en gpg4win-xxx-x.x.x.exe. Se le preguntará si desea permitir la instalación de este programa. Haga clic en el botón "Sí".
![image](tool_pgpwin7.png)

Se abrirá una ventana que le dará una visión general de lo que se instalará. Haga clic en el botón "Siguiente".
![image](tool_pgpwin8.png)

Se abrirá una ventana con el acuerdo de licencia. Haga clic en el botón "Siguiente".
![image](tool_pgpwin9.png)

El paquete GPG4Win Vanilla no tiene componentes para seleccionar, así que haga clic en el botón "Siguiente" nuevamente. Para el paquete GPG4Win-Light, deseleccione todos los componentes opcionales para instalar GnuPG solamente.
![image](tool_pgpwin10.png)

A continuación, podrá elegir dónde está instalado GPG. No cambie la configuración predeterminada. Haga clic en el botón "Siguiente".
![image](tool_pgpwin11.png)

Las siguientes dos ventanas tendrán algunas opciones de instalación. Haga clic en el botón "Siguiente" y luego haga clic en el botón "Instalar":
![image](tool_pgpwin12.png)![image](tool_pgpwin13.png)

Verá una ventana con una barra de progreso; cuando termine, dirá "Instalación completada". Haga clic en el botón "Siguiente" de nuevo.
[image](tool_pgpwin14.png)

Finalmente, estás en el último paso de la instalación. Quite la marca de verificación junto a "Mostrar el archivo README" y haga clic en el botón "Finalizar".
![image](tool_pgpwin15.png)

Eso es. Ahora vamos a instalar Mozilla Thunderbird.

### 3.2 Instalación de Mozilla Thunderbird

Al igual que GPG4Win, instala Mozilla Thunderbird haciendo doble clic en el archivo Thunderbird Setup 24.6.0.exe. Como de costumbre, se le preguntará si desea ejecutar este archivo. Haga clic en el botón "Ejecutar".
[image](tool_pgpwin16.png)

Se le preguntará si desea permitir que Mozilla Thunderbird realice un cambio en su computadora al instalar el software. Haga clic en el botón "Sí".
![image](tool_pgpwin17.png)

Verá la ventana de configuración de Mozilla Thunderbird. Haga clic en el botón "Siguiente".
![image](tool_pgpwin18.png)

A continuación, podrá elegir entre una configuración estándar y una configuración personalizada. Mantenga la selección de configuración estándar y haga clic en el botón "Siguiente".
![image](tool_pgpwin18.png)

Se le dará un resumen de dónde se instalarán los archivos de Mozilla Thunderbird. Haga clic en el botón "Instalar".
![image](tool_pgpwin19.png)

Cuando se complete el proceso de instalación, verá una ventana final que le permite iniciar Mozilla Thunderbird. Haga clic en el botón "Finalizar".
![image](tool_pgpwin20.png)

### 3.3. Instalacion de enigmail

**Paso 1. Preparación**

Cuando se inicie Mozilla Thunderbird por primera vez, verá esta pequeña ventana de confirmación preguntando acerca de algunas configuraciones predeterminadas. Recomendamos hacer clic en el botón "Establecer como predeterminado".
[image](tool_pgpwin21.png)

A continuación, se le preguntará si desea una nueva dirección de correo electrónico. Haga clic en el botón "Omitir esto y usar mi correo electrónico existente". Ahora configurará Mozilla Thunderbird para enviar y recibir correos electrónicos. Si está acostumbrado a solo leer y enviar correos electrónicos a través de gmail.com, outlook.com o yahoo.com, Mozilla Thunderbird será una experiencia nueva, pero no es tan diferente en general.
![image](tool_pgpwin22.png)

**Paso 2. Agregar una cuenta de correo a Mozilla Thunderbird**

Se abrirá una nueva ventana.
[image](tool_pgpwin23.png)

Ingrese su nombre, dirección de correo electrónico y la contraseña de su cuenta de correo electrónico. Mozilla no tiene acceso a su contraseña ni a su cuenta de correo electrónico. Haga clic en el botón "Continuar".
![image](tool_pgpwin24.png)

En muchos casos, Mozilla Thunderbird detectará automáticamente la configuración necesaria. En algunos casos, Mozilla Thunderbird no tiene información completa y tendrá que ingresarla usted mismo. Aquí hay un ejemplo de las instrucciones que Google proporciona para Gmail:

Servidor de correo entrante (IMAP) - Requiere SSL
- imap.gmail.com
- Puerto: 993
- Requiere SSL: Sí

Servidor de correo saliente (SMTP): requiere TLS
- smtp.gmail.com
- Puerto: 465 o 587.
- Requiere SSL: Sí
- Requiere autenticación: Sí
- Use la misma configuración que el servidor de correo entrante

**Nombre completo o Nombre para Mostrar:** [su nombre o seudónimo]

**Nombre de cuenta o nombre de usuario:** su dirección completa de Gmail (nombredeusuario@gmail.com). Usuarios de Google Apps, ingresen nombredeusuario@su_dominio.com

**Dirección de correo electrónico:** su dirección de Gmail completa (nombredeusuario@gmail.com) Usuarios de Google Apps, ingresen su nombre de usuario@su_dominio.com

**Contraseña:** su contraseña de Gmail

**Si usa la autenticación de dos factores con Google (y, dependiendo del modelo de amenaza, ¡probablemente debería!) No puede usar su contraseña de Gmail estándar con Thunderbird. En su lugar, deberá crear una nueva contraseña específica de la aplicación para que Thunderbird acceda a su cuenta de Gmail. Consulte [la Guía de Google] (https://support.google.com/mail/answer/1173270?hl=es) para hacer esto.**

Cuando toda la información se ingrese correctamente, haga clic en el botón "Listo".
![image](tool_pgpwin25.png)

Mozilla Thunderbird comenzará a descargar copias de su correo electrónico a su computadora. Intenta enviar un correo electrónico de prueba a sus amigos.

**Paso 3. Instalando Enigmail**

Enigmail se instala de manera diferente a Mozilla Thunderbird y GPG4Win. Como se mencionó anteriormente, Enigmail es un complemento para Mozilla Thunderbird. Haga clic en el botón "Menú", también llamado botón Hamburguesa, y seleccione "Complementos".
![image](tool_pgpwin26.png)

Se le llevará a la pestaña Administrador de Complementos.
![image](tool_pgpwin27.png)

Haga clic en la rueda dentada para abrir un pequeño menú y seleccione "Instalar complemento desde archivo" que abrirá una ventana de selección de archivos.
![image](tool_pgpwin28.png)

Es muy probable que la ventana de selección de archivos se abra en la carpeta Descargas. Si no es así, vaya a la carpeta de Descargas (donde se guardó Enigmail) haga clic en enigmail-1.7-tb + sm.xpi y luego haga clic en el botón "Abrir".
![image](tool_pgpwin29.png)

Ahora verá una pequeña ventana que le pedirá que confirme si desea instalar Enigmail. Haga clic en el botón "Instalar ahora".
![image](tool_pgpwin30.png)

Después de instalar el complemento Enigmail, Mozilla Thunderbird le pedirá que reinicie el navegador para activar Enigmail. Haga clic en el botón "Reiniciar ahora" y Mozilla Thunderbird se reiniciará.
[image](tool_pgpwin31.png)

Cuando Mozilla Thunderbird se reinicie, se abrirá una ventana adicional que iniciará el proceso de configuración del complemento Enigmail. Mantenga seleccionado el botón "Sí, deseo que el asistente me ayude a comenzar" y haga clic en el botón "Siguiente".
![image](tool_pgpwin32.png)

Enigmail le proporciona tres opciones para manejar el correo. La opción predeterminada es cifrar los correos electrónicos si tiene la "clave pública" de otra persona, Enigmail cifrará el correo electrónico que envíe pero dejará los correos electrónicos sin cifrar si aún no tiene la clave pública del destinatario. También tiene la opción de cifrar correos electrónicos todo el tiempo a todas las personas con claves PGP, lo que significa que tendrá que encontrar las claves públicas para las personas para las que aún no las tiene, o desactivar el cifrado automático por completo y solo usar PGP cuando sea dirigido
![image](tool_pgpwin33.png)

No sabemos cuál es la opción adecuada para usted, pero creemos que la opción "Conveniente encriptación automática" es una buena opción. Si tiene dudas, elija "No cifrar mis mensajes de forma predeterminada". Haga clic en el botón "Siguiente".

Ahora tiene una opción para firmar digitalmente todos los correos electrónicos salientes. Firmar su correo electrónico con PGP le permite al destinatario verificar que usted envió el mensaje y que su contenido no fue alterado. Haga clic en el botón "Firmar mis mensajes de manera predeterminada" para activar esta función. La desventaja de hacer esto, sin embargo, es que también puede marcar a cualquier persona a la que le envíe correo que use PGP. [En algunas partes del mundo] (www.cryptolaw.org/) (incluyendo China, Irán, Bielorrusia y algunos estados del Medio Oriente) el uso de cifrado sin licencia, incluso para uso personal, es ilegal, por lo que es posible que tenga muy buenas razones para no dejar que otros sepan que usas PGP.

Haga clic en el botón "Siguiente".
![image](tool_pgpwin34.png)

Ahora verá una opción para que Enigmail realice algunos cambios en la configuración de Mozilla Thunderbird.
![image](tool_pgpwin35.png)

Si hace clic en el botón Detalles, puede revisar cuáles son esos cambios.
![image](tool_pgpwin36.png)

Las siguientes opciones se pueden desmarcar (volver a habilitar), para una transición más fluida, si usa PGP/Mime de forma predeterminada (lo configuraremos más adelante):

- Deshabilitar texto fluido
- Ver el cuerpo del mensaje como texto plano
- No escribir mensajes HTML
La opción final previene posibles problemas en el cifrado y descifrado de su correo electrónico. Tenga en cuenta que al seleccionar esta casilla se eliminará la posibilidad de enviar texto en negrita, subrayado o coloreado. Después de revisar los cambios, haga clic en el botón "Aceptar".


La pequeña ventana se cerrará. Haga clic en el botón "Siguiente".

Ahora comenzará a crear su clave privada y pública.

### 4 Creando una clave pública y una clave privada

La instalación y configuración del complemento Enigmail está completa. Ahora tendrás la opción de crear tu par de claves pública y privada. Esto supone que no ha creado una clave privada anteriormente.

Haga clic en el botón "Siguiente".
![image](tool_pgpwin37.png)

A menos que ya haya configurado más de una cuenta de correo electrónico, Enigmail elegirá la cuenta de correo electrónico que ya haya configurado. Lo primero que deberá hacer es crear una frase de contraseña segura para su clave privada. Consulte la **[Lección de contraseñas](umbrella://information/passwords)** para obtener más información sobre cómo hacerlo.

Asegúrese de haber escrito esta frase de contraseña en un papel hasta que la haya memorizado. Manténgalo en un lugar donde pueda saber si se lo ha tomado o visto (como su billetera o cartera). Solo asegúrese de no dejar este papel tirado.

Haga clic en el botón "Siguiente".

Enigmail mostrará información sobre su clave privada, así como los ajustes de configuración. Recomendamos crear claves de longitud de 4096 bits. Haga clic en el botón "Siguiente".
![image](tool_pgpwin38.png)

**Su clave caducará en un momento determinado; cuando eso suceda, otras personas dejarán de usarlo por completo para nuevos correos electrónicos, aunque es posible que no reciba ninguna advertencia o explicación sobre el motivo. Por lo tanto, es posible que desee marcar su calendario y prestar atención a este problema aproximadamente un mes antes de la fecha de vencimiento.**

Es posible extender la vida útil de una clave existente dándole una nueva fecha de vencimiento posterior, o es posible reemplazarla con una nueva clave creando una nueva desde cero. Es posible que ambos procesos requieran contactar a las personas que le envían correos electrónicos y asegurarse de que obtengan la clave actualizada; El software actual no es muy bueno para automatizar esto. Así que haga un recordatorio; Si piensa que no podrá administrarlo, puede considerar configurar la clave para que nunca caduque, aunque en ese caso otras personas podrían intentar usarla cuando se comuniquen con usted en el futuro, incluso si ya no tiene la clave privada o ya no usa PGP.

Enigmail generará la clave y cuando esté completa, se abrirá una pequeña ventana que le pedirá que genere un certificado de revocación. Es importante tener este certificado de revocación ya que le permite invalidar la clave privada y la pública. Es importante tener en cuenta que simplemente eliminar la clave privada no invalida la clave pública y puede hacer que las personas le envíen correo cifrado que no puede descifrar.

Haga clic en el botón "Generar Certificado".
![image](tool_pgpwin39.png)

Se abrirá una ventana para proporcionarle un lugar para guardar el certificado de revocación. Si bien puede guardar el archivo en su computadora, le recomendamos que lo guarde en una unidad USB que no esté utilizando y que guarde la unidad en un lugar seguro. También recomendamos eliminar el certificado de revocación de la computadora con las claves, solo para evitar la revocación involuntaria.

Aún mejor, guarde este archivo en un disco cifrado separado. Elija la ubicación donde está guardando este archivo y haga clic en el botón "Guardar".
![image](tool_pgpwin40.png)

Ahora Enigmail le dará más información sobre cómo guardar el archivo de certificado de revocación nuevamente. Haga clic en el botón "Aceptar".
![image](tool_pgpwin41.png)

Finalmente, ha terminado con la generación de la clave privada y la clave pública. Haga clic en el botón "Finalizar".
![image](tool_pgpwin42.png)

### 5 Pasos opcionales

### 5.1 Mostrar identificadores de clave largos

Los siguientes pasos son completamente opcionales, pero pueden ser útiles al usar OpenPGP y Enigmail. En pocas palabras, la identificación de la clave es una pequeña parte de la huella digital. Cuando se trata de verificar que una clave pública pertenece a una persona en particular, la huella digital es la mejor manera. Cambiar la pantalla predeterminada hace que sea más fácil leer las huellas digitales de los certificados que conoce. Haga clic en el botón de configuración, luego en la opción Enigmail, luego en Gestión de Claves.
![image](tool_pgpwin43.png)

Se abrirá una ventana que muestra dos columnas: Nombre e ID de clave.
!![image](tool_pgpwin43.png)

En el extremo derecho hay un pequeño botón. Haga clic en ese botón para configurar las columnas. Desmarque la opción ID de clave y haga clic en la opción Huella digital.
![image](tool_pgpwin44.png)

Ahora las columnas se verán así:
[image](tool_pgpwin45.png)

Ahora está configurado para enviar y recibir correo electrónico regular y encriptado. A continuación, pasará por los pasos para encontrar a las personas con las que intercambiar correo cifrado.

### 5.2 Utilizando PGP/MIME

Hay un último paso de configuración opcional para habilitar PGP/MIME que facilita el envío de archivos adjuntos encriptados y firmados.

Puede encontrar esta configuración haciendo clic en el botón Menú, desplazándose sobre Opciones y luego haciendo clic en Configuración de la Cuenta. Se abrirá la ventana Configuración de la Cuenta.
![image](tool_pgpwin46.png)

Cuando se abra la ventana Configuración de la cuenta, haga clic en la pestaña Seguridad de OpenPGP y luego haga clic en la casilla junto a Usar PGP/MIME de forma predeterminada. A continuación, haga clic en el botón Aceptar. Ahora Enigmail usará PGP/MIME por defecto.
![image](tool_pgpwin47.png)

**El uso de PGP no encripta completamente su correo electrónico para que el remitente y la información recibida estén encriptados. Cifrar la información del remitente y el destinatario interrumpiría el correo electrónico. El uso de Thunderbird con el complemento Enigmail le brinda una manera fácil de cifrar y descifrar el contenido de su correo electrónico.**

### 6.1 Hacer saber a los demás que está usando PGP

Ahora que tiene PGP, desea que otros sepan que lo está utilizando para que también puedan enviarle mensajes cifrados utilizando PGP.

Veamos tres formas diferentes en que puede hacer saber a la gente que está utilizando PGP.

**a) Informe a la gente que está usando PGP con un correo electrónico**

Puede enviar fácilmente su clave pública a otra persona enviándole una copia como un archivo adjunto.

Haga clic en el botón "Escribir" en Mozilla Thunderbird.
![image](tool_pgpwin48.png)

Ingrese una dirección y un asunto, tal vez algo como "mi clave pública", haga clic en el menú Enigmail y seleccione la opción "Adjuntar mi Clave Pública".
![image](tool_pgpwin49.png)

Puede enviar el correo electrónico y el destinatario podrá descargar y utilizar la clave pública que envió.

Si se utiliza este método, es una buena idea que el destinatario verifique la huella digital de su clave pública en alguna otra forma de comunicación, en caso de que el correo electrónico ya esté siendo interceptado y manipulado.

**b) Informe a la gente que está utilizando PGP en tu sitio web**

Además de informar a las personas por correo electrónico, puede publicar su clave pública en su sitio web. La forma más fácil es subir el archivo y vincularlo. Esta guía no explicará cómo hacer esas cosas, pero debe saber cómo exportar el certificado como un archivo para usar en el futuro.

Haga clic en el botón de configuración, luego en la opción Enigmail, luego en Gestión de Claves.

Resalte el certificado en negrita, luego haga clic derecho para abrir el menú y seleccione Exportar claves a archivo.
![image](tool_pgpwin50.png)

Una pequeña ventana aparecerá con tres botones. Haga clic en el botón "Exportar Solo Claves Públicas".
![image](tool_pgpwin51.png)

Asegúrate de no hacer clic en el botón "Exportar Claves Secretas" porque exportar la clave secreta podría permitir que otras personas suplantaran su identidad si pueden adivinar su contraseña.

Ahora se abrirá una ventana para que pueda guardar el archivo. Para que sea más fácil encontrarlo en el futuro, guarde el archivo en la carpeta Documentos.
![image](tool_pgpwin52.png)

Ahora puede usar este archivo como desee.

**c) Suba a un servidor de claves**

Los servidores de claves facilitan la búsqueda y descarga de claves públicas. La mayoría de los servidores de claves modernos se están sincronizando, lo que significa que una clave pública cargada en un servidor finalmente llegará a todos los servidores.

Aunque cargar su clave pública en un servidor de claves podría ser una manera conveniente de informarle a las personas que tiene un certificado PGP público, debe saber que debido a la naturaleza de cómo funcionan los servidores de claves, no hay forma de eliminar las claves públicas una vez que se cargan. , solo puede marcarlas como revocadas.

**Antes de cargar su clave pública en un servidor de claves, es bueno tomarse un momento para considerar si desea que todo el mundo sepa que tiene una clave pública sin la capacidad de eliminar esta información más adelante.**

Si elige cargar su clave pública a los servidores de claves, volverá a la ventana Gestión de Claves de Enigmail.

Haga clic en el elemento del menú Servidor de Claves y seleccione la opción Cargar Claves Públicas.
![image](tool_pgpwin53.png)

### 6.2 Encontrar a otras personas que están usando PGP

**a) Obtención de una clave pública por correo electrónico**

Puede obtener una clave pública que se le envíe como adjunto en un correo electrónico.
![image](tool_pgpwin54.png)

Haga doble clic en el nuevo mensaje y se abrirá una nueva pestaña. Observe el archivo adjunto en la parte inferior de la ventana. Haga clic con el botón derecho en el archivo adjunto y seleccione "Importar Clave OpenPGP". Se abrirá una pequeña ventana que le dará los resultados de la importación. Haga clic en el botón Aceptar.
![image](tool_pgpwin55.png)

Si vuelve a abrir la ventana de administración de claves de Enigmail, puede verificar el resultado. Su clave PGP está en negrita porque tiene tanto la clave privada como la pública. La clave pública que acaba de importar no está en negrita porque no contiene la clave privada.
![image](tool_pgpwin56.png)

**b) Obtención de una clave pública como archivo**

Es posible que obtenga una clave pública descargándola de un sitio web o que alguien la haya enviado a través del software de chat. En un caso como este, asumirá que descargó el archivo a la carpeta de Descargas.

Abra el Enigmail Key Manager y haga clic en el menú "Archivo". Seleccione "Importar Claves Desde Archivo".
![image](tool_pgpwin57.png)

La clave pública puede tener terminaciones de nombre de archivo muy diferentes, como .asc, .pgp o .gpg. Seleccione el archivo y haga clic en el botón "Abrir".
![image](tool_pgpwin58.png)

Se abrirá una pequeña ventana que le dará los resultados de la importación. Haga clic en el botón "Aceptar".
![image](tool_pgpwin59.png)

**c) Obtención de una clave pública de un servidor de claves**

Los servidores de claves pueden ser una forma muy útil de obtener claves públicas. Intente buscar una clave pública. Abra el administrador de claves, luego haga clic en el menú "Servidor de Claves" y seleccione "Buscar Claves".
![image](tool_pgpwin60.png)

Aparecerá una pequeña ventana con un campo de búsqueda. Puede buscar por una dirección de correo electrónico completa, una dirección de correo electrónico parcial o un nombre. En este caso, buscará certificados que contengan "eff.org".
![image](tool_pgpwin61.png)

Una ventana más grande aparecerá con muchas opciones. Si se desplaza hacia abajo, notará que algunos certificados están en cursiva y en gris. Estos son certificados que han sido revocados o caducados por su cuenta.
![image](tool_pgpwin62.png)

Tomemos las claves públicas de Danny O'Brien, por ejemplo, tiene un certificado vencido o revocado y un certificado válido. Seleccione el certificado válido haciendo clic en el cuadro de la izquierda y luego presione el botón OK.
![image](tool_pgpwin63.png)

En algunos casos, una persona puede tener más de un certificado, todos los cuales parecen ser válidos. Tenga en cuenta que es posible que cualquier persona cargue un certificado público para otra persona, y que una de estas claves no pertenezca a la persona que posee la dirección de correo electrónico asociada. En este caso, la verificación de la huella digital es extremadamente importante.

Aparecerá una pequeña ventana de notificación que le informará si tuvo éxito:
![image](tool_pgpwin64.png)

El Enigmail Key Manager ahora le mostrará los certificados agregados:
![image](tool_pgpwin65.png)

### 7.1 Enviando correo cifrado PGP

Ahora enviará su primer correo electrónico cifrado a un destinatario. En la ventana principal de Mozilla Thunderbird, haga clic en el botón "Escribir". Una nueva ventana se abrirá.
![image](tool_pgpwin66.png)

Escriba su mensaje e ingrese un destinatario. Para esta prueba, seleccione un destinatario cuya clave pública ya tenga. Enigmail lo detectará y automáticamente cifrará el correo electrónico.
![image](tool_pgpwin67.png)

_Tenga en cuenta que la línea de asunto no estará encriptada, así que elija algo inocuo, como "hola"._

Cuando haga clic en el botón "Enviar", se abrirá una ventana para ingresar la contraseña a su Clave PGP. ¡Recuerde que esto es diferente de su contraseña de correo electrónico!

Ingrese su contraseña, luego haga clic en el botón "OK" y su correo electrónico será cifrado y enviado.
![image](tool_pgpwin68.png)

El cuerpo del correo electrónico fue encriptado y transformado. Por ejemplo este texto:
![image](tool_pgpwin69.png)

Será transformado en:
![image](tool_pgpwin70.png)

### 7.2 Recepción de correo cifrado PGP

Revisemos lo que sucede cuando recibe un correo electrónico cifrado. Tenga en cuenta que Mozilla Thunderbird le está avisando que tiene correo nuevo. Haga clic en el mensaje.
![image](tool_pgpwin71.png)

Se abrirá una pequeña ventana que le pedirá la contraseña de la clave PGP. Recuerde: No ingrese su contraseña de correo electrónico. Haga clic en el botón "Aceptar".
![image](tool_pgpwin72.png)

Ahora el mensaje se mostrará descifrado.
![image](tool_pgpwin73.png)

### 8 Revocando la clave PGP

**a) Revocar su clave PGP a través de la interfaz de Enigmail**

Las claves PGP generadas por Enigmail caducan automáticamente después de cinco años. Por lo tanto, si pierde todos sus archivos, puede esperar que la gente sepa pedirle otra clave una vez que la clave haya caducado.

Es posible que tenga una buena razón para deshabilitar la clave PGP antes de que caduque. Quizás quiera generar una clave PGP nueva y más fuerte. La forma más fácil de revocar su propia clave PGP en Enigmail es a través del Enigmail Key Manager.
![image](tool_pgpwin74.png)

Haga clic con el botón derecho en su clave PGP (está en negrita) y seleccione la opción "Revocar Clave".
![image](tool_pgpwin75.png)

Se abrirá una ventana que le permitirá saber qué sucede y solicitará su confirmación. Haga clic en el botón "Revocar Clave".
![image](tool_pgpwin76.png)

Se abre la ventana de contraseña, ingrese su contraseña para la clave PGP y haga clic en el botón "Aceptar".
![image](tool_pgpwin77.png)

Ahora se abrirá una nueva ventana que le permitirá saber que tuvo éxito. Haga clic en el botón "Aceptar".
![image](tool_pgpwin78.png)

Cuando regrese a la ventana de Administración de claves de Enigmail, notará un cambio en su clave PGP. Ahora está en gris y en cursiva.
![image](tool_pgpwin79.png)

**b) Revocar una clave PGP con un certificado de revocación**

Como se mencionó anteriormente, las claves PGP generadas por Enigmail caducan automáticamente después de cinco años. Entonces, si pierde todos sus archivos, puede estar seguro de que la gente sabrá que le pedirá otra clave una vez que la clave haya caducado.

Como mencionamos anteriormente, es posible que tenga una buena razón para deshabilitar la clave PGP antes de que caduque.

Del mismo modo, otros pueden tener buenas razones para revocar una clave existente.

Es posible que amigos le envíen certificados de revocación como aviso de que desean revocar su clave.

En la sección anterior, es posible que haya notado que Enigmail genera e importa un certificado de revocación internamente cuando utiliza el Gestor de Claves de Enigmail para revocar una clave. Como ya tiene un certificado de revocación, usará el que generó anteriormente para revocar su propia clave.

Comience con el Gestor de Claves de Enigmail, haga clic en el menú "Archivo" y seleccione "Importar Claves desde Archivo".
![image](tool_pgpwin80.png)

Se abrirá una ventana para que pueda seleccionar el certificado de revocación. Haga clic en el archivo y haga clic en el botón "Abrir".
![image](tool_pgpwin81.png)

Recibirá una notificación de que el certificado se importó correctamente y que se revocó una clave. Haga clic en el botón "Aceptar".
![image](tool_pgpwin82.png)

Una vez que haga clic en el botón "Aceptar", volverá al Gestor de Claves de Enigmail y verá que el certificado revocado está en gris y en cursiva.
![image](tool_pgpwin83.png)

Si la clave que revocó es la suya y cargó previamente su clave pública a los servidores de claves, querrá volver a cargar la clave ahora revocada en los servidores de claves, para que otros vean que ya no la usen.

Ahora que tiene todas las herramientas adecuadas, intente enviar su propio correo electrónico cifrado con PGP.