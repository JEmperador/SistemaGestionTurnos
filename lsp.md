# Principio de Sustitución de Liskov (LSP)
Establece que una subclase debe poder reemplazar a su clase base sin alterar el comportamiento del programa. Es un principio de comportamiento.

## Motivación
___Inconveniente:___ Si una función trabaja con objetos de tipo ``Person``, debería poder recibir una instancia de ``Patient`` o ``Doctor`` y funcionar sin errores. Pero si Doctor no implementa correctamente métodos esperados, como ``getHealthInsuranceNumber()``, podría lanzar errores, romper flujos o producir comportamientos incoherentes.

___Cómo lo soluciona:___ Aplicando LSP, se asegura que todas las subclases respeten el contrato de la clase base. Si ``Person`` define ciertos métodos o propiedades, todas las subclases deben comportarse de forma compatible, aunque internamente lo manejen distinto.

___Ejemplo del mundo real:___ Si en una oficina todos los empleados deben marcar su entrada, no importa si es el jefe o el recepcionista: todos deben usar el mismo mecanismo. Si uno no puede (por ejemplo, porque no tiene tarjeta), rompe el sistema.

## Estructura de Clases
![LSP](https://github.com/user-attachments/assets/b84d928d-439a-4108-8eef-4a2408e230ac)
<br>
[Link](https://drive.google.com/file/d/1Z4reb_GMqzaY3vnk0VsPoGShB23T0PPo/view?usp=sharing) a diagrama .uxf para ser utilizado en para [UMLetino](https://www.umletino.com/)
