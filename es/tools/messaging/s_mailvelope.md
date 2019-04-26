---
index: 7
title: Mailvelope
---
Mailvelope  
====================

Webmail Seguro

**Lección para leer: [Protección de Archivos] (umbrella://information/protecting-files), [Email](umbrella://communications/email)**
**Nivel:** Avanzado
**Tiempo requerido:** 30-60 minutos.
**Actualizado:** Abril de 2018 (algunas imágenes datan de versiones anteriores)
**Fuentes: ** Security in a Box, [MAILVELOPE - CIFRADO OPENPGP PARA WEBMAIL] (https://securityinabox.org/en/guide/mailvelope/web/).

**Usar Mailvelope le brindará:**

- La capacidad de enviar y recibir correo electrónico cifrado de extremo a extremo que no pueden ser leídos por terceros.
- La capacidad de firmar su correo electrónico digitalmente y autenticar el correo electrónico firmado de otros.


**Ubicación de la Descarga:** [https://www.mailvelope.com/en]((https://www.mailvelope.com/en))
**Versión utilizada en esta guía:** 1.5.1
**Licencia:** Software libre y de código abierto
**Requisitos del Sistema:** **Mozilla Firefox**, **Google Chrome** o **Chromium** ejecutándose en LINUX, Windows o Mac.




# 1. Introducción

Mailvelope es una extensión del navegador que le permite cifrar, descifrar, firmar y autenticar mensajes de correo electrónico y archivos con OpenPGP. (Una extensión del navegador es un componente de software que agrega características adicionales a su navegador web). Funciona con el correo web y no requiere que descargue ni instale software adicional. Si bien Mailvelope carece de muchas de las funciones proporcionadas por Thunderbird, Enigmail y GnuPG, es probablemente la forma más fácil para que los usuarios de correo web comiencen a aprovechar el cifrado de extremo a extremo.

## 1.0 Cosas que debe saber sobre Mailvelope antes de comenzar

Mailvelope se basa en una forma de *criptografía de clave pública* que requiere que cada usuario genere su propio par de *claves*. Este *par de claves* se puede usar para cifrar, descifrar y firmar contenido digital, como mensajes de correo electrónico. Incluye una *clave privada* y una *clave pública*:

- Su **clave privada** es extremadamente sensible. Cualquier persona que haya logrado obtener una copia de esta clave podrá leer el contenido cifrado que fue diseñado solo para usted. También podrían firmar mensajes, por lo que parecía que *venían de su parte*. Su *clave privada* está, en sí misma, encriptada a una frase de contraseña que elegirá cuando genere su *par de claves*. Debe elegir una frase de contraseña segura y tener cuidado de no permitir que nadie acceda a su *clave privada*. Utilizará su *clave privada* para descifrar los mensajes que le envíen aquellos que tienen una copia de su *clave pública*.

- Su **clave pública** está destinada a ser compartida con otros y no puede usarse para leer un mensaje cifrado o falsificar uno firmado. Una vez que tenga la clave pública de un corresponsal, puede comenzar a enviarle mensajes cifrados. Solo ella podrá descifrar y leer estos mensajes porque solo ella tiene acceso a la *clave privada* que coincide con la *clave pública* que está utilizando para cifrarlos. De manera similar, para que alguien le envíe a *usted* un correo electrónico cifrado, debe obtener una copia de su *clave pública*. Es importante verificar que la *clave pública* que está utilizando para cifrar el correo electrónico realmente pertenezca a la persona con la que está tratando de comunicarse. Si usted o su interlocutor son engañados para que cifren el correo electrónico con la clave pública incorrecta, su conversación no será segura.

Mailvelope también le permite adjuntar firmas digitales a sus mensajes. Si *firma* un mensaje usando su *clave privada*, cualquier destinatario con una copia de su *clave pública* puede verificar que usted lo envió y que su contenido no fue manipulado. Del mismo modo, si tiene una *clave pública* correspondiente, puede verificar sus firmas digitales.

Mailvelope te permite:

- Generar un par de claves de cifrado
- Exportar su clave pública para que pueda compartirla con otros
- Importar claves públicas de otras personas
- Redactar, cifrar y firmar mensajes de correo electrónico
- Descifrar y autenticar mensajes
- Cifrar, adjuntar y descifrar archivos

Sus corresponsales no tienen que usar Mailvelope, pero sí tienen que usar algún tipo de cifrado OpenPGP, algunos de los cuales se enumeran a continuación.

Dado que Mailvelope es una extensión del navegador, solo funcionará con el navegador en el que se instaló. Si desea utilizar Mailvelope con un navegador diferente, tendrá que volver a instalarlo. Esto es cierto incluso si ambos navegadores están en la misma computadora. También tendrá que exportar todas sus claves e importarlas a la nueva copia de Mailvelope.


## 1.1 Otras herramientas como Mailvelope

Debido a que Mailvelope es una extensión del navegador, funciona en la mayoría de los sistemas operativos de escritorio. Esto incluye GNU / Linux, Microsoft Windows y Mac OS X. No funciona en dispositivos móviles Android o iOS. A continuación se presentan algunas alternativas gratuitas y de código abierto:

- [**Thunderbird con Enigmail**] (../../thunderbird/windows) completa el cliente de correo electrónico con cifrado PGP agregado para GNU/Linux, Microsoft Windows y Mac OS X
- [**GPG4Win**] (https://www.gpg4win.org/) Conjunto de herramientas de cifrado de archivos y correo electrónico de PGP para Microsoft Windows
- [**GPG Tools Suite**] (https://gpgtools.org/) para Mac OS X
- [**gpg4usb**] (https://www.gpg4usb.org/) herramienta PGP portable e independiente para GNU/Linux y Microsoft Windows
- [**Mailpile**] (https://www.mailpile.is/) Un venidero cliente de correo compatible con OpenPGP para GNU/Linux, Microsoft Windows y Mac OS X


# 2. Generar y compartir claves de cifrado.

Antes de que pueda comenzar a cifrar y descifrar el correo electrónico, debe seguir tres pasos preparatorios:

- Genere su par de claves de cifrado (o impórtelo si ya tiene uno)
- Exporte su clave pública y envíela a sus contactos.
- Importe claves públicas de sus contactos.


## 2.1 Generar un par de claves

Para generar su par de claves, abra el navegador donde instaló Mailvelope y siga los pasos a continuación.

**Paso 1**. **Haga clic** en el icono de candado de **Mailvelope** en la barra de herramientas de su navegador para activar la siguiente pantalla:

![](mailvelope-all-en-v01-002.png)

**Paso 2**. **Haga clic** en **[Opciones]** para activar la pantalla de *Opciones* de Mailvelope

![](mailvelope-all-en-v01-003.png)

**Paso 3**. **Haga clic** en **[Generar clave]** y **escriba** su información en los campos, como se muestra a continuación:

![](mailvelope-all-en-v01-004.png)

**Importante:**

- Elija una contraseña segura para proteger su clave privada. (Aprenda a crear [Contraseñas] seguras (umbrella://information/passwords/beginner).)
- No tiene que usar su nombre real al generar su clave, pero debe ingresar la dirección de correo electrónico de la cuenta con la que desea usar Mailvelope. Si lo desea, puede crear una nueva cuenta de correo electrónico específicamente para este propósito.
- Le recomendamos que genere un par de claves único para cada cuenta de correo electrónico que desee usar con Mailvelope.

**Paso 4**. **Desmarque** el cuadro *Cargar clave pública al Servidor  de Claves de Mailvelope*

**Paso 5**. **Haga clic** en **[Enviar]** para comenzar a generar su par de claves:

![](mailvelope-all-en-v01-005.png)

Cuando termine, Mailvelope mostrará: "**Éxito. Nueva clave generada e importada al conjunto de claves**".

**Paso 6**. **Haga clic** en *Mostrar claves* para ver su nuevo par de claves, como se muestra en la siguiente sección



## 2.2 Exportar y enviar su clave pública con Mailvelope

Debe compartir su clave pública con otros para que le envíen un correo electrónico cifrado. También debe compartir la *huella digital* completa de su clave, a través de un canal diferente, para que sus corresponsales puedan verificar que la clave pública que usted les envió realmente le pertenece. **Nunca debe compartir su clave privada**, ya que cualquier persona que tenga una copia de ella puede descifrar los mensajes que se le envíen y firmarlos para que parezcan provenir de usted.

Para exportar su clave pública con Mailvelope, siga los pasos a continuación.

**Paso 1**. En la pestaña del navegador **Opciones de Mailvelope**, **seleccione** la pestaña **Gestión de Claves** y luego **haga clic** en **[Mostrar Claves]**, a la izquierda.

![](mailvelope-all-en-v01-006.png)

**Paso 2**. ** Haga clic en ** la clave que desea exportar. (En nuestro caso, la clave pública que acabamos de generar es la única que tenemos).

Esto activará la siguiente pantalla:

![](mailvelope-all-en-v01-007.png)

Esta pantalla muestra, entre otras cosas, la huella digital de su par de claves. Por ejemplo, la huella digital del par de claves que acabamos de generar para *ekaterina@riseup.net* es **3B9F 54DD 571A 6F77 251D 92E7 E8B1 F5E6 FBB4 EFFE**.

**Paso 3**. ** Haga clic** en la **pestaña** Exportar.

![](mailvelope-all-en-v01-008.png)

**Importante:** Asegúrese de que **[Público]** esté seleccionado en la parte superior de la pantalla. Si se selecciona *[Privado]* o *[Cualquiera]*, terminará exportando su clave privada. Nunca debe enviar su clave privada a otra persona ni subirla a un servidor. (Las únicas razones por las que puede querer exportar su clave privada son hacer una copia de seguridad cifrada o migrar sus claves a un nuevo navegador web). El nombre de archivo predeterminado debe terminar con "_Pub.asc".

**Paso 5**. **Haga clic** en **[Guardar]** para guardar su clave pública

**Paso 6**: envíe el archivo que acaba de exportar (*Elena_Katerina_Pub.asc*, en este caso) a los corresponsales con los que desea intercambiar correos electrónicos cifrados.



## 2.3 Importar una clave pública con Mailvelope

Antes de poder cifrar un mensaje a un corresponsal, debe importar su clave pública. Para importar la clave pública de un corresponsal utilizando Mailvelope, siga los pasos a continuación.

**Paso 1**. Después de recibir una clave pública como archivo adjunto, guarde el archivo en algún lugar de su computadora.

**Paso 2**. En la pestaña del navegador **Opciones de Mailvelope**, **seleccione** la pestaña **Gestión de Claves** y luego **haga clic** en **[Importar Claves]** a la izquierda.

![](mailvelope-all-en-v01-009.png)

En esta pantalla, puede:

- Buscar un servidor de clave pública ingresando el nombre, la dirección de correo electrónico o la ID de su correspondiente
- Seleccionar un archivo de texto que contenga una clave
- Copiar y pegar el bloque de texto dentro de un archivo de clave

Los pasos a continuación suponen que recibió un archivo de clave y lo guardó en su computadora, por lo que usaremos la segunda opción.

**Paso 3**. **Haga clic** en **[Seleccionar un texto de clave para importar]**.

**Paso 4**. **Navegue** al archivo clave en su computadora y **haga clic** en **[Importar]**

Cuando termine, Mailvelope mostrará algo como: "**¡Éxito! Clave pública 6764717C5D64FBB6 del usuario Mansour <mansour@riseup.net> importada al repositorio de claves**"

Si hace clic en **[Mostrar claves]**, a la izquierda, en la pestaña **Gestión de Claves**, debería ver su clave pública recién importada:

![](mailvelope-all-en-v01-010.png)

Antes de enviar un mensaje cifrado a este corresponsal, debe verificar su clave.



## 2.4 Verificar la clave pública de un corresponsal

Ahora debe verificar que la clave que ha importado proviene realmente de la persona a la que cree que pertenece. Usted y sus corresponsales de correo electrónico deben pasar por este proceso para cada clave pública que reciba.

Para verificar la clave pública de su corresponsal, comuníquese con él utilizando un medio de comunicación que le permita estar absolutamente seguro de que está hablando con la persona adecuada. Las reuniones en persona son las mejores, pero las conversaciones de voz y video son aceptables si está seguro de que puede reconocer la voz o la apariencia. Intercambiará huellas dactilares de claves públicas, que no es necesario que se mantengan en secreto, por lo que esta conversación no tiene que ser confidencial siempre que se abstenga de hablar de temas delicados.

Tanto usted como su interlocutor deben verificar las huellas digitales de las claves públicas que ha intercambiado. Una huella digital es una serie única de números y letras que identifica una clave. Puede usar la sección **Mostrar Claves** de la pestaña **[Gestión de Claves]** en **Opciones de Mailvelope** para determinar:

- La huella digital del par de claves que ha generado.
- La huella digital de las claves públicas de otras personas que ha importado.

Para ver la huella digital de un par de claves en particular, siga los pasos a continuación:

**Paso 1**. **Haga clic** en **[Mostrar claves]**, a la izquierda, en la pestaña **Gestión de Claves**.

![](mailvelope-all-en-v01-010.png)

**Paso 2**. **Haga clic** en la clave que desee verificar

![](mailvelope-all-en-v01-035.png)

En la ventana Detalles de Clave, verá la **huella digital** de la clave seleccionada. Por ejemplo, la huella digital de ekaterina@riseup.net es *3B9F 54DD 571A 6F77 251D 92E7 E8B1 F5E6 FBB4 EFFE*.

Su corresponsal también debe llevar a cabo estos pasos. Para verificar las huellas dactilares:

- Lea la huella digital de su par de claves a su corresponsal,
- Pídale que verifique que la huella digital que tiene para su clave pública coincide con lo que acaba de decirle.
- Haga que su corresponsal le lea la huella digital de su clave pública,
- Verifique que la huella digital que tiene para su clave pública coincida con lo que le acaba de decir.
- Si las huellas digitales no coinciden, vuelva a intercambiar las claves públicas y repita el proceso.

Nota: Debido a que las huellas digitales de clave no son sensibles, puede anotar fácilmente la huella dactilar que le lea su interlocutor. Luego, cuando tenga más tiempo, puede verificar que coincida con la huella digital que tiene para su clave pública. Esta es también la razón por la que algunas personas imprimen sus huellas digitales en sus tarjetas de negocio.


## 2.5 Hacer copia de seguridad y recuperar todas sus claves

Los pares de claves que ha generado y las claves públicas que ha recopilado y verificado son el elemento más importante de su instalación de Mailvelope. Puede guardar todas estas claves en un solo archivo para hacer una copia de seguridad de ellas. Consulte [Recuperarse de la pérdida de información] (../../backup) para planificar una estrategia de copia de seguridad segura. Recomendamos actualizar esta copia de seguridad cada vez que genere un nuevo par de claves o importe y verifique una clave pública importante.

**Importante:** Debido a que este archivo contendrá su clave privada, no debe subirla a un servidor ni a ningún tipo de "almacenamiento en la nube".


**Para guardar todas sus claves en un solo archivo**, siga los pasos a continuación desde la pestaña Mailvelope **Gestión de Claves**

**Paso 1**. **Haga clic** en **[Mostrar Claves]**

![](mailvelope-all-en-v01-011.png)

**Paso 2**. **Haga clic** en **[Exportar]**

![](mailvelope-all-en-v01-012.png)

**Nota:** Puede elegir cualquier nombre y ubicación para el archivo que contendrá sus claves. En este ejemplo, usaremos el nombre predeterminado: **all_keys.asc**

**Paso 3**. **Haga clic** en **[Guardar]**

**Paso 4**. Haga una copia de seguridad de este archivo y luego elimínelo de su computadora.

**Importante:** Este archivo contiene su(s) clave(s) privada(s), por lo que debe mantener su copia de seguridad segura. Por ejemplo, es posible que desee almacenarlo en un contenedor cifrado de VeraCrypt en un dispositivo de almacenamiento USB bien oculto.

**Para importar todas las claves en este archivo**, siga los pasos para *Importar la clave pública de un corresponsal* en la Sección 2.3.


# 3. Configure Mailvelope para trabajar con su servicio de correo web

Mailvelope viene preconfigurado para trabajar con varios servicios de correo web, incluido Gmail. Puede verificar si Mailvelope ya está configurado para trabajar con su proveedor de correo web iniciando sesión en su cuenta de correo electrónico y redactando un nuevo mensaje. Debería ver un botón de Mailvelope en la esquina superior derecha del área de mensajes, como se muestra a continuación:

![](mailvelope-all-en-v01-016.png)

Si ve este botón, puede omitir los pasos restantes en esta sección.

Para hacer que Mailvelope funcione con la interfaz de correo web *Roundcube * utilizada por [Riseup] (https://mail.riseup.net) y otros proveedores, siga los pasos a continuación. Siguiendo un proceso similar, también debería poder configurar Mailvelope para otros proveedores de correo web.


**Paso 1**. **Inicie** el navegador en el que instaló Mailvelope

**Paso 2**. **Inicie sesión** en su cuenta de correo electrónico.

**Paso 3**. **Navegue** a su bandeja de entrada y **abra** cualquier mensaje de correo electrónico

**Paso 4**. **Haga clic** en el icono de candado de Mailvelope en la barra de herramientas de su navegador para abrir el menú de Mailvelope como se muestra a continuación

![](mailvelope-all-en-v01-013.png)

**Paso 5**. **Haga clic** en **[Agregar]** para mostrar una pantalla que contiene una **Lista de Proveedores de Correo Electrónico**

![](mailvelope-all-en-v01-014.png)

En la parte inferior de esta lista, debería ver una nueva entrada para **mail.riseup.net**.

**Paso 6**. Vuelva a la pestaña del navegador con su webmail.

**Paso 7**. **Haga clic en redactar** para escribir un nuevo correo electrónico.

**Paso 8**. **Haga clic** en el icono de candado de Mailvelope en la barra de herramientas de su navegador para abrir el menú de Mailvelope como se muestra a continuación

![](mailvelope-all-en-v01-015.png)

**Paso 8**. **Haga clic** en **[Agregar]** de nuevo.

Su navegador mostrará una vez más una pantalla que contiene una **Lista de Proveedores de Correo Electrónico**.

**Paso 9**. **Cierre** esta pestaña del navegador y vuelva a su webmail.

**Paso 10**. **Recargue** la página en la que está redactando un nuevo correo electrónico.

Debería ver un botón de Mailvelope en la esquina superior derecha del área de mensajes, como se muestra a continuación:

![](mailvelope-all-en-v01-016.png)


# 4. Cifrar y descifrar mensajes y archivos.

Después de intercambiar las claves y asegurarse de que Mailvelope esté configurado para trabajar con su proveedor de correo web, puede comenzar a cifrar y descifrar los mensajes.

Para obtener una explicación de cómo funciona Mailvelope, consulte la sección [Cosas que debe saber sobre esta herramienta antes de comenzar] (#things-you-should-know-about-mailvelope-before-you-startr), más arriba. Y tenga en cuenta que Mailvelope solo protege el *contenido* de los mensajes y archivos adjuntos. **La siguiente información nunca está encriptada:**

- La línea *Asunto*.
- La dirección de correo electrónico del remitente.
- Las direcciones de correo electrónico de los destinatarios.
- Nombres de archivos adjuntos
- Cualquier nombre real que pueda estar asociado con remitentes y destinatarios ("**Elena S. Katerina**", por ejemplo, en la siguiente dirección de correo electrónico: "**Elena S. Katerina <ekaterina@riseup.net>**")

Por lo tanto, elija sus líneas de asunto con cuidado y considere crear un par de claves para al menos una cuenta de correo electrónico que no incluya su nombre real.

Finalmente, cuando envíe un correo electrónico encriptado, tenga la seguridad de que una copia, encriptada a su clave pública, se colocará en su carpeta de correo enviado.



## 4.1 Cifrado de mensajes con Mailvelope

Con el navegador en el que instaló Mailvelope, inicie sesión en una cuenta de correo web con la cual Mailvelope se haya configurado para funcionar, luego comience a escribir un nuevo mensaje y siga los pasos a continuación:

**Paso 1**. Rellene los campos **Para:**, **Cc:** y **Asunto:**, como de costumbre:

![](mailvelope-all-en-v01-017.png)

**Nota:** Si no ve el botón Mailvelope en la esquina superior derecha del área de mensajes, consulte la sección *Configurar mailvelope para trabajar con su proveedor de correo web*, arriba.

**Paso 2**. **Haga clic** en el botón Mailvelope en la esquina superior derecha del área de mensajes para abrir la ventana **Redactar Email** de Mailvelope.

![](mailvelope-all-en-v01-018.png)

**Paso 3**. **Escriba** tu mensaje.

**Importante:** *Si pretende cifrar un mensaje, debe escribirlo en la ventana especial **Redactar Email** de Mailvelope, en lugar del área de texto normal que muestra su interfaz de correo web.* De lo contrario, su proveedor de correo web puede grabar borradores sin terminar, mientras escribe, sin que usted lo sepa.

Todas las direcciones de correo electrónico en los campos **Para:**, **Cc:** y **Bcc:** se copiarán en el campo *destinatarios* de la ventana *Redactar Correo electrónico* de Mailvelope's. Su mensaje se cifrará en todas las claves públicas asociadas con las direcciones que se muestran aquí (y también en su propia clave pública). Puede agregar o eliminar direcciones manualmente en la ventana *Redactar Email*. Si alguna de estas direcciones está **marcada en rojo**, indica que no tiene una clave pública para ese destinatario y que no podrá enviar el mensaje a menos que elimine ese destinatario u obtenga su clave pública.

**Nota:** Debido a la forma en que funciona OpenPGP, no debe confiar en el campo **Bcc** para ocultar la existencia de algunos destinatarios de otros destinatarios.

**Paso 3**. Cuando haya terminado de seleccionar destinatarios y redactar su mensaje, **haga clic en [Encriptar]**. Su mensaje se cifrará y se transferirá al área de mensajes normal de su correo web.

![](mailvelope-all-en-v01-019.png)

**Paso 4**. **Haga clic en [Enviar]**.


## 4.2 Descifrando mensajes con Mailvelope

Con el navegador en el que instaló Mailvelope, inicie sesión en una cuenta de correo web con la cual Mailvelope se haya configurado para funcionar, abra un mensaje cifrado que se le ha enviado y siga los pasos a continuación:

Mailvelope detectará automáticamente si un mensaje entrante está encriptado. Mostrará el icono de Mailvelope sobre el mensaje cifrado, como se muestra a continuación

![](mailvelope-all-en-v01-020.png)

**Paso 1**. ** Haga clic** en el icono de Mailvelope para activar la pantalla de contraseña.

**Paso 2**. **Escriba** la frase de contraseña que eligió cuando generó su par de claves

![](mailvelope-all-en-v01-021.png)

**Importante:** Si marca la casilla *Recordar contraseña temporalmente*, Mailvelope recordará su contraseña durante 30 minutos. (Puede cambiar este período de tiempo en las Opciones de Mailvelope). Recomendamos desactivar esta casilla a menos que esté a punto de descifrar muchos mensajes.

**Paso 3**. **Haga clic en** **[OK] ** para descifrar el mensaje

![](mailvelope-all-en-v01-022.png)

**Nota:** Si Mailvelope muestra un mensaje que dice: *¡Error! No se encontró una clave privada para este mensaje*, significa que el remitente no cifró este mensaje en su clave pública (y puede que ni siquiera *tenga* su clave pública). No podrá descifrar el mensaje. Póngase en contacto con el remitente y pídale que vuelva a enviar el mensaje cifrado a su clave. También es posible que desee enviarle su clave y ofrecerle verificar su huella digital.

**Importante**: En general, no es una buena idea hacer copias sin cifrar de mensajes cifrados o archivos adjuntos y almacenarlos en su computadora.

## 4.3 Firmar mensajes y verificar firmas con Mailvelope

Además de cifrar los mensajes a la clave pública de otra persona, Mailvelope puede *firmarlos* con su propia clave privada. De esa manera, los destinatarios que tienen su clave pública pueden verificar que un mensaje en particular realmente vino de usted y no se modificó en tránsito.

Mailvelope no le permite actualmente firmar y cifrar el mismo mensaje.


### 4.3.1 Firmar un mensaje

Para firmar un mensaje, siga los pasos a continuación.

**Paso 1**. Redacte un mensaje en la ventana * Redactar Email* de Mailvelope, como se muestra a continuación:

![](mailvelope-all-en-v01-029.png)

**Paso 2**. **Haga clic** en **[Firmar]**.

![](mailvelope-all-en-v01-030.png)

**Paso 3**. **Seleccione** una clave privada para usar al firmar el mensaje.

**Paso 4**. **Haga clic** en **[Aceptar]**.

**Paso 5**. **Escriba** la frase de contraseña para la clave que ha seleccionado.

![](mailvelope-all-en-v01-031.png)

Tenga en cuenta que deseleccionamos la opción *Recordar contraseña temporalmente*.

**Paso 6**. **Haga clic** en **[Aceptar]**.

El mensaje firmado se copiará en el área de mensajes de su correo web, como se muestra a continuación:

![](mailvelope-all-en-v01-032.png)

**Importante:** Cuando firma un correo electrónico, no se cifrará. Tenga en cuenta que todavía puede leer el contenido del mensaje anterior. El bloque de texto *debajo* del mensaje es la firma digital. No edite el mensaje antes de enviarlo. Si lo hace, se le informará a los destinatarios que su firma no es válida.

**Paso 7**. **Haga clic** en **[Enviar]**.



### 4.3.2 Verificando un mensaje firmado

Para verificar un mensaje firmado, siga los pasos a continuación mientras ve el mensaje.

![](mailvelope-all-en-v01-033.png)

**Paso 1**. **Haga clic** en el sobre con el sello rojo que se muestra sobre el mensaje.

Si tiene la clave pública para este remitente, debe aparecer un cuadro verde sobre el mensaje para hacerle saber que la clave privada correspondiente *la firmó* y que no se modificó durante el transporte.

![](mailvelope-all-en-v01-034.png)

**Importante:** Si ve un cuadro rojo que dice *Firma no válida*, es posible que el mensaje haya sido manipulado o enviado por otra persona. Debe comunicarse con la persona en el campo **De:** utilizando algún otro canal de comunicación y confirmar que ella lo envió.

Si ve un cuadro amarillo que dice *Firmado con una clave desconocida*, significa que no tiene una clave pública que se corresponda con la clave privada utilizada para firmar el mensaje. No podrá verificar la firma hasta que obtenga y valide la clave pública correcta.

## 4.4 Cifrado y descifrado de archivos con Mailvelope

Mailvelope también puede cifrar y descifrar archivos. Los archivos cifrados se pueden adjuntar a los mensajes de correo electrónico.

### 4.4.1 Encriptar y adjuntar archivos

Para cifrar un archivo, siga los pasos a continuación utilizando el navegador en el que instaló Mailvelope.

**Paso 1**. **Haga clic** en el icono de bloqueo de Mailvelope en la barra de herramientas de su navegador y **seleccione** **Opciones** para abrir la pestaña del navegador **Opciones de Mailvelope**.

**Paso 2**. **Seleccione** la pestaña **[Cifrado de Archivo]**.

**Paso 3**. **Haga clic** en **Cifrado** en el lado izquierdo.

**Paso 4**. **Haga clic** en **[+ Agregar]** para seleccionar los archivos que desea cifrar, como se muestra a continuación.

![](mailvelope-all-en-v01-023.png)

En este ejemplo, seleccionamos un archivo de imagen llamado *picture.png*. Puede agregar más de un archivo. Cada uno de ellos se cifrará por separado a las claves públicas que seleccione.

**Paso 5**. **Haga clic** en **[Siguiente]**.

![](mailvelope-all-en-v01-024.png)

**Paso 6**. **Seleccione** un corresponsal para quien desea cifrar los archivos seleccionados.

**Paso 7**. **Haga clic** en **[Agregar]**.

En este ejemplo seleccionamos claves tanto para Elena como para Mansour. **Puede seleccionar más de una persona, incluyéndo a uno mismo.**

**Paso 8**. **Haga clic** en **[Encriptar]**.

![](mailvelope-all-en-v01-025.png)

**Paso 9**. **Haga clic** en **[Guardar todo]** para guardar los archivos cifrados.

Los archivos cifrados se guardarán donde el navegador guarde los archivos descargados (lo más probable es que la carpeta *Descargas*). Los archivos encriptados tendrán una nueva extensión, *.asc*. Por ejemplo, *foto.png* se convertirá en *foto.png.asc*. Ahora puede enviar los archivos cifrados como archivos adjuntos utilizando la función de archivo adjunto normal de su proveedor de correo web.

**Importante:** Tenga en cuenta que todavía tiene la versión sin cifrar en su computadora en algún lugar, así que asegúrese de enviar la versión cifrada (la que termina en *.asc*). Además, recuerde que *el nombre de archivo original aún está visible* y no se cifrará. Así que elija un nombre que no revele información confidencial.



### 4.4.2 Descifrar archivos

Para descifrar un archivo, siga los pasos a continuación. Si el archivo cifrado se le envió como un archivo adjunto, estos pasos asumen que ya lo ha guardado en algún lugar de su computadora.

**Paso 1**. **Haga clic** en el icono de candado de Mailvelope en la barra de herramientas de su navegador y **seleccione** **Opciones** para abrir la pestaña del navegador **Opciones de Mailvelope**.

**Paso 2**. **Seleccione** la pestaña **[Cifrado de Archivo]**

**Paso 3**. **Haga clic** en **Descifrado** en el lado izquierdo.

**Etapa 4**. **Haga clic** en **[Agregar]** y seleccione un archivo que desee descifrar.

![](mailvelope-all-en-v01-026.png)

Puede seleccionar varios archivos cifrados, siempre y cuando todos estén cifrados utilizando la misma clave pública.

**Paso 5**. **Haga clic** en **[Siguiente]**.

**Paso 6**. **Escriba** la frase de acceso a su clave privada.

![](mailvelope-all-en-v01-027.png)

Tenga en cuenta que deseleccionamos la opción *Recordar contraseña temporalmente*.

**Paso 7**. **Haga clic** en **[Aceptar]**.

![](mailvelope-all-en-v01-028.png)

**Paso 8**. **Haga clic** en **[Guardar todo]** para guardar los archivos descifrados.

Los archivos cifrados se guardarán donde el navegador guarde los archivos descargados (lo más probable es que la carpeta *Descargas*).



# Preguntas Frecuentes

**P**: ¿Se puede instalar Mailvelope en diferentes navegadores como Safari u Opera?

**R**: No. En este momento, Mailvelope solo funciona como complemento / extensión en **Mozilla Firefox** y **Google Chrome o Chromium**.

**P**: ¿Para cuántas cuentas puedo generar pares de claves?

**R**: Tantas como necesite.

**P**: ¿Mailvelope almacena mis claves privadas en algún lugar en línea (por ejemplo, en una nube)?

**R**: No, las claves privadas se almacenan en su computadora. Para **Firefox**, está en un directorio de perfil, para **Chrome o Chromium** es un directorio de datos de usuario. Sin embargo, las claves públicas se pueden cargar en el servidor de claves de Mailvelope.

**P**: ¿Mailvelope permite crear claves que pueden funcionar solo por tiempo limitado?

**R**: No en este momento.

**P**: ¿Se puede instalar Mailvelope para una versión portátil de un navegador?

**R**: Sí. Una vez que lo haga, puede copiar la carpeta del navegador que contiene la instalación de Mailvelope y todas las claves a un USB y utilizarla en otra computadora.