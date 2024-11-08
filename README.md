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
El sitio web ofrecerá las distintas herramientas destinadas a la gestión del Gimnasio Iron Haven.<br>
Se podrá tener un registro de todos los clientes, con sus membresías contratadas y pagos de las mismas. Los clientes podrán definir metas que los motiven a mejorar su estado físico. También tendrán a su disposición el registro de sus medidas corporales.<br>
El gimnasio dicta diferentes clases, por lo que es de interés que los clientes puedan inscribirse a las mismas.<br>
Por otra parte, los entrenadores contarán con la posibilidad de crear rutinas para los clientes, asignando ejercicios que tendrán videos explicativos.<br>
Sería interesante que los entrenadores (administradores del sitio) puedan redactar noticias que sean visibles para todos los visitantes del sitio web del gimnasio. Por último, un sistema de chat añadiría mucho valor a los procesos de negocio.


### Modelo
[imagen del modelo](https://github.com/AgustinStringa/tp-dsw-proposal/blob/main/modelo_dominio.drawio.pdf)


## Alcance Funcional 

### Alcance Mínimo 

Regularidad:
|Req|Detalle|
|:-|:-|
|CRUD simple|1. CRUD Trainer<br>2. CRUD ClassType<br>3. CRUD Exercise<br>4. CRUD Client<br>5. CRUD MembershipType|
|CRUD dependiente|1. CRUD Class {depende de ClassType}<br>2. CRUD  Registration {depende de Class y Client}<br>3. CRUD Membership {depende de Client y MembershipType}<br>4. CRUD Routine {depende de Client, Trainer y Exercise}|
|Listado<br>+<br>detalle| 1. Listado de cliente filtrado por nombre a buscar, muestra nombre, apellido y correo electrónico de los clientes que coinciden con el texto ingresado => detalle CRUD Cliente<br> 2. Listado de clases filtrado por día, entrenador y tipo de clase => detalle CRUD Clases|
|CUU/Epic|1. Asignar Rutina<br>2. Registrar ejecución de ejercicio (Cliente)|


Adicionales para Aprobación
|Req|Detalle|
|:-|:-|
|CRUD |1. CRUD Goal<br>2. CRUD Progress<br>3. CRUD News<br>4. CRUD Payment<br>5. CRUD Message|
|CUU/Epic|1. Inscribirse a una Clase<br>2. Obtener listado de clientes con membresías pendientes de pago |


### Alcance Adicional Voluntario

|Req|Detalle|
|:-|:-|
|Listados |1.  Listado de precios actuales de las membresías, filtrado por fecha de última actualización => detalle muestra precio de la membresía y cantidad de clientes anotados <br>2. Listado de ejercicios por cliente => detalle de tipo de ejercicios, cantidad de series, repeticiones que se deben realizar junto con su video descriptivo |
|CUU/Epic|1. Registrar nuevas medidas corporales<br>2. |
|Otros|1. Aviso de finalización de membresía por mail e inbox de la web<br>2. Notificación de registro al sistema por mail|
