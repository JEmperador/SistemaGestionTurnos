# Introducción al Diseño Orientado a Objetos

## Descripción del paradigma orientado a objetos

La Programación Orientada a Objetos (POO) es un paradigma de programación que utiliza objetos y clases para organizar el código de manera modular y reutilizable. Es importante porque facilita la gestión de sistemas complejos y promueve la reutilización del código.

## Los cuatro fundamentos de POO

1. **Abstracción**: Representar características esenciales de un objeto.
2. **Encapsulamiento**: Ocultar los detalles internos de un objeto.
3. **Herencia**: Crear nuevas clases a partir de clases existentes.
4. **Polimorfismo**: Permitir que diferentes clases respondan al mismo mensaje.

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
   - **Flujo principal**: Ingresar datos del paciente y guardar en el sistema.
   - **Precondiciones**: El paciente no debe estar registrado previamente.
   - **Postcondiciones**: El paciente queda registrado en el sistema.

2. **Asignar Turno**
   - **Actor**: Recepcionista
   - **Descripción**: Asignar un turno a un paciente.
   - **Flujo principal**: Seleccionar paciente, médico y horario disponible.
   - **Precondiciones**: El paciente y el médico deben estar registrados.
   - **Postcondiciones**: El turno queda asignado y confirmado.

3. **Cancelar Turno**
   - **Actor**: Paciente o Recepcionista
   - **Descripción**: Cancelar un turno asignado.
   - **Flujo principal**: Seleccionar turno y marcarlo como cancelado.
   - **Precondiciones**: El turno debe estar asignado previamente.
   - **Postcondiciones**: El turno queda cancelado y se notifica al paciente.

4. **Consultar Historial**
   - **Actor**: Médico o Recepcionista
   - **Descripción**: Consultar el historial de turnos de un paciente.
   - **Flujo principal**: Seleccionar paciente y ver su historial.
   - **Precondiciones**: El paciente debe tener turnos registrados.
   - **Postcondiciones**: Se muestra el historial de turnos.

5. **Enviar Notificación**
   - **Actor**: Sistema
   - **Descripción**: Enviar notificación de cambio en un turno.
   - **Flujo principal**: Detectar cambio y enviar notificación.
   - **Precondiciones**: El turno debe estar asignado.
   - **Postcondiciones**: La notificación es enviada al paciente y al médico.

## Boceto inicial del diseño de clases

![Boceto de diseño de clases](enlace_a_la_imagen)