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


| Atributo          | S/C | Mono/Poli | ID/Desc    | Oblig | Card | Tipo(SQL) | Dominio |
| ----------------- | --- | --------- | ---------- | ----- | ---- | --------- | ------- |
| codigo            | S   | MONO      | ID         | SI    | 1..1 | VARCHAR   |         |
| descripcion       | S   | MONO      | DESCRIPTOR | SI    | 1..1 | VARCHAR   |         |
| caracteristicas   | S   | MONO      | DESCRIPTOR | SI    | 1..1 | VARCHAR   |         |
| cantidad_animales | S   | MONO      | DESCRIPTOR | SI    | 1..1 | VARCHAR   |         |
| nombre_vulgar     | S   | MONO      | DESCRIPTOR | SI    | 1..1 | VARCHAR   |         |
|                   |     |           |            |       |      |           |         |




