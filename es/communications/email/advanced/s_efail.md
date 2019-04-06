---
index: 6
title: Efail
---
**Efail**
=====================================

**Fecha:** 15 de mayo de 2018.

Esta semana, los investigadores de seguridad publicaron información sobre las vulnerabilidades en los clientes de correo electrónico de PGP que podrían exponer el contenido pasado o futuro, incluso si estaba cifrado. EFF [advirtió] (https://www.eff.org/deeplinks/2018/05/not-so-pretty-what-you-need-know-about-e-fail-and-pgp-flaw-0) a usuarios de estos clientes de correo electrónico deshabilitar o desinstalar complementos de PGP y cambiar a otro método de comunicación seguro. La lista de clientes de correo electrónico incluye Thunderbird con Enigmail, que se recomienda en las guías de herramientas de Umbrella PGP para [Linux] (umbrella://lesson/pgp-for-linux), [Mac OS] (umbrella://lesson/pgp-for-mac-os-x), y [Windows] (umbrella://lesson/pgp-for-windows).) .
.

Esto es lo que necesita saber:

* Los servicios de mensajería segura como Signal son más fáciles, más comunes y, por lo tanto, más confiables que el cifrado de correo electrónico. Así que este es un buen consejo. Si está enviando información confidencial, hágalo en un mensaje seguro en lugar de un correo electrónico. (Obtenga más información sobre [enviar un mensaje] (umbrella://lesson/sending-a-message).)
* EFF sugiere desactivar los clientes de correo electrónico de PGP para evitar que descifren mensajes automáticamente, lo que *podría* hacer que el contenido sea vulnerable. Este también es un buen consejo, pero como dice la EFF, es un recurso provisional "conservador". *No* significa que el cifrado PGP es inseguro, o que debe enviar correo electrónico sin cifrar.
* Como en todos los escenarios de seguridad, considere su modelo de amenaza personal. (Obtenga más información sobre [gestión de la información](umbrella://lesson/managing-information).) Si corre un alto riesgo de ataques sofisticados y dirigidos contra el contenido de correo electrónico cifrado, será apropiado realizar una pausa conservadora. Si su riesgo es bajo, puede que no lo sea.

Si elige continuar utilizando el correo electrónico, cifrarlo utilizando PGP es mucho mejor que no cifrarlo. Pero haga lo siguiente:

1. Asegúrese de que todo el software que está ejecutando esté actualizado. Instale nuevas actualizaciones *inmediatamente*. (Hará esto de todos modos si ha leído la lección de Umbrella [malware](umbrella://lesson/malware) lesson.)
2. Verifique la [configuración] (https://twitter.com/GPGTools/status/995986721891405825?s=19) en su cliente de correo electrónico para obtener una opción para "Cargar contenido remoto en los mensajes". Esta opción debe estar deshabilitada o *desactivada*. Esto se debe a que el ataque supone que un pirata informático ya puede acceder a su correo electrónico cifrado y cambiar el código HTML que extrae parte del contenido, como imágenes, desde un servidor remoto. Ese cambio podría permitirles ver todo el correo electrónico sin cifrado si el cliente de correo electrónico aún no ha implementado la actualización correcta.
3.  Siga los desarrollos de Efail cuidadosamente. Publicaremos actualizaciones en Twitter [@_SecurityFirst] (https://twitter.com/_SecurityFirst).