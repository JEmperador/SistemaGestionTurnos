# Introducción al Diseño Orientado a Objetos

## Descripción del paradigma orientado a objetos

La Programación Orientada a Objetos (POO) es un paradigma de programación que utiliza objetos y clases para organizar el código de manera modular y reutilizable. Es importante porque facilita la gestión de sistemas complejos y promueve la reutilización del código.

## Los cuatro fundamentos de POO

1. **Abstracción**: Representar las características y métodos esenciales de un objeto.
   - Ejemplo: Tomando como referencia el concepto de Vehículo, podemos abstraer sus propiedades fundamentales como la Marca y el Modelo, así como sus acciones principales como Acelerar(), Detenerse(), Girar() y EncenderLuces(). Si bien un automóvil, una motocicleta, una camioneta, un avión y un barco son tipos de vehículos con mecanismos internos muy diferentes para realizar estas acciones, a un nivel abstracto, comparten estas características y comportamientos esenciales desde la perspectiva de un usuario o de una interacción general con el concepto de "vehículo".
2. **Encapsulamiento**: Exponer solo los datos necesarios y ocultar los detalles internos de un objeto.
   - Ejemplo: El número de motor o el número de chasis de un vehículo son datos internos y únicos que no se exponen directamente a los posibles compradores. Esta información, crucial para la identificación y verificación legal del vehículo, se revela únicamente a los propietarios autorizados y bajo circunstancias específicas (como la verificación registral). Este mecanismo de encapsulamiento previene el uso indebido de dicha información y protege la singularidad e identidad del vehículo.
3. **Herencia**: Crear nuevas clases heredando características y métodos de clases existentes.
   - Ejemplo: Si definimos una clase base Vehiculo con atributos como Marca y Modelo, y métodos como Arrancar(), Detenerse() y Girar(), mediante la herencia podemos crear clases más específicas como Auto y Moto. Estas clases Auto y Moto heredarán automáticamente los atributos y métodos de Vehiculo, y a su vez, podrán incorporar atributos y métodos propios (como numeroDePuertas en Auto o cilindrada en Moto) o modificar el comportamiento de los métodos heredados para adaptarlos a sus particularidades.
4. **Polimorfismo**: Permitir que un objeto se comporte de diferentes formas dependiendo del contexto.
   - Ejemplo: Consideremos una clase base Vehiculo que define un método como obtenerTipoDeDesplazamiento(). Las clases derivadas como Auto, Moto, Camion, Avion y Barco heredarán este método, pero cada una lo implementará de forma diferente para reflejar su modo particular de desplazamiento (por ejemplo, "terrestre sobre ruedas" para auto, camión y moto; "aéreo" para avión; "acuático" para barco). Una función que reciba un objeto de tipo Vehiculo podría invocar el método obtenerTipoDeDesplazamiento(), y el resultado variaría dinámicamente en función del tipo concreto de vehículo que se le haya pasado como argumento.

## Requisitos iniciales del sistema

1. Registrar pacientes y profesionales de la salud.
2. Asignar turnos según la disponibilidad de los profesionales.
3. Llevar un historial de turnos realizados.
4. Enviar notificaciones por correo electrónico o mensaje de texto.
5. Proteger la información de contacto de pacientes y profesionales.

## Casos de uso

1. **Registrar Paciente**
   - **Actor**: Recepcionista
   - **Descripción**: Registrar un nuevo paciente en el sistema.
   - **Flujo principal**: La recepcionista solicita al paciente su DNI, Apellido y Nombre, Fecha de Nacimiento y datos de contacto (correo electrónico y número de celular). El registro se realiza de forma presencial en todos los casos, y se debe verificar que el DNI y los datos brindados coincidan con la identidad del paciente.
   Una vez confirmado el registro, se notifica al paciente vía correo electrónico o mensaje de texto.
   - **Precondiciones**: El paciente no debe estar registrado previamente.
   - **Postcondiciones**: El paciente queda registrado en el sistema y se lo notifica.

2. **Asignar Turno**
   - **Actor**: Recepcionista
   - **Descripción**: Asignar un turno a un paciente.
   - **Flujo principal**: Se verifica la identidad del paciente mediante su DNI, Apellido y Nombre, ya sea de forma presencial o virtual.
   Se comprueba que no tenga un turno asignado en el mismo horario del mismo día, y se procede a asignar un médico (ya registrado en el sistema) y un horario disponible.
   Una vez confirmada la asignación, se informa al paciente por correo electrónico o mensaje de texto.
   - **Precondiciones**: El paciente y el medico deben estar registrados, a su vez no debe tener un turno asignado previamente a la misma hora el mismo dia.
   - **Postcondiciones**: El turno queda asignado y se notifica al paciente.

3. **Cancelar Turno**
   - **Actor**: Paciente o Recepcionista
   - **Descripción**: Cancelar un turno asignado.
   - **Flujo principal**: Se valida la identidad del paciente mediante DNI, Apellido y Nombre, ya sea presencial o virtualmente.
   Se comprueba que exista un turno previamente asignado que coincida con los datos provistos (médico y horario) y que el mismo se encuentre activo.
   Luego se procede a actualizar su estado a cancelado. Una vez confirmada la cancelación, se informa al paciente por los medios de contacto registrados.
   - **Precondiciones**: El paciente y el medico deben estar registrados, a su vez el turno debe estar asignado previamente.
   - **Postcondiciones**: El turno queda cancelado y se notifica al paciente.

4. **Consultar Historial**
   - **Actor**: Médico o Recepcionista
   - **Descripción**: Consultar el historial de turnos de un paciente.
   - **Flujo principal**: Se selecciona al paciente mediante su DNI, ya sea de forma presencial o virtual.
   Se verifica la existencia de turnos previamente cargados y se validan sus respectivos estados.
   - **Precondiciones**: El paciente deben estar registrado, poseer turno/os previamente solicitado/os .
   - **Postcondiciones**: Se muestra el historial de turnos.

5. **Enviar Notificación**
   - **Actor**: Sistema
   - **Descripción**: Enviar notificación de cambio en un turno.
   - **Flujo principal**: Al detectarse una modificación en el estado del turno y/o en la información del paciente o del médico, el sistema procede a enviar notificaciones automáticas utilizando los datos de contacto disponibles.
   - **Precondiciones**: El paciente debe estar registrado, el turno debe estar asignado.
   - **Postcondiciones**: La notificación es enviada al paciente y al médico.

6. 

## Boceto inicial del diseño de clases

![Boceto de diseño de clasesV1](https://github.com/user-attachments/assets/e4d63f42-a61d-4891-9083-a10e265d890b)

[Link](https://drive.google.com/file/d/1vm-yOXY54Wm_AMSY3Fgsf0Nyrai0VTsE/view?usp=sharing) de archivo uxf para [umletino](https://www.umletino.com/)
