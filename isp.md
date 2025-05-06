# Principio de Segregación de Interfaces (ISP)
Este principio establece que una clase no debe verse obligada a depender de métodos que no utiliza. Es un principio de diseño de interfaces.

## Motivación
___Inconveniente:___ Al crear una interfaz para `Person` que incluye métodos como `registerNurse()` o `getDetailDoctor()`, se está forzando a todas las clases que implementen esa interfaz, incluyendo a clases que dependen de `Person`, a incluir métodos que no necesitan. Esto no solo genera una implementación innecesaria, sino que también acopla el código a funcionalidades que no le conciernen, dificultando su mantenimiento y comprensión.

Esto viola el **Principio de Segregación de Interfaces (ISP)**, que establece que "los clientes no deben verse obligados a depender de interfaces que no utilizan".

___Solución propuesta:___ Haciendo uso de **ISP**, se deben dividir las interfaces en otras más pequeñas y especializadas. Por ejemplo:
 - `PatientRegistration` para `Patient` consumido mediante `IPatientService`.
 - `DoctorUpdateData` para `Doctor` consumido mediante `IDoctorService`.

 Cada clase puede implementar únicamente las interfaces que le son relevantes. Esto reduce el acoplamiento, mejora la cohesión y hace que los cambios futuros afecten solo a las partes necesarias del sistema. Además, el uso de servicios concretos para cada interfaz favorece un diseño más ordenado y mantenible.

___Ejemplo del mundo real:___ Un formulario digital para pacientes y médicos debería tener campos diferentes. No tendría sentido que el médico complete su "número de obra social" como si fuera paciente, o que el paciente tenga que ingresar su "matrícula profesional". De igual manera, en el código, cada clase o componente debe tener acceso únicamente a lo que realmente necesita y utilizar interfaces adecuadas a su contexto.

## Estructura de Clases
![ISP](https://github.com/user-attachments/assets/fe234fb9-ea73-48ae-a67b-6679aaadadec)
<br>
[Link](https://drive.google.com/file/d/1Jk70HP7A-h6k1oya4vKevlVkqEszgFyE/view?usp=sharing) a diagrama .uxf para ser utilizado en para [UMLetino](https://www.umletino.com/)
