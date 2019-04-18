---
index: 10
title: PGP para Linux
---
# GUÍA DE HERRAMIENTAS PGP PARA LINUX

## Guía de Herramientas de PGP para Linux
Correo cifrado para Linux

**Lección para leer:
- [Correo Electrónico](umbrella://communications/email)**
**Requisitos de la computadora:** Una conexión a Internet, una computadora con Linux, una cuenta de correo electrónico
**Versión utilizada en esta guía:**
- Linux: Debian 7.0 ("Wheezy")
- Mozilla Thunderbird 24.8.1
- Enigmail 1.6
- GPG4Win 1.4.18
**Licencia:** Software Libre; mezcla de licencias de software libre
**Nivel:** Experto
**Otras lecturas:** [https://www.gnupg.org/documentation/guides.html](https://www.gnupg.org/documentation/guides.html)
**Tiempo requerido:** 30-60 minutos.

**Usar PGP le dará:**
- La capacidad de proteger sus comunicaciones por correo electrónico para que nadie las lea, excepto sus destinatarios.
- La capacidad de demostrar que un correo electrónico provino de una persona en particular, en lugar de ser un mensaje falso enviado por otro remitente (de otra manera es muy fácil que el correo electrónico sea fabricado). Ambas son defensas importantes si se lo busca por vigilancia o información errónea.

**Nota:** Si le preocupa que el correo electrónico encriptado con PGP no sea seguro después de que se informaron las vulnerabilidades en mayo de 2018, lea la sección Efail de nuestra lección avanzada de [correo electrónico](umbrella://communications/email).

### 1.0 Antes de comenzar

Para usar Pretty Good Privacy (PGP), deberá instalar algún software adicional que funcione con su programa de correo electrónico actual. También deberá crear una clave privada, que mantendrá privada. La clave privada es lo que usará para descifrar los correos electrónicos que se le envíen y para firmar digitalmente los correos electrónicos que envíe para mostrar que realmente provienen de usted. Finalmente, aprenderá cómo distribuir su clave pública, una pequeña porción de información que otros deberán conocer antes de que puedan enviarle correo cifrado y que puedan usar para verificar los correos electrónicos que envíe.

Esta guía le mostrará cómo usar PGP con un sistema operativo estilo Linux usando Mozilla Thunderbird, un popular cliente de correo electrónico gráfico de código abierto.

Actualmente no puede usar PGP directamente con un servicio de correo electrónico web como Gmail, Hotmail, Yahoo! Correo, o Outlook Live. Todavía puede utilizar su dirección de correo web; solo tendrá que configurarla con el programa Thunderbird en su computadora.

**Tenga en cuenta que ambos extremos de la conversación de correo electrónico deben utilizar un software compatible con PGP para que funcione.**

La gente normalmente usará esto solo en sus dispositivos personales, no en dispositivos compartidos. Afortunadamente, PGP está disponible para la mayoría de las computadoras de escritorio y dispositivos móviles, y puede apuntarlas a estas guías para ayudarles a configurar su propia versión.

### 2.0 Instalando Thunderbird, GnuPG y Enigmail

PGP es un estándar abierto, lo que significa que más de una pieza de software puede usarlo. El software que vamos a utilizar para PGP se llama GnuPG. También agregaremos un complemento a Thunderbird llamado Enigmail, que le permite utilizar GnuPGP desde Thunderbird. Las siguientes instrucciones requieren cierta comodidad con la línea de comandos.

Si está usando una distribución basada en Red Hat como Red Hat o Fedora Core, abra un terminal y ejecute estos comandos:

_sudo yum install gnupg thunderbird thunderbird-enigmail_

Si está utilizando una distribución basada en Ubuntu como Ubuntu o Linux Mint, abra un terminal y escriba estos comandos para asegurarse de que tiene instalado el software correcto:

_sudo apt-get install gnupg thunderbird enigmail_

Si está utilizando la distribución Debian, encontrará que Thunderbird se llama "Icedove". Al igual que Debian en general, esto es por razones totalmente razonables pero algo oscuras. Aparte del nombre, es exactamente el mismo programa: no volveremos a mencionar Icedove, pero puedes reemplazar "Thunderbird" por Icedove en el resto de esta guía, y todo debería seguir funcionando.

Use este comando en la Terminal para instalarlo:

_sudo apt-get install gnupg icedove enigmail_

### 2.1 Configurando Thunderbird

Ahora que ha instalado Thunderbird, ábralo como lo haría con otra aplicación en su máquina (puede elegirlo de una lista de aplicaciones en un menú, o escribir su nombre en una búsqueda de aplicaciones). Verá aparecer el primer asistente de ejecución.
![image](tool_pgplin1.png)

Para configurar su dirección de correo electrónico existente, haga clic en "Omitir esto y usar mi correo electrónico existente" y luego ingrese su nombre, dirección de correo electrónico y la contraseña de su cuenta de correo electrónico.
![image](tool_pgplin2.png)

Si utiliza un servicio de correo electrónico gratuito popular como Gmail, Thunderbird debería poder detectar automáticamente su configuración de correo electrónico cuando haga clic en "Continuar".

**Si usa la autenticación de dos factores con Google (y, dependiendo del modelo de amenaza, ¡probablemente debería!) No puede usar su contraseña de Gmail estándar con Thunderbird. En su lugar, deberá crear una nueva contraseña específica de la aplicación para que Thunderbird acceda a su cuenta de Gmail. Consulte [la propia guía de Google] (https://support.google.com/mail/answer/1173270?hl=es) para hacer esto.**
![image](tool_pgplin3.png)

Si no es así, es posible que deba configurar manualmente sus configuraciones IMAP y SMTP. Si no sabe cómo hacerlo, hable con su proveedor de correo electrónico o pregúntele a un técnico que esté familiarizado con su proveedor de correo electrónico (por lo tanto, una persona de TI en el trabajo o un amigo técnico que use el mismo ISP que usted; no necesita saber cómo usar PGP, pero puede preguntarles "¿Conoce la configuración de IMAP y SMTP para mi dirección de correo electrónico?").

### 2.2 Configurando Enigmail

Enigmail es un complemento para Thunderbird que cifra y descifra los correos electrónicos codificados con PGP, y facilita un poco más el manejo de las claves públicas y privadas. Si tiene la última versión de Enigmail, se le presentará con el Asistente de Configuración de Enigmail.
![image](tool_pgplin4.png)

Si no lo ve, puede usar esta opción de menú de Thunderbird para que aparezca. Haga clic en las tres líneas horizontales (el "menú hamburguesa") a la derecha de la ventana de Thunderbird.
![image](tool_pgplin5.png)

Esta es la primera opción que Enigmail le ofrece: tres opciones para manejar cuándo cifre su correo.
![image](tool_pgplin6.png)

La opción predeterminada es cifrar los correos electrónicos si tiene la "clave pública" de otra persona, Enigmail cifrará el correo electrónico que envíe pero dejará los correos electrónicos sin cifrar si aún no tiene la clave pública del destinatario. También tiene la opción de cifrar correos electrónicos todo el tiempo a todas las personas con claves PGP, lo que significa que tendrá que encontrar las claves públicas para las personas para las que aún no las tiene, o desactivar el cifrado automático por completo y solo usar PGP cuando sea dirigido

No sabemos cuál es la opción adecuada para usted, pero creemos que la opción "Encriptación automática conveniente" es una buena opción. Si tiene dudas, elija "No cifrar mis mensajes de forma predeterminada".

Haga clic en el botón "Siguiente".
![image](tool_pgplin6.png)

Ahora tiene una opción para firmar digitalmente todos los correos electrónicos salientes. Firmar su correo electrónico con PGP le permite al destinatario verificar que usted envió el mensaje y que su contenido no fue alterado. Haga clic en el botón "Firmar mis mensajes de manera predeterminada" para activar esta función.

La desventaja de hacer esto, sin embargo, es que también puede marcar a cualquier persona a la que le envíe correo que use PGP. [En algunas partes del mundo] (www.cryptolaw.org/) (incluyendo China, Irán, Bielorrusia y algunos estados del Medio Oriente) el uso de cifrado sin licencia, incluso para uso personal, es ilegal, por lo que es posible que tenga muy buenas razones para no dejar que otros sepan que usa PGP.

Haga clic en el botón "Siguiente".

Ahora verá una opción para que Enigmail realice algunos cambios en la configuración de Mozilla Thunderbird.
![image](tool_pgplin7.png)

Si hace clic en el botón Detalles, puede revisar cuáles son esos cambios.

Las siguientes opciones se pueden desmarcar (volver a habilitar), para una transición más fluida, si usa PGP/Mime de forma predeterminada (lo configuraremos más adelante):
- Deshabilitar texto fluido
- Ver el cuerpo del mensaje como texto plano
- No redacte mensajes HTML

La opción final evita posibles problemas en el cifrado y descifrado de su correo electrónico. Tenga en cuenta que al seleccionar este cuadro se eliminará la posibilidad de enviar texto en negrita, subrayado o coloreado. Después de revisar los cambios, haga clic en el botón "Aceptar".

Ahora comenzará a crear su clave privada y pública.

### 2.3 Creando una clave pública y una clave privada

La instalación y configuración del complemento Enigmail está completa. Ahora tendrás la opción de crear tu par de claves pública y privada. Esto supone que no ha creado una clave privada anteriormente.
![image](tool_pgplin8.png)

Haga clic en el botón "Siguiente".

A menos que ya haya configurado más de una cuenta de correo electrónico, Enigmail elegirá la cuenta de correo electrónico que ya haya configurado. Lo primero que deberá hacer es crear una frase de contraseña segura para su clave privada. Consulte la **[Lección de contraseñas](umbrella://information/passwords)** para obtener más información sobre cómo hacerlo.

Enigmail mostrará información sobre su clave privada, así como los ajustes de configuración. Recomendamos crear claves de longitud de 4096 bits. Haga clic en el botón "Siguiente".
![image](tool_pgplin9.png)

**Su clave caducará en un momento determinado; cuando eso suceda, otras personas dejarán de usarla por completo para nuevos correos electrónicos, aunque es posible que no reciba ninguna advertencia o explicación sobre el motivo. Por lo tanto, es posible que desee marcar su calendario y prestar atención a este problema aproximadamente un mes antes de la fecha de vencimiento.**

Es posible extender la vida útil de una clave existente dándole una nueva fecha de vencimiento posterior, o es posible reemplazarla con una nueva clave creando una nueva desde cero. Es posible que ambos procesos requieran contactar a las personas que le envían correos electrónicos y asegurarse de que obtengan la clave actualizada; El software actual no es muy bueno para automatizar esto. Así que haz un recordatorio para ti mismo; Si piensa que no podrá administrarlo, puede considerar configurar la clave para que nunca caduque, aunque en ese caso otras personas podrían intentar usarla cuando se comuniquen con usted en el futuro, incluso si ya no lo hace. tener la clave privada o ya no usar PGP.

Enigmail generará la clave y cuando esté completa, se abrirá una pequeña ventana que le pedirá que genere un certificado de revocación. Es importante tener este certificado de revocación ya que le permite invalidar la clave privada y la pública. Es importante tener en cuenta que simplemente eliminar la clave privada no invalida la clave pública y puede hacer que las personas le envíen correo cifrado que no puede descifrar.
![image](tool_pgplin10.png)

Haga clic en el botón "Generar Certificado".

Se abrirá una ventana para proporcionarle un lugar para guardar el certificado de revocación. Si bien puede guardar el archivo en su computadora, le recomendamos que lo guarde en una unidad USB que no esté utilizando y que guarde la unidad en un lugar seguro. También recomendamos eliminar el certificado de revocación de la computadora con las claves, solo para evitar la revocación involuntaria.

Aún mejor, guarde este archivo en un disco cifrado separado. Elija la ubicación donde está guardando este archivo y haga clic en el botón "Guardar".

Ahora Enigmail le dará más información sobre cómo guardar el archivo de certificado de revocación nuevamente. Haga clic en el botón "Aceptar".

Finalmente, ha terminado con la generación de la clave privada y la clave pública. Haga clic en el botón "Finalizar".

### 2.4 Pasos opcionales

### 2.4.1 Mostrar identificadores de clave largos

Los siguientes pasos son completamente opcionales, pero pueden ser útiles al usar OpenPGP y Enigmail. En pocas palabras, la identificación de la clave es una pequeña parte de la huella digital. Cuando se trata de verificar que una clave pública pertenece a una persona en particular, la huella digital es la mejor manera. Cambiar la pantalla predeterminada hace que sea más fácil leer las huellas digitales de los certificados que conoce. Haga clic en el botón de configuración, luego en la opción Enigmail, luego en Administración de claves.
![image](tool_pgplin11.png)

Se abrirá una ventana que muestra dos columnas: Nombre e ID de Clave.
![image](tool_pgplin12.png)

En el extremo derecho hay un pequeño botón. Haga clic en ese botón para configurar las columnas. Desmarque la opción ID de clave y haga clic en la opción Huella digital.
![image](tool_pgplin13.png)

Ahora cambie el ancho de la columna de Huella Digital moviendo el mouse hacia las líneas entre los encabezados de cada columna (es decir, justo a la izquierda del encabezado "ID de Clave" en la parte superior de la lista de claves), y arrastre la línea hasta el izquierda. Siga moviéndose hacia la izquierda hasta que pueda ver toda la identificación de la clave, de esta manera:

Ahora las columnas se verán así:
![image](tool_pgplin14.png)

Ahora está configurado para enviar y recibir correo electrónico regular y encriptado. A continuación, pasará por los pasos para encontrar a las personas con las que intercambiar correo cifrado.

**El uso de PGP no encripta completamente su correo electrónico como para que la información del remitente y el destinatario está encriptada. Cifrar la información del remitente y el destinatario interrumpiría el correo electrónico. El uso de Thunderbird con el complemento Enigmail le brinda una manera fácil de cifrar y descifrar el contenido de su correo electrónico.**

### 3.0 Informar a otros que está usando PGP

**a) Informar a la gente que está usando PGP con un correo electrónico**

Puede enviar fácilmente su clave pública a otra persona enviándole una copia como un archivo adjunto.

Haga clic en el botón "Escribir" en Mozilla Thunderbird.

Ingrese una dirección y un asunto, tal vez algo como "mi clave pública", haga clic en el menú Enigmail y seleccione la opción "Adjuntar Mi Clave Pública".
![image](tool_pgplin15.png)

Ahora puede enviar el correo electrónico y el destinatario podrá descargar y utilizar la clave pública que envió.

**Si se usa este método, es una buena idea que el destinatario verifique la huella digital de su clave pública en alguna otra forma de comunicación, en caso de que el correo electrónico ya esté siendo interceptado y manipulado.**

**b) Que la gente sepa que está utilizando PGP en su sitio web**

Además de informar a las personas por correo electrónico, puede publicar su clave pública en su sitio web. La forma más fácil es subir el archivo y vincularlo. Esta guía no explicará cómo hacer esas cosas, pero debe saber cómo exportar el certificado como un archivo para usar en el futuro.

Haga clic en el botón de configuración, luego en la opción Enigmail, luego en Administración de Claves.

Resalte su certificado en negrita, luego haga clic con el botón derecho para abrir el menú y seleccione Exportar claves a archivo.
![image](tool_pgplin16.png)

Una pequeña ventana aparecerá con tres botones. Haga clic en el botón "Exportar Solo Claves Públicas".
![image](tool_pgplin17.png)


**Asegúrese de no hacer clic en el botón "Exportar Claves Secretas" porque exportar la clave secreta podría permitir que otras personas se hagan pasar por usted si pueden adivinar su contraseña.**

Ahora se abrirá una ventana para que pueda guardar el archivo. Para que sea más fácil encontrarlo en el futuro, guarde el archivo en la carpeta Documentos.

Ahora puede usar este archivo como desee.

**c) Subiendo a un servidor de claves**

Los servidores de claves facilitan la búsqueda y descarga de claves públicas. La mayoría de los servidores de claves modernos se están sincronizando, lo que significa que una clave pública cargada en un servidor finalmente llegará a todos los servidores.

Aunque cargar su clave pública en un servidor de claves podría ser una manera conveniente de informarle a las personas que tiene un certificado PGP público, debe saber que debido a la naturaleza de cómo funcionan los servidores de claves, no hay forma de eliminar las claves públicas una vez que se cargan. , solo puede marcarlas como revocadas.

**Antes de cargar su clave pública en un servidor de claves, es bueno tomarse un momento para considerar si desea que todo el mundo sepa que tiene una clave pública sin la capacidad de eliminar esta información más adelante.**

Si elige cargar su clave pública a los servidores de llaves, volverá a la ventana Gestión de Claves de Enigmail.

Haga clic en el elemento del menú Servidor de claves y seleccione la opción Cargar Claves Públicas.
![image](tool_pgplin18.png)

### 3.1 Encontrar a otras personas que están usando PGP

**a) Obtención de una clave pública por correo electrónico**

Es posible que reciba una clave pública que se le envíe como un archivo adjunto de correo electrónico.
[image](tool_pgplin19.png)

Observe el archivo adjunto en la parte inferior de la ventana. Haga clic con el botón derecho en el archivo adjunto y seleccione "Importar clave OpenPGP". Se abrirá una pequeña ventana que le dará los resultados de la importación. Haga clic en el botón Aceptar.

Si vuelve a abrir la ventana de administración de claves de Enigmail, puede verificar el resultado. Su clave PGP está en negrita porque tiene tanto la clave privada como la pública. La clave pública que acaba de importar no está en negrita porque no contiene la clave privada.
![image](tool_pgplin20.png)

**b) Obtener una clave pública como archivo**

