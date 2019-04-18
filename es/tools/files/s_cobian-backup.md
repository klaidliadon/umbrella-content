---
index: 2
title: Cobian Backup
---
# GUÍA DE HERRAMIENTA DE COBIAN BACKUP

## Cobian Backup
Haciendo copia de seguridad de los archivos de su computadora

**Lección para leer: [Copia de seguridad](umbrella://information/backing-up)**
**Ubicación de la descarga:** [http://www.cobiansoft.com/cobianbackup.html] (http://www.cobiansoft.com/cobianbackup.htm)
**Requisitos de la computadora:**
- XP, 2003, Vista, 2008, Windows 7
- Windows 95, 98 y ME son compatibles con la versión 7 de Cobian.
**Versión utilizada en esta guía:** Cobian 10
**Licencia:** Freeware
**Nivel:** Intermedio
**Tiempo requerido:** 30 minutos.

### 1. Cosas que debe saber sobre esta herramienta antes de comenzar

Cobian Backup se utiliza para archivar (o hacer una copia de respaldo) de sus archivos y directorios. Las copias de seguridad se pueden almacenar en otros directorios o unidades en su computadora, otras computadoras en la red de la oficina o en dispositivos extraíbles (CD, DVD y memorias USB). Cobian Backup le permite archivar sus directorios y archivos de forma regular. Funciona de forma silenciosa en segundo plano en su sistema (es decir, en la bandeja del sistema), verifica su programación y ejecuta el proceso de copia de seguridad cuando es necesario. Cobian Backup también puede comprimir y cifrar archivos a medida que genera el archivo de copia de seguridad.

- Usar Cobian le dará:
- La posibilidad de realizar copias de seguridad de todos los documentos, archivos y carpetas.
- La capacidad de comprimir y descomprimir sus archivos de copia de seguridad.
- La capacidad de cifrar y descifrar sus archivos archivados

**Instalación de Cobian - en breve**
- Abra www.cobiansoft.com/cobianbackup.htm
- Haga clic en el enlace "Descargar Cobian Backup" en la página.
- Guarde el instalador, luego encuéntrelo y haga doble clic en él
- Lea la 'Nota de instalación' a continuación antes de continuar
- Una vez que haya instalado con éxito Cobian, puede eliminar el programa de instalación de su computadora.

### 2.0 Cómo instalar Cobian Backup

**Nota de instalación:** Antes de comenzar el proceso de instalación, verifique que tenga las últimas versiones de **Microsoft Windows Installer** y **Microsoft.NET Framework**.

Instalar Cobian Backup es un procedimiento relativamente fácil y rápido.

**Paso 1.** Haga doble clic en "cbsetup.exe"; Puede aparecer el cuadro de diálogo _Abrir Archivo - Advertencia de seguridad_. Si lo hace, haga clic en "Ejecutar" para activar el _extracción de la barra de estado de recursos_ progreso, seguido de unos momentos más tarde por la siguiente pantalla:
![image](tool_cobian1.png)

**Paso 2.** Haga clic en "Siguiente" para activar _Por favor lea y acepte la pantalla del acuerdo de licencia_, marque la opción _Acepto_, y luego haga clic en "Siguiente" nuevamente para activar la siguiente pantalla:
![image](tool_cobian2.png)

**Paso 3.** Haga clic en "Siguiente" para activar la siguiente pantalla:
![imagen](tool_cobian3.png)

**Paso 4.** Verifique la opción _Use Local System account_ en el panel _Service options_, para que se asemeje a la Figura 3 anterior. Esta opción garantiza que Cobian Backup se ejecutará de forma silenciosa en segundo plano todo el tiempo, de modo que las copias de seguridad se realizarán según lo programado.

**Paso 5.** Haga clic en "Siguiente" para activar el siguiente mensaje:
![imagen](tool_cobian4.png)

**Paso 6.** Haga clic en "Sí" para activar la siguiente pantalla de instalación, y luego haga clic en "Siguiente" para continuar con el proceso de instalación.

**Paso 7.** Haga clic en "Listo" para completar el proceso de instalación. Una vez que se haya completado el proceso de instalación, aparecerá el ícono Cobian Backup en la **bandeja del sistema de Windows**.

### 2.1 Cómo hacer una copia de seguridad de sus directorios y archivos

En esta sección, aprenderá cómo realizar una copia de seguridad o archivo simple de un archivo y / o carpeta específicos. Cobian Backup utiliza una _tarea de copia de seguridad_ que se puede configurar para incluir un grupo específico de archivos y/o carpetas. Una tarea de copia de seguridad se puede configurar para que se ejecute en un día y hora específicos.

Para crear una nueva tarea de copia de seguridad, realice el siguiente paso:

**Paso 1.** Haga clic en "Programar" para crear una nueva tarea de copia de seguridad y active la ventana _Nueva tarea_ de la siguiente manera:
![imagen](tool_cobian5.png)

La barra lateral izquierda enumera una serie de pestañas y sus pantallas asociadas, que se utilizan para configurar diferentes opciones y parámetros de copia de seguridad, se muestran en el panel de la derecha. Todas las opciones en la pestaña _General_ se describen a continuación:

### 2.1.1 Descripciones de opciones

_Nombre de la tarea:_ Este campo de texto _Nombre de la tarea_ le permite ingresar un nombre para la tarea de copia de seguridad. Utilice un nombre que identifique la naturaleza de la copia de seguridad. Por ejemplo, si la copia de seguridad va a contener archivos de video, podría llamarlo _Video Backup_.

_Deshabilitado:_ Esta opción debe dejarse sin marcar.
Advertencia: la habilitación de la opción _Deshabilitado_ anulará el resto de las opciones y evitará que la tarea de copia de seguridad se ejecute.

_Incluir subdirectorios:_ Esta opción le permite incluir todos los subdirectorios / carpetas dentro de un directorio/carpeta seleccionado para la tarea de copia de seguridad. Este es un método eficaz para realizar copias de seguridad de una gran cantidad de carpetas y/o archivos. Como ejemplo, si selecciona la carpeta _Mis documentos_ y marca esta opción, todos los archivos y carpetas en _Mis documentos_ se incluirán en la tarea de copia de seguridad.

_Crear copias de seguridad separadas usando marcas de tiempo:_ Esta opción le permite especificar que la fecha y la hora de la tarea de copia de seguridad se incluirán automáticamente en el nombre de la carpeta que contiene su archivo de copia de seguridad. Esta es una buena idea porque significa que podrá identificar fácilmente cuándo se realizó la copia de seguridad.
_Utilice la lógica de atributos de archivo:_ Esta opción solo es relevante cuando elige realizar una copia de seguridad incremental o diferencial (ver más abajo). Los atributos del archivo contienen información sobre el archivo.

**Nota:** La siguiente opción solo está disponible para las versiones del sistema operativo Windows más recientes _e_ incluyendo Windows XP.

_Use Volume Shadow Copy:_ Esta opción le permite hacer una copia de seguridad de los archivos que están bloqueados.
Cobian Backup verifica esta información para determinar si ha habido un cambio en el archivo fuente desde la última vez que se realizó una copia de seguridad. Si luego ejecuta una copia de seguridad _Differential_ o _Incremental_, el archivo se actualizará.

**Nota:** Solo podrá ejecutar una copia de seguridad completa o "ficticia" si _deshabilita esta opción_ (la opción de copia de seguridad ficticia se explica a continuación).

### 2.1.2 Descripciones del tipo de copia de seguridad

_Full:_ Esta opción significa que todos los archivos en la ubicación de origen se copiarán a su directorio de respaldo. Si ha habilitado la opción _Crear copias de seguridad separadas usando la marca de tiempo_, tendrá varias copias de la misma fuente (identificadas por la fecha y la hora de la copia de seguridad en el título de la carpeta). De lo contrario, Cobian Backup sobrescribirá la versión anterior (si existe).

_Incremental:_ Esta opción significa que el programa verificará si los archivos seleccionados para la copia de seguridad se han cambiado desde que se realizó la última copia de seguridad. Si no ha habido ningún cambio, se omitirá durante el proceso de copia de seguridad, lo que ahorrará tiempo de copia de seguridad. La opción _Utilizar atributo de archivo lógico_ debe ser verificada para poder realizar esta copia de seguridad.

_Diferencial:_ El programa verificará si se ha cambiado la fuente desde la última **copia de seguridad completa**. Si no hay necesidad de copiar ese archivo, se omitirá, lo que ahorrará tiempo de respaldo. Si ha ejecutado una copia de seguridad completa anteriormente en el mismo conjunto de archivos, entonces puede continuar haciendo una copia de seguridad utilizando el método diferencial.

_Dummy task:_ Puede usar esta opción para que su computadora ejecute o cierre programas en ciertos momentos. Esta es una opción más avanzada que no es realmente relevante para nuestro procedimiento de copia de seguridad básico.

**Paso 2.** Haga clic en "Aceptar" para confirmar sus opciones de búsqueda y parámetros para su tarea de copia de seguridad.

### 2.2 Cómo crear un archivo de copia de seguridad

Para comenzar a crear un archivo de copia de seguridad, realice los siguientes pasos:

**Paso 1.** Haga clic en "Archivos" en la barra lateral izquierda de la ventana _Nueva tarea_ para mostrar una versión _blank_ de la siguiente pantalla:
![image](tool_cobian6.png)

**Paso 2.** Seleccione los archivos que desea copiar. (En _Figura 3_ arriba, la carpeta _My Documents_ está seleccionada.)

**Paso 3.** Haga clic en "Agregar" en el panel _Source_ para activar el menú _Directory_.

**Paso 4.** Seleccione _Directorio_ si desea hacer una copia de seguridad de un directorio completo, y _Files_ para hacer una copia de seguridad de archivos individuales. Para especificar los archivos o directorios individuales de los que se realizará una copia de seguridad, seleccione _Manualmente_, y escriba la ruta del archivo o el directorio para la copia de seguridad.

**Nota:** Puede agregar tantos archivos o directorios como quieras. Si desea realizar una copia de seguridad de los archivos que se encuentran actualmente en su servidor FTP, elija la opción de sitio FTP (tendrá que tener los datos de inicio de sesión del servidor apropiados).

Cuando haya seleccionado los archivos y / o carpetas, aparecerán en el área _Source_. Como puede ver en _Figura 3_ arriba, la carpeta _My Documents_ se muestra allí, lo que significa que esta carpeta ahora se incluirá en la tarea de copia de seguridad.

El panel _Destination_ especifica dónde se almacenará la copia de seguridad.

**Paso 5.** Haga clic en "Agregar" en el panel _Destination_para activar el menú Directorio.

**Paso 6.** Seleccione _Directorio_ para abrir una ventana del navegador donde selecciona la carpeta de destino para su archivo de copia de seguridad.

**Nota:** Si desea crear varias versiones del archivo de respaldo, puede especificar varias carpetas aquí. Si seleccionó la opción _Manual_, debe escribir la ruta completa a la carpeta donde desea guardar la copia de seguridad. Para usar un servidor de Internet remoto para almacenar su archivo, seleccione la opción de sitio FTP (tendrá que tener los datos de inicio de sesión del servidor apropiados).

La pantalla ahora debe parecerse al ejemplo anterior, ejemplo de archivo(s) y/o carpeta(s) en el área de origen y carpeta(s) en el área de destino. Sin embargo, ¡no hagas clic en _OK_ todavía! Aún necesita establecer un horario para su copia de seguridad.

### 2.3 Cómo programar su tarea de copia de seguridad

Para que su copia de seguridad automática funcione, debe completar la sección Programar. Esta sección le permite especificar cuándo desea que se realice la copia de seguridad.
Para configurar las opciones de programación, realice los siguientes pasos:

**Paso 1.** Seleccione "Programar" en la barra lateral izquierda para activar el siguiente panel:
![image](tool_cobian7.png)

Las opciones _Schedule type_ se enumeran en el menú desplegable, y se describen a continuación:

_Once:_ La copia de seguridad se realizará una sola vez en la fecha y hora especificadas en el área _Fecha / Hora_.

_Daily:_ La copia de seguridad se realizará todos los días a la hora especificada en el área _Date/Time_.

_Weekly:_ La copia de seguridad se realizará en los días de la semana seleccionados. En el ejemplo anterior, la copia de seguridad se realizará los viernes. Puede seleccionar otros días también. La copia de seguridad se realizará en todos los días seleccionados a la hora especificada en el área _Fecha/Hora_.

_Monthly:_ La copia de seguridad se realizará en los días ingresados en el cuadro de días del mes a la hora especificada en el área _Fecha/Hora_.

_Yearly:_ La copia de seguridad se realizará en los días ingresados en el cuadro de días del mes, durante el mes especificado y en el momento especificado en el área Fecha/Hora.

_Timer:_ La copia de seguridad se realizará repetidamente en los intervalos especificados en el cuadro de texto Temporizador en el área _Fecha/Hora_.

_Manually:_ Tendrá que ejecutar la copia de seguridad desde la ventana principal del programa.

**Paso 2.** Haga clic en "Aceptar" para confirmar las opciones y la configuración del programa de copia de seguridad de la siguiente manera:
![image](tool_cobian8.png)

Una vez que haya decidido un cronograma de copia de seguridad, habrá completado el paso final. La copia de seguridad ahora se ejecutará en las carpetas especificadas de acuerdo con la programación que ha elegido.

### 3.0 Cómo comprimir su archivo de copia de seguridad

**Paso 1.** Cree una tarea de copia de seguridad como se documenta en la sección 2.3, que contiene los archivos de copia de seguridad que desea archivar.

**Paso 2.** Seleccione "Archivar" en la barra lateral izquierda para activar la pantalla _Nueva tarea_ de la siguiente manera:
![image](tool_cobian9.png)

El panel **Compresión** se usa para especificar el método para comprimir su copia de seguridad.

**Nota:** La compresión se utiliza para reducir la cantidad de espacio para el almacenamiento de archivos. Si tiene un montón de archivos viejos que usa solo ocasionalmente, pero aún desea conservar, tendría sentido almacenarlos en un formato donde ocupen el menor espacio posible. La compresión funciona eliminando una gran cantidad de codificación innecesaria de sus documentos, mientras deja intacta la información importante. La compresión no daña tus datos originales. Los archivos no son visibles cuando están comprimidos. El proceso debe revertirse y sus archivos deben 'descomprimirse' cuando desee verlos nuevamente.

Las tres subopciones en la lista desplegable _Compression type_ son:

_No Compression: _ Esta opción no realiza ninguna compresión, como cabría esperar.

_Compresión Zip: _ Esta opción es la técnica de compresión estándar para los sistemas **Windows** y la más conveniente. Los archivos una vez creados pueden abrirse con herramientas estándar de Windows (o puede descargar el programa [ZipGenius] (http://www.zipgenius.it/) para acceder a ellos).

La selección de un tipo de compresión listado automáticamente habilita la sección _Split options_, y su correspondiente lista desplegable.

Las _Split options_ se aplican al almacenamiento en medios extraíbles, por ejemplo, CD, DVD, disquetes y memorias USB. Las diversas opciones de división subdividirán el archivo en tamaños que se ajustarán al dispositivo de almacenamiento que elija.

Ejemplo: supongamos que está archivando una gran cantidad de archivos y desea grabarlos en un CD. Sin embargo, su tamaño de archivo resulta ser más grande que 700 MB (el tamaño de un CD). La función de división dividirá el archivo en partes más pequeñas o iguales a 700 MB, que luego podrá grabar en sus CD. Si planea realizar una copia de seguridad en el disco duro de su computadora, o los archivos que desea respaldar son más pequeños que el dispositivo en el que planea almacenarlos, puede omitir esta sección.

Las siguientes opciones están disponibles cuando hace clic en la lista desplegable _Split options_. Su elección dependerá del tipo de dispositivo de almacenamiento extraíble disponible para usted.
![image](tool_cobian10.png)

- Disquete 3,5 ". Esta opción es lo suficientemente grande como para realizar una copia de seguridad de una pequeña cantidad de documentos
- Zip - Disco Zip (verifique la capacidad de la que está usando). Necesitará una unidad Zip especial en su computadora y los discos personalizados.
- CD-R: CD (verifique la capacidad de la que está utilizando). Necesitará una grabadora de CD en su computadora y un programa de grabación de CD (vea la versión [DeepBurner Free] (http://www.deepburner.com/) u otra [herramientas de grabación de disco] (http://www.thefreecountry.com/utilities/dvdcdburning.shtml)).
- DVD (verifique la capacidad de la que está utilizando). Necesitará una grabadora de DVD en su computadora y un programa de escritura de DVD (consulte la versión [DeepBurner Free] (http://www.deepburner.com/) u otra [herramientas de grabación de disco] (http://www.thefreecountry.com/utilities/dvdcdburning.shtml)).

Si está realizando una copia de seguridad en varios dispositivos de memoria USB, es posible que desee establecer un tamaño personalizado.

Para ello, realice los siguientes pasos:

**Paso 1.** **Seleccione** la opción _Custom size_ (bytes), luego escriba el tamaño del archivo en bytes en el campo de texto.

Para darle una idea de los tamaños.
- 1 KB (kilobyte) = 1024 bytes: un documento de texto de una página realizado en Open Office es aproximadamente 20kb
- 1 MB (megabyte) = 1024 KB: una foto tomada con una cámara digital suele tener entre 1 y 3 MB
- 1 GB (gigabyte) = 1024 MB: aproximadamente media hora de una película con calidad de DVD

**Nota:** Al elegir un tamaño personalizado para dividir la copia de seguridad de un CD o DVD, Cobian Backup no copiará la copia de seguridad en su dispositivo extraíble automáticamente. Más bien, creará su archivo en esos archivos en la computadora y tendrá que grabarlos usted mismo en el CD o DVD.

_Password Protect: _ Esta opción le permite ingresar una contraseña para proteger el archivo. Simplemente escriba y luego vuelva a escribir una contraseña en los dos cuadros provistos. Cuando intente descomprimir el archivo, se le pedirá la contraseña antes de que comience la tarea.

**Nota:** Si desea asegurar su archivo, debe pensar en usar otro método que no sea una contraseña. Cobian Backup le permite cifrar su archivo. Esto se trata a continuación.

_Comentario:_ Esta opción le permite escribir algo descriptivo sobre el archivo, pero no es un requisito.

### 3.1 Cómo descomprimir su archivo de copia de seguridad

Para descomprimir su copia de seguridad, realice los siguientes pasos:

**Paso 1. Selecciona > Herramientas > Descompresor.**

La ventana del descompresor aparece como sigue:
![image](tool_cobian11.png)

**Paso 2.** Haga clic en el ícono de abrir archivo para abrir una ventana de navegación que le permita seleccionar el archivo que desea descomprimir.

**Paso 3.** Seleccione el archivo (archivo _.zip_ o _.7x_) y luego haga clic en "Aceptar".

**Paso 4.** Seleccione un directorio en el que desempaquetará (dará salida) al archivo archivado.

**Paso 5.** Haga clic en el icono de compresión para abrir otra ventana que le permite elegir la carpeta en la que desempaquetar el archivo.

**Paso 6.** Seleccione una carpeta y luego haga clic en "Aceptar".

Use el Explorador de Windows para ver los archivos que van a esa carpeta.

### 4.0 Acerca del cifrado

El cifrado puede ser una necesidad para aquellos que desean mantener su copia de seguridad a salvo del acceso no autorizado. El cifrado es el proceso de codificación, o codificación, de datos de tal manera que parece ininteligible para cualquiera que no tenga la clave específica necesaria para decodificar el mensaje. Para obtener más información sobre el cifrado, lea la [Lección sobre la protección de archivos](umbrella://information/protecting-files).

### 4.1 Cómo cifrar su archivo de copia de seguridad

El panel _Strong encryption_ se utiliza para especificar el método de cifrado que se utilizará.

**Paso 1.** Haga clic en el cuadro desplegable _Encryption_ type para activar su lista de diferentes métodos de encriptación.

Para simplificar las cosas, le recomendamos que elija entre los métodos _Blowfish_ o _Rijndael_ (128 bits). Estos brindarán una excelente seguridad para su archivo y le permitirán acceder a los datos cifrados con una contraseña elegida.

**Paso 2.** Seleccione el tipo de _Cifrado_ que desea usar.

**Nota:** _Rijndael_ y _Blowfish_ ofrecen aproximadamente el mismo nivel de seguridad. _DES_ es más débil pero el proceso de cifrado es más rápido.

**Paso 3.** Escriba y vuelva a escribir la contraseña en los dos cuadros provistos.

La fuerza de la contraseña se indica mediante la barra marcada "Calidad de contraseña". Cuanto más se mueva la barra hacia la derecha, más fuerte será la frase de contraseña. Consulte la **[Lección de contraseñas](umbrella://information/passwords)** para obtener información sobre cómo crear y almacenar contraseñas seguras.

**Paso 4.** Haga clic en "Aceptar".

### 4.2 Cómo descifrar su archivo de copia de seguridad

Descifrar su archivo de copia de seguridad es fácil y rápido. Para descifrar su archivo de copia de seguridad, realice los siguientes pasos:

**Paso 1. Seleccione > Herramientas > Descifrar y Claves**

_Esto activará la ventana de descifrado y claves de la siguiente manera:_
![image](tool_cobian12.png)

**Paso 2.** Haga clic en "Seleccionar" para seleccionar el archivo que desea descifrar.

**Paso 3.** Haga clic en "Destino" para seleccionar la carpeta en la que se almacenará el archivo descifrado.

**Paso 4.** Seleccione el mismo tipo de cifrado que seleccionó anteriormente, en la sección 4.1 Cómo cifrar su archivo de copia de seguridad, en la lista desplegable _Methods_.

**Paso 4. Seleccione** el método de cifrado adecuado (el que utilizó para cifrar su archivo de copia de seguridad).

**Paso 5.** Escriba su frase de contraseña en los campos de texto _Passphrase_.

**Paso 6.** Haga clic en "Decrypt!"

El(los) archivo(s) serán descifrados a la ubicación que usted especificó. Si los archivos también fueron comprimidos, deberá descomprimirlos como se describe en la sección 3.1 Cómo descomprimir su copia de seguridad.