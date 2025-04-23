# Principio de Abierto/Cerrado (OCP)
Este principio establece que una entidad debe estar abierta a la extensión pero cerrada a la modificación. Es un principio de diseño orientado a la evolución del sistema sin romper lo que ya funciona.

## Motivación
___Inconveniente:___ Si a futuro se incorpora un nuevo rol, como ``Nurse``, y la lógica está directamente en clases como ``Person`` o ``Doctor``, hay que modificar esas clases para agregar lógica nueva. Esto es riesgoso porque puede romper funcionalidades ya probadas.

___Cómo lo soluciona:___ Diseñando el sistema para depender de abstracciones (``Person`` como clase base, por ejemplo), de esa forma, extenderla con nuevas clases (``Nurse``, ``Admin``, etc.) que sobrescriben métodos, sin tocar código anterior.

___Ejemplo del mundo real:___ Un software de recetas puede aceptar ingredientes nuevos sin modificar el sistema. Solo agregás una clase nueva con los métodos requeridos y listo, sin tocar el código ya existente.

## Estructura de Clases
![OCP](https://github.com/user-attachments/assets/af3d202e-40b9-4b99-875f-dfac10067102)
<br>
[Link](https://drive.google.com/file/d/1BqbDcyZK-_6ShKtLORUC7wF9N5DWcMlN/view?usp=sharing) a diagrama .uxf para ser utilizado en para [UMLetino](https://www.umletino.com/)
