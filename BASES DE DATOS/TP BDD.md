[]()![[Bases-de-Datos-Casos-de-Estudio-de-Modelado-de-Datos.pdf]]

## RESERVA ECOLOGICA

Empleados: legajo, nombre, apellido, tipo_documento, num_documento, CUIL, telefono, direccion(calle, numero, piso y depto), email, fecha_nacimiento, fecha_inicio, fecha_baja, 


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
  Dominio: 
  D_tipo_documento = {DNI, PASAPORTE, LIBRETA CÍVICA, LIBRETA DE ENROLAMIENTO}