Android Studio es el entorno de desarrollo integrado (IDE) oficial para el desarrollo de aplicaciones de Android basado en JetBrains IntelliJ IDEA. Con Android Studio, puede desarrollar aplicaciones para todos los dispositivos Android. En este tema, repasaremos el proceso de instalación y describiremos las funciones básicas de este IDE.

## Instalando
Primero, debe descargar el instalador de Android Studio. Todo lo que tiene que hacer es visitar el sitio web oficial de [desarrolladores de Android](https://developer.android.com/studio "desarrolladores de Android") , hacer clic en el botón "Descargar Android Studio" y aceptar los términos y condiciones. Una vez finalizada la descarga, inicie el archivo.

Abra el archivo de instalación y haga clic en "Siguiente". Verá una lista de componentes que puede instalar. Se recomienda instalar el **Dispositivo Virtual Android (AVD)** . Con esta herramienta, podrá ejecutar y probar sus aplicaciones directamente en su computadora. Si su computadora no cumple con los [requisitos](https://developer.android.com/studio/run/emulator#requirements "requisitos") , simplemente puede desmarcar esta opción.

Luego, selecciona la carpeta donde te gustaría tener tu Studio. Espere a que el instalador extraiga todo lo que necesita en su máquina. Después de eso, inicie Android Studio.

Se le pedirá que importe la configuración. Si es la primera vez que usa Android Studio, simplemente presione "Aceptar" y aparecerá el asistente de configuración. Ahora puedes elegir el tipo de configuración: Estándar o Personalizada.

Elija "Estándar" si no quiere lidiar con un montón de configuraciones, y el IDE hará todo el trabajo por usted. Si elige "Personalizado", podrá seleccionar dónde desea tener su **Kit de desarrollo de software (SDK)** y si desea configurar su dispositivo virtual de inmediato.

![](https://ucarecdn.com/9e6124ba-4133-478b-b3b5-d0fd9599eb9b/)

> Sugerencia: evite usar una ruta de ubicación larga que no sea ASCII para el SDK de Android.Sugerencia: evite usar una ruta de ubicación larga que no sea ASCII para el SDK de Android.

¡Casi estámos allí! Ahora, Android Studio descargará todos los archivos necesarios. Cuando haya terminado, haga clic en "Finalizar". Felicidades: ¡has instalado Android Studio con éxito!

Después de abrir el IDE, aparecerá la pantalla de Inicio:

![](https://ucarecdn.com/e45b4400-5c9b-4df0-a809-eba10cc81370/)

Aquí puede ver las funciones más utilizadas de esta pantalla. Puede crear un nuevo proyecto de Android Studio presionando el botón correspondiente o abrir un proyecto existente desde su computadora. Además, al presionar el botón "Configurar", podrá acceder rápidamente a las configuraciones principales del IDE, como cambiar el tema o el tamaño de fuente, instalar nuevos complementos, etc.

## Configurando tu primer proyecto
Creemos un nuevo proyecto y veamos cómo se ve la ventana principal:

[https://ucarecdn.com/02c4c97d-c808-428f-a77a-b27803e8bcd0/](https://ucarecdn.com/02c4c97d-c808-428f-a77a-b27803e8bcd0/)

Aquí, debe seleccionar una plantilla de proyecto. Puede elegir entre varias plantillas para cualquier tipo de dispositivo Android: teléfonos, tabletas, dispositivos portátiles, televisores, Android Auto e incluso Android Things. En este momento, solo queremos crear una aplicación para un dispositivo Android. Haga clic en la actividad vacía y presione "Siguiente".

![](https://ucarecdn.com/d18bf9a5-0a82-4b58-b366-fdac888a078e/)

Elige un nombre para tu proyecto. Luego, configure la ubicación para guardar el proyecto y el lenguaje de programación para su aplicación. Introduzca su empresa o su apodo en el campo "Nombre del paquete". Por lo general, se ve como "domain.companyname.appname" .

Después de eso, debe elegir la versión mínima de SDK que admitirá su aplicación. Elija sabiamente: no seleccione la versión más reciente o muy antigua de Android. Las versiones realmente antiguas son difíciles de mantener y tienen menos usuarios, y las versiones nuevas también tienen un número limitado de usuarios. Experimente con diferentes versiones de SDK y preste atención al porcentaje de dispositivos que podrán ejecutar su aplicación. A partir de 2020, la mejor opción probablemente sea API 21-23.

Haga clic en "Finalizar". ¡Felicitaciones, ha creado con éxito su proyecto! Android Studio construirá su proyecto y verá la **ventana principal** :

![](https://ucarecdn.com/87947f05-7d85-4fc6-aa4a-00bc4c703acf/)

## Descripción del proyecto
A primera vista, esto puede parecer un poco confuso, pero no te preocupes: lo resolverás paso a paso.

En el lado izquierdo, puede ver su **Vista del proyecto** . Le brinda acceso rápido a sus recursos, código y archivos de compilación. Su código se encuentra en la carpeta "java", y los activos de su proyecto, como imágenes, íconos, fuentes y textos, se encuentran en la carpeta "res". Si no desea distraerse de su código, siempre puede ocultar la estructura de su proyecto haciendo clic en el botón "Proyecto" en la barra lateral izquierda.

En el lado derecho, verá sus archivos abiertos. Esto se llama la **ventana Editor** . Puede cambiar entre sus archivos en la barra de navegación.

En la parte superior, puede ver la ruta al archivo que ha abierto y una barra de herramientas. **La barra** de herramientas le permite realizar una gran variedad de acciones, como compilar, depurar y ejecutar su aplicación. También tiene muchas herramientas útiles de Android que te ayudarán en el proceso de desarrollo más adelante.

Mire todos estos botones alrededor de la ventana de su IDE: estas son las herramientas que le dan acceso a tareas específicas como búsqueda, control de versiones, archivos de dispositivos y más. Los más utilizados son "Logcat", "TODO" y "Terminal".

La **barra de estado** se encuentra en la parte inferior. Allí, puede ver el estado de su IDE y proyecto. Todas las advertencias, sugerencias y mensajes se muestran en la barra de estado.
