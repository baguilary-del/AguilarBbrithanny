##Aplicación para gestionar citas personales con fechas, horas y descripciones. 
## Proposito
El propósito principal del sistema Agenda Personal de Citas es brindar a los usuarios una herramienta digital eficiente para organizar, registrar y consultar sus compromisos personales o laborales de manera sencilla y accesible. Con esta aplicación, el usuario podrá programar citas con información detallada como fecha, hora, lugar y descripción, asegurando una mejor gestión del tiempo y evitando olvidos o superposición de eventos.
## Descripción General del Sistema y de los Usuarios
El sistema Agenda Personal de Citas consiste en una aplicación informática que permite registrar y administrar citas personales de forma sencilla y ordenada. Su interfaz gráfica mostrará un menú principal con opciones para agregar nuevas citas, modificar o eliminar las existentes, buscar citas por fecha o palabra clave, y visualizar todas las citas programadas.
Además, incluirá una función de notificaciones o alertas que recordará al usuario sus próximos compromisos con antelación configurable.
El sistema almacenará los datos de manera local en el dispositivo, asegurando la disponibilidad de la información incluso sin conexión a internet. Su diseño prioriza la simplicidad, accesibilidad y usabilidad, de modo que cualquier usuario, sin conocimientos técnicos, pueda utilizarlo con facilidad.
## Requerimientos funcionales 
ID	Nombre del requisito	Descripción	Criterios de aceptación
RF1	Registro de citas	El sistema permitirá al usuario registrar una nueva cita indicando fecha, hora, lugar, descripción y personal de contacto	El sistema debe guardar las citas correctamente y mostrar un mensaje de confirmación en menos de 3 segundos

RF2	Visualización de calendario 	El sistema mostrará al usuario un calendario con todas las citas registradas, organizadas por día, semana o mes 	El usuario debe poder visualizar el calendario completo sin errores en menos de 2 segundos
RF3	Edición y cancelación de citas	El sistema permitirá modificar o cancelar citas previamente registradas
	El sistema debe actualizar o eliminar la cita correctamente y mostrar mensaje de confirmación en menos de 3 segundos 
RF4	Notificaciones y recordatorios 	El sistema enviara notificaciones o recordatorios antes del inicio de cada citas, según la configuración del usuario 	El sistema debe generar la notificación en el tiempo establecido y mostrarla correctamente al usuario 
RF5	Historial de citas 	El sistema permitirá consultar el historial de citad pasadas, mostrando hora, fecha, lugar y observaciones asociadas 	El usuario debe visualizar el historial completo y sin errores, con todos los datos registrados correctamente
## requerimientos no funcionales 
ID	Nombre del requisito	Descripción	Tipo	Criterios de aceptación

RFN1	Tiempo de respuesta del sistema 	El sistema deberá responder a las acciones del usuario (registro, edición o consulta de citas) en un tiempo máximo de 2 segundos.	Requerimiento del producto (rendimiento)	En pruebas de usos normal, el tiempo de respuesta no debe superar los 2 segundos 

 El sistema no debe mostrar mensajes de espera prolongados ni bloqueos.
RFN2	Disponibilidad continua del servicio 	El sistema deberá mantenerse operativo de forma continua durante el 95% del tiempo mensual, garantizando el acceso al calendario y recordatorios.	Requerimiento de la organización (Fiabilidad / Disponibilidad)	1. En simulaciones de fallos, el sistema se restablece automáticamente en menos de 1 minuto 

 En pruebas de disponibilidad, el sistema debe alcanzar una operatividad mínima del 95 %
RFN3	Protección de datos personales	
El sistema deberá proteger toda la información del usuario (datos personales, agenda, contactos y citas) mediante cifrado y autenticación segura.
Requerimiento externo	Requerimiento Externo (Legal / Ético)
	1. Auditorías de seguridad confirman la correcta implementación del cifrado AES-256.2. Solo usuarios autenticados pueden acceder a la información personal.3. El sistema cumple con la Ley Orgánica de Protección de Datos Personales.
## Registro de pruebas Unitarias y de Validación:
Tipo de pruebas	Requerimientos asociados	Datos de entrada	Resultados esperados	Resultados
obtenidos
Unitarias	RF1 - Registro de citas 	Fecha: 25/ 10/ 2025 Hora: 10:30 
Descripción: “ reunión medica”
Contacto: “ Carlos Pérez ”	El sistema registra la cita registrada exitosamente en menos de 3 segundo 	Cita registrada correctamente. Tiempo de respuesta: 2.3 s
Unitarias
	RF2 - Visualización del calendario 	Solicitud de vista mensual desde la interfaz principal 	El sistema muestra el calendario completo con todas las citas registradas en menos de 2 segundos	Calendario cargado correctamente. Tiempo de carga: 1.9 s
Unitarias	RF4 – Edición y cancelación de citas 	Cita ID #012 modificada (nuevo horario: 11:00)	El sistema actualiza la cita y muestra mensaje de confirmación de modificación en menos de 3 segundos.	Cita modificada correctamente. Mensaje mostrado en 2.4 s
Validaciones	RFN1 – 
Tiempo de respuesta del sistema 	20 usuarios registrando y visualizando citas simultáneamente	El sistema responde sin errores y mantiene tiempo medio de respuesta menor a 2 segundos.	Sistema estable. Tiempo medio: 1.7 s. Sin errores.
Validaciones	RFN3 – 
Protección de datos personales 	Solicitud de inicio de sesión y registro de datos personales	El sistema solicita consentimiento, aplica cifrado AES-256 y restringe acceso a usuarios no autenticados.	Consentimiento solicitado. Cifrado verificado. Acceso restringido correctamente.
## Tipos de mantenimientos
El sistema presentó dos situaciones problemáticas principales, y para cada una se aplicaron tres tipos de mantenimiento: correctivo, preventivo y perfectivo.
## Reflexion final
Las pruebas realizadas permiten asegurar que los requerimientos definidos se cumplen correctamente. Las   pruebas unitarias confirman que las funciones básicas del sistema —como registrar, editar y visualizar citas— operan sin errores. Las pruebas de validación, por su parte, verifican que el comportamiento del sistema coincide con lo esperado desde el punto de vista del usuario, garantizando que las búsquedas y notificaciones funcionen como se diseñaron. Gracias a este proceso, se pueden detectar posibles fallos tempranamente y corregirlos antes de la implementación definitiva. En conjunto, las pruebas no solo validan los requerimientos, sino que también aseguran la calidad, usabilidad y confiabilidad del software, cumpliendo con el objetivo de ofrecer una herramienta útil y eficiente para la gestión personal de citas.