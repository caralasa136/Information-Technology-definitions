# Some information technology definitions

##**Patrones de diseño**


Los patrones de diseño son la base para la búsqueda de soluciones a problemas comunes en el desarrollo de software y otros ámbitos en el diseño de interfaces. Para que una solución sea considerada un patrón debe poseer ciertas características:

> - **Efectividad**
> - **Ser reutilizable**


**Patrón singleton:**


Está diseñado para restringir la creación de objetos pertenecientes a una clase o el valor de un tipo a un único objeto, su intención consiste en garantizar que una clase sólo tenga una instancia y proporcionar un punto de acceso global a ella. Se implementa creando un método en nuestra clase que cree una instancia del objeto sólo si todavía no existe alguna. Para asegurar que la clase no puede ser instanciada nuevamente se regula el alcance del constructor (encapsulamiento).

El patrón **singleton** provee una única instancia global gracias a:

> - La propia clase es responsable de crear la única instancia.
> - Permite acceso global a diha instancia mediante un método de clase.
> - Declara el constructor de clase como privado para que no sea instanciable directamente.


**Factory Method:**


Consiste en utilizar una clase contructora abstracta con unos cuántos métodos definidos y otros abstractos. La clase abstracta tiene métodos concretos que usan algunos de los abstractos; según usemos una u otra hija de esta clase abstracta, tendremos diferentes comportamientos.

Definimos el creador concreto:


```java
public class ConcreteCreator extends Creator{
    public Product factoryMethod() {
        return new ConcreteProduct();
    }
}
```


Definimos el producto y su implementación concreta:


```java
public interface Product{
    public void operacion();
}

public class ConcreteProduct implements Product{
    public void operacion(){
        System.out.println("Una operación de este producto");
    }
}
```


**Patrón Builder:**


Es usado para permitir la creación de una variedad de objetos complejos desde un objeto fuente, éste objeto se compone de una variedad de partes que contribuyen individualmente a la creación de cada objeto complejo a través de un conjunto de llamadas a interfaces comúnes de la clase Builder.


**Clases:**
> - Builder:
>-Interfaz abstracta para crear productos
> - Concrete Builder:
>-Implementación del builder
>-Construye y reúne las partes necesarias para construir los productos
> - Director:
>-Construye un objeto usando el patrón Builder
> - Producto:
>-El objeto complejo bajo construcción



##**¿Qué es ADB en Android?**


**Android Debut Bridge** es una herramienta de software que nos permite interactuar con nuestro smartphone Android desde un ordenador. A través de ADB podemos ejecutar comandos para copiar archivos desde el ordenador al teléfono o viceversa, flashear el firmware completo e incluso reiniciar el dispositivo en modo recovery.


##**¿Para que sirve el operador “final” en java?**


Indica que una variable es de tipo constante, no admitirá cambios después de su declaración y asignación de valor. **final** determina que un atributo no puede ser sobrescrito o redefinido, es decir funcionará como una constante.


##**¿Qué lenguajes soportan la sobrecarga de operadores?**


La sobrecarga de operadores es uno de los mecanismos que nos permite ampliar las capacidades de los lenguajes de programación orientados a objetos.
Algunos lenguajes que soportan ésta característica son:
> - C
> - C#
> - C++
> - Python
> - Java


Es una herramienta bastante útil.


##**¿Qué es el Gradle en Android?**


**Gradle** es una herramienta para automatizar la construcción de nuestros proyectos, por ejemplo las tareas de compilación, testing, empaquetado y el despliegue de los mismos. Es muy flexible para la configuración, pero además ya tiene armadas las tareas para las mayoría de los proyectos por default. Esta herramienta es usado por grandes proyecto **Open Source** como **Spring**, **Hibernate**, y **Grails**. (También lo usan empresas como **LinkedIn** para sus proyectos).

**¿Por qué Google ha creado Gradle?**
Google ha creado uno de los sistemas de compilación más avanzados del mercado para permitir a todos los usuarios escribir sus propios scripts sin necesidad de aprender ningún nuevo lenguaje, disminuyendo asi la curva de aprendizaje y permitiendo llegar a un mayor público la programación en Android.

**¿Qué ventajas tiene?**
> - Permite reutilizar facilmente código.
> - Hace sencilla la tarea de configurar y personalizar la compilación.
> - Permite la distribución sencilla de código al resto del mundo, y fomenta el trabajo en equipo.
> - Gestiona las dependencias de forma potente y cómoda (está basado en Maven).
> - Permite la compilación desde consola, lo que nos puede hacer más sencilla la tarea de compilación en sistemas sin el entorno de desarrollo montado.
> - Lo más importante es que hace increíblemente fácil la creación de diferentes versiones de la aplicación, por ejemplo para hacer múltiples versiones para móviles o tables, versiones de pago o gratuitas, etc..


##**¿Qué es la inyección de dependencias?**


En informática, inyección de dependencias es un patrón de diseño orientado a objetos, en el que se suministran objetos a una clase en lugar de ser la propia clase quien cree el objeto. El término fue acuñado por primera vez por Martin Fowler.
