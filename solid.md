# Anexo - Principios SOLID

Estos principios permiten diseñar software flexible, mantenible y escalable.

__S - Single Responsibility Principle (SRP)__
<br>
Indica que cada clase tiene una única razón para cambiar, es decir, una sola responsabilidad.
Ayuda a mantener el código claro, modular y fácil de testear.

__O - Open/Closed Principle (OCP)__
<br>
Es decir, clases deben estar abiertas a extensión, pero cerradas a modificación.
Permite agregar nuevas funcionalidades sin tocar el código existente.

__L - Liskov Substitution Principle (LSP)__
<br>
Los objetos de una clase derivada deben poder reemplazar a los de su clase base sin alterar el comportamiento del programa.
Garantiza herencias correctas y uso seguro de polimorfismo.

__I - Interface Segregation Principle (ISP)__
<br>
Ninguna clase debe depender de interfaces que no usa.
Fomenta interfaces específicas y evita que clases tengan métodos innecesarios.

__D - Dependency Inversion Principle (DIP)__
<br>
Las clases deben depender de abstracciones (interfaces), no de implementaciones concretas.
Facilita la reutilización, testeo e independencia entre módulos.

- [Responsabilidad Única (SRP)](srp.md)
- [Abierto/Cerrado (OCP)](ocp.md)
- [Sustitución de Liskov (LSP)](lsp.md)
- [Segregación de Interfaces (ISP)](isp.md)
- [Inversión de Dependencias (DIP)](dip.md)