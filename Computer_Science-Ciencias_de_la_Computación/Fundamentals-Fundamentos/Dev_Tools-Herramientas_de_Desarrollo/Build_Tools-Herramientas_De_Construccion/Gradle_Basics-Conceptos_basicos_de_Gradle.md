**Gradle **es una herramienta de automatización moderna que ayuda a crear y administrar proyectos escritos en Java, Kotlin, Scala y otros lenguajes basados ​​en JVM. Describe las dependencias del proyecto y determina cómo construir un proyecto. Gradle utiliza un sistema de complementos bien diseñado, por eso es una herramienta altamente extensible. Puede usar complementos para el control automático de versiones, pruebas automáticas, informes sobre la compilación, etc.

Una de las mejores cosas de Gradle es su lenguaje específico de dominio (DSL) [basado en Groovy ](https://en.wikipedia.org/wiki/Apache_Groovy "basado en Groovy ")que brinda a los desarrolladores una forma específica de crear scripts de compilación personalizados. Los desarrolladores de Kotlin son especialmente afortunados ya que Gradle también comenzó a admitir Kotlin para dichos scripts. Por lo tanto, hay dos idiomas para escribir los scripts de compilación de Gradle (Groovy y Kotlin) y puede elegir cualquiera de ellos.

> Tenga en cuenta que DSL es un lenguaje informático especializado en un dominio de aplicación particular (como la automatización de compilación). Esto contrasta con un lenguaje de propósito general (GPL), que es ampliamente aplicable en todos los dominios.Tenga en cuenta que DSL es un lenguaje informático especializado en un dominio de aplicación particular (como la automatización de compilación). Esto contrasta con un lenguaje de propósito general (GPL), que es ampliamente aplicable en todos los dominios.

![](https://ucarecdn.com/363cc5f1-3524-4532-a103-d7e519bf2132/)

Hoy en día, Gradle es un estándar de facto para crear aplicaciones de Android. Sin embargo, los programadores lo usan para el desarrollo del lado del servidor y del escritorio, reemplazando gradualmente otras herramientas de compilación con él. Aquí está la [lista completa de características](https://gradle.org/features/ "lista completa de características") , si desea obtener más información sobre ellas.

## Los conceptos clave
Las características clave de Gradle son las siguientes:

- **Archivos de configuración**. Gradle usa varios tipos de archivos de configuración para describir cómo construir un proyecto.

- **Construido por convención**. Un programador no necesita especificar cada paso de construcción que debe realizarse. En cambio, Gradle usa la configuración y el comportamiento predeterminados. Aunque, cada paso del proceso de compilación predeterminado se puede personalizar si es necesario.

- **Gestión de dependencias.** Gradle descarga automáticamente bibliotecas externas específicas y resuelve casos de conflicto con dependencias. Puede declarar tantas dependencias como necesite para un proyecto.

- **Construye _** Gradle permite a los programadores diseñar compilaciones comprensibles bien estructuradas y fáciles de mantener. También admite casos complejos, como proyectos múltiples o construcciones parciales.

- **Facilidad de migración** . Gradle puede adaptarse fácilmente a cualquier estructura de proyecto que tengas. Por lo tanto, siempre puede desarrollar su proyecto exactamente de la manera que desee.

- **DSL **(basado en Groovy y Kotlin) para escribir scripts en archivos de configuración.

## Descargando e instalando Gradle
Puede descargar Gradle desde el [sitio web oficial](https://gradle.org/releases/ "sitio web oficial") y descomprimir el archivo en algún lugar de su computadora. Recomendamos elegir la versión 5.0 o superior.

Para instalar Gradle, siga las [instrucciones de instalación](https://gradle.org/releases/ "instrucciones de instalación") para su sistema operativo.

Para verificar que la instalación se ha completado correctamente, ejecute el siguiente comando:


```c
gradle -v
```
El resultado debería ser similar a:

```c
------------------------------------------------------------
Gradle 5.6.4
------------------------------------------------------------
```
Su versión de Gradle puede diferir; lo principal es que el comando debería funcionar con éxito. Si tiene errores, intente buscarlos en Google, lea los documentos o escríbanos un comentario que describa su problema.

## Conclusión
Aunque es otra herramienta de compilación, las compilaciones de Gradle son más ordenadas y concisas gracias a su DSL. Proporciona una rica infraestructura para construir, probar, automatizar y entregar su proyecto. A continuación, aprenderemos cómo crear el proyecto Gradle más simple.

