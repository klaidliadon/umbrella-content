---
index: 17
title: Signal para iOS
---
Signal para iOS
=========================

Mensajes Seguros

**Lección para leer: [Enviar un mensaje](umbrella://communications/sending-a-message)**
**Nivel**: Principiante - Intermedio
**Tiempo requerido**: 15 - 20 minutos.
**Publicado:** Abril de 2018 (algunas imágenes datan de versiones anteriores)
**Fuentes:** EFF, autodefensa de vigilancia [Cómo: Usar Signal en iOS] (https://ssd.eff.org/en/module/how-use-signal-ios); Security in a Box [SIGNAL PARA ANDROID] (https://securityinabox.org/en/guide/signal/android/).

**Usar Signal le dará:**

- La capacidad de enviar mensajes cifrados de extremo a extremo de grupo, texto, imagen y video, y tener conversaciones telefónicas cifradas con otros usuarios de Signal.

**Ubicación de descarga**: La [Apple App Store] (https://itunes.apple.com/us/app/signal-private-messenger/id874139669?mt=8)

**Requisitos del sistema**: iOS 8.0 o posterior. Compatible con iPhone, iPad y iPod touch.
(es necesario tener una cuenta de Apple que se vinculará a la instalación de la aplicación).

**Versión utilizada en esta guía**: Signal iOS 2.8.1

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
* Open Whisper Systems, los fabricantes de Signal, utilizan la infraestructura de otras compañías (Apple en iOS) para enviar alertas a sus usuarios cuando reciben un mensaje nuevo. Eso significa que algunos metadatos, o información sobre quién está recibiendo mensajes y cuándo se recibieron, pueden filtrarse a estas compañías.




Instalando Signal - Private Messenger en su iPhone
----------------------------------------------------------------------

### Paso 1: Descargar e instalar Signal - Private Messenger

En su dispositivo iOS, ingrese a la App Store y busque "Signal". Seleccione [Signal - Private Messenger] (https://itunes.apple.com/us/app/signal-private-messenger/id874139669?mt=8) Por Open Whisper Systems.

Toque "OBTENER" para descargar la aplicación, luego "INSTALAR". Es posible que se le solicite ingresar sus credenciales de ID de Apple. Una vez que se haya descargado, haga clic en "ABRIR" para iniciar la aplicación.

### Paso 2: Regístrese y Verifique su Número de Teléfono

Ahora verá la siguiente pantalla. Ingrese su número de teléfono móvil y toque "Verificar Este Dispositivo".

![](tool_signalios_resized000.png)

![](tool_signalios_resized001.png)

Para verificar su número de teléfono, se le enviará un SMS con un código de seis dígitos. Ahora se le solicitará que ingrese ese código y luego presione "Enviar Código de Verificación".

![](tool_signalios_resized002.png)

Una vez completado este proceso, Signal solicitará acceso a sus contactos. Pulse "Continuar".

![](tool_signalios_resized003.png)

Signal solicitará permiso para enviarle notificaciones. Presione "Aceptar".

![](/tool_signalios_resized004.png)

 

Usando Signal
------------------------------

Para poder utilizar Signal, la persona a la que llama debe tener Signal instalado. Si intenta llamar o enviar un mensaje a alguien que usa la aplicación Signal y no tiene ninguna de las aplicaciones mencionadas anteriormente, la aplicación le preguntará si desea invitarla por SMS, pero no le permitirá completar su llamada o enviar un mensaje desde el interior de la aplicación.

Signal le proporciona una lista de otros usuarios de Signal en sus contactos. Para hacer esto, los datos que representan los números de teléfono en su lista de contactos se cargan en los servidores de Signal, aunque estos datos se eliminan casi de inmediato.

 

Cómo Enviar un Mensaje Encriptado
--------------------------------------------------

Tenga en cuenta que Open Whisper Systems, los fabricantes de Signal, utilizan la infraestructura de otras compañías para enviar alertas a sus usuarios cuando reciben un mensaje nuevo. Utiliza Google en Android, y Apple en iPhone. Eso significa que la información sobre quién está recibiendo mensajes y cuándo se recibieron puede filtrarse a estas compañías.

Para comenzar, toque el ícono de escribir en la esquina superior derecha de la pantalla.

![](tool_signalios_resized005-compose.png)

Verá una lista de todos los usuarios registrados de Signal en sus contactos.

![](tool_signalios_resized008.png)

Cuando toca en un contacto, le llevará a la pantalla de mensajes de texto para su contacto. Desde esta pantalla, puede enviar mensajes de texto, imagen o video cifrados de extremo a extremo.

![](tool_signalios_resized010.png)

### Cómo Iniciar una Llamada Encriptada

Para iniciar una llamada cifrada a un contacto, seleccione ese contacto y luego toque el ícono del teléfono.

![](tool_signalios_resized010-phone.png)

En este punto, Signal puede pedir permiso para acceder al micrófono. Presione "Aceptar".

![](tool_signalios_resized011.png)

Una vez que se establece una llamada, su llamada se cifra.

### Cómo Iniciar una Llamada de Video Encriptada

Para hacer una llamada de video encriptada, simplemente llame a alguien como se describe anteriormente:

![](tool_signalandroid_initial_video_screen.png)

y toque el icono de la cámara de video. Es posible que tenga que permitir que Signal acceda al video desde su cámara. Esto comparte su video con su amigo (es posible que su amigo tenga que hacer lo mismo).


### Cómo Iniciar un Chat Grupal Cifrado

Puede enviar un mensaje de grupo cifrado tocando el ícono de escribir en la esquina superior derecha de la pantalla (el cuadrado con un lápiz apuntando hacia el centro), y luego tocando el ícono en el mismo lugar con tres figuras.

![](tool_signalios_resized005-compose.png)

![](tool_signalios_resized008-group.png)

En la siguiente pantalla, podrá nombrar el grupo y agregar participantes al mismo. Después de agregar participantes, puede tocar el ícono "+" en la esquina superior derecha de la pantalla.

![](tool_signalios_resized023-plus.png)

Esto iniciará el chat de grupo.

![](tool_signalios_resized024.png)

Si desea cambiar el nombre del grupo o agregar o eliminar participantes, esto se puede hacer desde la pantalla de chat del grupo tocando el ícono de desbordamiento (los tres puntos en la esquina superior derecha de la pantalla) y seleccionando "Editar grupo".

### Cómo Verificar sus Contactos

En este punto, puede verificar la autenticidad de la persona con la que está hablando, para asegurarse de que su clave de cifrado no fue manipulada o reemplazada por la clave de otra persona cuando su aplicación la descargó (un proceso llamado verificación de clave). La verificación es un proceso que tiene lugar cuando usted está físicamente en presencia de la persona con la que está hablando.

Primero, abra la pantalla donde puede enviar un mensaje a su contacto, como se describe anteriormente. Desde esta pantalla, toque el nombre de su contacto en la parte superior de la pantalla.

![](tool_signalios_resized010-name.png)

En la siguiente pantalla, toque "Verificar Números de Seguridad".

![](tool_signalios_resized015-verify.png)

Ahora será llevado a una pantalla que muestra un código QR y una lista de "números de seguridad". Este código será único para cada contacto diferente con el que esté conversando. Haga que su contacto navegue a la pantalla correspondiente para conversar con usted, para que también tengan un código QR en su pantalla.

![](tool_signalios_resized016.png)

De vuelta en su dispositivo, presione "Escanear Código". En este punto, Signal puede pedir permiso para acceder a la cámara. Presione "Aceptar".

![](tool_signalios_resized017.png)

Ahora podrá usar la cámara para escanear el código QR que se muestra en la pantalla de su contacto. Alinee su cámara al código QR:

![](tool_signalios_resized018.png)

Con suerte, su cámara escaneará el código de barras y mostrará un diálogo "¡Números de Seguridad Verificados!", así:

![](tool_signalios_resized019.png)

Esto indica que ha verificado su contacto con éxito. Si, en cambio, su pantalla se ve así, algo salió mal:

![](tool_signalios_resized020.png)

Es posible que desee evitar discutir temas delicados hasta que haya verificado las claves con esa persona.

_Nota para usuarios avanzados: la pantalla que muestra su código QR también tiene un ícono para compartir su número de seguridad_ en la esquina superior derecha. La verificación en persona es el método preferido, pero es posible que ya haya autenticado su contacto con otra aplicación segura, como PGP. Como ya ha verificado su contacto, puede usar de forma segura la confianza establecida en esa aplicación para verificar_ _números en Signal, sin tener que estar físicamente en presencia de su contacto. En este caso, puede compartir su número de seguridad con esa aplicación tocando el ícono "compartir" y enviar a su contacto su número de seguridad._

### Mensajes que Desaparecen

Signal tiene una función llamada mensajes que desaparecen, lo que garantiza que los mensajes se eliminarán de su dispositivo y del dispositivo de su contacto una cierta cantidad de tiempo elegido después de que sean vistos. Para habilitar la desaparición de mensajes para una conversación, abra la pantalla donde podrá enviar mensajes a su contacto. Desde esta pantalla, toque el nombre del contacto en la parte superior de la pantalla, luego toque el control deslizante junto a "Mensajes que Desaparecen".

![](tool_signalios_resized015-slider.png)

Aparecerá un control deslizante que le permite elegir la rapidez con la que desaparecerán los mensajes:

![](tool_signalios_resized021.png)

Después de seleccionar una opción, puede tocar el ícono "<" en la esquina superior izquierda de la pantalla, y debería ver información en la conversación que indica que se han habilitado los "mensajes que desaparecen".

![](tool_signalios_resized022.png)

Ahora puede enviar mensajes con la seguridad de que se eliminarán después de la cantidad de tiempo elegida.