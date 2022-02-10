En este tema, aprenderá cómo crear un proyecto Gradle simple y cómo Gradle lo administra. Suponemos que ya ha instalado Gradle en su computadora. De lo contrario, siga [las instrucciones de instalación](https://gradle.org/install/ "las instrucciones de instalación") . Para verificar que la instalación se haya realizado correctamente, ejecute el gradle -vcomando. Si obtiene errores, intente buscarlos en Google, lea los documentos o escríbanos un comentario que describa el problema.

## Los conceptos clave de Gradle
Comencemos con una introducción a los conceptos clave en Gradle:** proyectos y tareas .**

- Un **proyecto** puede representar **algo que se va a construir **(p. ej., un archivo JAR o un archivo ZIP) o **algo que hacer** (p. ej., implementar la aplicación). Cada compilación de Gradle contiene uno o más proyectos.
- Una** tarea** es una sola pieza de trabajo que realiza una compilación. Esto puede incluir la compilación de clases, la ejecución de pruebas, la generación de documentos, etc. Cada proyecto es esencialmente una colección de una o varias tareas.

La siguiente imagen ilustra las relaciones entre estos conceptos:

![](https://ucarecdn.com/2ad089d5-37be-4d25-af1e-b26138a4af76/)

En casos simples, una compilación contendrá un solo proyecto con varias tareas. Esta será una situación común en su proceso de aprendizaje. No se preocupe, si los conceptos parecen un poco abstractos. Estudiaremos un ejemplo más específico pronto.

## Inicializar un proyecto básico administrado por Gradle
Inicialicemos un nuevo proyecto con Gradle usando una terminal en su sistema operativo.

En el futuro, lo más probable es que no tenga que hacer esto manualmente, ya que los IDE modernos pueden hacerlo automáticamente.

1. Cree un nuevo directorio para almacenar archivos de su proyecto y acceda a él.

```c
mkdir gradle-demo
cd gradle-demo
```

2. Invoque el `gradle init`comando para generar un proyecto simple. Las versiones modernas de Gradle le pedirán que complete varios parámetros en un formulario de diálogo. Para familiarizarse con el proceso, simplemente elija `basic`como tipo de proyecto y `Groovy`como script de compilación DSL.

Este comando producirá el siguiente resultado:

```c
> Task :init

BUILD SUCCESSFUL in 10s
2 actionable tasks: 2 executed
```
Gradle realizó algunas tareas por usted y ahora hay un proyecto simple con la estructura más básica:

.
```c
├── build.gradle
├── gradle
│   └── wrapper
│       ├── gradle-wrapper.jar
│       └── gradle-wrapper.properties
├── gradlew
├── gradlew.bat
└── settings.gradle
```
Aquí hay información breve sobre todos los archivos generados:

- `El build.gradle`archivo es un archivo principal que especifica el proyecto de Gradle, incluidas sus tareas y bibliotecas externas. Por ahora, este archivo no contiene nada útil, pero en proyectos reales, a menudo se actualiza con nueva información.
- Los archivos `gradle-wrapper.jar`, `gradle-wrapper.properties`y pertenecen `gradlew`a `gradlew.bat`Gradle Wrapper, que le permite ejecutar Gradle sin su instalación manual.
- El `settings.gradle`archivo especifica qué proyectos incluir en su compilación. Este archivo es opcional para una compilación que tiene un solo proyecto, pero es obligatorio para una compilación de varios proyectos.

Construyamos nuestro proyecto invocando el `gradle build`comando desde la misma ubicación donde `build.gradle`reside. Producirá una salida como esta:

```c
> Task :buildEnvironment

------------------------------------------------------------
Root project
------------------------------------------------------------

...

BUILD SUCCESSFUL in 725ms
1 actionable task: 1 executed
```
Entonces, el proyecto se construyó con éxito con una tarea ejecutada.

> También puede invocar` build`y otros comandos como `./gradlew build`para sistemas basados ​​en Unix y `gradlew.bat build`para Windows. Descargará automáticamente Gradle y ejecutará el comando especificado. El uso de contenedores permite a los desarrolladores comenzar a trabajar con un proyecto basado en Gradle sin tener que instalarlo manualmente.

## Modificar el archivo de compilación
Hagamos que nuestra compilación sea más interesante agregando algunas propiedades y una tarea al `build.gradle`archivo usando Groovy DSL.

```c
description = "A basic Gradle project"

task helloGradle {
    doLast {
        println 'Hello, Gradle!'
    }
}
```
Aquí, establecemos la `description`propiedad y definimos una tarea simple que imprime un mensaje de 'hola'. Hay una salida después de ejecutar la tarea con el` gradle -q helloGradle`comando:

```c
> Task :buildEnvironment

------------------------------------------------------------
Root project - A basic Gradle project
------------------------------------------------------------

...

> Task :helloGradle
Hello, Gradle!

BUILD SUCCESSFUL in 831ms
2 actionable tasks: 2 executed
```

Esta compilación se completó con 2 tareas ejecutadas. Nuestra nueva tarea imprimió el `Hello, Gradle!`mensaje. Además, modificamos la descripción del proyecto en el archivo build. El `-q`argumento simplemente simplifica la salida del comando.

> También puede usar Kotlin como DSL dentro del archivo de compilación. Para permitirlo, debe especificar Kotlin como DSL al crear un proyecto. En este caso, el nombre del archivo será build.gradle.kts.También puede usar Kotlin como DSL dentro del archivo de compilación. Para permitirlo, debe especificar Kotlin como DSL al crear un proyecto. En este caso, el nombre del archivo será `build.gradle.kts.`

## La lista de todas las tareas.
Si desea ver todas las posibles tareas de Gradle para realizar, simplemente ejecute el` gradle tasks --all`comando. La lista incluirá también nuestras tareas:

```c
> Task :tasks

------------------------------------------------------------
Tasks runnable from root project - A basic Gradle project
------------------------------------------------------------

Build Setup tasks
-----------------
init - Initializes a new Gradle build.
wrapper - Generates Gradle wrapper files.

Help tasks
----------
buildEnvironment - Displays all buildscript dependencies declared in root project 'gradle-demo'.
...

Other tasks
-----------
helloGradle
```
En un proyecto real, la lista de tareas será mucho más grande porque, además de las tareas estándar, contendrá muchas tareas de varios complementos (como el complemento de Java o Kotlin).

Hemos considerado todos los archivos relacionados con Gradle del proyecto simple generado de forma aislada de cualquier archivo de código fuente.

## Conclusión
Aprendió los conceptos clave de los proyectos de Gradle y estudió todos los archivos de un proyecto generado simple de forma aislada de cualquier archivo de código fuente. ¡Ahora es el momento de combinar Gradle con tu lenguaje de programación favorito!
