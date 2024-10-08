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
El sitio web ofrecerá la gestión de un gimnasio no sólo de sus clientes, sino también de sus entrenadores. Además, incluirá creación de rutinas con videos demostrativos, sistema de pagos con alertas y herramientas de comunicación interna (mensajería).


### Modelo
[imagen del modelo](https://github.com/AgustinStringa/tp-dsw-proposal/blob/main/modelo_dominio.drawio.pdf)


## Alcance Funcional 

### Alcance Mínimo 

Regularidad:
|Req|Detalle|
|:-|:-|
|CRUD simple|1. CRUD Entrenador<br>2. CRUD Tipo de clase<br>3. CRUD Tipo de membresía<br>4. CRUD Cliente |
|CRUD dependiente|1. CRUD Ejercicio {depende de} CRUD Entrenador <br>2. CRUD  Progreso {depende de} CRUD Cliente|
|Listado<br>+<br>detalle| 1. Listado de cliente filtrado por nombre a buscar, muestra nombre, apellido y correo electrónico de los clientes que coinciden con el texto ingresado => detalle CRUD Cliente<br> 2. Listado de precios actuales de las membresías, filtrado por fecha de última actualización => detalle muestra precio de la membresía y cantidad de clientes anotados|
|CUU/Epic|1. Asignar Rutina<br>2. Registrar ejecución de ejercicio (Cliente)|


Adicionales para Aprobación
|Req|Detalle|
|:-|:-|
|CRUD |1. CRUD Meta<br>2. CRUD Progreso<br>3. CRUD Noticias<br>4. CRUD Pago<br>5. CRUD Ejercicio hecho de rutina<br>6.CRUD precio de tipo de rutina (en observacion)|
|CUU/Epic|1. Asignar Clase<br>2. Obtener listado de cuotas pendientes de pago |


### Alcance Adicional Voluntario

|Req|Detalle|
|:-|:-|
|Listados |1. Listado de clases filtrado por día => detalle de cantidad de usuarios inscriptos y profesor/es que la dan <br>2. Listado de ejercicios por cliente => detalle de tipo de ejercicios, cantidad de series, repeticiones que se deben realizar junto con su video descriptivo |
|CUU/Epic|1. Registrar nuevas medidas corporales<br>2. |
|Otros|1. Aviso de finalización de membresía por mail e inbox de la web|