Es posible que obtenga una clave pública descargándola de un sitio web o que alguien la haya enviado a través del software de chat. En un caso como este, asumirá que descargó el archivo a la carpeta de Descargas.

Abra el Gestor de Claves de Enigmail y haga clic en el menú "Archivo". Seleccione "Importar Claves desde Archivo".

La clave pública puede tener terminaciones de nombre de archivo muy diferentes, como .asc, .pgp o .gpg. Seleccione el archivo y haga clic en el botón "Abrir". Se abrirá una pequeña ventana que le dará los resultados de la importación. Haga clic en el botón "Aceptar".

**c) Obtener una clave pública de un servidor de claves**

Los servidores de claves pueden ser una forma muy útil de obtener claves públicas. Intenta buscar una clave pública. Abra el administrador de claves, luego haga clic en el menú "Servidor de Claves" y seleccione "Buscar Claves".
![image](tool_pgplin21.png)

Aparecerá una pequeña ventana con un campo de búsqueda. Puede buscar por una dirección de correo electrónico completa, una dirección de correo electrónico parcial o un nombre. En este caso, buscará certificados que contengan "eff.org".
![image](tool_pgplin22.png)

Una ventana más grande aparecerá con muchas opciones. Si se desplaza hacia abajo, notará que algunos certificados están en cursiva y en gris. Estos son certificados que han sido revocados o caducados por su cuenta.
![image](tool_pgplin23.png)

