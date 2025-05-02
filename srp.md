# Principio de Responsabilidad Única (SRP)
Este principio busca que cada clase tenga una única razón para cambiar. Es un principio de diseño de responsabilidad. Si una clase tiene múltiples responsabilidades, un cambio en una puede afectar a las demás.

## Motivación
___Inconveniente:___ Tanto la clase `Patient` como la clase `Doctor` comparten atributos básicos de una persona, como `documentType`, `documentNumber`, `name`, `lastName`, entre otros. Sin embargo, también presentan diferencias importantes en cuanto a sus responsabilidades y datos específicos. Además, algunos métodos relacionados con estas clases —como los procesos para dar de alta a un paciente o a un doctor— pueden verse afectados por cambios mínimos, lo que hace que el código sea más difícil de mantener y escalar.

Esto viola el **Principio de Responsabilidad Única (SRP)**, que establece que una clase debe tener una única razón para cambiar. En este caso, si cambian los datos personales o la lógica propia de un `Doctor`, también podría verse afectada la clase `Patient`, y viceversa, lo que indica un acoplamiento innecesario.

___Solución propuesta:___ Empleando **SRP**, se propone separar claramente las responsabilidades. Podemos introducir una clase `Person` que contenga los atributos comunes a cualquier persona, como los datos identificatorios básicos. Luego, `Patient` y `Doctor` pueden heredar o componer esta clase y mantener únicamente los atributos y comportamientos que les son propios. 

Además, mediante el uso de **interfaces** y **servicios**, podemos aislar aún más las acciones específicas de cada tipo de entidad, evitando así la duplicación de lógica y facilitando la mantenibilidad y escalabilidad del sistema.

___Ejemplo del mundo real:___ En un hospital, la oficina de admisión se encarga de registrar tus datos personales, mientras que otras áreas se ocupan de los estudios clínicos o de la atención médica. No es necesario que estas funciones estén unidas. Del mismo modo, en el diseño de software, es recomendable mantener una clara separación de responsabilidades. Así, un cambio en la lógica de atención médica no afectará la forma en que se registran los datos personales, y viceversa.

## Estructura de Clases
![SRP](https://github.com/user-attachments/assets/33a598bc-41eb-40b8-88d4-515039bf0670)
<br>
[Link](https://drive.google.com/file/d/1RhbiAJEjSBePJRSgYoT31V1Ral4kFDeO/view?usp=sharing) a diagrama .uxf para ser utilizado en para [UMLetino](https://www.umletino.com/)
