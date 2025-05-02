# Principio de Inversión de Dependencias (DIP)
Establece que los módulos de alto nivel no deben depender de módulos de bajo nivel, sino de abstracciones. Es un principio de arquitectura.

## Motivación
___Inconveniente:___ La clase `SistemaGestionTurnos` depende directamente de las clases concretas como `Patient` y `Doctor` para poder crear turnos. Esto viola el **Principio de Inversión de Dependencias (DIP)**, ya que una clase de alto nivel está dependiendo de clases de bajo nivel, en lugar de depender de abstracciones.

___Solución propuesta:___ Aplicando **DIP**, la clase `SistemaGestionTurnos`, en adelante `ShiftManagementSystem`, debe depender de interfaces, no de implementaciones concretas. Es decir, en lugar de depender directamente de `Patient`, `Doctor` o cualquier otra, debe trabajar con interfaces como `IPatientService`, `IDoctorService`, etc. De este modo, la lógica del sistema de turnos se vuelve más flexible, reutilizable y desacoplada, permitiendo que se puedan agregar o modificar roles sin afectar el funcionamiento general del sistema.

___Ejemplo del mundo real:___ En un hospital, todas las personas (doctores, pacientes, personal administrativo, etc.) comparten datos básicos como nombre, apellido y documento. Si el sistema de turnos necesitara trabajar directamente con los datos específicos de cada uno, se volvería complejo y rígido. En cambio, al trabajar con una abstracción común como `Persona`, el sistema puede interactuar con cualquiera de ellos sin depender de detalles concretos, facilitando así su escalabilidad y mantenimiento.

## Estructura de Clases
![DIP](https://github.com/user-attachments/assets/7c5e0331-1914-4531-abb1-a1188cfef593)
<br>
[Link](https://drive.google.com/file/d/1PhuTlvZfFz43mejSKmyiLwN3Z8JqeSD1/view?usp=sharing) a diagrama .uxf para ser utilizado en para [UMLetino](https://www.umletino.com/)
