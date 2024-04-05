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
[imagen del modelo](https://drive.google.com/file/d/1brjXgvFV6FmMOpHA6S5FL4rNYijHlRnv/view?usp=sharing)


## Alcance Funcional 

### Alcance Mínimo 

Regularidad:
|Req|Detalle|
|:-|:-|
|CRUD simple|1. CRUD Cliente<br>2. CRUD Ejercicio<br>3. CRUD Tipo de membresía<br>4. CRUD Entrenador|
|CRUD dependiente|1. CRUD Precio de tipo de membresía {depende de} CRUD Tipo de membresía<br>2. CRUD  Progreso {depende de} CRUD Cliente|
|Listado<br>+<br>detalle| 1. Listado de cliente filtrado por nombre a buscar, muestra nombre, apellido y correo electrónico de los clientes que coinciden con el texto ingresado => detalle CRUD Cliente<br> 2. Listado de precios actuales de las membresías, filtrando por fecha de última actualización => detalle muestra precio de la membresía y cantidad de clientes anotados|
|CUU/Epic|1. Cambiar el tipo de membresía de un cliente<br>2. Inscribirse a una clase|


Adicionales para Aprobación
|Req|Detalle|
|:-|:-|
|CRUD |1. CRUD Meta<br>2. CRUD Progreso<br>3. CRUD Noticias<br>4. CRUD Precio tipo de membresía<br>5. CRUD Pago<br>6. CRUD Tipo de clase<br>7. CRUD Ejercicio hecho de rutina|
|CUU/Epic|1. Crear una rutina mensual<br>2. Obtener listado de cuotas pendientes<br>3. |


### Alcance Adicional Voluntario

|Req|Detalle|
|:-|:-|
|Listados |1. Listado de clases filtrado por día => detalle de cantidad de usuarios inscriptos y profesor/es que la dan <br>2. |
|CUU/Epic|1. Registrar nuevas medidas corporales<br>2. |
|Otros|1. Aviso de finalización de membresía por mail e inbox de la web|
