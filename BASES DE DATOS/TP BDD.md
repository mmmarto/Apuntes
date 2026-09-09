[]()![[Bases-de-Datos-Casos-de-Estudio-de-Modelado-de-Datos.pdf]]

## RESERVA ECOLOGICA

1-Empleados: legajo, nombre, apellido, tipo_documento, num_documento, CUIL, telefono, direccion(calle, numero, piso y depto), email, fecha_nacimiento, fecha_inicio, fecha_baja, 


| Atributo         | S/C | Mono/Poli | ID/Desc    | Oblig | Card | Tipo(SQL) | Dominio          |
| ---------------- | --- | --------- | ---------- | ----- | ---- | --------- | ---------------- |
| Legajo           | S   | mono      | ID         | Si    | 1..1 | VARCHAR   |                  |
| nombre           | S   | mono      | descriptor | Si    | 1..1 | VARCHAR   |                  |
| apellido         | S   | mono      | descriptor | Si    | 1..1 | VARCHAR   |                  |
| tipo_documento   | S   | mono      | descriptor | Si    | 1..1 | VARCHAR   | D_tipo_documento |
| num_documento    | S   | mono      | descriptor | Si    | 1..1 | VARCHAR   |                  |
| CUIL             | S   | mono      | descriptor | Si    | 1..1 | VARCHAR   |                  |
| telefono         | S   | Poli      | descriptor | Si    | 1..n | INT       |                  |
| direccion        | C   | mono      | descriptor | Si    | 1..1 | -         |                  |
| -calle           | S   | mono      | descriptor | Si    | 1..1 | VARCHAR   |                  |
| -numero          | S   | mono      | descriptor | Si    | 1..1 | INT       |                  |
| -piso            | S   | mono      | descriptor | No    | 0..1 | INT       |                  |
| depto            | S   | mono      | descriptor | No    | 0..1 | INT       |                  |
| email            | S   | mono      | ID         | Si    | 1..1 | VARCHAR   |                  |
| fecha_nacimiento | S   | mono      | descriptor | Si    | 1..1 | DATE      |                  |
| fecha_inicio     | S   | mono      | descriptor | Si    | 1..1 | DATE      |                  |
| fecha_baja       | S   | mono      | descriptor | No    | 0..1 | DATE      |                  |
|                  |     |           |            |       |      |           |                  |
 
  
  Dominio: 
  D_tipo_documento = {DNI, PASAPORTE, LIBRETA CÍVICA, LIBRETA DE ENROLAMIENTO}


2-Ciudad:  nombre, codigo_postal

| Atributo      | S/C | Mono/Poli | ID/Desc    | Oblig | Card | Tipo(SQL) | Dominio |
| ------------- | --- | --------- | ---------- | ----- | ---- | --------- | ------- |
| nombre        | S   | mono      | descriptor | Si    | 1..1 | VARCHAR   |         |
| codigo_postal | S   | mono      | ID         | Si    | 1..1 | VARCHAR   |         |

3.Veterinario: matricula, , años

| Atributo  | S/C | Mono/Poli | ID/Desc    | Oblig | Card | Tipo(SQL) | Dominio |
| --------- | --- | --------- | ---------- | ----- | ---- | --------- | ------- |
| matricula | S   | MONO      | ID         | SI    | 1..1 | VARCHAR   |         |
| años      | S   | MONO      | DESCRIPTOR | SI    | 1..1 | INT       |         |

4-Especialidades: nombre, codigo

| Atributo | S/C | Mono/Poli | ID/Desc | Oblig | Card | Tipo(SQL) | Dominio |
| -------- | --- | --------- | ------- | ----- | ---- | --------- | ------- |
| nombre   | S   | MONO      | ID(alt) | SI    | 1..1 | VARCHAR   |         |
| codigo   | S   | MONO      | ID      | SI    | 1..1 | VARCHAR   |         |
ESPECIALIDAD
codigo | nombre
-------|------------
E01    | Cardiología
E02    | Oftalmología
E03    | Oncología
E04    | Ortopedia
E05    | Reproducción