Tomemos las claves públicas de Danny O'Brien, por ejemplo, tiene un certificado vencido o revocado y un certificado válido. Seleccione el certificado válido haciendo clic en el cuadro de la izquierda y luego presione el botón OK.
![image](tool_pgplin24.png)

En algunos casos, una persona puede tener más de un certificado, todos los cuales parecen ser válidos. Tenga en cuenta que es posible que cualquier persona cargue un certificado público para otra persona y que una de estas claves no pertenezca a la persona que posee la dirección de correo electrónico asociada. En este caso, verificar la huella digital es extremadamente importante.

Aparecerá una pequeña ventana de notificación que le informará si tuvo éxito, y el Enigmail Key Manager ahora le mostrará los certificados agregados:
![image](tool_pgplin25.png)

### 4.0 Enviando correo cifrado PGP

Ahora enviará su primer correo electrónico cifrado a un destinatario. En la ventana principal de Mozilla Thunderbird, haga clic en el botón "Escribir". Una nueva ventana se abrirá.

Escriba su mensaje e ingrese un destinatario. Para esta prueba, seleccione un destinatario cuya clave pública ya tenga. Enigmail lo detectará y automáticamente cifrará el correo electrónico (se puede decir que se cifrará con la llave dorada en la parte inferior derecha del correo electrónico).
![image](tool_pgplin26.png)

