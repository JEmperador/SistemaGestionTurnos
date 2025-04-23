# Principio de Inversión de Dependencias (DIP)
Establece que los módulos de alto nivel no deben depender de módulos de bajo nivel, sino de abstracciones. Es un principio de arquitectura.

## Motivación
___Inconveniente:___ La clase ``SistemaGestionTurnos`` depende directamente de ``Patient`` y ``Doctor`` para acceder a datos como ``email`` y ``contact``, creando código duplicado y acoplamiento fuerte. Cambios en ``SistemaGestionTurnos`` requieren modificar ambas clases.

___Cómo lo soluciona:___ La abstracción ``Person`` centraliza los datos comunes. ``IPatient`` e ``IDoctor`` heredan de ``Person``, mientras que ``SistemaGestionTurnos`` usa estas abstracciones (``IPatient``, ``IDoctor``). Elimina duplicación, reduce acoplamiento y facilita cambios futuros.

___Ejemplo del mundo real:___ Si conectás tu notebook a internet usando Wi-Fi o cable, da igual: siempre usás una interfaz de red. Cambiar el tipo de conexión no te obliga a cambiar tu sistema operativo.

## Estructura de Clases
![DIP](https://github.com/user-attachments/assets/7c5e0331-1914-4531-abb1-a1188cfef593)
<br>
[Link](https://drive.google.com/file/d/1PhuTlvZfFz43mejSKmyiLwN3Z8JqeSD1/view?usp=sharing) a diagrama .uxf para ser utilizado en para [UMLetino](https://www.umletino.com/)