5- Cuidadores: num_licencia, fecha_registro

| Atributo       | S/C | Mono/Poli | ID/Desc    | Oblig | Card | Tipo(SQL) | Dominio |
| -------------- | --- | --------- | ---------- | ----- | ---- | --------- | ------- |
| num_licencia   | S   | MONO      | ID         | SI    | 1..1 | VARCHAR   |         |
| fecha_registro | S   | MONO      | DESCRIPTOR | SI    | 1..1 | DATE      |         |

6- GUIAS

| Atributo       | S/C | Mono/Poli | ID/Desc    | Oblig | Card | Tipo(SQL) | Dominio |
| -------------- | --- | --------- | ---------- | ----- | ---- | --------- | ------- |
| num_licencia   | S   | MONO      | ID         | SI    | 1..1 | VARCHAR   |         |
| fecha_registro | S   | MONO      | DESCRIPTOR | SI    | 1..1 | DATE      |         |

7- IDIOMAS: codigo_ISO, nombre

| Atributo   | S/C | Mono/Poli | ID/Desc    | Oblig | Card | Tipo(SQL) | Dominio |
| ---------- | --- | --------- | ---------- | ----- | ---- | --------- | ------- |
| codigo_ISO | S   | MONO      | ID         | SI    | 1..1 | VARCHAR   |         |
| nombre     | S   | MONO      | DESCRIPTOR | SI    | 1..1 | VARCHAR   |         |

REQUISITO 8 NO VA EN ESTA PARTE

9- ESPECIES ANIMALES: codigo, descripcion, caracteristicas, cantidad_animales, nombre_vulgar, nombre_cientifico, peligro_de_extincion, grupo


| Atributo             | S/C | Mono/Poli | ID/Desc    | Oblig | Card | Tipo(SQL) | Dominio                |
| -------------------- | --- | --------- | ---------- | ----- | ---- | --------- | ---------------------- |
| codigo               | S   | MONO      | ID         | SI    | 1..1 | VARCHAR   |                        |
| descripcion          | S   | MONO      | DESCRIPTOR | SI    | 1..1 | VARCHAR   |                        |
| caracteristicas      | S   | MONO      | DESCRIPTOR | SI    | 1..1 | VARCHAR   |                        |
| cantidad_animales    | S   | MONO      | DESCRIPTOR | SI    | 1..1 | INT       |                        |
| nombre_vulgar        | S   | MONO      | DESCRIPTOR | SI    | 1..1 | VARCHAR   |                        |
| nombre_cientifico    | S   | MONO      | DESCRIPTOR | SI    | 1..1 | VARCHAR   |                        |
| peligro_de_extincion | S   | MONO      | DESCRIPTOR | SI    | 1..1 | VARCHAR   | D_peligro_de_extincion |
| grupo                | S   | MONO      | DESCRIPTOR | SI    | 1..1 | VARCHAR   | D_grupo                |

D_peligro_de_extincion = {Rojo, Amarillo, Verde}
D_grupo = {Mamíferos, Aves, Reptiles, Peces, Insectos, Arañas o Alacranes.}


10- ANIMALES: codigo, peso color, sexo


| Atributo | S/C | Mono/Poli | ID/Desc    | Oblig | Card | Tipo(SQL) | Dominio |
| -------- | --- | --------- | ---------- | ----- | ---- | --------- | ------- |
| codigo   | S   | MONO      | ID         | SI    | 1..1 | VARCHAR   |         |
| peso     | S   | MONO      | DESCRIPTOR | SI    | 1..1 | INT       |         |
| color    | S   | MONO      | DESCRIPTOR | SI    | 1..1 | VARCHAR   |         |
| sexo     | S   | MONO      | DESCRIPTOR | SI    | 1..1 | VARCHAR   | D_sexo  |

D_sexo = {masculino, femenino, hermafroditismo, determinado ambientalmente, sexualidad diversa}

	REQUISITO 14 PARTE B


11- PARQUES: nombre, codigo, coordenada_geografica(latitud, longitud)

