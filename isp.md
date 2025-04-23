# Principio de Segregación de Interfaces (ISP)
Indica que, por ejemplo, los clientes no deberían estar forzados a depender de interfaces que no usan. Es un principio de diseño modular.

## Motivación
___Inconveniente:___ Al crear una interfaz ``IPerson`` que incluye métodos como ``requestAppointment()`` o ``getMedicalHistory()``, se esta forzando a todas las clases que implementen esa interfaz, incluyendo ``Doctor``, a declarar métodos que no tiene sentido que usen. Esto aumenta el acoplamiento y la fragilidad del código.

___Cómo lo soluciona:___ Al dividir la interfaz en otras más pequeñas y especializadas (``IPatientActions``, ``IDoctorActions``), cada clase puede implementar solo lo que necesita. Así, los cambios en una parte del sistema no afectan innecesariamente a otras.

___Ejemplo del mundo real:___ Un formulario digital para pacientes y médicos debería tener campos diferentes. No tendría sentido que el médico complete su "número de obra social" como si fuera paciente.

## Estructura de Clases
![ISP](https://github.com/user-attachments/assets/fe234fb9-ea73-48ae-a67b-6679aaadadec)
<br>
[Link](https://drive.google.com/file/d/1Jk70HP7A-h6k1oya4vKevlVkqEszgFyE/view?usp=sharing) a diagrama .uxf para ser utilizado en para [UMLetino](https://www.umletino.com/)
