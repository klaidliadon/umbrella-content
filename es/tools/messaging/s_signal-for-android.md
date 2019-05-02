---
index: 16
title: Signal para Android
---
Signal para Android
==============================
Mensajes Seguros

* Lección para leer: [Enviar un mensaje](umbrella://communications/sending-a-message)**
**Nivel**: Principiante-Intermedio
**Tiempo requerido**: 15-20 minutos.
**Publicado:** Abril de 2018 (algunas imágenes datan de versiones anteriores)
**Fuentes:** EFF, EFF, Surveillance Self-Defense [Cómo: Usar Signal para Android] (https://ssd.eff.org/en/module/how-use-signal-android); Security in a Box [SIGNAL FOR ANDROID](https://securityinabox.org/en/guide/signal/android/).

**Usar Signal le dará:**

- La capacidad de enviar mensajes cifrados de extremo a extremo de grupo, texto, imagen y video, y tener conversaciones telefónicas cifradas con otros usuarios de Signal.

**Ubicación de descarga**: [Tienda de Google Play](https://play.google.com/store/apps/details?id=org.thoughtcrime.securesms).

**Requisitos del sistema**: Android 2.3 y versiones posteriores, con Google Play Services (es necesario tener una cuenta de Google que esté vinculada a la instalación de la aplicación).

**Versión utilizada en esta guía**: Signal 3.31.3

**Licencia:** GPLv3

**Otras lecturas**:

*   [http://support.whispersystems.org/](http://support.whispersystems.org/)
*   [https://signal.org/blog/standalone-signal-desktop/](https://signal.org/blog/standalone-signal-desktop/)
*   [https://whispersystems.org/blog/signal-video-calls/](https://whispersystems.org/blog/signal-video-calls/)


Introducción
-----------------
Signal es una aplicación de software de código abierto y gratuita para Android, iOS y Desktop que emplea cifrado de extremo a extremo, lo que permite a los usuarios enviar mensajes de grupo, texto, imagen y video cifrados de extremo a extremo, y tener conversaciones telefónicas cifradas. entre los usuarios de Signal.

Aunque Signal usa números de teléfono como contactos, las llamadas y los mensajes encriptados usan su conexión de datos; por lo tanto, ambas partes de la conversación deben tener acceso a Internet en sus dispositivos móviles. Debido a esto, los usuarios de Signal no incurren en tarifas de SMS y MMS para este tipo de conversaciones.

En Android, Signal puede reemplazar su aplicación de mensajería de texto predeterminada, por lo que dentro de Signal todavía es posible enviar mensajes SMS sin cifrar.

Nota:
* Signal impide que otros accedan al contenido de sus mensajes y llamadas de voz, pero no oculta el hecho de que está enviando mensajes cifrados o haciendo llamadas de voz cifradas. En algunos países, las herramientas de encriptación como Signal pueden llamar la atención o violar las restricciones legales.
* Open Whisper Systems, los creadores de Signal, utilizan la infraestructura de otras empresas (Google en Android) para enviar alertas a los usuarios cuando reciben un mensaje nuevo. Eso significa que algunos metadatos, o información sobre quién está recibiendo mensajes y cuándo se recibieron, pueden filtrarse a estas compañías.

Instalando Signal en su teléfono Android
----------------------------------------
### Paso 1: Descargar e Instalar Signal

En su dispositivo Android, ingrese a Google Play store y busque "Signal". Seleccione [Signal by Open Whisper Systems](https://play.google.com/store/apps/details?id=org.thoughtcrime.securesms) .

Después de tocar "Instalar", verá una lista de funciones de Android a las que Signal debe poder acceder para poder funcionar. Haga clic en "Aceptar".

Una vez que Signal haya terminado de descargarse, toque "Abrir" para iniciar la aplicación.

### Paso 2: Regístrese y Verifique su Número de Teléfono

Ahora verá la siguiente pantalla. Ingrese su número de teléfono móvil y pulse "Registrarse".

![](tool_signalandroid_resized000_0.png)

Luego se le pedirá que verifique su número de teléfono. Haga clic en "Continuar".

![](tool_signalandroid_resized001_0.png)

Para verificar su número de teléfono, se le enviará un SMS con un código de seis dígitos. Como Signal puede acceder a sus mensajes de texto SMS, reconocerá automáticamente cuando haya recibido el código y completará su registro.

![](tool_signalandroid_resized002_0.png)

Una vez finalizado este proceso, se le preguntará si desea que Signal sea su aplicación de SMS predeterminada. Esto puede ser útil para mantener todos sus mensajes en un solo lugar. Tenga en cuenta que si acepta esto, los mensajes enviados a los contactos que no tienen Signal instalada (incluso si los envía desde la aplicación de Signal) no se cifrarán.

 

Usando Signal
------------------------------

Para poder utilizar Signal, la persona a la que llama debe tener Signal instalado. Si intenta enviar un mensaje a alguien usando Signal y esa persona no tiene Signal instalada, se enviará un mensaje de texto estándar, no cifrado. Si intenta llamar a la persona, se realizará una llamada telefónica estándar.

Signal le proporciona una lista de otros usuarios de Signal en sus contactos. Para hacer esto, los datos que representan los números de teléfono en su lista de contactos se cargan en los servidores de Signal, aunque estos datos se eliminan casi de inmediato.

### Cómo Enviar un Mensaje Encriptado

Presione el ícono del lápiz en la esquina inferior derecha de la pantalla.

![](tool_signalandroid_resized003_0.png)

Verá una lista de todos los usuarios registrados de Signal en sus contactos. También puede ingresar el número de teléfono de un usuario de Signal que no esté en sus contactos. Cuando selecciona un contacto, se le llevará a la pantalla de mensajes de texto para su contacto. Tenga en cuenta que para los usuarios de Signal, verá el texto "Enviar mensaje de señal"; esto significa que el mensaje se cifrará. En esta pantalla, el ícono de "teléfono" en la esquina superior derecha de la pantalla indicará que puede hacer una llamada de voz cifrada usando Signal también. Desde esta pantalla, puede enviar mensajes cifrados de texto, imagen o video de extremo a extremo.

![](tool_signalandroid_resized006.png)

Para los usuarios que no tienen Signal instalada, verá el texto "Enviar SMS no protegidos", que no enviará el mensaje cifrado. En esta pantalla, el ícono "teléfono" en la esquina superior derecha de la pantalla hará una llamada telefónica normal, sin cifrar.

![](tool_signalandroid_resized004_0.png)

### Cómo Iniciar una Llamada Encriptada

Para iniciar una llamada cifrada a un contacto, seleccione ese contacto y luego toque el ícono del teléfono. Sabrá que el contacto puede aceptar llamadas de Signal si ve un ícono de un pequeño candado al lado del ícono del teléfono.

![](tool_signalandroid_resized006-1.png)

Una vez que se establece una llamada, su llamada se cifra.

### Cómo Iniciar una Llamada de Video Encriptada

Para hacer una llamada de video encriptada, simplemente llame a alguien como se describe anteriormente:

![](tool_signalandroid_initial_video_screen.png)

y toque el icono de la cámara de video. Es posible que tenga que permitir que Signal acceda al video desde su cámara. Esto comparte su video con su amigo (es posible que su amigo tenga que hacer lo mismo).

### Cómo Iniciar un Chat Grupal Encriptado

Puede enviar un mensaje de grupo cifrado tocando el ícono de desbordamiento (los tres puntos en la esquina superior derecha de la pantalla) y seleccionando "Nuevo grupo".

![](tool_signalandroid_resized020_0.png)

En la siguiente pantalla, podrá nombrar el grupo y agregar participantes al mismo.

![](tool_signalandroid_resized021_0.png)

![](tool_signalandroid_resized016_0.png)

Después de agregar participantes, puede tocar en la marca de verificación en la esquina superior derecha de la pantalla. Esto iniciará el chat de grupo.

![](tool_signalandroid_resized019_0.png)

Si desea cambiar el ícono de grupo, agregar o eliminar participantes, esto se puede hacer desde la pantalla de chat grupal tocando el ícono de desbordamiento (los tres puntos en la esquina superior derecha de la pantalla) y seleccionando "Actualizar grupo".

### Silenciar Conversaciones

A veces, las conversaciones pueden distraer. Una característica que es especialmente útil para los chats grupales es silenciar las notificaciones, por lo que no verá una notificación nueva cada vez que se emita un nuevo mensaje. Esto se puede hacer desde la pantalla de chat grupal tocando el ícono de desbordamiento (los tres puntos en la esquina superior derecha de la pantalla) y seleccionando "Silenciar notificaciones". Luego, puede seleccionar durante cuánto tiempo desea que se active el silencio. Esto también se puede aplicar a conversaciones individuales, si se desea.

### Cómo Verificar sus Contactos

En este punto, puede verificar la autenticidad de la persona con la que está hablando, para asegurarse de que su clave de cifrado no fue manipulada o reemplazada por la clave de otra persona cuando su aplicación la descargó (un proceso llamado verificación de clave). La verificación es un proceso que tiene lugar cuando usted está físicamente en presencia de la persona con la que está hablando.

Primero, abra la pantalla donde puede enviar un mensaje a su contacto, como se describe anteriormente. Desde esta pantalla, toca el ícono de desbordamiento (los tres puntos en la esquina superior derecha de la pantalla) y seleccione "Configuración de conversación".

![](tool_signalandroid_resized010_0.png)

En la siguiente pantalla, toque "Verificar números de seguridad".

![](tool_signalandroid_resized011_0.png)

Ahora se lo llevará a una pantalla que muestra un código QR y una lista de "números de seguridad". Este código será único para cada contacto diferente con el que esté conversando. Haga que su contacto navegue a la pantalla correspondiente para conversar con usted, para que también tengan un código QR en su pantalla.

![](tool_signalandroid_resized012_0.png)

De vuelta en su dispositivo, puede tocar su código QR, que utilizará la cámara para escanear el código QR que se muestra en la pantalla de su contacto. Alinee su cámara al código QR:

![](tool_signalandroid_resized014.png)

Con suerte, su cámara escaneará el código de barras y mostrará una marca de verificación, como esta:

![](tool_signalandroid_resized015.png)

Esto indica que ha verificado su contacto con éxito. Si, en cambio, su pantalla se ve así, algo salió mal:

![](tool_signalandroid_resized013.png)

Es posible que desee evitar discutir temas delicados hasta que haya verificado las claves con esa persona.

_Nota para usuarios avanzados: la pantalla que muestra su código QR también tiene un icono para compartir su número de seguridad en la esquina superior derecha. La verificación en persona es el método preferido, pero es posible que ya haya autenticado su contacto con otra aplicación segura, como PGP. Como ya ha verificado su contacto, puede usar la confianza establecida en esa aplicación para verificar los números de seguridad dentro de Signal, sin tener que estar físicamente en presencia de su contacto. En este caso, puede compartir su número de seguridad con esa aplicación tocando el ícono "compartir" y enviar a su contacto su número de seguridad._

### Mensajes que Desaparecen

Signal tiene una función llamada mensajes que desaparecen, lo que garantiza que los mensajes se eliminarán de su dispositivo y del dispositivo de su contacto una cierta cantidad de tiempo elegido después de que sean vistos. Para habilitar la desaparición de mensajes para una conversación, abra la pantalla donde podrá enviar mensajes a su contacto. Desde esta pantalla, toca el ícono de desbordamiento (los tres puntos en la esquina superior derecha de la pantalla) y selecciona "Mensajes que desaparecen".

![](tool_signalandroid_resized022_0.png)

Aparecerá una nueva pantalla que le permitirá elegir la rapidez con la que desaparecerán los mensajes:

![](tool_signalandroid_resized009.png)

Después de seleccionar una opción, debería ver información en la conversación que indica que se han habilitado los "mensajes que desaparecen".

![](tool_signalandroid_resized008_0.png)

Ahora puede enviar mensajes con la seguridad de que se eliminarán después de la cantidad de tiempo elegida.