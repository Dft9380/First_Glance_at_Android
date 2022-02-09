## ¿Qué es una herramienta de construcción?
Una **herramienta de compilación** es un programa que automatiza el proceso de creación de aplicaciones ejecutables a partir del código fuente. El proceso de compilación incluye compilar fuentes y vincular y empaquetar el código en una forma utilizable o ejecutable.

![](https://ucarecdn.com/4c951427-2fc3-4383-ace8-ac16e3f3a307/)

En proyectos pequeños (como proyectos de aprendizaje), los desarrolladores pueden invocar manualmente el proceso de compilación. Sin embargo, este enfoque no es eficiente para proyectos más grandes, cuando es bastante difícil hacer un seguimiento de lo que se necesita construir. La automatización del proceso de construcción minimiza el riesgo de error humano. Además, una herramienta de compilación automatizada generalmente se ejecuta más rápido que alguien que realiza los mismos pasos manualmente. Como consecuencia, un proceso de construcción automatizado mejora la calidad del producto y ahorra tiempo y dinero.

## ¿Qué pueden hacer las herramientas de construcción?
Las herramientas de compilación modernas pueden realizar una amplia variedad de tareas que los desarrolladores de software realizan en sus actividades diarias:

1. **Descarga y adición de dependencias. **Esto es especialmente conveniente cuando su proyecto depende de una gran cantidad de bibliotecas.
2. **Compilación del código fuente en bytecode .** Las herramientas de compilación invocarán el compilador para todos los archivos de su proyecto.
3.** Paquete de código compilado.** Tendrá un archivo de aplicación listo para producción como JAR, APK o algún otro.
4.** Ejecución de pruebas. **Por ejemplo, probar el archivo de la aplicación cada vez para comprobar si funciona correctamente. Permite a los programadores evitar errores después de modificar la aplicación.
5. **Implementación** en un entorno de producción.

Esta lista de tareas no está completa y puede ser diferente según la herramienta de compilación particular utilizada. Algunas características adicionales pueden estar disponibles; por ejemplo, puede usar algunas herramientas para generar documentación después de la compilación.

## Cree herramientas para proyectos basados ​​en Java
Existen tres herramientas de compilación principales para proyectos basados ​​en Java: **Apache Ant , Apache Maven** y **Gradle** .

**Apache Ant** se lanzó en 2000. Es la más antigua de estas tres herramientas de compilación. Los codificadores rara vez usan **Ant** en nuevos proyectos, pero aún ocurre en la práctica. Puede usar esta herramienta junto con **Apache Ivy **para administrar las dependencias.

**Apache Maven** se lanzó en 2004 y ahora es una de las opciones más populares para los desarrolladores de Java (especialmente para el desarrollo del lado del servidor). Muchos proyectos, tanto antiguos como nuevos, usan Maven como herramienta de compilación debido a sus poderosas posibilidades de administración de dependencias.

**Maven** sigue el concepto de Convención sobre configuración , lo que significa que un desarrollador necesita especificar solo aspectos no convencionales de la aplicación, y todos los aspectos estándar funcionan de manera predeterminada.

**Gradle **es una herramienta nueva en comparación con Ant y Maven. Fue lanzado en 2007 y ahora es estándar para las aplicaciones de Android. Además, los desarrolladores lo usan para el desarrollo de servidores y escritorios. **Gradle** tiene como objetivo "combinar el poder y la flexibilidad de Ant con la gestión de dependencias y las convenciones de Maven en una forma más efectiva de construir".

Todas estas herramientas de compilación son gratuitas y se pueden usar en cualquier sistema operativo.

> Nota: **Apache Maven** y **Gradle** son más que simples herramientas de compilación. Gestionan casi todo el ciclo de vida de una aplicación.Nota: Apache Maven y Gradle son más que simples herramientas de compilación. Gestionan casi todo el ciclo de vida de una aplicación.

También hay otra herramienta de construcción llamada **sbt** ( Scala Build Tool ). Se usa principalmente para proyectos de Scala, pero también puede usarlo para Java o Kotlin.

Si está interesado, [aquí ](https://en.wikipedia.org/wiki/List_of_build_automation_software "aquí ")puede encontrar una lista de herramientas de compilación para diferentes idiomas.

## Conclusión
En resumen, una herramienta de compilación es un software que crea aplicaciones ejecutables a partir del código fuente. El uso de una herramienta de construcción minimiza el riesgo de error humano, acelera el proceso, mejora la calidad del producto y ahorra tiempo y dinero. Las herramientas de compilación modernas realizan muchos trabajos, como descargar y agregar dependencias, compilar código fuente, empaquetar código compilado, ejecutar pruebas e implementar en un entorno de producción. Para proyectos basados ​​en Java, las herramientas de compilación más utilizadas son Apache Ant "viejo", el popular Apache Maven y un "nuevo" Gradle.

