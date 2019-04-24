---
index: 21
title: VeraCrypt
---
Guía de la Herramienta VeraCrypt
====================

Almacenamiento Seguro de Archivos

**Lección a leer: [Protección de Archivos] (umbrella://information/protecting-files) **
**Nivel:** Avanzado
**Tiempo requerido:** 30-60 minutos

**Usar VeraCrypt le dará:**

*   La capacidad de proteger sus archivos si su computadora o dispositivo de almacenamiento USB se extravía, es robado o confiscado
*   La capacidad de acceder y modificar el mismo conjunto de archivos confidenciales en computadoras con Windows, Mac OS X y Linux
*   Una forma segura de hacer copias de seguridad de archivos importantes

**Descargar Ubicación: ** [https://www.veracrypt.fr/en/Downloads.html]((https://www.veracrypt.fr/en/Downloads.html))

**Versión utilizada en esta guía:** 1.16

**Licencia:** Software Gratuito y de Código Abierto

**Requisitos del sistema:**

GNU/Linux (32-bit and 64-bit versions, kernel 2.6 or compatible)
Apple Mac OS X 10.7 or later, running the latest version of [FUSE for Mac OS](https://osxfuse.github.io/).
Microsoft Windows Server 2003, 2008, 2012; XP, Vista, 7, 8, 10

Nota: Se Requiere una cuenta de administrador para la instalación y para crear volúmenes


1\. Introducción
================

[**VeraCrypt**] (https://www.veracrypt.fr/en/Home.html) es un software_libre que le permite cifrar sus archivos. Es una versión actualizada del proyecto TrueCrypt sin mantenimiento, y está disponible para Microsoft Windows, Mac OS X y GNU / Linux. Aborda varias vulnerabilidades de seguridad que desde entonces se han identificado en TrueCrypt.

1.0. Cosas que debes saber sobre VeraCrypt antes de comenzar
------------------------------------------------------------

VeraCrypt protegerá sus archivos mediante la encriptación de ellos con una frase de contraseña. Se crea un área protegida, llamada _volumen_, en su ordenador o dispositivo de almacenamiento externo. Todo el volumen permanece dentro de un solo archivo llamado _contenedor_, que se puede abrir o _montar_ y cerrar o _desmontar_  usando VeraCrypt. Puede almacenar sus archivos de forma segura dentro de este contenedor.

Veracrypt también puede crear y gestionar volúmenes cifrados que ocupan _todo_  el espacio en un dispositivo de almacenamiento particular. Sin embargo, esta guía se centra en el uso de _contenedores_.

VeraCrypt utiliza cifrado _on-the-fly encryption_ para proteger sus datos. El cifrado on-the-fly cifra de manera transparente los archivos mientras son escritos a un volumen, y se descifran de manera transparente cuando son leídas. Puede copiar archivos a y desde un volumen VeraCrypt del mismo modo en que los copiaría a una carpeta o almacenamiento USB normal.

Veracrypt soporta tanto _volúmenes cifrados estándar_ y _volúmenes ocultos_. Cualquiera de los dos va a mantener sus archivos confidenciales, pero  _hidden volumes_ le permiten ocultar su información importante detrás de  datos menos sensibles con el fin de proteger, incluso si se ven obligados a revelar su contraseña de VeraCrypt. Esta guía cubre la creación y el uso de _volúmenes estándar_ y _volúmenes ocultos.

Recuerde, si usted olvida su contraseña, ¡perderá el acceso a sus datos! No hay manera de recuperar una contraseña perdida. Además, tenga en cuenta que el uso de la encriptación es ilegal en algunas jurisdicciones.

Para obtener más información acerca de VeraCrypt, consulte:

*   La [documentación oficial] (https://www.veracrypt.fr/en/Documentation.html)
*   Las [preguntas frecuentes oficiales] (https://www.veracrypt.fr/en/FAQ.html)

1.1 Otras herramientas como VeraCrypt
------------------------------

Ediciones con todas las funciones de **Windows** desde **Windows 7** contienen la utilidad de cifrado de disco copmleto **BitLocker**. (Esto incluye Windows 7 Ultimate, Windows 7 Enterprise, Windows 8 Pro, Windows 8 Enterprise y Windows 10 Pro).

Para **Mac OS X** podrá utilizar la utilidad **FileVault** para el cifrado de disco completo (o simplemente para cifrar el directorio personal). **Mac OS X** también tiene una **utilidad de disco** incorporada que puede crear volúmenes encriptados en dispositivos de almacenamiento USB, pero solo podrá acceder a estos volúmenes en una Mac.

Tanto **FileVault** (para **Mac OS X**)  y **BitLocker** (para **Windows**) son software de propietario. Como resultado, la seguridad que proporcionan no puede ser verificada independientemente. No obstante, es una buena idea habilitarlos, si es posible. Puede utilizar **VeraCrypt**, además de estas herramientas integradas, para proteger sus archivos más sensibles y para moverlos entre Linux, Mac OS X y Windows.

Muchas distribuciones de **GNU Linux**, incluyendo [**Ubuntu**] (http://www.ubuntu.com/), son compatibles con el cifrado de disco completo como una característica estándar. Se recomienda habilitar el cifrado de disco completo cuando se instala Linux, ya que es mucho más fácil que hacerlo más adelante. Además, se puede utilizar la **utilidad de disco** incluida en la mayoría de las distribuciones de Linux para crear un volumen cifrado en un dispositivo de almacenamiento USB. A diferencia de VeraCrypt, sin embargo, esto solo le permite acceder a sus archivos en otras computadoras Linux. Puede usar VeraCrypt para mover archivos entre Linux, Mac OS X y Windows.

2\. Instalando VeraCrypt
========================

Para instalar VeraCrypt en su computadora, siga los pasos a continuación:

**Paso 1**. **Haga doble clic** en el archivo de instalación llamado "VeraCrypt Setup 1.16.exe".

![imagen] (tool_veracrypt1.png)

_Figura 1: El instalador VeraCrypt_

Note: Mac OS users will be prompted to download [FUSE for Mac OS](https://osxfuse.github.io/), a software package needed to run VeraCrypt.  

**VeraCrypt** le pedirá si desea permitir al instalador realizar cambios en su PC, com ose muestra debajo.

![imagen] (tool_veracrypt2.png)

_Figura 2: Pantalla de Control de Acceso de Usuario de VeraCrypt_

**Paso 2**. **Haga clic** en **\[Sí \]** para ejecutar el programa de **instalación de VeraCrypt** , que activará la pantalla _licencia_

![imagen] (tool_veracrypt3.png)

_Figura 3: La licencia VeraCrypt_

**Paso 3**. ** Marque ** la casilla _Acepto los términos de la licencia_ para habilitar el botón **\[Siguiente\] **, luego **haga clic** en **\[Siguiente\]**. Podrá entonces elegir si desea _instalar_ VeraCrypt o _extraerlo_ para usarlo en _modo portable_

![imagen] (tool_veracrypt4.png)

_Figura 4: El asistente de instalación que muestra el modo de instalación predeterminado_

*   Modo _instalar:_ Esta opción es para usuarios que no tienen necesidad de ocultar el hecho de que **VeraCrypt** está instalado en su ordenador y que están dispuestos para instalarlo en cualquier _otro_ equipo en que necesitan acceso a **VeraCrypt**.
*   Modo _extraer:_ Esta opción es para los usuarios que deseen tener una versión portátil de **VeraCrypt** en un dispositivo de almacenamiento USB en lugar de instalarlo en un ordenador. La versión portátil se puede ejecutar en cualquier ordenador con Windows en el que el usuario tenga una cuenta de _Administrador_.

**IMPORTANTE**: Incluso en el modo portátil, **VeraCrypt** deja huellas en los equipos donde se utiliza. Estas huellas no revelarán el contenido de los archivos cifrados, pero pueden revelar el hecho de que **VeraCrypt** se utilizó en ese equipo.

**Nota**: Esta sección cubre _instalar_ **VeraCrypt** en su ordenador. Para aprender más acerca del uso de **VeraCrypt** en _modo portable_, vea ** **VeraCrypt Portable**, a continuación.

**Paso 4**. **Haga clic** en **\[Siguiente\] ** y elija dónde instalar **VeraCrypt**.

![imagen] (tool_veracrypt5.png)

_Figura 5: La ventana de Opciones de Instalación_

**Paso 5**. **Haga clic en** **\[Instalar\]** para comenzar a instalar **VeraCrypt** en la ubicación predeterminada en el equipo como se muestra a continuación

![imagen] (tool_veracrypt6.png)

_Figura 6: progreso del instalador de VeraCrypt_

Una vez terminado, el instalador le hará saber

![imagen] (tool_veracrypt7.png)

_Figura 7: Instalación exitosa de VeraCrypt_

**Paso 6**. **Haga clic** en **\[OK\]** para reconocer la finalización de la instalación y consierar hacer una donación a quienes desarrollan y mantienen **VeraCrypt**.

![imagen] (tool_veracrypt8.png)

_Figura 8: Solicitud de donación de VeraCrypt_

**Paso 7**. **Haga clic** en **\[Terminar\]** y considere leer el tutorial de **VeraCrypt**. 

![imagen] (tool_veracrypt9.png)

_Figura 9: El indicador del tutorial de VeraCrypt_

**Paso 8**. **Haga clic** en cualquiera de los botones para finalizar la instalación de **VeraCrypt**. Dependiendo de las preferencias de instalación, es posible que ahora tenga un acceso directo a **VeraCrypt** en el escritorio.

![imagen] (tool_veracrypt10.png)

_Figura 10: El acceso directo de aplicación VeraCrypt_

**IMPORTANTE**: Si no desea anunciar el hecho de que tiene archivos cifrados en el equipo, es posible que desee eliminar este acceso directo y, si tener el software de cifrado en el equipo pudiera provcocarle problemas _serios_, debería quitar **VeraCrypt** por completo, y luego, extraerlo en un dispositivo de almacenamiento USB en _modo portable_ (ver abajo).

**Nota**: A los usuarios se les motiva a consultar el [Tutorial para Principiantes de **VeraCrypt**] (https://www.veracrypt.fr/en/Beginner%27s%20Tutorial.html) al terminar con esta guía.

3\. Creando un volumen estándar
==============================

**VeraCrypt** le permite crear dos tipos de volúmenes cifrados: volúmenes _Ocultos_ y _Estándar_.

*   Los _volúmenes Estándar_ protegen sus archivos con una frase de contraseña que debe ser introducida para acceder
*   Los _volúmenes ocultos_ tienen _dos_ frases. Puede ingresar una de ellas para abrir un señuelo de volumen estándar en el que debería almacenar datos menos sensibles a los que desee "renunciar" si fuera necesario. Introducir la otra frase de contraseña abrirá el volumen oculto que contiene los archivos más importantes.

En esta sección aprenderá a crear un volumen **estándar**. Si desea crear un _volumen oculto_ debería completar esta sección, y luego continuar a **Creando un volumen oculto**, debajo.

Para crear un _volumen Estándar_ con **VeraCrypt**, realice los siguientes pasos.

**Paso 1**. Inicia **VeraCrypt** (**\[Inicio\]** \> **\[Programas\]** \> **\[VeraCrypt\]** \> **\[VeraCrypt\]**) para abrir la ventana de la aplicación.

![imagen] (tool_veracrypt11.png)

_Figura 1: La ventana principal de VeraCrypt_

**Paso 2**. **Haga clic** en *\[Crear Volumen\]** para activar el _Asistente de Creación de Volumen de VeraCrypt_ 

![imagen] (tool_veracrypt12.png)

_Figura 2: Ventana del Asistente de Creación de volúmenes_

Un archivo de contenedor VeraCrypt es un volumen cifrado que se almacena en un solo archivo. Este contenedor se puede renombrar, mover, copiar o borrar como cualquier otro archivo En esta sección, vamos a crear un archivo contenedor. Por favor, consulte la **[Documentación de VeraCrypt] (https://www.veracrypt.fr/en/Documentation.html)** para aprender más sobre otras opciones.

**Paso 3.** **Haga clic** en **\[Siguiente\]** para elegir el tipo de volumen que desea crear.

![imagen] (tool_veracrypt13.png)

_Figura 3: La ventana de Tipo de Volumen_

La ventana _Tipo de Volumen del Asistente de Creación de Volumen VeraCrypt_ le permite especificar si desea crear un volumen _Estándar_ u _Oculto_.

**Nota**: Por favor, consulte la sección **Creando un volumen oculto** para más información sobre cómo crear un volumen oculto.

**Paso 4**. Asegúrese de que _Volumen VeraCrypt Estándar_ esté seleccionado y **haga clic** en **\[Siguiente\]** para elegir un nombre y una ubicación para el archivo contenedor VeraCrypt.

![imagen] (tool_veracrypt14.png)

_Figura 4: El Asistente de Creación de Volúmenes - Entrada de Ubicación de Volumen_

**Paso 5**. **Haga clic** en **\[Seleccionar Archivo...\]** para elegir una ubicación.

![imagen] (tool_veracrypt15.png)

_Figura 5: Especifique la ubicación y el nombre de archivo del contenedor VeraCrypt que está a punto de crear_

**Paso 6**. Elija una ubicación y especifique un nombre para el archivo de _contenedor_ **VeraCrypt** que está a punto de crear.

Necesitará recordar dónde lo puso y cómo lo llama. En esta sección, crearemos nuestro _contenedor_ en el **Escritorio** y lo nombraremos **Mi volumen**. Si desea crear un volumen estándar **VeraCrypt** en un dispositivo de almacenamiento USB, simplemente navegue hasta el dispositivo (en lugar de su _Escritorio_) e ingrese el nombre de archivo.

**Consejo**: Puede usar cualquier nombre de archivo o extensión de archivo para su _contenedor_. Por ejemplo, puede nombrar su archivo contenedor _recetas.doc, _ o _vacaciones.mpg_ con la esperanza de que un observador casual piense que es un documento de _Microsoft Word_ o un archivo de video. Esta es una forma en que puede ayudar a disimular la existencia de un contenedor **VeraCrypt**, pero no funcionará en contra de alguien que tenga el tiempo y los recursos para buscar en su dispositivo a fondo.

**Paso 7**. **Haga clic** en **\[Guardar\]** para cerrar la ventana _Especificar Ruta y Nombre de Archivo_ y volver a la ventana _Asistente de Creación de Volúmenes_.

![imagen] (tool_veracrypt16.png)

_Figura 6: Asistente de Creación de Volúmenes mostrando la ventana Ubicación de Volumen_

**Paso 8**. **Haga clic** en **\[Siguiente\]** para activar la pantalla _Opciones de Cifrado_

![imagen] (tool_veracrypt17.png)

_Figura 7: Ventana de Opciones de Cifrado del Asistente de Creación de Volúmenes_

Aquí, puede elegir un método específico (o _algoritmo_) para usar al cifrar y descifrar los archivos almacenados en su contenedor **VeraCrypt**. _Las opciones predeterminadas se consideran seguras,_ por lo que probablemente debería dejarlas como están.

**Paso 9**. **Haga clic** en **\[Siguiente\]** y determine el tamaño del volumen cifrado.

![imagen] (tool_veracrypt18.png)

_Figura 8: el Asistente de Creación de Volúmenes mostrando la ventana Tamaño del Volumen_

La ventana _Tamaño de Volumen_ le permite especificar el tamaño del _contenedor_ que está a punto de crear. En esta sección, crearemos un volumen de 250 MB, pero es posible que desee especificar un tamaño diferente. Tenga en cuenta la cantidad de archivos y, lo que es más importante, los tipos de archivos que pretende almacenar en su volumen cifrado. Los archivos de imagen y videos, en particular, pueden llenar un pequeño contenedor **VeraCrypt** muy rápidamente.

**Consejo**: Si cree que puede querer hacer una copia de seguridad de su archivo contenedor en un CD, debe elegir un tamaño de 700 MB o menos. Para una copia de seguridad de DVD, debe ser de 4.5 GB o menos. Si pretende cargar el archivo contenedor en un servicio de almacenamiento en línea, deberá determinar un tamaño razonable en función de la velocidad de su conexión a Internet.

**Paso 10**. **Escriba** el tamaño del volumen que desea crear. Asegúrese de seleccionar el valor correcto para **KB** (kilobytes), **MB** (megabytes), **GB** (gigabytes) o **TB** (terabytes). Luego,**haga clic** en **\[Siguiente\]** para elegir una frase de contraseña.

![imagen] (tool_veracrypt19.png)

_Figura 9: Asistente de Creación de Volúmenes en la ventana de Contraseña de Volumen_

**IMPORTANT**: Choosing a strong passphrase is one of the most important steps you will perform when creating a **VeraCrypt** volume. The stronger the passphrase, the better. You don't have to choose your own passphrases (or even remember them!) if you use a _password manager_ like **KeePassXC**. Please refer to the **[Passwords]** (umbrella://information/passwords) lesson and [**KeePassXC Tool Guide**](umbrella://tools/encryption/s_keepassxc.md) guides to learn more about good passphrase practices.

**Paso 11**. **Escriba** su frase de contraseña y luego **vuelva a escribir** su frase de contraseña en el campo _Confirmar__ para activar el botón **\[Siguiente\]**.

**IMPORTANTE**: El botón "Siguiente" permanecerá deshabilitado hasta que coincidan las dos frases de contraseña que ingresó. Si su frase de contraseña es débil, verá una advertencia. ¡Considere cambiarla! Aunque **VeraCrypt ** aceptará cualquier frase de contraseña, sus datos no estarán seguros a menos que elija una contraseña robusta.

**Paso 12**. **Haga clic en **\[Siguiente\]** para seleccionar un tipo de sistema de archivos.

![imagen] (tool_veracrypt20.png)

_Figura 10: Asistente de Creación de Volúmenes en la ventana Formato de Volumen_

**Paso 13**. **Haga clic** en **\[Formato\]** para comenzar a crear su volumen estándar.

**Nota:** El valor predeterminado ("FAT") funcionará para la mayoría de las personas y es compatible con las computadoras Windows, Mac OS y Linux. Sin embargo, si pretende almacenar archivos de más de 4 GB (para un solo archivo), deberá seleccionar un tipo de sistema de archivos diferente. **NTFS ** funcionará en las computadoras con **Windows** y en la mayoría de las computadoras con Linux.

VeraCrypt ahora está listo para crear un volumen cifrado estándar dentro de un archivo contenedor. Si mueve el mouse dentro de la ventana _Asistente de Creación de Volumen VeraCrypt_, producirá datos aleatorios que ayudarán a fortalecer el cifrado.

![imagen] (tool_veracrypt21.png)

_Figura 11: Barra de progreso del Asistente de Creación de Volúmenes_

**VeraCrypt** ahora creará un archivo llamado _Mi Volumen_ en el _Escritorio_, como se especificó anteriormente. Este archivo contendrá un contenedor de _ volumen estándar_ de 250 MB **VeraCrypt**, que puede utilizar para almacenar sus archivos de forma segura. **VeraCrypt** te avisará cuando esté hecho.

![imagen] (tool_veracrypt22.png)

_Figura 12: Volumen creado exitosamente_

**Paso 14**. **Haga clic** en **\[OK\]** para confirmar la finalización del proceso de creación y volver al asistente de creación de volúmenes.

![imagen] (tool_veracrypt23.png)

_Figura 13: Salir o crear otro volumen encriptado_

**Paso 15**. **Haga clic** en **\[Salir\]** para cerrar _Asistente de Creación de Volúmenes VeraCrypt_ y volver a la ventana principal **VeraCrypt **. (Si **hace clic** en **\[Siguiente\]**, **VeraCrypt** comenzará a guiarlo por el proceso de creación de otro volumen cifrado).

Ahora debería ver su archivo _contenedor_ de 250 MB donde lo haya creado.

![imagen] (tool_veracrypt24.png)

_Figura 14: Archivo contenedor VeraCrypt recién creado en el Escritorio_

4\. Creando un volumen oculto
============================

En VeraCrypt, un _ volumen oculto_ se almacena dentro de tu  _volumen estándar_ cifrado, pero su existencia está oculta. Incluso cuando su volumen estándar está _montado_, no es posible confirmar la existencia de un volumen oculto sin su frase de contraseña (que es independiente de la del _ volumen estándar_).

Un _ volumen oculto_ es como un compartimiento secreto en un maletín cerrado. Almacena los archivos _señuelo_ que no le importa haber confiscado en el maletín mientras mantiene sus archivos más confidenciales en el compartimiento secreto. El punto de un _ volumen oculto_ es ocultar su propia existencia, ocultando así los archivos que contiene, incluso si se ve obligado a revelar la contraseña a su _volumen estándar_. Para que esta técnica sea efectiva, debe crear una situación en la que la persona que solicita ver sus archivos quedará satisfecha con lo que muestre. Para hacer esto, es posible que desee implementar algunas de las siguientes sugerencias:

*   Coloque algunos documentos confidenciales que no le importe haber expuesto en el volumen estándar. Esta información debe ser lo suficientemente sensible como para que tenga sentido que la mantenga en un volumen cifrado.
*   Actualice los archivos en el volumen estándar de forma regular. Esto creará la impresión de que realmente estás usando esos archivos.
*   Tenga en cuenta que alguien que quiera ver sus archivos puede conocer el concepto de volúmenes ocultos. Si está utilizando VeraCrypt correctamente, esta persona no podrá _probar_ que exista su volumen oculto, pero puede que lo "sospeche".

Como se mencionó anteriormente, un _volumen oculto_ se almacena técnicamente dentro de un _volumen estándar_. Es por eso que VeraCrypt a veces se refiere a ellos como volúmenes "internos" y "externos". Afortunadamente, no tiene que montar este último para acceder al primero. En cambio, VeraCrypt te permite crear dos frases de contraseña separadas: una que abre el _volumen estándar_ ("señuelo") y una que abre el _volumen oculto_ interno.

**Cómo crear un Volumen Oculto**

Hay dos formas diferentes de crear un _volumen oculto_, y ambas son muy similares al proceso de crear un _volumen estándar_.

*   El **Modo normal** lo guía a través del proceso de creación de un _volumen estándar_ y el _volumen oculto_ dentro de él. (Estará creando un maletín con un compartimento secreto).

*   El **Modo directo** supone que ya tiene un _volumen estándar_ en el que desea crear un _volumen oculto_. (Ya tiene el maletín, pero desea agregar el compartimiento secreto).


En esta sección, nos centraremos en el modo directo. Si aún no tiene un _volumen estándar_, simplemente siga los pasos descritos en la sección **Creando un volumen estándar** arriba, luego regrese a este punto.

**Paso 1**. Inicie VeraCrypt (**\[Inicio\]** \> **\[Todas las Aplicaciones\]** \> **\[VeraCrypt\]** \> **\[VeraCrypt\]**) para abrir la ventana principal de la aplicación.

![imagen] (tool_veracrypt25.png)

_Figura 1: La ventana principal de VeraCrypt_

**Paso 2**. ** Haga clic** en **\[Crear Volumen\]** para activar el _Asistente de Creación de Volúmenes VeraCrypt_.

![imagen] (tool_veracrypt26.png)

_Figura 2: La pantalla de Creación de Volumen de VeraCrypt_

**Paso 3**. **Haga clic** en **\[Siguiente\]** para aceptar la opción _Crear un contenedor de archivo cifrado_ predeterminado.

![imagen] (tool_veracrypt27.png)

_Figura 3: Creando un volumen oculto de VeraCrypt_

**Paso 4**. ** Marque** la opción **\[Volumen de VeraCrypt Oculto\]**.

**Paso 5**. **Haga clic** en **\[Siguiente\]** para elegir si desea crear su _volumen oculto_ usando _modo normal_ o _modo directo_.

![imagen] (tool_veracrypt28.png)

_Figura 4: Ventana de Modo - Asistente de Creación de Volúmenes de VeraCrypt_

**Paso 6**. **Marque** la opción **\[Modo Directo\]**.

**Paso 7**. **Haga clic** en **\[Siguiente\]** para seleccionar su _volumen estándar_ existente.

![imagen] (tool_veracrypt29.png)

_Figura 5: Pantalla de Ubicación del Volumen de VeraCrypt_

**Nota:** Asegúrese de que su _volumen estándar_ esté desmontado antes de seleccionarlo.

**Paso 8**. **Haga clic* en **\[Seleccionar archivo\]** y ubique su archivo de  _contenedor de volumen estándar_.

![imagen] (tool_veracrypt30.png)

_Figura 6: Selección de su archivo de contenedor de volumen estándar de VeraCrypt existente_

**Paso 9**. **Ubique** el archivo de contenedor y selecciónelo.

Si desea crear un contenedor VeraCrypt en un dispositivo de **almacenamiento USB**, simplemente navegue hasta el dispositivo (en lugar de una carpeta en su computadora) antes de elegir un nombre de archivo.

**Paso 10**. **Haga clic** en **\[Abrir\]** para volver al _Asistente de Creación de Volumen VeraCrypt_.

![imagen] (tool_veracrypt31.png)

_Figura 7: Contenedor de volumen estándar de VeraCrypt seleccionado_

**Paso 11**. **Haga clic** en **\[Siguiente\]** para ingresar la frase de contraseña de su volumen estándar existente.

![imagen] (tool_veracrypt32.png)

_Figura 8: Pantalla de Contraseña del Volumen Externo de VeraCrypt_

**Paso 12**. **Escriba** la frase de contraseña que seleccionó al crear el _volumen estándar_ que ha seleccionado.

**Paso 13**. **Haga clic** en **\[Siguiente\]** para preparar este _volumen estándar_ para la adición de un _ volumen oculto_.

![imagen] (tool_veracrypt33.png)

_Figura 9: Volumen estándar de VeraCrypt preparado_

**Paso 14**. **Haga clic** en **\[Siguiente\]** para seleccionar Opciones de Cifrado de Volumen Oculto.

![imagen] (tool_veracrypt34.png)

_Figura 10: Pantalla de Opciones de Cifrado de Volumen Oculto de VeraCrypt_

**Paso 15**. **Haga clic** en **\[Siguiente\]**, y se le pedirá que especifique el tamaño del _Volumen Oculto_ que está a punto de crear.

**Nota**: deje la configuración predeterminada de _Algoritmo de Cifrado_ y _Algoritmo de Hash_ para el _Volumen Oculto_ como se encuentra.

![imagen] (tool_veracrypt35.png)

_Figura 11: Pantalla de Tamaño de Volumen Oculto de VeraCrypt_

Como cuando creó su _volumen estándar_, considere la cantidad y los tipos de archivos que desea almacenar en su _volumen oculto._ Los archivos de imágenes y videos, en particular, pueden llenar un pequeño contenedor VeraCrypt muy rápidamente. Además, asegúrese de dejar algo de espacio para los archivos _señuelo_ en su _volumen estándar_. Si selecciona el tamaño máximo disponible para el _volumen oculto_, no podrá colocar más archivos en el _volumen estándar_ existente. (En esta sección, crearemos un volumen oculto de 200 MB dentro de un volumen estándar de 250 MB. Esto dejará aproximadamente 50 MB de espacio para los archivos _señuelo_).

**Paso 16**. **Escriba** el tamaño del volumen que desea crear. Asegúrese de seleccionar el valor correcto para **KB** (kilobytes), **MB** (megabytes), **GB** (gigabytes) o **TB** (terabytes).

**Paso 17**. **Haga clic** en **\[Siguiente\]** para elegir una frase de contraseña para su _volumen oculto_.

![imagen] (tool_veracrypt36.png)

_Figura 12: Pantalla de creación de Contraseña para Volumen Oculto de VeraCrypt_

You must now choose a passphrase for the _hidden volume_ that is _different_ from the one you chose for your _standard volume_. Again, remember to choose a strong passphrase. Please refer to the **[Passwords]** (umbrella://information/passwords) lesson to learn more.

**Consejo**: si usa un _gestor de contraseñas_ como **KeePassXC** y le preocupa que lo presionen para revelar el contenido de su contenedor **VeraCrypt **, puede guardar la frase de contraseña de su _volumen estándar_ (señuelo) en **KeePassXC**, pero deberá memorizar la frase de contraseña para su _volumen oculto._ De lo contrario, al entregar su frase de contraseña de **KeePassXC**, también revelará su frase de contraseña del _volumen oculto_.

**Paso 18**. **Elija** una frase de contraseña y **escríbala** dos veces.

**Paso 19**. **Haga clic** en **\[Siguiente\]** para activar la pantalla _Formato de Volumen Oculto_.

![imagen] (tool_veracrypt37.png)

_Figura 13: Pantalla de Formato de Volumen Oculto de VeraCrypt_

**Paso 20**. **Haga clic** en **\[Formato\]** para formatear el volumen oculto.

**Nota:** El valor predeterminado ("FAT") funcionará para la mayoría de las personas y es compatible con las computadoras Windows, Mac OS y Linux. Sin embargo, si pretende almacenar archivos de más de 4 GB (para un solo archivo), deberá seleccionar un tipo de sistema de archivos diferente. **NTFS** funcionará en computadoras con Windows y en la mayoría de las computadoras con Linux.

**VeraCrypt** ahora está listo para crear un volumen cifrado estándar dentro de un archivo contenedor. Si mueve el mouse dentro de la ventana _Asistente de Creador de Volúmenes VeraCrypt_, producirá datos aleatorios que ayudarán a fortalecer el cifrado.

![imagen] (tool_veracrypt38.png)

_Figura 14: Progreso del Formato de Volumen Oculto de VeraCrypt_

Cuando termine VeraCrypt, aparecerá una advertencia sobre la protección de los archivos en su _volumen oculto_ cuando agregue contenido a su _volumen estándar_.

![imagen] (tool_veracrypt39.png)

_Figura 15: Mensaje de advertencia de protección de Volumen Oculto de VeraCrypt_

**IMPORTANTE**: Esta advertencia está relacionada con la forma en que VeraCrypt oculta la existencia de su _volumen oculto_ (interno). Normalmente, cuando abre su _volumen estándar_ (externo), tanto VeraCrypt como Windows pensarán que ocupa todo el espacio disponible dentro de su archivo de contenedor cifrado. Alrededor de 250 MB en este ejemplo. (De hecho, creamos un volumen oculto de 200 MB y dejamos solo unos 50 MB para los archivos de señuelo en nuestro volumen estándar). VeraCrypt no puede advertirle si intenta copiar un archivo de 60 MB en ese volumen estándar de 50 MB. Esto se debe a que, _si  le advirtiera_, le revelaría a un observador que tenía espacio reservado para un _volumen oculto_. En su lugar, le permitirá copiar ese archivo de 60 MB. Y, al hacerlo, _eliminará o dañará los archivos dentro de su volumen oculto_.

En otras palabras, este diseño se basa en la suposición de que preferiría perder el contenido de su volumen oculto en vez de revelar su existencia.

Por lo tanto, siempre que desee agregar archivos señuelo a su volumen estándar, debe marcar el cuadro _proteger el volumen oculto contra el daño ..._ e ingresar tanto la frase de contraseña del volumen oculto como la frase de contraseña del volumen estándar. Si habilita esta función, VeraCrypt _podrá_ advertirte si intenta copiar demasiados datos en su volumen externo. (Claramente, si ingresa ambas frases de acceso delante de otra persona, se revelará la existencia de su _volumen oculto_, por lo que esto es algo que solo debe hacer en privado o en compañía de aquellos en quienes confía).

Los pasos específicos requeridos para modificar el contenido de su _volumen estándar_ se cubren con más detalle en la sección a continuación, **Protección de su volumen oculto al modificar el contenido de su volumen externo**.

**Paso 21**. **Haga clic** en **\[OK\]** para terminar de crear su _volumen oculto_.

![imagen] (tool_veracrypt40.png)

_Figura 16: La pantalla de Creación de Volumen Oculto de VeraCrypt_

**Paso 22**. **Haga clic** en **\[OK\]** para volver a la ventana principal de VeraCrypt.

Ahora puede almacenar archivos en su _volumen oculto_. Permanecerán indetectables incluso para alguien que haya obtenido la frase de contraseña para su _volumen estándar_.

5\. Usando su volumen de VeraCrypt
===============================

Esta sección de esta guía explica cómo usar volúmenes de VeraCrypt estándar y ocultos en Windows.

5.1. Montar un volumen
----------------------

En VeraCrypt, montar un volumen es ponerlo a disposición para su uso. Cuando monta un volumen con éxito, aparece como si hubiera conectado un dispositivo de almacenamiento extraíble a su computadora. Puede usar este disco como de costumbre para acceder, crear, modificar o eliminar archivos y carpetas. Cuando haya terminado de usarlo, puede desmontarlo y el nuevo disco desaparecerá. Puede montar un volumen oculto de la misma manera que un volumen estándar. Dependiendo de la frase de contraseña que ingrese, VeraCrypt determinará si se debe montar el volumen estándar u oculto.

Para montar su volumen, realice los siguientes pasos:

**Paso 1.** Inicie VeraCrypt (**Inicio** \> **Todas las Aplicaciones** \> **VeraCrypt** \> **VeraCrypt**) para abrir la ventana principal de la aplicación

**Paso 2.** **Seleccione** un disco de la lista en la ventana principal de **VeraCrypt **

![imagen] (tool_veracrypt41.png)

_Figura 1: la ventana principal de VeraCrypt con una unidad disponible seleccionada_

**Nota**: En la _Figura 1_, hemos elegido montar nuestro volumen cifrado en la unidad _F:_. Puede elegir cualquiera de las letras de unidad que se muestran cada vez que monta un volumen.

**Paso 3.** **Haga clic** en **\[Seleccionar Archivo...\]** y ubique su archivo _contenedor_ VeraCrypt.

![imagen] (tool_veracrypt42.png)

_Figura 2: La pantalla Seleccionar un Volumen de VeraCrypt_

**Paso 4.** **Seleccione** el archivo _contenedor_ que desea montar, luego **haga clic** en **\[Abrir\]** para volver a la ventana principal **VeraCrypt**. La ubicación de su archivo _contenedor_ se mostrará justo a la izquierda del botón **\[Seleccionar Archivo...\]** en el que hizo clic anteriormente.

![imagen] (tool_veracrypt43.png)

_Figura 3: la ventana principal de VeraCrypt con un contenedor seleccionado_

**Paso 5.** **Haga clic** en **\[Montar\]** para ingresar su frase de contraseña.

![imagen] (tool_veracrypt45.png)

_Figura 4: La pantalla Introducir Contraseña_

**Paso 6.** **Escriba** su frase de contraseña en el cuadro _Contraseña_.

Si su _contenedor_ tiene un volumen oculto, elija una de las siguientes opciones:

*   Para abrir un _volumen oculto_, ingrese su frase de contraseña para _volumen oculto_

*   Para abrir un _volumen estándar en un _contenedor_ que contiene un _volumen oculto_ — _mientras lo observa alguien a quien le gustaría ocultar la existencia de ese volumen_ — ingrese su frase de contraseña de  _volumen estándar_ 

*   Para abrir un _volumen estándar_ en un _contenedor_ que contiene un _volumen oculto_ — _para modificar sus archivos de "señuelo" mientras no lo están observando_ — lea, **Protegiendo su volumen oculto al modificar el contenido de su volumen exterior.**


**Paso 7.** **Haga clic** en **\[OK\]** para comenzar a montar el _volumen estándar_.

Si la frase de contraseña que ingresó es incorrecta, **VeraCrypt** le pedirá que la ingrese nuevamente. Si es correcta, su volumen cifrado se montará de la siguiente manera:

![imagen] (tool_veracrypt44.png)

_Figura 5: la ventana principal de VeraCrypt mostrando el volumen recién montado_

**Paso 8.** Ingresar al volumen montado

Hay dos formas de ingresar a un volumen montado:

1.  **Haga doble clic** en la entrada resaltada en la ventana principal de **VeraCrypt** como se muestra en _Figura 5_, arriba
2.  **Haga doble clic** en la letra de unidad correspondiente (aquí estamos usando _F:_) dentro de _Este Equipo_, como se muestra en _Figura 6_, a continuación

![imagen] (tool_veracrypt46.png)

_Figura 6: Acceso al volumen de VeraCrypt a través de "Este Equipo"_

El volumen que se muestra a continuación está vacío. Una vez que haya almacenado los archivos allí, serán accesibles (y editables) cada vez que abra el volumen.

![imagen] (tool_veracrypt47.png)

_Figura 7: Dentro del volumen de VeraCrypt montado_

Este disco virtual se comporta como un dispositivo de almacenamiento externo, excepto que está totalmente encriptado. Puede copiar archivos a y desde él como lo haría con un dispositivo de almacenamiento USB. Arrastrarlos y soltarlos, por ejemplo, o guardarlos directamente en el volumen desde otra aplicación. Los archivos se cifran automáticamente cuando los copia, mueve o guarda en este disco virtual. Y, cuando mueve un archivo _fuera_ del volumen VeraCrypt, se descifra automáticamente. Si su computadora se apaga, el volumen cifrado permanecerá inaccesible hasta que se vuelva a montar.

**IMPORTANTE:** Mientras su volumen de VeraCrypt está montado, los archivos que contiene no están protegidos y cualquier persona con acceso a su computadora puede acceder libremente. Para proteger sus archivos confidenciales, debe desmontar el volumen de VeraCrypt cuando no lo esté utilizando. Tenga esto en cuenta cuando se aleje de su computadora y en las circunstancias en las que se enfrenta a un mayor riesgo de confiscación o robo. Dejar sus volúmenes encriptados montados es como tener una caja fuerte y dejar la puerta abierta. Si reinicia o apaga su computadora, no podrá acceder a su volumen cifrado hasta que se vuelva a montar. Es posible que desee practicar hacer una de estas cosas lo más rápido posible.

**Consejo:** El simple hecho de cerrar la ventana principal haciendo clic en **\[Salir\]** no es suficiente para cerrar la aplicación por completo.

5.2. Desmontar un volumen
-------------------------

En VeraCrypt, desmontar un volumen es dejarlo no disponible para su uso. Para desmontar un volumen y asegurarse de que nadie pueda acceder a los archivos que contiene, a menos que conozcan la contraseña correcta, realice los siguientes pasos:

**Paso 1**. **Seleccione** el volumen de la lista de volúmenes montados en la ventana principal **VeraCrypt**

![imagen] (tool_veracrypt48.png)

_Figura 1: Selección del Volumen Estándar para ser desmontado_

**Paso 2**. **Haga clic** en **\[Desmontar\]** para desmontar el volumen **VeraCrypt**.

Para recuperar un archivo almacenado en su volumen estándar una vez que lo haya cerrado o desmontado, tendrá que volver a montarlo.

**IMPORTANTE**: asegúrese de desmontar su volumen **VeraCrypt** antes de:

*   Extraer el dispositivo de almacenamiento USB externo en el que está almacenado su _contenedor_ (si ha elegido mantenerlo en uno)
*   Poner su computadora en modo _Standby_ o _Hibernar_
*   Dejar su computadora desatendida
*   Entrar en una situación en la que es más probable que su computadora se pierda, sea robada o confiscada

**Paso 3**. **Haga clic derecho** en el icono de **VeraCrypt ** en la _Bandeja del Sistema_ —  en la esquina inferior derecha de su escritorio de Windows - y seleccione **\[Salir\]** para cerrar **VeraCrypt** por completo .

![imagen] (tool_veracrypt49.png)

_Figura 2: Saliendo de VeraCrypt en limpio con el ícono de la Bandeja del Sistema_

**Consejo**. Cuando se utiliza la versión instalada de **VeraCrypt** (a diferencia de la versión portable), simplemente cerrar la _ventana principal_ haciendo clic en **\[Salir\]** no es suficiente para salir de la aplicación por completo.

5.3. Protegiendo su volumen oculto al modificar el contenido de su volumen exterior
-------------------------------------------------- --------------------------------

Como se explica en la sección **Creación de un volumen oculto **, cuando monta un volumen **VeraCrypt **, puede elegir _Proteger el volumen oculto contra los daños causados por la escritura en el volumen exterior_. Esto le permite agregar nuevos archivos de "señuelo" a su volumen estándar sin el riesgo de eliminar o corromper accidentalmente el contenido de su volumen oculto. Sin embargo, no debe activar la función _Proteger volumen oculto_ cuando intente ocultar la existencia de su _volumen oculto_ de alguien que lo está obligando a ingresar su frase de contraseña, ya que hacerlo requiere que ingrese _ambas_ frases de contraseña (lo cual es una indicación bastante clara de que tiene un _volumen oculto_ en alguna parte).

Sin embargo, cuando actualice sus archivos señuelo en privado, debería habilitar esta función _siempre_. Y no se preocupe, _la casilla se desactivará automáticamente después de que desmonte el volumen._

Para usar la función _Proteger volumen oculto_, realice los siguientes pasos:

**Paso 1**. **Seleccione** una unidad de la lista en la ventana principal de **VeraCrypt**

![imagen] (tool_veracrypt50.png)

_Figura 1: La ventana principal de VeraCrypt con una unidad disponible seleccionada_

**Nota**: En la _Figura 1_, hemos elegido montar nuestro volumen cifrado en la unidad _F:_. Puede elegir cualquiera de las letras de unidad que se muestran cada vez que monta un volumen.

**Paso 2**. **Haga clic** en **\[Seleccionar archivo...\]** y ubique su archivo de contenedor VeraCrypt.

![imagen](tool_veracrypt51.png)

_Figura 2: La pantalla Seleccionar un Volumen de VeraCrypt_

**Paso 3**. **Seleccione** el archivo _contenedor_ que desea montar, luego **haga clic** en **\[Abrir\]** para volver a la ventana principal **VeraCrypt**. La ubicación de su archivo _contenedor_ se mostrará justo a la izquierda del botón **\[Seleccionar Archivo...\]** en el que hizo clic anteriormente.

![imagen](tool_veracrypt52.png)

_Figura 3: la ventana principal de VeraCrypt con un contenedor seleccionado_

**Paso 4**. **Haga clic** en **\[Montar\]** para abrir la pantalla _Ingresar Contraseña_

![imagen](tool_veracrypt53.png)

_Figura 4: La pantalla para Introducir Contraseña_

**Paso 5.** **Escriba** su frase de contraseña del **volumen exterior** en el cuadro _Contraseña_, como si fuera a montarlo normalmente, **pero no haga clic en \[OK\]**

**Paso 6.** **Haga clic** en **\[Opciones de Montaje...\]**, lo que le permitirá proteger su _volumen oculto_ mientras modifica el contenido de su _volumen estándar_

![imagen](tool_veracrypt54.png)

_Figura 5: Pantalla de Opciones de Montaje de VeraCrypt_

**Paso 7.** **Marque** la casilla etiquetada _Proteger el volumen oculto contra los daños causados al escribir en el volumen exterior_

**Paso 8.** **Escriba** su frase de contraseña del _volumen oculto_ donde se indica

**Paso 9.** **Haga clic** en **\[OK\]** para volver a la solicitud de contraseña

![imagen](tool_veracrypt55.png)

_Figura 6: Pantalla de Ingreso de Contraseña de VeraCrypt con el volumen oculto protegido_

**Paso 10.** **Haga clic** en **\[OK\]** para montar su _volumen estándar_ mientras protege su _volumen oculto_ de daños accidentales. VeraCrypt  avisará cuando esté listo.

![imagen](tool_veracrypt56.png)

_Figura 7: Pantalla "El volumen oculto ahora está protegido" de VeraCrypt_

**Paso 11.** **Haga clic** en **\[OK\]** para volver a la ventana principal de VeraCrypt.

![imagen](tool_veracrypt57.png)

_Figura 8: Pantalla "El volumen oculto ahora está protegido" de VeraCrypt_

**Paso 12.** Ingrese al volumen montado.

Como cuando se monta un volumen normalmente, hay dos formas de ingresar a un volumen montado:

1.  **Haciendo doble clic** en la entrada resaltada en la ventana principal de **VeraCrypt** como se muestra en la _Figura 8_, arriba
2.  **Haciendo doble clic** en la letra de unidad correspondiente (aquí estamos usando _F:_) dentro de _Este Equipo_

El volumen que se muestra a continuación está vacío. Pero, una vez que haya almacenado archivos de "señuelo" en su _volumen estándar_, podrá acceder a ellos siempre que lo monte. Y, si ha protegido su _volumen oculto_ con los pasos anteriores, podrá agregar o modificar archivos.

![imagen](tool_veracrypt58.png)

_Figura 9: dentro del volumen estándar montado de VeraCrypt con un volumen oculto protegido_

**Cuando haya terminado de modificar el contenido de su volumen estándar, puede desmontarlo siguiendo los pasos habituales**, que se describen en la sección **Desmontando un volumen**, arriba. Y, la próxima vez que vaya a montar un volumen, el cuadro _Proteger el volumen oculto contra los daños causados por la escritura en volumen exterior_ estará deseleccionado de forma predeterminada.

6\. Gestionando su contenedor VeraCrypt
=====================================

6.1. Importando contenido desde un volumen de TrueCrypt
----------------------------------------------

**VeraCrypt** puede montar **volúmenes TrueCrypt**. Sin embargo, dado que ya no se mantiene **TrueCrypt**, debe mover sus archivos a un volumen **VeraCrypt** tan pronto como sea posible. La forma más fácil de hacer esto es:

1.  Cree un nuevo volumen **VeraCrypt** tan grande como (o más grande que) su volumen **TrueCrypt** existente,
2.  Abra ambos volúmenes al mismo tiempo, y
3.  Copie todo desde el volumen **TrueCrypt** al volumen **VeraCrypt**

Para el primer elemento, arriba, vea **Creación de un volumen estándar** (y, si corresponde, **Creación de un volumen oculto**. Esta sección asume que ya tiene uno o más volúmenes **VeraCrypt** del tamaño adecuado. Los pasos a continuación abordan el proceso de mover archivos de un  _volumen estándar_ **TrueCrypt** a un _volumen estándar_ **VeraCrypt** que ya se ha montado. Si tiene archivos en _ambos_ volúmenes _estándar_ y _oculto_ de un contenedor **TrueCrypt**, simplemente asegúrese de que sus volúmenes **VeraCrypt** sean lo suficientemente grandes, luego siga los siguientes pasos dos veces, una para cada volumen.

Con la _ventana principal_ de **VeraCrypt** abierta y su nuevo volumen **VeraCrypt** montado, lleve a cabo los siguientes pasos:

![imagen] (tool_veracrypt59.png)

_Figura 1: Ventana principal de VeraCrypt mostrando un volumen montado_

**Paso 1**. **Haga clic** en una letra de unidad que no haya sido tomada por un volumen **VeraCrypt** montado.

**Paso 2**. **Haga clic** en **\[Seleccionar Archivo...\]** para elegir su contenedor **TrueCrypt**.

![imagen] (tool_veracrypt60.png)

_Figura 2: Elección de un contenedor TrueCrypt_

**Paso 3**. **Navegue** a su contenedor **TrueCrypt**.

**Etapa 4**. **Haga clic** en **\[Abrir\]** para volver a la _ventana principal_.

![imagen] (tool_veracrypt61.png)

_Figura 3: ventana principal de VeraCrypt con un contenedor TrueCrypt seleccionado_

**Paso 5**. **Haga clic** en **\[Montar\]** para ingresar la frase de contraseña para su volumen **TrueCrypt**.

![imagen] (tool_veracrypt62.png)

_Figura 4: La pantalla de contraseña de VeraCrypt en modo TrueCrypt_

**Paso 6**. **Marque** la casilla ** Modo TrueCrypt**

**Paso 7**. **Escriba** la frase de contraseña para su volumen TrueCrypt.

**Paso 8**. **Haga clic** en **\[OK\]** para volver a la ventana principal_

![imagen](tool_veracrypt63.png)

_Figura 5: Ventana principal de VeraCrypt con ambos volúmenes montados_

**Paso 9**. **Haga doble clic** en la letra de la unidad para su volumen **TrueCrypt** montado para ingresarlo.

![imagen](tool_veracrypt64.png)

_Figura 6: Dentro del volumen de TrueCrypt montado_

**Paso 10**. Vuelva a la _ventana principal_.

![imagen] (tool_veracrypt65.png)

_Figura 7: Ventana principal de VeraCrypt con ambos volúmenes montados_

**Paso 11**. **Haga doble clic** en la letra de la unidad para su contenedor **VeraCrypt ** montado para ingresar.

![imagen] (tool_veracrypt66.png)

_Figura 8: Volúmenes de TrueCrypt y VeraCrypt montados y mostrados lado a lado_

**Paso 12**. **Seleccione** el contenido de su volumen **TrueCrypt** y arrástrelos a la ventana que representa su volumen **VeraCrypt**.

![imagen] (tool_veracrypt67.png)

_Figura 9: Contenido de un volumen de TrueCrypt copiado en un volumen de VeraCrypt_

Después de que se hayan copiado los archivos, debe _desmontar_ ambos volúmenes.

**Paso 13**. Regrese a la _ventana principal_ de **VeraCrypt**.

![imagen] (tool_veracrypt68.png)

_Figura 10: Ventana principal de VeraCrypt_

**Paso 14**. **Seleccione** la letra de unidad para su volumen **TrueCrypt** montado.

**Paso 15**. **Haga clic** en **\[Dismount\]** para desmontar su volumen **TrueCrypt**.

![imagen] (tool_veracrypt69.png)

_Figura 11: Ventana principal de VeraCrypt_

**Paso 16**. **Seleccione** la letra de unidad para su volumen **VeraCrypt** montado.

**Paso 17**. **Haga clic** en **\[Desmontar\]** para desmontar su volumen **VeraCrypt**.

6.2. Cambiar una o ambas frases de contraseña para un contenedor
------------------------------------------------------

Para cambiar la frase de contraseña de un _volumen_ **VeraCrypt**, comience desde la pantalla principal y siga los pasos a continuación. Estos pasos se aplican tanto a _volúmenes estándar_ como a _volúmenes ocultos_ dentro de _contenedores_ **VeraCrypt**. Sin embargo, si desea cambiar las frases de contraseña de ambos, deberá pasar por este proceso dos veces.

![imagen] (tool_veracrypt70.png)

_Figura 1: Ventana principal de VeraCrypt_

**Paso 1**. **Haga clic** en **\[Seleccionar Archivo...\]** para elegir el _contenedor_ para el que desea cambiar la frase de contraseña.

![imagen] (tool_veracrypt71.png)

_Figura 2: Seleccionando un archivo contenedor en VeraCrypt_

**Paso 2**. **Seleccione** su _contenedor_ **VeraCrypt**.

**Paso 3**. **Haga clic** en **\[Abrir\]** para volver a la _ventana principal_.

![imagen] (tool_veracrypt72.png)

_Figura 3: Ventana principal de VeraCrypt_

**Paso 4**. **Haga clic** en **\[Volúmenes\]**.

**Paso 5**. **Seleccione** **\[Cambiar Contraseña de Volumen...\] ** como se muestra a continuación.

![imagen] (tool_veracrypt73.png)

_Figura 4: Cambiando la frase de contraseña de un volumen de VeraCrypt_

Esto activará la pantalla **Cambiar Contraseña**

![imagen] (tool_veracrypt74.png)

_Figura 5: Pantalla de cambio de contraseña de VeraCrypt_

**Consejo:** Si tiene un volumen estándar y un volumen oculto en este contenedor, VeraCrypt determinará automáticamente qué contraseña cambiará según lo que ingrese en el campo **\[Contraseña Actual\]**. Si desea cambiar ambas contraseñas, deberá realizar este proceso dos veces.

**Paso 6**. **Escriba** su frase de contraseña actual.

**Paso 7**. **Escriba** su nueva frase de contraseña dos veces.

**Paso 8**. **Haga clic** en **\[OK\]** para comenzar a generar una nueva clave.

**Nota:** Las versiones anteriores de VeraCrypt pueden mostrar una advertencia sobre su valor de "Personal Iterations Multiplier (PIM)" aunque haya elegido una frase de contraseña segura. Si ve esta advertencia, vuelva a verificar que su frase de contraseña tenga más de 20 caracteres y que la casilla Usar PIM esté desactivada. Luego haga clic en \[Sí\] para continuar.

![imagen] (tool_veracrypt75.png)

_Figura 6: Barra de progreso de cambio de contraseña de VeraCrypt_

Cuando esté listo, **VeraCrypt** mostrará la pantalla _Enriquecimiento Aleatorio_.

![imagen] (tool_veracrypt76.png)

_Figura 7: Pantalla de Enriquecimiento Aleatorio de VeraCrypt_

**Consejo:** Al mover el mouse alrededor de la pantalla _Enriquecimiento Aleatorio_, puede aumentar la fuerza del cifrado que proporciona **VeraCrypt**.

**Paso 9**. **Haga clic** en **\[Continuar\]** para continuar con el proceso de cambiar su frase de contraseña.

![imagen] (tool_veracrypt77.png)

_Figura 8: Barra de progreso de cambio de contraseña de VeraCrypt_

**VeraCrypt** le avisará cuando termine de generar una nueva clave para su volumen cifrado

![imagen] (tool_veracrypt78.png)

_Figura 9: La frase de contraseña de VeraCrypt cambió exitosamente_

**Paso 10**. **Haga clic** en **\[OK\]** para completar el proceso de cambiar su contraseña.

**IMPORTANTE:** Cambiar su frase de contraseña no cambia la clave de cifrado real utilizada para proteger sus datos. En la práctica, esto significa que cualquier persona con las siguientes tres cosas podrá acceder a los archivos en su contenedor VeraCrypt _incluso después de que haya cambiado su frase de contraseña_:

*   Una copia de su "antiguo" contenedor de VeraCrypt (desde _antes_ de haber canbuado la frase de contraseña)
*   La frase de contraseña a ese antiguo contenedor VeraCrypt
*   Una copia de su "nuevo" contenedor de VeraCrypt (desde _después_ de haber cambiado la frase de contraseña)

Por lo tanto, **si sospecha que alguien podría tener tanto una copia de su contenedor como el conocimiento de su frase de contraseña, debería hacer algo más que cambiar su frase de contraseña**. En su lugar, debe generar un contenedor completamente nuevo (con una nueva frase de contraseña), luego, copiar ahí sus archivos y eliminar el contenedor antiguo.

7\. VeraCrypt Portable
======================

7.1. Diferencias entre las versiones instaladas y porables de VeraCrypt.
-------------------------------------------------------------------------

Al extraer **VeraCrypt** en modo portable, puede usarlo para proteger sus archivos confidenciales sin instalar el software en su computadora de la manera habitual. En algunas situaciones, este enfoque podría ayudarle a ocultar el hecho de que utiliza **VeraCrypt** en absoluto. Esto, a su vez, hará que sea menos evidente que está almacenando datos cifrados.

Si extrae la versión portable de **VeraCrypt** en un dispositivo de almacenamiento USB, junto con su archivo _contenedor_ cifrado, podrá acceder a sus archivos en casi toda computadora con Windows. Sin embargo, tenga en cuenta que sus dispositivos de almacenamiento externo sean tan seguros como las computadoras a las que los conecta. Descifrar indiscriminadamente sus archivos confidenciales en un hardware desconocido puede exponerlo a un malware capaz de leer el contenido de su _volumen encriptado_ mientras está "abierto" (o incluso capturar su frase de contraseña **VeraCrypt** cuando la ingresa).

Hay muy pocas diferencias entre las versiones instaladas y portables de **VeraCrypt**, la más significativa es que la versión portable no le permite cifrar el disco de su sistema. Funciona mejor con archivos de _contenedor_ cifrados.

7.2. Extracción de la versión portable de VeraCrypt.
-------------------------------------------------

**Nota**: Deberá crear la carpeta en la que extraerá la versión portable de **VeraCrypt**, generalmente en un dispositivo de almacenamiento USB o en algún lugar de su disco duro, antes de extraerlo.

**Paso 1**. **Navegue** a la ubicación donde desea extraer la versión portátil de **VeraCrypt**.

**Paso 2**. ** Haga clic derecho** para activar su menú contextual.

**Paso 3**. **Seleccione** el elemento _Nuevo_ del menú, luego **seleccione** el elemento _Carpeta_ del submenú, como se muestra a continuación.

![imagen] (tool_veracrypt79.png)

_Figura 1: Creando una carpeta en Windows_

**Paso 4**. **Escriba** un nombre para la carpeta en la que está a punto de extraer **VeraCrypt**.

**Paso 5**. **Presione** _Enter_ para terminar de nombrar la nueva carpeta.

![imagen] (tool_veracrypt80.png)

_Figura 2: Nombrando una carpeta en Windows_

**Paso 6**. **Haga doble clic** en el instalador de **VeraCrypt** para abrir la pantalla de instalación.

![imagen] (tool_veracrypt81.png)

_Figura 3: El instalador de VeraCrypt_

**Paso 7**. **Haga doble clic** en el instalador de **VeraCrypt** para activar la pantalla Control de Cuenta de Usuario.

![imagen] (tool_veracrypt82.png)

_Figura 4: La pantalla de Control de Cuenta de Usuario de VeraCrypt_

**Paso 8**. **Haga clic** en **\[Sí\]** para cargar la pantalla de licencia.

![imagen] (tool_veracrypt83.png)

_Figura 5: La pantalla de la licencia de VeraCrypt_

* Paso 9**. **Haga clic** en _Acepto los términos de la licencia_.

**Paso 10**. **Haga clic** en **\[Siguiente\]** para activar el instalador.

![imagen] (tool_veracrypt84.png)

_Figura 6: La pantalla principal de instalación de VeraCrypt_

**Paso 11 **. **Seleccione** _Extraer_

**Paso 12**. **Haga clic** en **\[Siguiente\]** para activar la pantalla de advertencia del controlador.

Las dos pantallas de advertencia a continuación son solo la forma en que VeraCrypt le informa que tendrá que descartar una pantalla de _Cuenta de Control de Usuario_ (UAC) cada vez que inicie la versión portable de **VeraCrypt**. (No tendrá que hacer esto si instala el software normalmente).

![imagen] (tool_veracrypt85.png)

_Figura 7: Un mensaje relacionado con cómo la versión portable de VeraCrypt instala los controladores de Windows_

**Paso 13**. **Haga clic** en **\[OK\]** para activar otra pantalla de advertencia relacionada con el controlador.

![imagen] (tool_veracrypt86.png)

_Figura 8: Una advertencia sobre la necesidad de reconocer una advertencia de Control de Cuentas de Usuario al iniciar la versión portable de VeraCrypt_

**Paso 14**. **Haga clic** en **\[Sí\]** para comenzar a elegir su ubicación de extracción.

![imagen] (tool_veracrypt87.png)

_Figura 9: Pantalla de Opciones de Extracción_

**Paso 15**. **Haga clic** en **\[Examinar\]** para elegir su ubicación de extracción.

![imagen] (tool_veracrypt88.png)

_Figura 10: eligiendo dónde extraer la versión portátil de VeraCrypt_

En esta guía, extraeremos la versión portable de **VeraCrypt** en la carpeta "VCP" que creamos en el _Paso 1_. Esta carpeta se encuentra dentro de un dispositivo de almacenamiento USB llamado "Almacenamiento USB (D :)".

**Paso 16**. Ubique y seleccione la carpeta dentro de la cual desea extraer la versión portable de **VeraCrypt**.

**Paso 17**. **Haga clic** en **\[OK\]** para volver a la pantalla _Opciones de Extracción_.

![imagen] (tool_veracrypt89.png)

_Figura 11: La pantalla Opciones de Extracción después de elegir una ubicación_

**Paso 18**. **Haga clic** en **\[Extraer\]** para comenzar a extraer **VeraCrypt**. El instalador de **VeraCrypt** le avisará cuando esté listo.

![imagen] (tool_veracrypt90.png)

_Figura 12: La pantalla de progreso de extracción de archivo_

![imagen] (tool_veracrypt91.png)

_Figura 13: La versión portable de VeraCrypt extraída con éxito_

**Paso 19**. **Haga clic** en **\[OK\]** para activar la solicitud de donación.

![imagen] (tool_veracrypt92.png)

_Figura 14: Solicitud de donación de VeraCrypt_

**Paso 20**. **Haga clic** en **\[Finalizar\]** para completar la extracción de la versión portable de **VeraCrypt**.

**IMPORTANTE**: Si extrajo la versión portable de **VeraCrypt** a un dispositivo de almacenamiento USB para ocultar el hecho de que lo está usando en su computadora, asegúrese de **eliminar el instalador** de su computadora.

7.3. Iniciandola versión portable de VeraCrypt.
------------------------------------------------

**Paso 1**. **Navegue** a la carpeta donde extrajo la versión portable de **VeraCrypt**.

**Paso 2**. **Haga doble clic** ya sea en el archivo **VeraCrypt** (_Figura 1_, a continuación) o el archivo **VeraCrypt-x64** (_Figure 2_), dependiendo de si su sistema de Windows es de 32 bits o 64 bits.

![imagen] (tool_veracrypt93.png)

_Figura 1: El lanzador de VeraCrypt portable de 32 bits_

![imagen] (tool_veracrypt94.png)

_Figura 2: El lanzador de VeraCrypt portable de 64 bits_

Esto activará la ventana _Control de Cuenta de Usuario_ de **VeraCrypt**

![imagen] (tool_veracrypt95.png)

_Figura 2: La pantalla de Control de Cuenta de Usuario de VeraCrypt_

**Paso 3**. **Haga clic** en **\[Sí\]** para iniciar la versión porable de **VeraCrypt**.

![imagen] (tool_veracrypt96.png)

_Figura 3: La ventana principal de VeraCrypt_

Ahora puede utilizar **VeraCrypt** como de costumbre para crear, administrar, montar y desmontar _ volúmenes cifrados_. Cuando salga de la versión portable de **VeraCrypt**, descargará sus controladores de Windows y saldrá limpiamente. **Si está ejecutando la versión portable de VeraCrypt desde un dispositivo de almacenamiento USB, asegúrese de cerrar los volúmenes abiertos y salir del programa antes de expulsar y retirar el dispositivo de almacenamiento.**

**Consejo:** Para salir completamente de la versión _instalada_ de **VeraCrypt**, incluso después de haber hecho clic en **\[Salir\]** para cerrar la ventana principal, debe hacer clic con el botón derecho en el icono de _Bandeja del Sistema_ y seleccione **\[Salir\]**. La versión portátil no requiere este paso adicional.

Preguntas Frecuentes
===

**_P_**: ¿Tendré que pasar todo mi tiempo escribiendo frases de contraseña en **VeraCrypt**?

**_R_**: No, solo necesita ingresar su frase de contraseña una vez para abrir un volumen cifrado. Después de eso, puede acceder a sus archivos sin una frase de contraseña hasta que cierre el volumen.

**_P_**: ¿Puedo desinstalar **VeraCrypt** si ya no lo quiero? Si lo hago, ¿mis archivos permanecerán encriptados?

**_R_**: Sí. Puede desinstalar **VeraCrypt** abriendo la _Terminal_, escribiendo `sudo veracrypt-uninstall.sh` e ingresando la frase de contraseña que usa para iniciar sesión en su computadora. Más tarde, puede volver a instalar **VeraCrypt** para acceder a los archivos en sus contenedores, que permanecerán encriptados y no se eliminarán cuando elimine **VeraCrypt**. De manera similar, si transfiere su archivo de contenido cifrado a otra computadora, necesitará su contraseña y el programa **VeraCrypt** para abrirlo.

**_P_**: ¿Qué tipo de información requiere cifrado?

**_R_**: Idealmente, debería cifrar todos sus documentos, imágenes y cualquier otro archivo que contenga información privada y confidencial. Y, si su sistema operativo lo admite, debe configurar una encriptación completa del disco para que todos sus archivos estén cifrados siempre que su computadora esté apagada.

**_P_**: ¿Qué tan seguros estarán mis archivos?

**_R_**: **VeraCrypt** ha sido probado y revisado de forma independiente por expertos en seguridad para verificar su desempeño y para determinar si proporciona o no todas las funciones que afirma admitir. Los resultados sugieren que **VeraCrypt** ofrece un nivel de protección muy alto. Sin embargo, elegir una contraseña segura es esencial para la seguridad de sus datos.

**_P_**: ¿Por qué usaría un _volumen oculto_?

**_R_**: Los volúmenes estándar_ de **VeraCrypt ** protegen sus archivos con un cifrado sólido. Los volúmenes ocultos, que proporcionan el mismo nivel de cifrado, están diseñados para ofrecerle más opciones si alguien exige su frase de contraseña de **VeraCrypt**. En lugar de renunciar a su frase de contraseña de volumen oculto, puede renunciar a su frase de contraseña de volumen estándar. Si se le solicita, puede negar que tiene un _volumen oculto_. Sin embargo, para utilizar esta función correctamente, comprenderá mejor su propio entorno de seguridad, comprenderá bien cómo funciona **VeraCrypt** y un conjunto convincente de archivos "señuelo" en su _volumen estándar_.

**_P_**:  ¿Cómo instalo mi _volumen estándar_ original en lugar del que está oculto?

**_R_**: Todo depende de la frase de contraseña que ingrese en la pantalla de contraseña. Si ingresa la frase de contraseña del _volumen estándar_, **VeraCrypt** montará el _volumen estándar_. Si ingresa la frase de contraseña del _volumen oculto_, **VeraCrypt** montará el _volumen oculto_. De esa manera, si alguien le exige que abra su contenedor **VeraCrypt**, puede montar el _volumen estándar_ y negar la existencia de un _volumen oculto_. Bajo las circunstancias adecuadas, esto podría ser suficiente para que usted salga del apuro y se salga de problemas.

**_P_**: ¿Es posible dañar o eliminar inadvertidamente un _volumen oculto_?

**_R_**: Sí. Si continúa agregando archivos a su _volumen estándar_ hasta que se quede sin espacio para su volumen oculto, su _volumen oculto_ se dañará o se destruirá. Hay una opción cuando monta el volumen estándar que puede usar para proteger su _volumen oculto_ para que no se dañe al modificar el contenido de su _volumen estándar_. No debe usar esta opción mientras está siendo observado, ya que revela la existencia de un _volumen oculto_.

**_P_**: ¿Puedo cambiar el tamaño de un volumen de VeraCrypt después de crearlo?

**_R_**: No. Tendrá que crear un nuevo contenedor con un volumen más grande, luego mover sus archivos del volumen anterior al nuevo. Puede hacer esto montando ambos volúmenes al mismo tiempo. Esto se aplica tanto a los volúmenes estándar como a los ocultos.

**_P_**: ¿Puedo usar herramientas como **chkdsk** en el contenido de un volumen montado de **VeraCrypt **?

**_R_**: Los volúmenes **VeraCrypt ** se comportan como dispositivos de almacenamiento normales, por lo que es posible usar cualquier herramienta de comprobación / reparación / desfragmentación del sistema de archivos en el contenido de cualquier volumen **VeraCrypt** montado.

**_P_**: ¿Es posible cambiar la contraseña para un _volumen oculto_?

**_R_**: Sí. La función de cambio de frase de contraseña se aplica tanto a _volumen estándar_ como a _volúmenes ocultos_. Simplemente escriba la frase de contraseña del _volumen oculto_ en el campo Contraseña Actual de la pantalla de cambio de contraseña.

*   [**Preguntas Frecuentes Oficiales de VeraCrypt**](https://www.veracrypt.fr/en/FAQ.html)