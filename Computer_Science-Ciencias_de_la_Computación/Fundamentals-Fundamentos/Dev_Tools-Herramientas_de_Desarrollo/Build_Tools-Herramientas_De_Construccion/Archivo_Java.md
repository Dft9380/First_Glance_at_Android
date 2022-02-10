## ¿Qué es el archivo Java?
**Java Archive (JAR)** es un formato de archivo independiente de la plataforma para empaquetar varios archivos y distribuirlos como una sola unidad. Por lo tanto, es útil si su aplicación contiene muchos archivos.

![](https://ucarecdn.com/76368b85-f033-4ac7-9185-dfaa43238e44/)

Estos son los principales beneficios de un archivo JAR:

- puede agregar múltiples archivos de diferentes tipos;
- es un archivo comprimido (con un algoritmo **ZIP** ) que reduce el tamaño de la aplicación y facilita su traslado a través de una red;
- puede firmarlo digitalmente (esta función no se tratará en este tema).

Un JRE puede iniciar una aplicación empaquetada en un JAR, pero para crear un JAR necesita usar un JDK.

## La estructura de un archivo JAR
Un archivo JAR es simplemente una agregación de archivos de código de bytes ( .class), archivos de configuración (p. ej., .json, .xml), imágenes e incluso clips de sonido en un solo archivo comprimido. Todos los archivos, excepto los archivos de código de bytes, generalmente se denominan **recursos** .
También se recomienda que un archivo JAR contenga un archivo especial denominado MANIFEST.MFen una carpeta especial denominada META-INF. Este archivo debe describir el archivo JAR en sí mismo (un manifiesto es un tipo de metadatos): su versión, el autor, etc.

Aquí está el ejemplo de una estructura de un archivo JAR:

```c
example.jar
├── META-INF
│   └── MANIFEST.MF
├── second
│   ├── Main.class
│   └── MyIcon.png
└── third
    └── another
        └── OneMore.class
```
Por lo general, un archivo JAR tiene un conjunto de **paquetes.class** agrupados por . Por ahora, imagine un paquete simplemente como un directorio o algunos directorios anidados. En nuestro ejemplo, hay dos paquetes: y . Además, para representar un nombre de paquete específico, se usan **puntos en lugar de barras** (por lo que la notación sería correcta en este caso). Finalmente, hay algunas reglas para nombrar los paquetes. Por ejemplo, un nombre puede contener letras y dígitos, pero no guiones ( )`.secondthird/anotherthird.another-`

Como puede ver, JAR puede tener varios paquetes y muchos `.class` archivos y/o recursos en estos paquetes.

El archivo de manifiesto tiene un conjunto de encabezados. El nombre y el valor están separados por dos puntos ( `:`). Echa un vistazo a un pequeño ejemplo a continuación:

```c
Manifest-Version: 1.0
Created-By: 9.0.1 (Oracle Corporation)
Main-Class: second.Main
```

La característica clave aquí es el encabezado opcional `Main-Class`que define la ruta relativa de una clase con el mainmétodo para iniciar la aplicación. El valor no debe tener la `.class`extensión adjunta al nombre de la clase.

> Es importante recordar que la **última línea** del archivo de manifiesto debe terminar con una **nueva línea o un retorno de carro** , o no se analizará correctamente.Es importante recordar que la última línea del archivo de manifiesto debe terminar con una nueva línea o un retorno de carro , o no se analizará correctamente.

## Ejecutar un archivo JAR
Hay dos formas de ejecutar un archivo JAR, dependiendo de si desea usar `Main-Class`el encabezado en el archivo de manifiesto o no.

- si este encabezado no está presente o desea especificar la clase principal manualmente, ejecute:
```c
java -cp app-without-main-class-header.jar path.to.Main
```
El último parámetro aquí es el nombre completo de la clase (con paquetes). La `-cp`opción significa **classpath** , es decir, rutas a todos los JAR que el JRE debe escanear en busca de código de bytes y recursos. Si lo desea, puede repetir varios `-cp path-to-Nth.jar`pares de parámetros para proporcionar al JRE varios archivos JAR diferentes.

- si este encabezado está presente, ejecute:
```c
java -jar app-with-main-class-header.jar
```
Puede intentar ejecutar ambos comandos localmente con estos dos archivos JAR (descomprima los archivos de nivel superior):

- [una aplicación de demostración sin encabezado de clase principal](https://stepik.org/media/attachments/lesson/123928/app1.zip "una aplicación de demostración sin encabezado de clase principal") (la ruta principal es `myapp.Main`);
- [una aplicación de demostración con encabezado de clase principal .](https://stepik.org/media/attachments/lesson/123928/app2.zip "una aplicación de demostración con encabezado de clase principal .")
Ambos imprimen la misma línea:



    Hello, Java
Además, puede encontrar algunos archivos JAR en Internet e intentar ejecutarlos. Al mismo tiempo, puede ver su estructura interna: simplemente reemplace `.jar`y `.zip`abra estos archivos como archivos comprimidos.

## Conclusión
Ahora sabe qué es JAR, en qué consisten los archivos JAR y cómo ejecutarlos en su computadora. No hemos discutido aquí cómo crear un JAR. Por lo general, los desarrolladores usan herramientas de compilación (como Maven o Gradle) o un IDE (como IntelliJ IDEA o Eclipse), que tratamos en otros temas. También puede crearlos simplemente fusionando algunos archivos en un `.zip`archivo y renombrándolo en un` .jar`archivo.

Si desea obtener más información sobre la estructura del archivo JAR, lea la [especificación .](https://docs.oracle.com/javase/7/docs/technotes/guides/jar/jar.html "especificación .")
