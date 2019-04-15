---
index: 5
title: K9 y Open Keychain
---
# GUÍA DE HERRAMIENTAS DE K-9 Y OPEN KEYCHAIN


**Lección para leer: [Correo electrónico avanzado](umbrella://communications/email/advanced).**
**Nivel**: Avanzado
**Publicado:** Mayo 2018
**Fuentes:** Security in a Box, [K9 CON APG PARA ANDROID] (https://securityinabox.org/en/guide/k9/android/), Open Keychain [Preguntas frecuentes] (https://www.openkeychain.org/faq/).

**K-9 Mail** es un cliente de correo electrónico de código abierto y gratuito para dispositivos Android.

**Open Keychain** es una aplicación gratuita y de código abierto que le permite cifrar, descifrar y firmar archivos, mensajes o correos electrónicos utilizando el cifrado de clave pública como OpenPGP. Se basa en el código de una herramienta similar llamada APG, ahora sin mantenimiento.

**El uso de K-9 Mail con Open Keychain le dará:**
- La capacidad de utilizar correo electrónico cifrado en su dispositivo Android.

**Ubicación de la descarga:** [K-9 Mail] (https://play.google.com/store/apps/details?id=com.fsck.k9) y [Open Keychain](https://play.google.com/store/apps/details?) en la tienda Google Play.
**Requisitos de software:** Android 4.0.3 y superior.
**Versión utilizada en esta guía**: 5.403 (Correo K-9); 5.0.2 (Open Keychain)
**Licencia**: FOSS.

# 1. Introducción

**K-9 Mail** es un cliente completo de correo electrónico que le permitirá enviar y recibir correos electrónicos de una o más cuentas de correo electrónico en su dispositivo Android, y hacerlo de manera más segura con [Open Keychain](https://play.google.com/store/apps/details?id=org.sufficientlysecure.keychain&hl=en_GB).

**Nota:**
- Los servicios de mensajería segura como Signal son una mejor opción para la comunicación sensible que el correo electrónico.
- Transferir una clave de cifrado privada a su teléfono puede hacer que el correo electrónico en el dispositivo sea más seguro, pero también hace que la clave sea más vulnerable a la pérdida o la intercepción. (Open Keychain describe el riesgo en su [sitio web](https://www.openkeychain.org/faq/#are-my-secret-keys-safe-on-my-mobile-device).)
- Los *destinatarios* y el *asunto* no pueden ocultarse a nadie que supervise su correo electrónico, incluso si el correo electrónico está cifrado.

Antes de comenzar a utilizar **K-9 Mail** necesitará:
- Una conexión a internet en su teléfono.
- Una cuenta de correo electrónico que admita conexiones POP3 o IMAP seguras. (Vea qué configuraciones usaría con los proveedores de correo electrónico más comunes [aquí] (https://k9mail.github.io/documentation/accounts/providerSettings.html).
- Un par de claves OpenPGP y claves públicas de las personas con las que se comunicará.

(Obtenga más información acerca del cifrado de clave pública/privada en la lección [email](umbrella://communications/email). Aprenda cómo generar su propia clave en las guías de herramientas para [Mailvelope] (umbrella://tools/messagging/s_mailvelope.md), o PGP para [LINUX] (umbrella://tools/pgp/s_pgp-for-linux.md), [Mac OSX] (umbrella://tools/pgp/s_pgp-for-mac-os-x.md), o [Windows] (umbrella://tools/pgp/s_pgp-for-windows.md).)

# 2. Instalar y configurar el K9 Mail

## 2.1 Instalar

**Paso 1.** Descargue e instale K-9 Mail de la tienda [Google Play] (https://play.google.com/store/apps/details?id=com.fsck.k9). Revise los permisos que otorga la aplicación cuidadosamente para asegurarse de que está de acuerdo.

![](tool_k9_1.png)

**Paso 2.** **Toque** *Abrir* para ejecutar la aplicación por primera vez.

## 2.2 Configurar

Haga clic en *Siguiente* para comenzar la configuración de la cuenta.

Donde sea posible, **K-9 Mail** intentará configurar su cuenta automáticamente. Si esto no es posible, o si desea tener más control sobre el proceso de configuración de la cuenta, también puede configurarlo manualmente.

**Paso 1:** Ingrese su dirección de correo electrónico y contraseña en los campos provistos y toque *Siguiente*.

![](tool_k9_2.png)

K-9 Mail se conectará a Internet e intentará obtener la configuración de su cuenta.

**Nota**: Es posible que los usuarios con la autenticación de dos factores habilitada en su cuenta de correo electrónico deban tomar un paso adicional para usar el correo K-9.

Por ejemplo:
* Los usuarios de Gmail deben permitir que las aplicaciones menos seguras accedan a sus cuentas en la configuración y generar una contraseña de un solo uso. Lea más [aquí] (https://support.google.com/accounts/answer/6010255?hl=es).
* Los usuarios de Yahoo pueden permitir aplicaciones que utilizan un inicio de sesión menos seguro en la Configuración de la cuenta. Lea más [aquí] (https://help.yahoo.com/kb/SLN27791.html?guccounter=1).

(Los proveedores clasifican el correo K-9 como "menos seguro" porque no usa el mismo protocolo de autenticación. Pero las herramientas de código abierto de confianza como el correo K-9 todavía se consideran seguras para el correo electrónico cifrado).


**Paso 2**: ingrese su nombre tal como desea que se muestre en todos los correos electrónicos salientes, asigne un nombre a la cuenta para distinguir entre varias cuentas. Toque *Hecho*.

**Paso 3:** Envíese un correo electrónico desde su computadora para asegurarse de que pueda leerlo en K-9 Mail.

**Nota:** Si elige *configuración manual,* se le pedirá que seleccione la configuración para su tipo de correo electrónico (IMAP/POP/Exchange), y la configuración del servidor entrante y saliente. Consulte la configuración de su cliente de correo electrónico en su computadora para obtener esta información.

- Para la configuración del servidor, siempre asegúrese de que el *tipo de seguridad* esté configurado en *STARTTLS* o *SSL/TLS*. **Nunca** usa la opción *ninguno*.

- Si K-9 Mail muestra una advertencia sobre el certificado de su conexión segura, *no lo ignore,* verifique que el certificado realmente pertenece a su servidor de correo. Si no lo hace, sus comunicaciones podrían ser interceptadas. Debería ver una huella digital SHA-1 al final de la advertencia. Verifique en su computadora si el certificado instalado de su servidor de correo tiene la misma huella digital, o busque una manera de verificar el certificado de su servidor de correo directamente de su proveedor.


Recomendamos que use **K-9 Mail** además del cliente de correo electrónico de su computadora. Cuando descargue un correo electrónico, no lo eliminará del servidor de manera predeterminada, ya que también desea recibir el correo electrónico en su computadora. Pero esta y otras configuraciones pueden ser cambiadas. Mantenga presionada la cuenta que acaba de configurar y seleccione *configuración de la cuenta* en el menú, o toque los tres puntos en la esquina inferior derecha de la aplicación y seleccione Ajustes para revisar sus opciones.


# 3. Enviar y recibir correo electrónico cifrado

**Paso 1:** En Ajustes, toque *Criptografía*. Si aún no lo ha hecho, K-9 Mail le pedirá que descargue Open Keychain. Una vez que haya descargado Open Keychain, selecciónelo en K-9 Mail.

![](tool_k9_5.png)

Antes de que pueda comenzar a enviar y recibir correo electrónico cifrado, debe asegurarse de tener todas sus claves OpenPGP importadas en Open Keychain.

# 4. Configurar Open Keychain

Toque Open Keychain para abrir la aplicación. En Ajustes, toque *Administrar mis claves*.

![](tool_k9_6.png)  

**Opción 1:** Si está utilizando PGP por primera vez o si desea crear una nueva clave, toque *Crear mi clave* y siga las instrucciones.

**Opción 2:** Si ya tiene una clave PGP y desea usarla en su dispositivo Android, abra el programa que usa para gestionar las claves en su computadora (como GPG Keychain o Mailvelope) y exporte su propia clave, incluyendo su clave privada o secreta. Guarde el archivo en un lugar seguro.

**Nota:** Su clave privada puede utilizarse para hacerse pasar por usted y descifrar sus comunicaciones cifradas. Transferirla a un dispositivo móvil es arriesgado porque el archivo podría perderse o interceptarse.

Si elige transferir su archivo de clave privada, tome precauciones:

- Conecte su dispositivo Android confiable a su computadora confiable usando un cable USB para transferirlo directamente, o habilite Bluetooth en su computadora confiable y su dispositivo Android confiable (verifique que coincidan los códigos de emparejamiento) y use la función "enviar archivo al dispositivo"; o,
- Consulte el consejo de [Open Keychain] (https://www.openkeychain.org/faq/#what-is-the-best-way-to-transfer-my-own-key-to-openkeychain) para proteger su clave con contraseña usando la línea de comando antes de transferirla por internet.

En la ventana *Gestionar mis claves* de Open Keychain, toque *Importar clave del archivo* y luego el icono del archivo. Navegue a la carpeta donde movió el archivo, selecciónelo y toque *ABRIR*. También puede usar *Importar clave del archivo* para transferir claves públicas que otras personas han compartido con usted. Las claves importadas con éxito ahora aparecerán en su lista de claves. Una vez que los vea en Open Keychain, elimine los archivos de su dispositivo. No los deje sentados en una carpeta.

(Para obtener más información sobre la administración de claves, lea las entradas de la parte Llavero y Firma de claves en el glosario de Umbrella).


# 5. Intercambiar correo electrónico cifrado con K9

**Paso 1:** Desde cualquier pantalla en **K-9 Mail** toque el ícono del sobre + para comenzar un nuevo correo electrónico a alguien con quien ya ha intercambiado claves públicas.

**Paso 2:** Agregue la dirección de correo electrónico del destinatario en el campo *Para*.

**Paso 3:**

![](tool_k9_7.png)

Presione el ícono de candado gris; se volverá verde cuando el cifrado esté activo.

![](tool_k9_8.png) 

**Paso 4:** Envíe el mensaje.

**Paso 5:** Cuando reciba una respuesta cifrada, K-9 Mail le solicitará automáticamente que ingrese su contraseña GPG y descifre el correo.