| Atributo              | S/C | Mono/Poli | ID/Desc    | Oblig | Card | Tipo(SQL) | Dominio |
| --------------------- | --- | --------- | ---------- | ----- | ---- | --------- | ------- |
| nombre                | S   | MONO      | ID(alt)    | SI    | 1..1 | VARCHAR   |         |
| codigo                | S   | MONO      | ID         | SI    | 1..1 | VARCHAR   |         |
| coordenada_geografica | C   | MONO      | DESCRIPTOR | SI    | 1..1 |           |         |
| -longitud             | S   | MONO      | DESCRIPTOR | SI    | 1..1 | FLOAT     |         |
| -latitud              | S   | MONO      | DESCRIPTOR | SI    | 1..1 | FLOAT     |         |


12-HORARIOS: dia, hora_apertura, hora_cierre

| Atributo      | S/C | Mono/Poli | ID/Desc    | Oblig | Card | Tipo(SQL) | Dominio |
| ------------- | --- | --------- | ---------- | ----- | ---- | --------- | ------- |
| dia           | S   | MONO      | ID         | SI    | 1..1 | VARCHAR   | D_dia   |
| hora_apertura | S   | MONO      | DESCRIPTOR | SI    | 1..1 | TIME      |         |
| hora_cierre   | S   | MONO      | DESCRIPTOR | SI    | 1..1 | TIME      |         |

D_dia = {Lunes, Martes, Miercoles, Jueves, Viernes, Sabado, Domingo}

13- HABITATS: codigo, nombre, coordenada(latitud, longitud), tipo, clima, vegetacion, extension

| Atributo   | S/C | Mono/Poli | ID/Desc    | Oblig | Card | Tipo(SQL) | Dominio      |
| ---------- | --- | --------- | ---------- | ----- | ---- | --------- | ------------ |
| codigo     | S   | MONO      | DESCRIPTOR | SI    | 1..1 | VARCHAR   |              |
| nombre     | S   | MONO      | DESCRIPTOR | SI    | 1..1 | VARCHAR   |              |
| coordenada | C   | MONO      | DESCRIPTOR | SI    | 1..1 |           |              |
| -latitud   | S   | MONO      | DESCRIPTOR | SI    | 1..1 | FLOAT     |              |
| -longitud  | S   | MONO      | DESCRIPTOR | SI    | 1..1 | FLOAT     |              |
| tipo       | S   | MONO      | DESCRIPTOR | SI    | 1..1 | VARCHAR   | D_tipo       |
| clima      | S   | MONO      | DESCRIPTOR | SI    | 1..1 | VARCHAR   | D_clima      |
| vegetacion | S   | MONO      | DESCRIPTOR | SI    | 1..1 | VARCHAR   | D_vegetacion |
| extension  | S   | MONO      | DESCRIPTOR | SI    | 1..1 | FLOAT     |              |

D_tipo = {Aviario, Acuario, Delfinario, Terrario}
D_clima = {Tropical, Seco, Templado, Continental, Polar}
D_vegetacion= {Pantano, Lago, Rio, Mar, Tundra, Taiga, Selva, Bosque, Desierto, Sabana}

14- TRATAMIENTO: numero, diagnostico, descripcion(medicamentos, alimentacion), sugerencia, fecha, hora

| Atributo    | S/C | Mono/Poli | ID/Desc    | Oblig | Card | Tipo(SQL) | Dominio |
| ----------- | --- | --------- | ---------- | ----- | ---- | --------- | ------- |
| numero      | S   | MONO      | ID         | SI    | 1..1 | VARCHAR   |         |
| diagnostico | S   | MONO      | DESCRIPTOR | SI    | 1..1 | VARCHAR   |         |
| descripcion | S   | MONO      | DESCRIPTOR | SI    | 1..1 | VARCHAR   |         |
| sugerencia  | S   | MONO      | DESCRIPTOR | NO    | 0..1 | VARCHAR   |         |
| fecha       | S   | MONO      | DESCRIPTOR | SI    | 1..1 | DATE      |         |
| hora        | S   | MONO      | DESCRIPTOR | SI    | 1..1 | TIME      |         |