**Tenga en cuenta que la línea de asunto no estará encriptada, así que elija algo inocuo, como "hola".**

Cuando haga clic en el botón "Enviar", se le abrirá una ventana para ingresar la contraseña a su Clave PGP. Recuerde que esto es diferente de su contraseña de correo electrónico!

Ingrese su contraseña, luego haga clic en el botón "OK" y su correo electrónico será cifrado y enviado.

El cuerpo del correo electrónico fue encriptado y transformado. Por ejemplo, nuestro texto anterior, se convirtió a esto:
![image](tool_pgplin27.png)

### 4.1 Recepción de correo cifrado PGP

Revisemos lo que sucede cuando recibe un correo electrónico cifrado. Primero, haga clic en el mensaje.

Se abrirá una pequeña ventana que le pedirá la contraseña de la clave PGP. Recuerde: No ingrese su contraseña de correo electrónico. Haga clic en el botón "Aceptar".
![image](tool_pgplin28.png)

Ahora el mensaje se mostrará descifrado.
![image](tool_pgplin29.png)

### 5.0 revocando la clave PGP

**a) Revocar su clave PGP a través de la interfaz de Enigmail**

Las claves PGP generadas por Enigmail caducan automáticamente después de cinco años. Por lo tanto, si pierde todos sus archivos, puede esperar que la gente sepa que debe pedirle otra clave una vez que la clave haya caducado.

