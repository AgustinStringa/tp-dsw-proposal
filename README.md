# Propuesta TP DSW

## Grupo
### Integrantes
* 51338 - Stringa, Agustín Nicolás
* 50376	- Danteo, Elías Tomás
* 51445 - De Bernardo, Aarón
* 51424 - Gramaglia, Francisca 

### Repositorios
* [frontend_app](https://github.com/AgustinStringa/tp-dsw-frontendapp)
* [backend_app](https://github.com/AgustinStringa/tp-dsw-backendapp)

## Tema
### Descripción
Nuestro sitio web web ofrece diferentes herramientas destinadas a la gestión del Gimnasio Iron Haven.<br>
El sitio cuenta con información para visitantes (potenciales clientes) y posee 2 niveles de acceso: uno para entrenadores y otro para clientes.<br>
Los entrenadores cumplen el rol de administradores del sistema. Pueden gestionar y administrar usuarios, clases, membresías y crear rutinas para los clientes. Tienen acceso a estadísticas valiosas para la empresa, como lo son los ingresos del último mes, cantidad de membresías activas, clases que se brindan, entre otras.<br>
Por su parte, los clientes pueden comprar membresías para asistir al gimnasio a través de la autogestión (mediante la plataforma de pagos Stripe), inscribirse a clases y registrar la ejecución de los ejercicios asignados. Disponen de secciones exclusivas para establecer metas y registrar progresos (medidas corporales, peso, porcenaje de grasa).<br>
Los usuarios de cualquier tipo, pueden comunicarse a través de un chat. Además, el sistema notifica mediante correos electrónicos la proximidad del vencimiento de una membresía, la disponibilidad de una nueva clase y el registro correcto de un usuario en la plataforma. Por otra parte, se ejecutan tareas diarias automáticamente, que se encargan de enviar notificaciones al cliente y liberar cupos en las diferentes clases (ocupados por clienes que dejaron de asistir al gimnasio).<br>


### Modelo
[enlace al modelo](https://github.com/AgustinStringa/tp-dsw-proposal/blob/main/modelo-dominio-gimnasio.drawio.pdf)


## Alcance Funcional 

### Alcance Mínimo 

Regularidad:
|Req|Detalle|
|:-|:-|
|CRUD simple|1. CRUD Trainer<br>2. CRUD ClassType<br>3. CRUD Exercise<br>4. CRUD Client<br>5. CRUD MembershipType|
|CRUD dependiente|1. CRUD Class {depende de ClassType}<br>2. CRUD  Registration {depende de Class y Client}<br>3. CRUD Membership {depende de Client y MembershipType}<br>4. CRUD Routine {depende de Client, Trainer y Exercise}|
|Listado<br>+<br>detalle| 1. Listado de clientes filtrado por nombre a buscar, muestra nombre, apellido y correo electrónico de los clientes que coinciden con el texto ingresado => detalle CRUD Cliente<br> 2. Listado de clases filtrado por día, entrenador y tipo de clase => detalle CRUD Clases|
|CUU/Epic|1. Asignar Rutina<br>2. Registrar ejecución de ejercicio (Cliente)|


Adicionales para Aprobación
|Req|Detalle|
|:-|:-|
|CRUD |1. CRUD Goal<br>2. CRUD Progress<br>3. CRUD Payment<br>4. CRUD Message|
|CUU/Epic|1. Inscribirse a una Clase<br>2. Obtener listado de clientes con membresías pendientes de pago |


### Alcance Adicional Voluntario

|Req|Detalle|
|:-|:-|
|Listados |1.  Listado de precios actuales de las membresías, filtrado por fecha de última actualización => detalle muestra precio de la membresía y cantidad de clientes anotados <br>2. Listado de ejercicios por cliente => detalle de tipo de ejercicios, cantidad de series, repeticiones que se deben realizar junto con su video descriptivo |
|CUU/Epic|1. Realizar la compra de una membresía de manera online (para el cliente mediante Stripe)<br>2. Aviso de finalización de membresía por correo electrónico, mediante una tarea automarizada |
|Otros|1. Notificación de registro al sistema por mail<br>2. Utilización de WebSocket para el live-chat|
