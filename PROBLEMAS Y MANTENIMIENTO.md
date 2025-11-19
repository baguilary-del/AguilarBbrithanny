## Propuestas de mantenimiento 
## Propósito del sistema
El sistema permite al usuario organizar y administrar sus citas personales, registrando:
Fecha
Hora
Descripción del evento
Estado (pendiente, completada, cancelada)
El objetivo es ofrecer orden, recordatorio y control sobre actividades personales o laborales.

## Actores del sistema
Usuario principal: Persona que registra y administra sus citas.
Sistema: Guarda, ordena y muestra la información.
(Opcional) Servicio de notificaciones: Sistema externo que envía recordatorios.

## Entradas del sistema
El usuario proporcionará:
Fecha de la cita (formato YYYY-MM-DD)
Hora de la cita (24h)
Descripción de la cita
Acciones: crear, modificar, eliminar o consultar citas

## Procesos del sistema
El sistema debe realizar los siguientes procesos:

✔ A. Registro de nuevas citas

Verificar formato correcto de fecha y hora

Revisar que no haya choques de horarios

Guardar la cita en la lista o base de datos

✔ B. Consulta de citas

Mostrar todas las citas

Mostrar solo las de una fecha específica

Mostrar próximas citas

✔ C. Edición

Cambiar fecha, hora, descripción o estado

Validar nuevamente la disponibilidad del horario

✔ D. Eliminación

Remover la cita seleccionada del registro
## Salidas del sistema

Lista de citas por día

Lista de próximas citas

Mensajes de error (fecha inválida, hora ocupada, campos vacíos)

Confirmaciones (cita creada, editada, eliminada)

## Requisitos funcionales

Registrar citas con fecha, hora y descripción

Modificar citas existentes

Eliminar citas

Consultar todas las citas o por fecha

Evitar citas duplicadas en la misma fecha-hora

Ordenar citas cronológicamente

## Requisitos no funcionales

Usabilidad: interfaz simple e intuitiva

Fiabilidad: datos coherentes sin duplicación

Disponibilidad: idealmente 24/7 si se guarda en la nube

Rendimiento: debe responder de forma rápida aun con muchas citas

Seguridad: proteger datos personales (si se manejan nubes o usuarios)

## Posibles problemas del sistema

Conflictos de horarios
Dos citas a la misma hora generan inconsistencias.

Datos inválidos
Fechas o horas introducidas con formato incorrecto.

Pérdida de información
Si los datos solo se guardan en memoria y no en almacenamiento permanente.

Duplicación de citas
El usuario podría registrar dos citas iguales sin querer.

Falta de orden
Si el sistema no ordena cronológicamente, se vuelve difícil de usar.

Errores en la edición
Cambiar una cita puede generar un conflicto con otra.

Recordatorios no enviados (si se implementan)
Problemas con permisos de notificaciones o dispositivos.

## Mantenimiento del sistema
✔ Mantenimiento correctivo

Arregar errores de carga de datos

Corregir fallas en validaciones de fecha/hora

Arreglar problemas en búsquedas o filtrados

✔ Mantenimiento preventivo

Revisar el formato y la integridad de los datos

Optimizar búsquedas y ordenamiento

Actualizar dependencias o librerías

✔ Mantenimiento evolutivo

Agregar recordatorios por correo o notificación

Implementar sincronización con Google Calendar

Crear categorías (salud, trabajo, ocio)

Añadir citas recurrentes (semanales/mensuales)

## Conclusión del análisis

Este sistema es esencial, escalable y de bajo riesgo, pero requiere:

Buen control de datos

Validación estricta de fechas y horas

Manejo adecuado de conflictos

Una estructura flexible para ampliar funciones

Con una base sólida, puede evolucionar en una aplicación completa de agenda digital.