Es posible que tenga una buena razón para deshabilitar la clave PGP antes de que caduque. Quizás quiera generar una clave PGP nueva y más robusta. La forma más fácil de revocar su propia clave PGP en Enigmail es a través del Gestor de Claves de Enigmail. Haga clic con el botón derecho en su clave PGP (está en negrita) y seleccione la opción "Revocar Clave".
![image](tool_pgplin30.png)

Se abrirá una ventana que le permitirá saber qué sucede y solicitará su confirmación. Haga clic en el botón "Revocar Clave".
![image](tool_pgplin31.png)

Se abre la ventana de contraseña, ingrese su contraseña para la clave PGP y haga clic en el botón "Aceptar".

Ahora se abrirá una nueva ventana que le permitirá saber que tuvo éxito. Haga clic en el botón "Aceptar".

Cuando regrese a la ventana Gestor de Claves de Enigmail, notará un cambio en su clave PGP. Ahora está en gris y en cursiva.
![image](tool_pgplin32.png)

**b) Revocar una clave PGP con un certificado de revocación**

Como se mencionó anteriormente, las claves PGP generadas por Enigmail caducan automáticamente después de cinco años. Entonces, si pierde todos sus archivos, puede estar seguro de que la gente sabrá que le pedirá otra clave una vez que la clave haya caducado.

