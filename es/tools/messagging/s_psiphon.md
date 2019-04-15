---
index: 14
title: Psiphon
---
# GUIA DE HERRAMIENTAS DE PSIPHON

Elusión de la Censura

**Lección para leer: [Internet](umbrella://communications/the-internet)**
**Ubicación de descarga:** [Google Play] (https://play.google.com/store/apps/details?id=com.psiphon3.subscription), [Apple App store] (https://itunes.apple.com/us/app/psiphon/id1276263909?ls=1&mt=8) o [Psiphon] (https://psiphon.ca/en/download.html).
**Requisitos de la computadora:** Una conexión a Internet y un dispositivo con Windows, Android 2.3 o posterior, o iOS 10.2 o posterior (iOS 8 para el navegador Psiphon)
**Licencia:** Software libre de código abierto; GNU GPL Versión 3
**Nivel:** Principiante
**Otra lectura:** [https://psiphon.ca/en/user-guide.html◆ (https://psiphon.ca/en/user-guide.html)
**Tiempo requerido:** 5 minutos.

**Usar Psiphon le dará:**
- La capacidad de sortear de forma segura la censura de Internet para acceder a sitios web y aplicaciones bloqueados mediante una red privada virtual (VPN).

### 1. Antes de comenzar

- Tenga cuidado con las copias maliciosas de Psiphon y solo descargue de fuentes oficiales.

![image](tool_psiphon10.png)
![image](tool_psiphon11.png)
![image](tool_psiphon12.png)

- Psiphon está pensado principalmente como una herramienta de evasión de la censura, en lugar de una que garantiza el anonimato.
- Debido a que Psiphon está basado en VPN, es capaz de apoderarse de todo su tráfico de Internet, no solo de los sitios web.
- Si no ha activado Psiphon de forma activa, no está utilizando la VPN. (Solo tener Psiphon en su computadora no es suficiente.)
- Las páginas web pueden cargarse más lentamente cuando se utiliza una VPN. Esto es normal, porque el navegador no se conecta directamente al sitio web.
- Algunos servicios VPN pagos pueden ser más rápidos que los gratuitos como Psiphon, pero debe tener cuidado antes de confiarle a su empresa su información, ya que podría compartirla con las autoridades o venderla a otras compañías.
- El tráfico entre su dispositivo y el servidor VPN está encriptado. Sin embargo, el tráfico entre ese servidor y un sitio web que no sea HTTPS *no* estará cifrado. (Lo mismo se aplica a otros servicios de Internet, como cuando se conecta con Outlook o Thunderbird a un proveedor de correo electrónico no SSL).

### 2. Psiphon para Android

Descargue Psiphon Pro de la tienda [Google Play] (https://play.google.com/store/apps/details?id=com.psiphon3.subscription).

Si no tiene acceso a la tienda Google Play, seleccione Psiphon Pro para Android en la página de descarga oficial de Psiphon (https://psiphon.ca/en/download.html?10Years). (Verifique que el archivo descargado sea auténtico [aquí] (https://psiphon.ca/en/faq.html#authentic-android).) Es posible que deba [habilitar el sideloading](https://psiphon.ca/en/faq.html#android-enable-sideloading).)

Abra la aplicación y haga clic en *inicio* para conectarse a la red Psiphon.

![image](tool_psiphon5.png)

Seleccione el modo de Dispositivo Completo para hacer un túnel de todas las aplicaciones a través de Psiphon. (Es posible que esta opción no esté disponible para versiones anteriores de Android. En su lugar, puede usar el navegador dedicado Psiphon, pero solo la actividad en línea realizada en el navegador usará Psiphon. Otras aplicaciones se conectarán mediante su conexión a Internet habitual).

![image](tool_psiphon6.png)

La "P" de Psiphon en la esquina superior izquierda de su dispositivo indica que Psiphon se está ejecutando.

### 3. Psiphon para Windows

Descargue la última versión de Psiphon para Windows [aquí] (https://psiphon.ca/en/download.html). Verifique que el archivo descargado sea auténtico [aquí] (https://psiphon.ca/en/faq.html#authentic-windows).)

Cuando ejecute el programa, debería ver un aviso de seguridad que muestra que este programa es un producto legítimo de Psiphon Inc.

Psiphon comienza a conectarse automáticamente cuando lo ejecuta. Mientras se está conectando, se muestra un icono giratorio. La conexión con el servidor Psiphon se establece cuando se muestra el icono de la marca verde.

Cuando cierra el programa, Psiphon se desconecta automáticamente. También puede hacer clic en el icono para alternar la conexión.

### 4. Psiphon para iOS

Descargue Psiphon desde la [Apple App Store] (https://itunes.apple.com/us/app/psiphon/id1276263909?ls=1&mt=8).

Abra la aplicación y haga clic en el botón gris *Desconectado*.

![image](tool_psiphon7.png)

El botón se pondrá rojo cuando se esté conectando, y verde cuando se conecte.

![image](tool_psiphon8.png) ![image](tool_psiphon9.png)

Un icono de "VPN" en la esquina superior izquierda de su dispositivo indica que Psiphon se está ejecutando, lo que significa que otras aplicaciones accederán a Internet a través de Psiphon.

Para usar el navegador dedicado Psiphon para iOS se requiere una [descarga] separada (https://itunes.apple.com/us/app/psiphon-browser/id1193362444?mt=8), pero funciona en iOS 8 o posterior, mientras que La aplicación principal de Psiphon requiere iOS 10.2 o posterior. Si usa el navegador, solo la actividad en línea realizada en el navegador usará Psiphon. Otras aplicaciones se conectarán utilizando su conexión a Internet regular.