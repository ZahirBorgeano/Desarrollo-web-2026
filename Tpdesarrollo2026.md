```
Equipo Trabajo desarrollo web 2026
Integrantes Brian Andrada
Versión 1
Fecha 02/06/
Docente Pablo Pedernera
```
## Descripción del sistema y contexto real

Plataforma web y aplicación integradas para gestión de turnos de una empresa del sector
salud de gran alcance con distintas sedes en Argentina. Actualmente posee una página
web con funciones limitadas. Se requiere crear una nueva plataforma unificada con una app
que a su vez facilite las posibles acciones relacionadas a los turnos tales como información
sobre especialidades ,solicitudes, cancelaciones, reasignaciones,etc.
El objetivo de la plataforma es facilitar la gestión de citas y turnos, tanto para clientes
individuales como para empresas de servicios. Permitirá a los usuarios reservar citas de
manera rápida y sencilla, y a las empresas gestionar sus agendas de forma eficiente. A
través de funciones como reservas en tiempo real, recordatorios automáticos y sugerencias
de horarios disponibles, la plataforma busca minimizar ausencias y maximizar la ocupación
de los turnos disponibles.

## Identificación de stakeholders

Usuarios finales :
Profesional de la salud
Pacientes
Empleados administrativos
Cliente directo:
Sanatorio Escoces
Patrocinador: Dirección de gestión y servicios generales
Desarrolladores y Mantenedores: NewDevs srl
Administradores del Sistema
Administradores técnicos: área infraestructura de NewDevs srl
Soporte técnico: helpdesk NewDevs srl


# Requisitos funcionales

```
● Registro de usuarios : Registro e inicio de sesión mediante correo electrónico,
número de teléfono o redes sociales.
● El sistema debe permitir agendar turnos online por fecha medico especialidad
● Historial médico : De existir, el médico puede acceder al historial del paciente
● El sistema debe enviar emails , whatsapp y notificaciones en la app como
recordatorio de los turnos.
● (Deseable )El sistema gestionará la lista de espera posible en aquellos casos de
cancelación de turnos , notificando a usuarios en espera sobre la posibilidad de
reservar el turno liberado.
```
## Requisitos no funcionales

```
● La interfaz debe contemplar un uso amigable e intuitiva para personas de la tercera
edad
● Los datos vinculados los pacientes deben estar cifrados y cumplir con normativas de
privacidad
● Sincronización: Actualización en tiempo real entre las agendas de todos los
dispositivos
```
## Historias de uso:

Solicitud de turnos
* Como paciente:
* seleccionar el servicio, el profesional y el horario disponible en un calendario
* para pactar una cita
Visualización de turnos- consulta y modificación:
* como paciente
* quiero ver un menú donde visulizar los datos completos de mis turnos solicitados y
generar cambios (cancelaciones) si fuese necesario
* para usar como recordatorio o realizar cambios


Notificaciones
* como paciente
*quiero recibir notificaciones/avisos
* para no olvidar un turno y poder recordar los detalles específicos (horario, lugar, médico,
posibles estudios médicos solicitados )
Módulo Profesionales / Prestadores. Configuración de disponibilidad
*Como profesional,
*quiero definir mis días de atención, horarios laborales, duración estimada por consulta y
excepciones (días libres o feriados),
*para gestionar mi tiempo de manera autónoma y que el sistema ofrezca turnos únicamente
en mis horas disponible
Gestión de la agenda diaria
*Como recepcionista,
*quiero visualizar la grilla de turnos de todos los profesionales en tiempo real
*para organizar y controlar el flujo de atención de manera eficiente.

# Casos de uso:

### CU-

**Iniciar sesion**
DATOS GENERALES
Identificador CU-RR-001 Fecha: ____ / ____ / ________
1 El Usuario ingresa a la URL o abre la aplicación del sistema de turnos.
2 El Sistema despliega el formulario de inicio de sesión solicitando las credenciales (Correo
electrónico / Matrícula profesional y Contraseña).
3 El Usuario introduce sus credenciales válidas y hace clic en el botón "Ingresar".


4 El Sistema verifica que la cuenta esté activa y consulta el rol asignado al usuario.
5 El Sistema genera un token de sesión seguro y redirige al usuario a su panel de control
correspondiente:
● Paciente: Redirige a la sección "Mis Turnos / Reservar Cita".
● Médico: Redirige a la sección "Agenda del Día / Historial de Pacientes".
● Recepcionista: Redirige a la sección "Panel de Recepción / Gestión de Salas de
Espera".
CU-
**Reservar turno**
DATOS GENERALES
Identificador CU-RR-002 Fecha: ____ / ____ / ________
1 El Paciente selecciona la opción "Reservar Turno" en su panel de control.
2 El Sistema solicita los criterios de búsqueda. El paciente puede filtrar por:
● Especialidad médica (ej. Cardiología, Pediatría).
● Nombre del Profesional.
● Sede / Sucursal.
● Modalidad (Presencial o Telemedicina).
3 El Paciente selecciona los filtros deseados y presiona "Buscar".
4 El Sistema muestra un calendario dinámico con los días y horarios disponibles que
coinciden con la búsqueda.
5 El Paciente selecciona una fecha y una hora específica.
6 El Sistema muestra el resumen del turno (Fecha, Hora, Médico, Sede) y solicita confirmar
la cobertura médica registrada del paciente.
7 El Paciente confirma los datos y hace clic en "Confirmar Reserva".
8 El Sistema bloquea el horario seleccionado en la agenda del médico, registra el turno en
estado "Confirmado" y genera un código único de reserva.
9 El Sistema muestra una pantalla de éxito y envía un comprobante automático al paciente
por correo electrónico y/o WhatsApp.


## Modelo Entidad-Relación

Entidad - ( Atributos)
Paciente (Nro_cliente, cuit, nombre completo, teléfono, email , dni)
Medico (ID de profesional,nombre completo, teléfono, email , dni, especialidad, sede de
atención )
Turnos (nro_cliente, id profesional, fecha hora, id_turno, estado del turno )

## Referencias y fuentes

Stakeholders: https://www.nngroup.com/articles/know-your-users
https://www.interaction-design.org/literature/topics/user-research
Casos de uso , historias de uso:
"User Stories Applied: For Agile Software Development" – Mike Cohn
