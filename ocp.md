# Principio de Abierto/Cerrado (OCP)
Este principio establece que una entidad debe estar abierta a la extensión pero cerrada a la modificación. Es un principio de diseño orientado a la evolución del sistema sin romper lo que ya funciona.

## Motivación
___Inconveniente:___ Si quisiéramos agregar un nuevo rol, como `Nurse`, podríamos pensar en reutilizar la clase `Doctor` como base. Sin embargo, esto sería un error de diseño, ya que `Nurse` y `Doctor` no comparten necesariamente los mismos comportamientos ni responsabilidades. Reutilizar una clase inadecuada implicaría modificar constantemente `Doctor` cada vez que necesitemos adaptar algo para `Nurse`, violando así el **Principio de Abierto/Cerrado (ORP)**.

___Solución propuesta:___ Aplicando **OCP**, el sistema debe estar **abierto a la extensión pero cerrado a la modificación**. Esto se logra creando una clase base `Person` que contenga los datos comunes (como `documentNumber`, `name`, `lastName`, etc.) y luego extenderla mediante clases como `Doctor`, `Patient`, `Nurse`, `Admin`, entre otras.

Cada clase concreta podrá tener sus propios atributos y comportamientos sin afectar las demás. Además, mediante el uso de interfaces y servicios específicos para cada rol, podemos mantener un diseño desacoplado y flexible, favoreciendo la evolución del sistema sin romper su estructura.

___Ejemplo del mundo real:___ En un hospital, al principio solo puede haber un `Doctor` para atender pacientes. Con el tiempo, se incorpora nuevo personal como `Nurse`, personal administrativo, o técnicos de laboratorio.  
Cada uno cumple funciones distintas, pero todos forman parte del sistema hospitalario. El software debe ser capaz de adaptarse a esta diversidad sin alterar lo ya construido, simplemente extendiendo el sistema para incluir nuevas entidades sin modificar el código existente.

## Estructura de Clases
![OCP](https://github.com/user-attachments/assets/a38f8080-c592-4ba3-be39-0e4f8584e46b)
<br>
[Link](https://drive.google.com/file/d/1pn4xhkA0dYJSIFR3W7fnIM5IqVNSZ7IV/view?usp=sharing) a diagrama .uxf para ser utilizado en para [UMLetino](https://www.umletino.com/)


