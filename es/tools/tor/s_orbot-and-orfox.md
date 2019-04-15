---
index: 9
title: Orbot y Orfox
---
Orbot y Orfox
---

Navegación Web con Privacidad Mejorada para Android

**Lección para leer: [Internet](umbrella://communications/the-internet), [Teléfonos Móviles](umbrella://communications/mobile-phones)**
**Nivel**: Principiante
**Tiempo requerido**: 15 minutos.
**Publicado:** abril de 2018
**Fuentes:** Planificador de seguridad (Citizen Lab), [Orbot y Orfox] (https://securityplanner.org/#/tool/orbot-and-orfox); Security in a Box, [ORBOT PARA ANDROID] (https://securityinabox.org/en/guide/orbot/android/), The Guardian Project, [Orbot v16: ¡una apariencia completamente nueva y más fácil de usar!]  (https://guardianproject.info/2018/01/05/orbot-v16-a-whole-new-look-and-easier-to-use/)

**Usar Orbot y Orfox juntos le dará:**
- La capacidad de ocultar su identidad en línea de los sitios web y otros servicios al usar ciertas aplicaciones de Android.
- La capacidad de ocultar sus actividades de navegación al utilizar Orfox.
- La capacidad de eludir la censura de Internet y el filtrado en línea cuando se utiliza Orfox.

**Ubicación de la descarga:** [Orbot] (https://play.google.com/store/apps/details?id=org.torproject.android) and [Orfox] (https://play.google.com/store/apps/details?id=info.guardianproject.orfox) en la tienda Google Play.
**Requisitos de software:** Varía según el dispositivo (Orbot); Android 4.0.3 y superior (Orfox)
**Versión utilizada en esta guía**: Versión 16 (Orbot) Fennec-52.7.3esr / TorBrowser-7.5.3 / Orfox-1.5.2-RC-1 (Orfox)
**Licencia**: FOSS (principalmente GPLv2)


# 1. Introducción

Orbot permite que otras aplicaciones en dispositivos Android utilicen Internet de forma más segura a través de la red Tor. (Obtenga más información sobre [**Tor**](umbrella://communications/the-internet/advanced).) Orfox es una versión de Tor Browser para Android que usa Orbot para conectarse a la red Tor.

Recuerde, si usa Orfox para volver al contenido que ya ha creado sin usar Orfox, como en una publicación de blog, el sitio que aloja el contenido aún sabrá su ubicación real.

Si quiere un anonimato más fuerte mientras usa Orfox:

*   Nunca acceda a cuentas hechas con su nombre real.
*   Nunca dé sus datos personales.
*   Evita hacer las cosas que haces cuando no tratas de ser anónimo.


# 2. Instalar y configurar Orbot


## 2.1 Instalar Orbot

**Paso 1:** En su dispositivo Android, **descargue** e **instale** la aplicación desde  [Google Play store](https://play.google.com/store/apps/details?id=org.torproject.android) presionando INSTALAR.

![](orbot-and-002.png)

**Nota:** **Orbot** también se puede descargar desde la tienda de terceros [F-Droid] (https://guardianproject.info/fdroid/).


## 2.2 Configurar Orbot

**Paso 1:** Haga clic en **Abrir.**

![](orbot-and-005.png)

**Paso 2:** **Pase** a por las pantallas de bienvenida en el asistente de configuración, o toque la flecha Siguiente.

![](orbot-and-006.png) ![](orbot-and-007.png)

**Paso 3:** Si su acceso a la red Tor puede estar bloqueado, es posible que deba usar un puente.

![](orbot-and-009.png)  

![](orbot-and-010.png)

Si no está seguro de si necesita un puente, pruébalo sin ello primero. Para obtener más información sobre los puentes, lea *Configuración avanzada de Orbot: use un puente Tor* a continuación.

**Paso 4:** Si desea acceder a una aplicación que está bloqueada, use Orbot como una VPN (red privada virtual) haciendo clic en **Elegir Aplicaciones**.

![](orbot-and-008.png)

Seleccione las aplicaciones individuales que desea usar con **Orbot** y haga clic en *Aceptar*.

> "En lugar de promover algún tipo mágico automático de "habilitar Tor para todo mi dispositivo ", queremos centrarnos en las formas de permitir que aplicaciones específicas pasen por Tor, de una manera que podamos garantizar que sea lo más segura posible". —The Guardian Project, [27 de octubre de 2017] (https://guardianproject.info/2017/10/27/no-more-root-features-in-orbot-use-orfox-vpn-instead/)

Tenga en cuenta que muchas aplicaciones, como las que requieren que inicie sesión, socavarán su anonimato incluso si el tráfico de Internet se canaliza a través de Orbot. Este paso lo ayudará si un firewall o un filtro está bloqueando una aplicación individual, pero no lo convierte en anónimo.


![](orbot-and-011.png)

![](orbot-and-012.png)

Cuando haya terminado con la configuración, se le presentará la pantalla **Orbot** desactivada.

![](orbot-and-013.png)

# 3. Comience a usar Orbot

**Paso 1:** Toque el icono gris de Orbot en el centro de la pantalla hasta que se vuelva amarillo.

![](orbot-and-014.png) 

**Paso 2:** Cuando se conecta, Orbot se pone verde.

![](orbot-and-015.png) 

**Paso 3:** Toque el ícono verde hasta que se vuelva gris para desconectarse, o haga clic en el ícono del menú en la parte superior derecha de la pantalla y seleccione Salir para salir de la aplicación.

![](orbot-and-019.png)

**Paso 4:** Toque *Global (Automático)* para seleccionar de una lista de ubicaciones donde puede aparecer el tráfico de Internet.

![](orbot-and-022.png)

**Paso 5.** Alternar el modo VPN *Activado* para acceder a las aplicaciones enumeradas mediante el túnel de su tráfico de Internet a través de Orbot. Agregue más aplicaciones a la lista haciendo clic en *Aplicaciones habilitadas para Tor* en la parte inferior de la pantalla.


# 4. Configuración avanzada de Orbot: use un puente Tor

Si el acceso a Tor está restringido o si desea disimular el hecho de que está usando Tor, puede configurar Orbot para que use *puentes*. Obtenga más información sobre puentes en la guía de herramientas [Tor para LINUX] (umbrella://tools/tor/s_tor-for-linux.md)

**Paso 1:** Toque el icono del menú en la parte superior derecha y seleccione *Configuración*. Desplácese hacia abajo hasta *Bridges.* Marque la casilla junto a *Usar Puentes*.

![](orbot-and-025.png)

**Paso 2:** Si conoce la *dirección IP* de un *puente* que desea usar, toque *dirección IP y puerto de puentes*. Ingrese la dirección IP y toque *OK*.

![](/media/orbot-and-026.png)

**Paso 3:** Reinicie **Orbot** para comenzar a usar el *bridge*.

Puede leer más sobre los puentes en el [sitio web del proyecto Tor] (https://bridges.torproject.org/).


# 5. Instalar Orfox

**Paso 1:** En su dispositivo Android, **descargue** e **instale** la aplicación desde [Google Play store] (https://play.google.com/store/apps/details?id=info.guardianproject.orfox).

**Nota:** **Orfox** también se puede descargar desde la tienda de terceros [F-Droid] (https://guardianproject.info/fdroid/).

**Paso 2:** Para abrir Orfox, **toque** el ícono de la aplicación.

**Orfox** le dará la opción de conectarse a _https: //check.torproject.org_, para asegurarse de que su conexión a la red **Tor** esté funcionando. Si se puede conectar, verá un mensaje que te dice que su _navegador está configurado para usar Tor_. Si **Orfox** no puede conectarse al sitio web, verá un mensaje de error en el navegador. Si esto sucede, compruebe que Orbot se está ejecutando.

**Paso 3:** Para navegar a sitios web, **toque** el área en la parte superior de la pantalla y escriba la dirección que desea visitar. Presione *Go* en el teclado en pantalla.


# 6. Borrar el historial de su navegador Orfox

**Paso 1:** Para borrar manualmente su historial de navegación y caché, y ocultar los sitios web que ha visitado en Orfox, toque el ícono del menú principal con tres puntos en la esquina superior derecha, luego *Configuración*.

**Paso 2:** Pulse en *Borrar datos privados,* luego *BORRAR DATOS,* para eliminar datos de las categorías enumeradas.

Nota: Al configurar esto, no podrá presionar el botón Atrás para ver las páginas web que ya ha visitado.

**Paso 3:** Vuelva al menú *Configuración* y seleccione *Privacidad.* Seleccione _ Eliminar datos privados al salir_ para borrar automáticamente los datos privados cuando sale de la aplicación a través del menú principal.

Nota: Seleccionar *Nueva pestaña privada* en el menú principal también evitará que Orfox grabe cualquier historial de navegación. Los archivos que descargue y las páginas web que marque aún se guardarán en su dispositivo.

# 7. Personalice su seguridad de navegador

Orfox incluye una función de control deslizante de seguridad que le permite elegir entre las configuraciones de seguridad Estándar, Segura y Más segura. Toque en el icono del menú principal con tres puntos en la esquina superior derecha, luego *Configuración de Orfox*. Las configuraciones más seguras y seguras harán que algunas funciones del sitio web se rompan, pero estará menos expuesto a las vulnerabilidades que los piratas informáticos pueden explotar para atacarle.