Como mencionamos anteriormente, es posible que tenga una buena razón para deshabilitar la clave PGP antes de que caduque.

Del mismo modo, otros pueden tener buenas razones para revocar una clave existente.

Es posible que los amigos le envíen certificados de revocación como aviso de que desean revocar su clave.

En la sección anterior, es posible que haya notado que Enigmail genera e importa un certificado de revocación internamente cuando utiliza el Administrador de claves de Enigmail para revocar una clave. Como ya tiene un certificado de revocación, usará el que generó anteriormente para revocar su propia clave.

Comience con el Gestor de Claves de Enigmail, haga clic en el menú "Archivo" y seleccione "Importar Claves desde Archivo".
![image](tool_pgplin33.png)

Se abrirá una ventana para que pueda seleccionar el certificado de revocación. Haga clic en el archivo y haga clic en el botón "Abrir". Recibirá una notificación de que el certificado se importó correctamente y que se revocó una clave. Haga clic en el botón "Aceptar".
![image](tool_pgplin34.png)

Una vez que haga clic en el botón "Aceptar", volverá al Administrador de claves de Enigmail y verá que el certificado revocado está en gris y en cursiva.
![image](tool_pgplin35.png)

Si la clave que revocó es la suya y cargó previamente su clave pública a los servidores de claves, querrá volver a cargar la clave ahora revocada en los servidores de claves, para que otros vean que ya no deben usarla.

Ahora que tiene todas las herramientas adecuadas, intente enviar su propio correo electrónico cifrado con PGP.