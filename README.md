# ChaoticDSL
## ¿Qué es?
Chaotic es un lenguaje de programación esotérico inspirado en Discord, una aplicación de mensajería grupal. Este lenguaje con su propio léxico, sintaxis y semántica se compila a Java para entonces poder ejecutarse en cualquier JVM.

Es un lenguaje con variables globales y procedural. Cuenta con varias de las funcionalidades básicas de otros lenguajes de programación, además permite el uso de Excepcion (la excepción más general de Java) y el uso de arrays o arreglos. 
## Como clonar el proyecto
Este proyecto fue trabajado con EclipseIDE empleando herramientas para el desarrollo de DSLs, el cual puede descargarse desde la [página oficial de Eclipse](https://www.eclipse.org/downloads/packages/release/juno/sr2/eclipse-ide-java-and-dsl-developers). 

Esta herramienta genera una gran cantidad de archivos y código, el cual muchas veces tiene referencia a directorios del ordenador en que se trabaja, por lo que la forma más sencilla de "clonar" el proyecto, es copiando 3 archivos principales, los cuales generan a todos los demás. Para esto, siga los siguientes pasos:
* **Crear el proyecto**
    
    Ingrese a la herramienta de Eclipse y haga click en `New Project`, busque la opción `XText Project` e ingrese la siguiente información:
    - **Project name:** chaotic
    - **Languaje name:** edu.upb.lp.Chaotic
    - **Languaje extension:** chat

    Haga click en `Finish` y espere a que se cree el proyecto.

* **Copiar el Léxico y la Sintaxis**

    Busque dentro del directorio `chaotic/src/edu.upb.lp` el archivo `Chaotic.xtext` y abralo. Dentro, copie el contenido de [Chaotic.xtext](chaotic/src/edu/upb/lp/Chaotic.xtext) ubicado en este repositorio.

* **Generar archivos**

    En el directorio actual se encuentra el archivo `GenerateChaotic.mwe2`, haga click derecho, busque la opción `Run as` y seleccione la opción `Run Workflow`.
    
    Una vez terminado el proceso, es necesario crear un pequeño entorno de desarrollo para el lenguaje, para esto, damos click derecho en el botón `Run` e ingresamos a la opción `Run configurations`, una vez dentro, se debe buscar la opción `Launch Runtime Eclipse`. 

    Estos 2 procedimientos generarán archivos y carpetas para copiar los otros 2 archivos necesarios para el proyecto.

* **Copiar el Validador**

    Busque el directorio `chaotic/src/edu.upb.lp.validation` y ubique el archivo `ChaoticValidator.java`, dentro copie el contenido de [ChaoticValidator.java](chaotic/src/edu/upb/lp/validation/ChaoticValidator.java) ubicado en este repositorio.

* **Copiar el Generador**

    Busque en el directorio `chaotic/src/edu.upb.lp.generator` el archivo `ChaoticGenerator.xtend` y abralo. Dentro, copie el contenido de [ChaoticGenerator.xtend](chaotic/src/edu/upb/lp/generator/ChaoticGenerator.xtend)

* **Abrir el Entorno de desarrollo**

    Una vez copiados todos los archivos el proyecto esta listo para probarse, para esto, vuelva a lanzar el proceso `Launch Runtime Eclipse`. Una vez abierto, puede crear cualquier archivo con la terminación `.chat` y empezar a programar, cada vez que guarde archivos con esta terminación, se generará código Java automáticamente, el cual puede ejecutar y probar.

    Un ejemplo de archivo en Chaotic se puede encontrar en [Fibonacci.chat](./Fibonacci.chat) 