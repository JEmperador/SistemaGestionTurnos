# Principio de Sustitución de Liskov (LSP)
Establece que una subclase debe poder reemplazar a su clase base sin alterar el comportamiento del programa. Es un principio de comportamiento.

## Motivación
___Inconveniente:___ Supongamos que las clases `Patient` o `Doctor` implementan métodos que no están definidos en su clase base `Person`, o que su comportamiento difiere notablemente. En ese caso, se rompe el **Principio de Sustitución de Liskov (LSP)**, ya que los objetos derivados (`Patient`, `Doctor`) no pueden ser utilizados de manera intercambiable con la clase base (`Person`) sin alterar la lógica del sistema.

___Solución propuesta:___ Para cumplir con **LSP**, es fundamental que todas las subclases respeten el contrato de la clase base. Si `Person` define ciertos métodos o propiedades, entonces `Patient`, `Doctor`, y cualquier otra subclase como `Nurse`, deben comportarse de manera coherente con esas definiciones, incluso si su implementación interna varía.

Una forma efectiva de lograr esto es mediante el uso de interfaces. Así, cada clase concreta puede implementar comportamientos específicos mientras garantiza la compatibilidad estructural y de comportamiento definida por la abstracción. Al centralizar estas interfaces en servicios, también se logra mayor orden y claridad en el diseño general del sistema.

___Ejemplo del mundo real:___ En una empresa, todos los empleados deben registrar su ingreso mediante el mismo sistema, ya sea el director o el recepcionista. Si uno de ellos no puede hacerlo (por ejemplo, porque no tiene tarjeta o porque usa un sistema distinto), el flujo se rompe y deja de ser confiable. En software, ocurre lo mismo cuando una subclase no cumple con las expectativas establecidas por su clase base.

## Estructura de Clases
![LSP](https://github.com/user-attachments/assets/b84d928d-439a-4108-8eef-4a2408e230ac)
<br>
[Link](https://drive.google.com/file/d/1Z4reb_GMqzaY3vnk0VsPoGShB23T0PPo/view?usp=sharing) a diagrama .uxf para ser utilizado en para [UMLetino](https://www.umletino.com/)
