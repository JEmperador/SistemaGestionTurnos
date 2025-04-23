# Principio de Responsabilidad Única (SRP)
Este principio busca que cada clase tenga una única razón para cambiar. Es un principio de diseño de responsabilidad. Si una clase tiene múltiples responsabilidades, un cambio en una puede afectar a las demás.

## Motivación
___Inconveniente:___ En el modelo original, una clase como ``Patient`` podría estar encargada tanto de gestionar datos personales como de manejar turnos médicos, mezclando funcionalidades que pertenecen a diferentes contextos. Si a futuro cambia la lógica de turnos (por ejemplo, existan turnos virtuales), se debe modificar ``Patient``, lo cual puede traer errores a otras partes del sistema que no tienen nada que ver con turnos.

___Cómo lo soluciona:___ Separando responsabilidades, podríamos tener una clase ``Person`` para los datos personales, y otra ``SistemaGestionTurnos`` para gestionar turnos. Así, un cambio en una no impacta en la otra.

___Ejemplo del mundo real:___ En un hospital, la oficina de admisión gestiona tus datos, y otra área se encarga de tus estudios clínicos. No tienen por qué estar juntas. En software, deberíamos diseñar igual.

## Estructura de Clases
