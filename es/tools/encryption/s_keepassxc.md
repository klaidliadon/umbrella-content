---
index: 6
title: KeePassXC
---
KeePassXC
=========

Administrador de contraseña segura

**Lección para leer: [Contraseñas](umbrella://information/passwords/advanced).**
**Nivel**: Principiante
**Tiempo requerido**: 5 minutos de configuración para una vida de uso de contraseña segura y feliz.
**Publicado:** abril 2018
**Fuentes:** Surveillance Self-Defense (EFF), [Cómo: Usar KeePassXC] (https://ssd.eff.org/en/module/how-use-keepassxc); [https://github.com/keepassxreboot/keepassxc/wiki](https://github.com/keepassxreboot/keepassxc/wiki).

**Usar KeepassXC le dará:**
\* La capacidad de usar muchas contraseñas diferentes en diferentes sitios y servicios sin tener que memorizarlas.

**Ubicación de la descarga:** Para Windows / Mac / Linux: [https://keepassxc.org/download](https://keepassxc.org/download)
**Requisitos de la computadora:** Windows 7 o superior, MacOS X 10.7 o superior, Linux (la mayoría de las distribuciones)
**Versión utilizada en esta guía**: KeePassXC 2.2.0 (KeePassXC es una versión multiplataforma del programa KeePass solo para Windows).
**Licencia**: FOSS (principalmente GPLv2)

Introducción
------------

KeePassXC es un administrador de contraseñas multiplataforma que le permite almacenar todas sus contraseñas en una ubicación. Un administrador de contraseñas es una herramienta que crea y almacena contraseñas para usted, por lo que puede usar muchas contraseñas diferentes en diferentes sitios y servicios sin tener que memorizarlas. Solo necesita recordar una contraseña maestra que le permita acceder a la base de datos del administrador de contraseñas cifradas de todas sus contraseñas.

_Hay varios programas con nombres similares a KeePassXC, como KeePassX, KeePass y KeePass2. Algunos de estos se basan en el mismo código, mientras que otros simplemente usan el mismo formato de base de datos. Esta guía recomienda_ [_KeePassXC_](https://keepassxc.org/) _porque es multiplataforma y está desarrollada más activamente que algunas de las alternativas._

Nota: el uso de un administrador de contraseñas crea un único punto de falla y establece un objetivo obvio para los malos actores o adversarios. La investigación sugiere que muchos administradores de contraseñas de uso común tienen vulnerabilidades, así que tenga cuidado al determinar si esta es o no la herramienta adecuada para usted.

Cómo funciona KeePassXC
-------------------

KeePassXC trabaja con bases de datos de contraseñas, que son archivos que almacenan una lista de todas sus contraseñas. Estas bases de datos se cifran cuando se almacenan en el disco duro de su computadora. Entonces, si su computadora está apagada y alguien la roba, no podrán leer sus contraseñas.

Las bases de datos de contraseñas se pueden cifrar utilizando una contraseña maestra. Ya que su contraseña maestra protege todas sus otras contraseñas, debe hacerlo lo más fuerte posible. (Aprenda a crear buenas [Contraseñas](umbrella://information/passwords/beginner).)

Usando una contraseña maestra
-----------------------

Una contraseña maestra actúa como una clave: para abrir la base de datos de contraseñas, necesita la contraseña maestra correcta. Sin ella, nadie puede ver lo que está dentro de la base de datos de contraseñas. Cuando use una contraseña maestra para asegurar su base de datos de contraseñas, aquí hay algunas cosas que debe tener en cuenta.

*   ¡Esta contraseña descifrará todas sus contraseñas, por lo que debe ser fuerte! Debería ser difícil de adivinar y largo. Cuanto más tiempo pase, menos tendrá que preocuparse por tener caracteres especiales o mayúsculas o números. Así que haga su contraseña maestra una frase de contraseña. Una frase de contraseña es una cadena de palabras que son fáciles de recordar pero difíciles de adivinar para otros.
*   Puede crear una frase maestra segura [usando palabras regulares y aleatorias](https://www.eff.org/dice). Estas son más fáciles de recordar que las combinaciones no naturales de símbolos y letras mayúsculas. (Obtenga más información sobre [Contraseñas](umbrella://information/passwords).)

Empezando con KeePassXC
------------------------------

Instalar KeePassXC y lanzarlo. Haga clic en el menú Archivo y seleccione "Crear nueva Base de Datos". Se le pedirá que guarde su base de datos de contraseñas. Tenga en cuenta que puede mover el archivo de la base de datos de contraseñas más tarde a donde desee en su disco duro, o moverlo a otras computadoras; aún podrá abrirlo con KeePassXC y la contraseña, o el archivo de claves, que especificó anteriormente.

![](tool_keepassxc1._creating_an_account.png)

**_¿Qué es un archivo de claves?_** _El uso de un archivo de claves además de su contraseña maestra puede dificultar que alguien descifre su base de datos de contraseñas si le roban una copia. Puede usar cualquier archivo existente como archivo de claves; por ejemplo, una imagen de su gato podría usarse como archivo de claves. Solo debe asegurarse de que el archivo que elija nunca se modifique, porque si se modifica su contenido, ya no descifrará la base de datos de contraseñas. A veces, abrir un archivo en otro programa puede ser suficiente para modificarlo, así que no lo abra, excepto para desbloquear KeePassXC. (Sin embargo, es seguro mover o cambiar el nombre del archivo de claves). Por lo general, una contraseña maestra segura es suficiente por sí sola. Si elige usar un archivo de claves además de su contraseña maestra, asegúrese de almacenarlo por separado de su base de datos de contraseñas.

A continuación, aparecerá un cuadro de diálogo que le pedirá que ingrese una contraseña maestra y/o que use un archivo de claves. Seleccione la(s) casilla(s) de verificación apropiada(s) según su elección.

Si desea ver la contraseña que está ingresando (en lugar de ocultarla con puntos), haga clic en el botón con el ojo a la derecha.

![](tool_keepassxc2._creating_master_key.png)

Organizando contraseñas
--------------------

KeePassXC le permite organizar las contraseñas en "Grupos", que básicamente son solo carpetas. Puede crear, eliminar o editar grupos o subgrupos yendo al menú "Grupos" en la barra de menú, o haciendo clic con el botón derecho en un grupo en el panel izquierdo de la ventana de KeePassXC. Agrupar contraseñas no afecta ninguna de las funciones de KeePassXC, es solo una herramienta organizativa útil.

Almacenar/generar/editar contraseñas
------------------------------------

Para crear una nueva contraseña o almacenar una contraseña que ya tiene, haga clic con el botón derecho en el Grupo en el que desea almacenar la contraseña y elija "Agregar nueva entrada". (También puede elegir "Entradas > Agregar nueva entrada" en el barra de menú.) Para el uso básico de contraseña:

*   Ingrese un título descriptivo que pueda usar para reconocer la entrada de la contraseña en el campo "Título". Por ejemplo, este podría ser el nombre del sitio web o el servicio para el que está la contraseña.
*   Ingrese el nombre de usuario asociado con la entrada de contraseña en el campo "Nombre de usuario". (Si no hay un nombre de usuario, deje esto en blanco).
*   Introduzca su contraseña en el campo "Contraseña". Si está creando una nueva contraseña, haga clic en el icono de dados a la derecha. Es posible que desee hacer esto cuando se está registrando para un nuevo sitio web, o cuando está reemplazando contraseñas antiguas y débiles con frases de contraseña nuevas, únicas y aleatorias. "Después de hacer clic en el icono de dados, aparecerá un diálogo de generador de contraseña. Puedes usar esto para generar una contraseña aleatoria. Hay varias opciones en este cuadro de diálogo, que incluyen qué tipo de caracteres incluir y cuánto tiempo se necesita para crear la contraseña.
    *   Tenga en cuenta que si genera una contraseña aleatoria, no tiene que recordar (¡ni siquiera saber!) Cuál es esa contraseña. KeePassXC lo guarda para usted, y en cualquier momento que lo necesite podrá copiarlo / pegarlo en el programa apropiado. Este es el objetivo de un administrador de contraseñas: puede usar diferentes contraseñas aleatorias largas para cada sitio web / servicio, ¡sin siquiera saber cuáles son las contraseñas!
    *   Debido a esto, debe establecer la contraseña siempre que el servicio lo permita y utilice tantos tipos de caracteres diferentes como sea posible.
*   Una vez que esté satisfecho con las opciones, haga clic en "Generar" en la esquina inferior derecha para generar la contraseña y luego haga clic en "Aceptar". La contraseña aleatoria generada se ingresará automáticamente en los campos "Contraseña" y "Repetir" para usted. (Si no está generando una contraseña aleatoria, deberá ingresar la contraseña elegida nuevamente en el campo "Repetir").
*   Haga clic en Aceptar. Su contraseña ahora está almacenada en su base de datos de contraseñas. Para asegurarse de que se guarden los cambios, guarde la base de datos de contraseñas editada en "Archivo> Guardar base de datos". (Como alternativa, si cometió un error, puede cerrar y volver a abrir el archivo de la base de datos y se perderán todos los cambios). )

![](tool_keepassxc3._adding_an_entry.png)

Si necesita cambiar / editar la contraseña almacenada, puede elegir su Grupo y luego hacer doble clic en su título en el panel de la derecha, y el cuadro de diálogo "Nueva entrada" aparecerá de nuevo.

Uso Normal
----------

Para usar una entrada en su base de datos de contraseñas, haga clic con el botón derecho en la entrada y elija "Copiar nombre de usuario al portapapeles" o "Copiar contraseña al portapapeles". Vaya a la ventana / sitio web donde desea ingresar su nombre de usuario / contraseña y péguelo en el campo apropiado. (En lugar de hacer clic con el botón derecho en la entrada, también puede hacer doble clic en el nombre de usuario o la contraseña de la entrada que desea, y el nombre de usuario o la contraseña se copiarán automáticamente en su portapapeles).

![](tool_keepassxc4._viewing_the_database.png)

![](tool_keepassxc5._using_an_entry.png)

Otras Características
--------------

KeePassXC le permite:

*   Buscar en su base de datos utilizando el cuadro de búsqueda (el cuadro de texto en la barra de herramientas de la ventana principal de KeePassXC).
*   Ordenar sus entradas haciendo clic en el encabezado de la columna en la ventana principal.
*   “Bloquee” KeePassXC seleccionando “Herramientas > Bloquear bases de datos”. Esto le permite dejar KeePassXC abierto, pero debe solicitar su contraseña maestra (y/o archivo de claves) antes de que pueda acceder a su base de datos de contraseñas nuevamente. También puede hacer que KeePassXC se bloquee automáticamente después de un cierto período de inactividad. Esto puede evitar que alguien acceda a sus contraseñas si se aleja de su computadora o la pierde. Para habilitar esta función en macOS, seleccione "Preferencias > Configuración" en el menú y haga clic en las opciones de seguridad. Luego marque la casilla que dice "Bloquear la base de datos después de la inactividad de \[número\] segundos". Para Linux o Windows, elija "Herramientas > Configuración" en el menú y haga clic en las opciones de seguridad. Luego marque la casilla que dice "Bloquear la base de datos después de la inactividad de \[número\] segundos".

KeePassXC también puede almacenar más que solo nombres de usuario y contraseñas. Por ejemplo, puede crear entradas para almacenar cosas importantes como números de cuenta, claves de producto, información de viajero frecuente de la aerolínea o números de serie. No es obligatorio que los datos que ingrese en el campo "Contraseña" tengan que ser una contraseña. Simplemente ingrese lo que desea almacenar en el campo "Contraseña" en lugar de una contraseña real (y deje el campo "Nombre de usuario" en blanco si no hay un nombre de usuario) y KeePassXC lo recordará de manera segura y segura.

Cómo instalar la extensión del navegador
------------------------------------

Una extensión del navegador es un componente de software que agrega características adicionales a su navegador web. El uso de la extensión KeePassXC proporciona una manera conveniente para que su navegador y su aplicación KeePassXC se comuniquen. Esto le permitirá guardar o rellenar automáticamente las contraseñas en la web.

Para integrar KeePassXC en su navegador necesita:

1.  Habilitar el protocolo HTTP KeePassXC

    Vaya a "Preferencias> Configuración" en el menú y haga clic en las opciones de HTTP. Luego marque la casilla que dice "Habilitar el protocolo HTTP KeePassXC". Esto permite que KeePassXC y la extensión del navegador se comuniquen.

2.  Descarga la extensión del navegador

    Para Firefox, instale [Passifox] (https://addons.mozilla.org/en-US/firefox/addon/passifox/). Para Chrome, instale [chromeIPass] (https://chrome.google.com/webstore/detail/chromeipass/ompiailgknfdndiefoaoiligalphfdae). Una vez que la instalación haya sido exitosa, verá un pequeño ícono de candado en la barra de herramientas de su navegador.

    ![](tool_keepassxc6._chromeipass_extension.png)

3.  Conecte la extensión del navegador a KeePassXC

    Para que KeePassXC y su navegador se comuniquen. necesitas conectarlos creando una asociación. Mientras KeePassXC se está ejecutando, abra su navegador y haga clic en el icono de la extensión KeePass. Haga clic en "Conectar".

    Aparecerá un cuadro de diálogo "Nueva solicitud de diálogo de asociación de clave". Asigne un nombre descriptivo a este nombre de asociación, por ejemplo, Cromo. El uso de un nombre descriptivo le ayuda a identificar esta asociación en el futuro.

    ![](tool_keepassxc7._enabling_browser_extension.png)


Ahora que su navegador está conectado con KeePassXC, verá este mensaje cuando haga clic en el icono de la extensión KeePass.

El uso de Autofill puede ser malo para su privacidad. Para deshabilitarlo, desmarque la configuración "Completar automáticamente la entrada de credenciales únicas" y "Activar autocompletar para los campos de nombre de usuario".

¡Ya está todo hecho! Ahora puede guardar cualquier credencial que ingrese en la web. También podrá completar automáticamente sus nombres de usuario/contraseñas.

KeePassXC es un software robusto y fácil de usar, y le recomendamos que explore el programa para aprender todas las cosas útiles que puede hacer.