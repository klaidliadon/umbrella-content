---
index: 19
title: Tor en LINUX
---
Tor en Linux
=========================

Anonimato Online

**Lección para leer: [Internet](umbrella://communications/the-internet)**
**Nivel**: Principiante-Avanzado
**Tiempo requerido**: 15 minutos — 1 hora
**Publicado:** abril 2018
**Fuentes:** Surveillance Self-Defense (EFF), [Cómo: Usar Tor en Linux] (https://https://ssd.eff.org/es/module/como-usar-tor-en-linux); Security in a Box [TOR BROWSER FOR LINUX - ONLINE ANONYMITY AND CIRCUMVENTION](https://securityinabox.org/en/guide/torbrowser/linux/).

**Utilizar Tor le permitirá:**

* Ocultar su identidad digital de los sitios web que visita.
* Ocultar los sitios web que visita de los proveedores de servicios de Internet y los programas de vigilancia.
* Eludir la censura y el filtrado de Internet.
* Protegerse contra sitios web inseguros y potencialmente maliciosos a través de los complementos de navegador HTTPS Everywhere y NoScript

**Ubicación de la descarga: ** [https://www.torproject.org/download/download-easy.html.es](https://www.torproject.org/download/download-easy.html.es). Si no puede acceder a este sitio web, lea *Si la página de descarga está bloqueada*, a continuación.
**Requisitos de la computadora:** Una conexión a Internet, una computadora que ejecute su distribución de Linux favorita.
**Versión utilizada en esta guía**: Ubuntu 16.04.1 LTS; Tor Browser: 7.0.2
**Licencia**: Software libre; mezcla de Licencias de Software Libre

Introducción
-------------

Esta guía describe cómo usar [Tor Browser] (https://www.torproject.org/projects/torbrowser.html.es) en Linux.

Tor es un servicio administrado por voluntarios que proporciona privacidad y anonimato en línea al cubrir quién es usted y dónde se está conectando. El servicio también lo protege de la red Tor en sí misma; puede estar seguro de que permanecerá en el anonimato para otros usuarios de Tor.

Para las personas que pueden necesitar anonimato y privacidad ocasionales al acceder a sitios web, Tor Browser ofrece una forma rápida y fácil de usar la red Tor.

Tor Browser funciona como un navegador web, el programa que usa para ver sitios web. Los ejemplos incluyen Chrome, Firefox y Safari. Sin embargo, a diferencia de otros navegadores web, el Tor Browser envía sus comunicaciones a través de Tor, lo que dificulta que las personas que lo monitorean sepan exactamente lo que está haciendo en línea y las personas que monitorean los sitios que usa para saber desde dónde se encuentra. conectando.

Tenga en cuenta que solo las actividades que realice dentro de Tor Browser serán anónimas. Tener Tor Browser instalado en su computadora no hace que las cosas que usted hace en la misma computadora usando otro software (como su navegador web regular) sean anónimas.

**Otras lecturas**:

*   [https://www.torproject.org/docs/documentation.html.en](https://www.torproject.org/docs/documentation.html.en)
*   [https://tor.stackexchange.com/](https://tor.stackexchange.com/)
*   [https://www.eff.org/pages/tor-and-https](https://www.eff.org/pages/tor-and-https)
 

Obtener Tor Browser
-------------------------------------

Abra un navegador como Firefox o Chrome y vaya a:

[https://www.torproject.org/download/download-easy.html.es](https://www.torproject.org/download/download-easy.html.en)

Si está utilizando un motor de búsqueda para buscar Tor Browser, asegúrese de que la URL sea correcta.

No utilice ninguna otra fuente, y si se le solicita que acepte certificados de seguridad alternativos HTTPS (SSL/TLS), no continúe.

![](torforlinux1.png)

El sitio web habrá detectado su sistema operativo y obtendrá el archivo correcto para su sistema operativo. Si esto falla, puede hacer clic en el enlace al lado del botón púrpura para descargar la versión correcta.

Algunos navegadores le pedirán que confirme si desea descargar este archivo. Firefox muestra un cuadro emergente en el centro de la ventana del navegador. Para cualquier navegador, es mejor guardar el archivo antes de continuar. Haga clic en el botón Guardar.

Este ejemplo muestra la versión 7.0.2 de Tor Browser. Es posible que haya una versión más reciente de Tor Browser disponible para descargar en el momento en que lea esto, así que descargue y use la versión actual que proporciona el Proyecto Tor.

![](torforlinux2.png)


Instalación de Tor Browser
----------------------------------------

Una vez completada la descarga, vaya a su carpeta de descargas. Siempre debe asegurarse de confiar en el software que desea instalar y de obtener una copia auténtica del sitio oficial a través de una conexión segura. Como  sabe lo que quiere y sabe dónde obtener el software, y la descarga se realizó desde el sitio seguro HTTPS del Proyecto Tor, haga doble clic en el archivo "tor-browser-linux64-7.0.2_es-ES.tar.xz".

![](torforlinux3.png)

Después de hacer doble clic en el archivo comprimido de Tor Browser, espere a que se cargue y elija dónde desea extraer su contenido.

![](torforlinux4.png)

Una vez finalizada la extracción, abra la carpeta "tor-browser_es-ES" y haga doble clic en el archivo "Configuración de Tor Browser".

![](torforlinux5.png)
 

Usando Tor Browser
-----------------

Luego obtendrás una ventana que te permite modificar algunas configuraciones si es necesario. Es posible que tenga que volver y cambiar algunos ajustes de configuración, pero siga adelante e intente conectarse a la red Tor haciendo clic en el botón Conectar.

![](torforlinux6.png)

Se abrirá una nueva ventana con una barra naranja que ilustra la conexión de Tor Browser a la red Tor.

![](torforlinux7.png)

La primera vez que se inicia Tor Browser, puede llevar mucho tiempo; Pero sea paciente, en un minuto o dos, Tor Browser abrirá y lo felicitará.

![](torforlinux8.png)

Haga clic en el logotipo de Tor Onion en la parte superior izquierda de Tor Browser y luego en la Configuración de Privacidad y Seguridad.

![](torforlinux9.png)

Algunas características de un navegador web normal pueden hacerlo vulnerable a los ataques de intermediarios. Otras características han tenido errores previamente que revelaron las identidades de los usuarios. Mover el control deslizante de seguridad a una configuración alta desactiva estas funciones. Esto lo hará más seguro contra los atacantes bien financiados que pueden interferir con su conexión a Internet o usar nuevos errores desconocidos en estas características. Desafortunadamente, la desactivación de estas funciones puede inutilizar algunos sitios web. La configuración baja predeterminada es adecuada para la protección de la privacidad diaria, pero puede establecerla en alto si le preocupan los atacantes sofisticados o si no le importa si algunos sitios web no se muestran correctamente.

![](torforlinux10.png)

Finalmente, la navegación con Tor es diferente en algunos aspectos de la experiencia de navegación normal. Recomendamos leer [estos consejos] (https://www.torproject.org/download/download-easy.html.en#warning) para navegar correctamente con Tor y conservar su anonimato.

![](torforlinux11.png)

Ahora está listo para navegar en Internet de forma anónima con Tor.

## Compruebe si Tor Browser está funcionando

Tor Browser oculta su *dirección IP* de los sitios web que visita. Si funciona correctamente, parece que estás accediendo a sitios web desde una ubicación en Internet que

- Es diferente de su dirección IP normal
- No se puede vincular a su ubicación física

La forma más sencilla de confirmar esto es visitando el sitio web *Tor Check*, que se encuentra en [**https: //check.torproject.org/**] (https://check.torproject.org)

Si **no** está utilizando Tor, mostrará lo siguiente:

 ![](not-using-tor.png)


Si está utilizando Tor, se mostrará lo siguiente:

 ![](using-tor.png) 

Si desea verificar su dirección IP aparente utilizando un servicio que no está asociado con el Proyecto Tor hay muchas opciones en línea. Los ejemplos que admiten el cifrado *https* (lo que hace que sea más difícil para alguien *distinto* al proveedor de servicios "falsificar" el resultado) incluyen:

- [https://www.iplocation.net/](https://www.iplocation.net/)
- [https://www.ip2location.com/](https://www.ip2location.com/)

Si accede a estos sitios web *sin* utilizar el Navegador Tor, deberían mostrar su dirección IP real, que está vinculada a su ubicación física. Si accede a ellos a través del Tor Browser, deberían mostrar una dirección IP diferente.

## Cómo crear una nueva identidad

Puede crear una "nueva identidad" para Tor Browser. Cuando lo haga, Tor Browser seleccionará aleatoriamente un nuevo conjunto de relés Tor, lo que hará que parezca provenir de una dirección IP diferente cuando visite sitios web. Para ello, siga los pasos a continuación:

**Paso 1**. **Abra** el menú de Tor Browser

 ![](new-identity.png)

**Paso 2**. ** Seleccione ** *Nueva Identidad* en el menú.

Tor Browser borrará su historial de navegación y las cookies y luego se reiniciarán. Una vez que se haya reiniciado, puede confirmar que parece provenir de una nueva dirección IP como se describe en la sección anterior.

Problemas al Usar Tor Browser
-----------------

Si no puede conectarse, intente [solución de problemas] (https://www.torproject.org/docs/faq.html.en#DoesntWork).

Si aún no puede conectarse y sospecha que su acceso a Tor puede estar restringido, lea *Si la Red Tor está bloqueada*, a continuación.

Si planea viajar a un área donde sospecha que el acceso a Tor puede estar restringido, lea *Cómo reconfigurar el acceso a la red Tor*, a continuación.

#Si la Página de Descarga está Bloqueada

* Hay un espejo del Tor Browser Bundle en [Github] (https://github.com/TheTorProject/gettorbrowser).
* También puede enviar un correo electrónico a gettor@torproject.org con la versión que necesita (windows, osx o linux) en el cuerpo del mensaje.
* Envíe un mensaje directo que diga "ayuda" a [@get_tor] (https://twitter.com/get_tor) en Twitter para obtener instrucciones sobre cómo solicitar Tor a través de DM.

Antes de descargar un paquete Tor Browser en Linux, debe determinar si está ejecutando un sistema de **32 bits** o de **64 bits**. Antes de extraerlo, debes verificar que sea auténtico.

**Paso 1**. Inicie la aplicación *Terminal*

**Paso 2**. Ejecute el siguiente comando en *Terminal*:

`uname –m`

Si está ejecutando un sistema de **32-bits**, *Terminal* mostrará `i686` o` i386`. Si está ejecutando un sistema de **64 bits**, se mostrará `x86_64`.

**Paso 3**. **Haga clic** en el enlace de descarga y guarde el paquete en algún lugar conveniente (en su carpeta *Descritorio* o *Documentos*, por ejemplo, o en un dispositivo de almacenamiento USB). Necesitará el archivo **.Asc** para *verificar* la autenticidad del paquete al verificar su firma. (Consulte la [Guía del Proyecto Tor para verificar firmas] (https://www.torproject.org/docs/verifying-signatures.html.en)).

Verificar Tor Browser
------------------

GnuPG viene preinstalado en muchos sistemas Linux, por lo que probablemente pueda revisar la firma *Abrir PGP* de Tor Browser sin instalar software adicional. (Obtenga más información sobre PGP en la lección [Correo electrónico] (umbrella://communications/email/expert) y [Guía de herramienta PGP para LINUX] (umbrella://tools/pgp/s_pgp-for-linux.md).)

**Paso 1**. Importe la clave de firma del *Proyecto Tor* (**0x4E2C6E8793298290**) abriendo *Terminal* y ejecutando el siguiente comando:

`gpg --keyserver x-hkp://pool.sks-keyservers.net --recv-keys 0x4E2C6E8793298290`

En respuesta, *Terminal* debería mostrar lo siguiente:

 ![](torforlinux12.png) 

**Paso 2**. Puede mostrar información sobre esta tecla ejecutando el siguiente comando en *Terminal*:

`gpg --fingerprint 0x4E2C6E8793298290`

En respuesta, *Terminal* debería mostrar lo siguiente:

 ![](torforlinux13.png)

**Paso 3**. Usando *Terminal*, ingrese al directorio donde guardó uno de los dos archivos de paquetes del Tor Browser a continuación:

- *tor-browser-linux64-5.0.4_en-US.tar.xz* 
- *tor-browser-linux32-5.0.4_en-US.tar.xz*

Este directorio también debe contener uno de los siguientes dos archivos de firma:

- *tor-browser-linux64-5.0.4_en-US.tar.xz.asc* 
- *tor-browser-linux32-5.0.4_en-US.tar.xz.asc* 

**Importante**: En los ejemplos anteriores y siguientes, estos archivos son de la versión **5.0.4** de Tor Browser. **Sus archivos deberían tener números de versión más altos.**

**Paso 4**. Desde ese directorio, ejecute uno de los siguientes comandos en *Terminal* (dependiendo de si descargó la versión de 32 bits o la versión de 64 bits de Tor Browser)

- `gpg --verify ./tor-browser-linux32-5.0.4_en-US.tar.xz{.asc*,}`
- `gpg --verify ./tor-browser-linux64-5.0.4_en-US.tar.xz{.asc*,}`

En respuesta, *Terminal* debería mostrar lo siguiente:

 ![](torforlinux14.png)

Lo anterior verifica que la *clave privada* correspondiente a la *clave pública* que importó en el *Paso 1* se utilizó para generar el archivo de firma que descargó en el *Paso 5* de la sección anterior (y que este archivo de firma se aplica a el paquete Tor Browser que descargó en el *Paso 4* de la sección anterior).

**Importante**: Como puede ver, GPG muestra una advertencia sobre la clave utilizada para esta firma. Esto se debe a que en realidad no ha verificado la clave de firma del Proyecto Tor. La mejor manera de hacerlo es reunirse con los desarrolladores del Proyecto Tor en persona y pedirles la huella digital de su clave de firma. Para los fines de esta guía, confiamos en el hecho de que se utilizó una clave GPG del Proyecto Tor (**0x4E2C6E8793298290**) conocida para crear un archivo de firma que confirma la autenticidad del paquete de Tor Browser que descargó.


# Si la red Tor está Bloqueada

Si desea usar Tor Browser desde una ubicación donde la red Tor esté bloqueada, tendrá que usar un **repetidor de puente de red**. Los puentes no están listados en el directorio público de los repetidores Tor, por lo que son más difíciles de bloquear. Algunos puentes también admiten **transportes conectables**, que intentan ocultar su tráfico hacia y desde la red Tor. Esto ayuda a evitar que los filtros en línea identifiquen y bloqueen los repetidores de puente de red.

El transporte conectable predeterminado, llamado **obfs4**, también dificulta un poco más que otros se den cuenta de que se está conectando a la red Tor. Pero, en general, Tor no está diseñado para ocultar el hecho de que está utilizando Tor.

Puede obtener más información sobre los puentes en el [sitio web del Proyecto Tor] (https://bridges.torproject.org/). Hay dos formas de usar los puentes. Puede habilitar los **puentes proporcionados** o puede solicitar **puentes personalizados**.

### Puentes proporcionados

Puede usar los puentes proporcionados para conectarse a la red Tor realizando los siguientes pasos:

**Paso 1**. **Haga doble clic** en el archivo de **Configuración de Tor Browser**. Esto mostrará la pantalla de configuración de Tor Browser.

 ![](tor-running-1.png)


**Paso 2**. Si tiene acceso restringido, **haga clic** en **[Configurar]**.

![](tor-bridges-config.png)

**Paso 3**. **Seleccione** **Sí**

**Paso 4**. **Haga clic** en **[Siguiente]** para visualizar la pantalla *configuración de puente*

![](provided-bridges.png)

**Paso 5**. **Seleccione** **Conectar con los puentes provistos**

**Paso 6**. **Haga clic** en **[Siguiente]** para visualizar la pantalla *configuración de proxy local*

Tor Browser ahora le preguntará si necesita usar un *proxy local* para acceder a Internet. Los pasos a continuación asumen que usted no lo hace. Si *lo hace*, puede verificar la configuración normal de su navegador y copiar la configuración de su proxy. (En Firefox puede encontrar esta configuración en la pestaña *Opciones> Avanzadas> Red* de *Configuración de conexión*. En otros navegadores, puede encontrarla en *Opciones de Internet*. También puede usar la función *Ayuda* dentro de su navegador para más ayuda.

![](no-local-proxy.png)

**Paso 7**. **Seleccione** **No**

**Paso 8**. **Haga clic** en **[Conectar]** para iniciar Tor Browser

![](tor-running-2.png)

Después de unos momentos, Tor Browser se abrirá.


### Puentes personalizados

También puede conectarse a la red Tor a través de **puentes personalizados**, que son utilizados por menos personas que los **puentes proporcionados** y, por lo tanto, es menos probable que se bloqueen. Si no puede acceder al sitio web del Proyecto Tor, puede solicitar direcciones de puente personalizadas enviando un correo electrónico a **bridges@torproject.org** utilizando una cuenta *Riseup*, *Gmail* o *Yahoo*. Incluya la frase, **obtener puentes** en el cuerpo de su mensaje

Si *puede* acceder al sitio web del Proyecto Tor, puede obtener direcciones de puente personalizadas visitando **https://bridges.torproject.org/options** y siguiendo los pasos a continuación.

**Paso 1**. **Haga clic** en *¡Sólo dame los bridges!*

 ![](just-give-me-bridges.png)


**Paso 2**. Rellene el captcha y presione **enter**.

 ![](bridge-captcha.png)


Esto debería mostrar tres direcciones de puente.

 ![](bridge-lines.png)


**Paso 3**. Una vez que tenga sus direcciones de puente personalizadas, puede **escribirlas** en la pantalla *Configuración de Puente Tor* que se muestra a continuación.

 ![](custom-bridges.png) 


## Cómo reconfigurar el acceso a la red Tor

En cualquier momento, si necesita acceder a la red Tor de otra forma, por ejemplo, si ha viajado a un país que bloquea Tor, puede actualizar su configuración desde el navegador siguiendo estos pasos:

**Paso 1:** **Abra** el menú de Tor Browser

 ![](torbrowser-lin-en-v01-901.png)

**Paso 2.** **Seleccione** *Configuración de red Tor* para cambiar la forma en que Tor Browser se conecta a Internet.

 ![](custom-bridges.png)

Esta pantalla le permite habilitar o deshabilitar Puentes y agregar Puentes personalizados, entre otros cambios.

**Paso 3**. Cuando haya terminado, **haga clic** en **[OK]** y **reinicie** **Tor Browser**.