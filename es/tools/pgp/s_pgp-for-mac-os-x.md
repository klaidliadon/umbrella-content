---
index: 11
title: PGP para Mac OS
---
# GUÍA DE HERRAMIENTA PGP PARA MAC OS

Correo electrónico cifrado para Mac

**Lección para leer:
- [Email](umbrella://communications/email)**
**Ubicación de Descarga:**
 - [GPG Suite](https://gpgtools.org/)   
- [Mozilla Thunderbird](https://www.mozilla.org/thunderbird/)   
- [Enigmail](https://www.enigmail.net/home/index.php)  
**Requisitos de la computadora:** Una conexión a Internet, una computadora con Mac OS, una cuenta de correo electrónico
**Versión utilizada en esta guía:**
- GPG Suite Beta 4
- Mozilla Thunderbird 31.2.0
- Enigmail 1.7.2
**Licencia:** Software libre; mezcla de licencias de Software Libre
**Nivel:** Avanzado
**Otra lectura:** [http://support.gpgtools.org/](http://support.gpgtools.org/)
**Tiempo requerido:** 30-60 minutos.

**Usar PGP te dará:**
- La capacidad de proteger sus comunicaciones por correo electrónico para que nadie las lea, excepto sus destinatarios.
- La capacidad de demostrar que un correo electrónico provino de una persona en particular, en lugar de ser un mensaje falso enviado por otro remitente (de otra manera es muy fácil que el correo electrónico sea fabricado). Ambas son defensas importantes si se lo busca por vigilancia o información errónea.

**Nota:** Si le preocupa que el correo electrónico encriptado con PGP no sea seguro después de que se informaron las vulnerabilidades en mayo de 2018, lea la sección Efail de nuestra lección avanzada de [email] (umbrella://communications/email).

### 1.0 Antes de Comenzar

Para usar Pretty Good Privacy (PGP), deberá instalar algún software adicional que funcione con su programa de correo electrónico actual. También deberá crear una clave privada, que mantendrá privada. La clave privada es lo que usará para descifrar los correos electrónicos que se le envíen y para firmar digitalmente los correos electrónicos que envíe para mostrar que realmente provienen de usted. Finalmente, aprenderá cómo distribuir su clave pública, una pequeña porción de información que otros deberán conocer antes de que puedan enviarle correo cifrado y que puedan usar para verificar los correos electrónicos que envíe.

Esta guía le mostrará cómo usar PGP con un Mac de Apple (pero no con iPad o iPhone), ya sea con el programa de correo integrado de Mac, o con Mozilla Thunderbird, un popular programa alternativo de correo electrónico.

Actualmente no puede usar PGP directamente con un servicio de correo electrónico web como Gmail, Hotmail, Yahoo! Correo, o Outlook Live. Todavía puede utilizar su dirección de correo web; solo tendrá que configurarlo con el programa Thunderbird en tu computadora.

**Tenga en cuenta que ambos extremos de la conversación de correo electrónico deben utilizar un software compatible con PGP para que funcione.**

La gente normalmente usará esto solo en sus dispositivos personales, no en dispositivos compartidos. Afortunadamente, PGP está disponible para la mayoría de las computadoras de escritorio y dispositivos móviles, y puede apuntarlas a estas guías para ayudarles a configurar su propia versión. Esta guía es para usuarios de Mac.

### 2.0 Instalando GPGTools en su Mac

PGP es un estándar abierto, lo que significa que más de una pieza de software puede usarlo. El software que vamos a usar para PGP se llama GPG Suite, de GPG Tools, ya que funciona en Mac, es gratuito para cualquier persona y es de código abierto: el código fuente subyacente está disponible para que cualquier persona pueda buscar errores. y puertas traseras.

Una vez que se haya instalado GPG Suite, puede configurar sus claves por primera vez y luego habilitar PGP en Apple Mail y, opcionalmente, Thunderbird.

**Paso 1: Instale el programa.**

Primero, vaya a [https://www.gpgtools.org/](https://www.gpgtools.org/) en su navegador y seleccione "Descargar GPG Suite".
![image](tool_pgposx1.png)

Terminará con una imagen de disco en la que puede hacer clic para instalar el software. Si no está acostumbrado a instalar software de terceros en su computadora, consulte a un experto en Mac cercano: este es un paso en el que la mayoría de los técnicos pueden ayudarlo, incluso si no conocen el PGP o el cifrado.
![image](tool_pgposx2.png)

Al hacer clic en instalar le dará una lista de herramientas que se agregarán a su computadora.
![image](tool_pgposx3.png)

**_¿Qué es exactamente lo que estoy instalando aquí?_**

Estas son herramientas que, en su mayoría, funcionarán entre bastidores para que más de un programa en su Mac pueda usar PGP. Piense en ellos como programas que otros programas pueden usar, en lugar de aplicaciones que usará directamente. GPGMail le permite a Apple Mail enviar y leer correos electrónicos PGP, GPG Keychain Access le permite mantener sus claves privadas y públicas de la misma manera que puede guardar otras contraseñas en su Mac.

GPGServices agrega opcionalmente una función a OS X para permitirle usar PGP directamente en programas distintos al correo electrónico (por ejemplo, en un procesador de textos). GPGPreferences es para cambiar la configuración de PGP en las preferencias de Apple. Finalmente, MacGPG2 es la herramienta básica que cualquier programa debe utilizar para realizar el cifrado o la firma.

En octubre de 2014, el equipo de GPG Tools anunció que pronto se cobraría por GPGMail, la parte de su paquete que le permite usar GPG con la aplicación Mail de Apple. Este tutorial trata sobre el uso de GPG con Thunderbird, así que no usa ese componente. Puede usar la parte de costo cero de la suite GPG, como se describe aquí, si lo desea. Esta opción tiene la ventaja adicional de que todas estas herramientas son "software libre", lo que significa que aún se le permite examinar, editar y redistribuir libremente el código fuente subyacente de GPG Mail, por lo que son aún más seguros. Para obtener más información, consulte GPG Tools [Preguntas Frecuentes] (https://gpgtools.org/news.html) sobre su decisión.


Haga clic en "Continuar" para instalar GPG Suite.
![image](tool_pgposx4.png)

Cuando se complete la instalación, abra GPG Keychain (que se encuentra en su carpeta de aplicaciones) si no se abre automáticamente y le pide que genere sus claves PGP después de la instalación. Haga clic en "Nuevo" para generar sus claves PGP.
![image](tool_pgposx5.png)

**Paso 2: Cree su llave PGP**

A veces, cuando instala un nuevo software, su computadora lo acosará con preguntas que no tienen una respuesta obvia, sin darle ningún consejo sobre cómo responder. Éste es uno de esos momentos.

Es importante que dedique un poco de tiempo a pensar en las respuestas que brindará aquí, ya que cambiar los detalles de la clave PGP puede ser difícil más tarde y, si eligió publicar su clave en algún lugar, no podrá anular su publicación. (Todavía existen miles de claves públicas antiguas de la década de 1990, con los nombres y las antiguas direcciones de correo electrónico de las personas que las crearon en ese entonces).

Las claves PGP contienen un nombre y una dirección de correo electrónico que vinculan la clave con usted. La dirección de correo electrónico será una de las formas en que otros pueden descubrir qué clave usar cuando están cifrando un mensaje para usted.

**_¿Cuándo no debo poner mi nombre real o dirección de correo electrónico en mi clave PGP? ¿Cuándo no debería subir mi clave?_**

Para la mayoría de las personas, tiene sentido agregar una dirección de correo electrónico real a su clave y cargarla en los servidores de claves públicos: así es como la gente se corresponde con la clave correcta para usted. Pueden enviarle un correo electrónico directamente, y saber que se cifrará con la clave correcta, y cuando reciban un correo electrónico firmado de usted, la firma digital se marcará con su nombre.

Sin embargo, para algunas personas no tendrá sentido agregar su nombre real a su clave, por ejemplo, si su modelo de amenaza significa que tener su identidad públicamente vinculada a su clave (y la dirección de correo electrónico vinculada) no es una buena idea. Edward Snowden se comunicó con periodistas utilizando PGP y una dirección de correo electrónico anónima antes de revelar su identidad; su llave PGP ciertamente no estaba marcada con su nombre.

**La carga de su clave es una práctica normal, pero puede revelar que está utilizando el cifrado, incluso si no usa su propio nombre. Además, como veremos, otros pueden cargar su clave y asociar su propia clave con ella, lo que implica que usted y ellos tienen una conexión. Eso puede ser dañino si se está comunicando y no quiere que la gente lo sepa. También puede ser problemático si no te estás comunicando, pero tu atacante quiere que la gente piense que estás asociado.**

Aquí hay una guía general: si está pensando en usar un seudónimo en general, use ese seudónimo (y un correo electrónico alternativo) al etiquetar su clave. Si se encuentra en un entorno más peligroso, cuando no quiere que la gente sepa que está usando PGP en absoluto, o sabe con quién se está comunicando, no cargue su clave en los servidores de claves públicos, y asegúrese de que el grupo de personas con las que se está comunicando tampoco debe cargar su clave. Hay otras formas de verificar que las claves no dependen de que estén disponibles en el servidor de claves públicas. Consulte la guía de EFF para [Verificación de Claves] (https://ssd.eff.org/en/module/key-verification#overlay=en/node/37/) para más información.

Haga clic en el cuadro "Cargar clave pública después de la generación" si desea que otros encuentren su clave rápidamente para que puedan enviarle mensajes cifrados. Es como agregar su número de teléfono a un directorio telefónico público: no lo necesita, pero es conveniente para otros.

Antes de generar la clave, expanda "Opciones avanzadas". Puede dejar el comentario en blanco y dejar el tipo de clave "RSA y RSA (predeterminado)". Pero asegúrese de cambiar el campo Longitud a 4096.
![image](tool_pgposx6.png)

**Su clave caducará en un momento determinado; cuando eso suceda, otras personas dejarán de usarlo por completo para nuevos correos electrónicos, aunque es posible que no reciba ninguna advertencia o explicación sobre el motivo. Por lo tanto, es posible que desee marcar su calendario y prestar atención a este problema aproximadamente un mes antes de la fecha de vencimiento.**

Es posible extender la vida útil de una clave existente dándole una nueva fecha de vencimiento posterior, o es posible reemplazarla con una nueva clave creando una nueva desde cero. Es posible que ambos procesos requieran contactar a las personas que le envían correos electrónicos y asegurarse de que obtengan la clave actualizada; El software actual no es muy bueno para automatizar esto. Así que haga un recordatorio para usted mismo; Si piensa que no podrá administrarlo, puede considerar configurar la clave para que nunca caduque, aunque en ese caso otras personas podrían intentar usarla cuando se comuniquen con usted en el futuro, incluso si ya no lo hace. tener la clave privada o ya no usar PGP.

Cuando esté listo, haga clic en el botón "Generar clave".

Su computadora comenzará a generar su clave pública y privada. No debería tomar más de un par de minutos para terminar (toma un tiempo porque para crear sus claves, su computadora necesita reunir números al azar. Piense en ello como en su computadora que lanza un par de dados muchas, muchas, muchas veces.)
![image](tool_pgposx7.png)

Cuando haya terminado de generar su clave, la verá enumerada en GPG Keychain Access. Puede hacer doble clic en su clave para ver información sobre ella, incluida su "huella digital", una forma única de identificar su clave PGP.

Ahora es un buen momento para generar un certificado de revocación. (Un certificado de revocación es un archivo que puede generar y que anuncia que ya no confía en esa clave. La genera cuando aún tiene la clave secreta y la guarda para cualquier desastre futuro). En el futuro, si alguna vez se preocupa de que alguien ha copiado su clave privada, la borra o la pierde accidentalmente, o si olvida su contraseña, puede decirle a todos que ha sido revocada o cancelada, utilizando un certificado de revocación.

Es mejor crear uno ahora, porque necesita la clave privada y la contraseña para crear un certificado de revocación. Si lo deja para más tarde, puede perder uno u otr, y entonces será demasiado tarde. Así que cree un certificado haciendo clic en su clave, seleccionando "Clave" y luego "Crear Certificado de Revocación". Se le pedirá un lugar para guardar el archivo. Es posible que desee guardarlo con una copia de respaldo de la clave (consulte el siguiente paso).

**Paso 3: Copia de seguridad de su clave PGP**

Si pierde el acceso a su clave privada, no podrá descifrar ningún correo PGP entrante o su correo antiguo. Por otro lado, querrá mantener su clave privada lo más segura posible.

Es posible que desee guardar una copia de seguridad en una clave USB, que mantiene oculta de forma segura. Solo la necesitará si pierde su clave original, pero por seguridad querrá mantenerla fuera del alcance de sus potenciales atacantes.

**_¿Se pierde todo si mis atacantes obtienen mi clave privada PGP?_**

¿Qué sucede si le roban su Mac o le quitan la clave de respaldo? ¿Significa eso que sus mensajes PGP son vulnerables? No: si ha elegido una buena frase de contraseña y nadie ha podido saber cuál es, debería estar protegido en su mayor parte. Para estar seguro, es posible que desee revocar su clave anterior y crear una nueva clave PGP. Esto no impedirá que su antigua clave pueda descifrar su antiguo correo electrónico, pero desalentará a otras personas a usar la vieja clave para sus nuevos correos electrónicos.


Para hacer una copia de seguridad de su clave, abra GPG Keychain Access. Seleccione su clave y haga clic en "Exportar" en la barra de herramientas. Coloque su unidad USB en la máquina y selecciónela en la parte "Dónde" del cuadro de diálogo "Guardar como ...". Marque la casilla de verificación "Permitir exportación de clave secreta".

**OPCIÓN A) Configurando Apple Mail**

Cuando abra Apple Mail por primera vez, verá un asistente de primera ejecución que lo ayudará a configurar su dirección de correo electrónico. Complete su nombre, dirección de correo electrónico y contraseña de correo electrónico y haga clic en "Crear".
![image](tool_pgposx8.png)

**Asistente de configuración de la cuenta de correo**

Si utiliza servicios gratuitos de correo electrónico populares como Gmail, Mail debería poder detectar automáticamente su configuración de correo electrónico cuando haga clic en Continuar. Si no es así, es posible que deba configurar manualmente sus configuraciones IMAP y SMTP. Hable con la compañía que usa para el correo electrónico o pregúntele a alguien técnico que esté familiarizado con su proveedor de correo electrónico (por lo tanto, una persona de TI en el trabajo o un amigo técnico que use el mismo ISP que usted. No es necesario que sepan sobre PGP, pero puede preguntarles "¿Puedes configurar Apple Mail para mí?").
![image](tool_pgposx9.png)

**Auto-detección de configuración de cuenta de correo**



Cuando está redactando un mensaje nuevo, hay dos iconos justo debajo del campo Asunto. Hay un candado (cifrar el correo electrónico) y una estrella (firmar digitalmente el correo electrónico). Si el candado está cerrado, significa que este correo electrónico estará encriptado, y si la estrella tiene una marca de verificado, significa que este correo electrónico estará firmado digitalmente.


**Envío de Email Firmado o Cifrado PGP**
![image](tool_pgposx10.png)

Siempre puede firmar su correo electrónico, incluso si el destinatario no utiliza PGP. Debido a que la firma digital de correos electrónicos requiere su clave secreta, Mail abrirá una ventana que le pedirá su contraseña cuando firme por primera vez un correo electrónico.

Solo puede cifrar los correos electrónicos si la persona que está enviando un correo electrónico utiliza PGP y usted tiene la clave pública de esa persona. Si el ícono del candado de encriptación está desbloqueado y atenuado para que no pueda hacer clic en él, esto significa que primero debe importar la clave pública del destinatario. Pídales que se lo envíen o use la aplicación GPG Keychain Access para encontrar la clave desde un servidor de claves público.

Para estar absolutamente seguro, deberá verificar las claves que recibe del servidor de claves o de su colega. Consulte la guía de EFF para [Verificación de Claves](https://ssd.eff.org/en/module/key-verification#overlay=en/node/37/)  para obtener más información.

**OPCIÓN B) Usar PGP con Mozilla Thunderbird**

Este tutorial muestra cómo usar GPG con el cliente de correo gratuito y de código abierto Thunderbird de Mozilla, junto con el complemento Enigmail para el cifrado de correo electrónico.

Primero, descargue Thunderbird desde [https://www.mozilla.org/thunderbird](https://www.mozilla.org/thunderbird), monte la imagen del disco como lo hizo con las herramientas GPG y arrastre Thunderbird hasta las Aplicaciones. Cuando lo abra por primera vez, le preguntará si desea configurarlo como su cliente de correo electrónico predeterminado. Continúe y haga clic en "Establecer como Predeterminado".
![image](tool_pgposx11.png)

Luego verá el primer asistente de ejecución. Para configurar su dirección de correo electrónico existente, haga clic en "Omitir esto y usar mi correo electrónico existente". Luego ingrese su nombre, dirección de correo electrónico y la contraseña de su cuenta de correo electrónico.
![image](tool_pgposx12.png)

Si utiliza servicios gratuitos de correo electrónico populares como Gmail, Thunderbird debería poder detectar automáticamente su configuración de correo electrónico cuando haga clic en Continuar. Si no es así, es posible que deba configurar manualmente las configuraciones de IMAP y SMTP; pida ayuda a su ISP o a un amigo técnico que sepa sobre la configuración de correo electrónico. A veces, Thunderbird puede simplemente adivinar la configuración correcta.

**Si usa la autenticación de dos factores con Google (y, dependiendo del modelo de amenaza, ¡probablemente debería!) No puede usar su contraseña estándar de Gmail con Thunderbird. En su lugar, deberá crear una nueva contraseña específica de la aplicación para que Thunderbird acceda a su cuenta de Gmail. Consulte la [guía de Google] (https://support.google.com/mail/answer/1173270?hl=en) for doing this.** ![image](tool_pgposx13.png)

Una vez que haya terminado de configurar Thunderbird para revisar tu correo electrónico, haga clic en "Listo". Luego haga clic en "Bandeja de entrada" en la parte superior izquierda para cargar sus correos electrónicos.

Ahora que ha instalado y configurado Thunderbird para que funcione con su correo electrónico, debe instalar [Enigmail] (https://www.enigmail.net/home/index.php), el complemento GPG para Thunderbird. En Thunderbird, haga clic en el icono de menú en la parte superior derecha y elija Complementos.
![image](tool_pgposx14.png)

Busque "enigmail" en el cuadro de búsqueda en la parte superior derecha.
![image](tool_pgposx15.png)

Haga clic en el botón Instalar junto a la extensión de Enigmail para descargar e instalar Enigmail. Cuando termine, haga clic en "Reiniciar Ahora" para reiniciar Thunderbird.

La primera vez que ejecuta Thunderbird con Enigmail habilitado, se abre el Asistente de configuración de OpenPGP. Haga clic en "Cancelar". Vamos a configurar manualmente Enigmail en su lugar.

Haga clic en el botón de menú, desplace el mouse sobre Preferencias y elija Configuración de Cuenta.
![image](tool_pgposx16.png)

Vaya a la pestaña de Seguridad de OpenPGP. Asegúrese de que la casilla "Habilitar compatibilidad con OpenPGP (Enigmail) para esta identidad" esté marcada. Se debe seleccionar "Usar ID de clave OpenPGP específica", y si su clave no está ya seleccionada, puede hacer clic en "Seleccionar Clave" para seleccionarla.

También debe marcar "Firmar mensaje no cifrado de forma predeterminada", "Firmar mensajes cifrados de forma predeterminada" y "Usar PGP/MIME de forma predeterminada", pero no (para la mayoría de las personas) "Cifrar mensajes de forma predeterminada".

Si la mayoría de las personas a las que envía correos electrónicos usan PGP (o si desea animarles a hacerlo), es posible que desee cifrar de forma predeterminada. Sería ideal cifrar todos los correos electrónicos que envíe, pero eso no siempre es posible. Recuerde que solo puede enviar correos electrónicos cifrados a otras personas que utilizan PGP, y necesita tener sus claves públicas en su llavero. Para la mayoría de las personas, la elección manual de cifrar cada correo electrónico que envíe probablemente funcionará mejor.
![image](tool_pgposx17.png)

Luego haga clic en "Aceptar" para guardar todas las configuraciones.

¡Felicidades, ahora ha configurado Thunderbird y Enigmail! Aquí hay un par de punteros rápidos:

- Puede hacer clic en el botón de menú, desplazarse sobre OpenPGP y abrir Gestión de Claves para ver el administrador de claves PGP que está integrado en Enigmail. Es muy similar a GPG Keychain Access, y es su elección cuál utiliza.
- Cuando está redactando un nuevo mensaje, hay dos iconos en la esquina inferior derecha de la ventana: un bolígrafo (firmar digitalmente el correo electrónico) y una llave (cifrar el correo electrónico). Si los iconos son dorados significa que están seleccionados, y si son plateados significa que no están seleccionados. Haga clic en ellos para alternar la firma y el cifrado del correo electrónico que está escribiendo.
![image](tool_pgposx18.png)