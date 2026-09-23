
1. Sucursales: codigo(SUC, codigoPostal, numSucursal), fechaDeCreacion, direccion(calle, numero), email, usuarioIG, telefonosFijo, telCel

| Atributo        | S/C | Mono/Poli | ID/Desc | Oblig | Card | Tipo(SQL) | Dominio |
| --------------- | --- | --------- | ------- | ----- | ---- | --------- | ------- |
| codigo          | C   | M         | ID      | SI    |      |           |         |
| -SUC            | S   | M         | DESC    | SI    |      | VARCHAR   |         |
| -codigoPostal   | S   | M         | DESC    | SI    |      | VARCHAR   |         |
| -numSucursal    | S   | M         | DESC    | SI    |      | INT       |         |
| fechaDeCreacion | S   | M         | DESC    | SI    |      | DATE      |         |
| direccion       | C   | M         | DESC    | SI    |      |           |         |
| -calle          | S   | M         | DESC    | SI    |      | VARCHAR   |         |
| -numero         | S   | M         | DESC    | SI    |      | INT       |         |
| email           | S   | M         | ID      | SI    |      | VARCHAR   |         |
| usuarioIG       | S   | M         | ID      | SI    |      | VARCHAR   |         |
| telefonosFijo   | S   | P         | DESC    | SI    | 1..N | VARCHAR   |         |
| telCel          | S   | M         | DESC    | SI    |      | VARCHAR   |         |


2. Ciudades: nombre, codigoPostal

| Atributo     | S/C | Mono/Poli | ID/Desc | Oblig | Card | Tipo(SQL) | Dominio |
| ------------ | --- | --------- | ------- | ----- | ---- | --------- | ------- |
| nombre       | S   | M         | Desc    | SI    |      | VARCHAR   |         |
| codigoPostal | S   | M         | ID      | SI    |      | VARCHAR   |         |


3. Provincias: codigo, nombre

| Atributo | S/C | Mono/Poli | ID/Desc | Oblig | Card | Tipo(SQL) | Dominio |
| -------- | --- | --------- | ------- | ----- | ---- | --------- | ------- |
| codigo   | S   | M         | ID      | SI    |      | VARCHAR   |         |
| nombre   | S   | M         | ID      | SI    |      | VARCHAR   |         |


4. Productos: codigoBarra, descripcion, precioUni

| Atributo    | S/C | Mono/Poli | ID/Desc | Oblig | Card | Tipo(SQL) | Dominio |
| ----------- | --- | --------- | ------- | ----- | ---- | --------- | ------- |
| codigoBarra | S   | M         | ID      | SI    |      | VARCHAR   |         |
| descripcion | S   | M         | D       | SI    |      | VARCHAR   |         |
| precioUni   | S   | M         | D       | SI    |      | DOUBLE    |         |

5. Empleados: legajo, CUIL, tipoDocumento, numDoc, nombre, apellido, direccion(calle, numero, depto, piso), email(unico), fechaInicio, fechaNacimiento, celular, codigoID, fechaFin

| Atributo        | S/C | Mono/Poli | ID/Desc | Oblig | Card | Tipo(SQL) | Dominio          |
| --------------- | --- | --------- | ------- | ----- | ---- | --------- | ---------------- |
| legajo          | S   | M         | ID      | SI    |      | VARCHAR   |                  |
| CUIL            | S   | M         | ID      | SI    |      | VARCHAR   |                  |
| tipoDocumento   | S   | M         | D       | SI    |      | VARCHAR   | D_tipo_documento |
| numDoc          | S   | M         | D       | SI    |      | VARCHAR   |                  |
| nombre          | S   | M         | D       | SI    |      | VARCHAR   |                  |
| apellido        | S   | M         | D       | SI    |      | VARCHAR   |                  |
| direccion       | C   | M         | D       | SI    |      |           |                  |
| -calle          | S   | M         | D       | SI    |      | VARCHAR   |                  |
| -numero         | S   | M         | D       | SI    |      | VARCHAR   |                  |
| -depto          | S   | M         | D       | SI    |      | VARCHAR   |                  |
| -piso           | S   | M         | D       | SI    |      | VARCHAR   |                  |
| email           | S   | M         | ID      | SI    |      | VARCHAR   |                  |
| fechaInicio     | S   | M         | D       | SI    |      | Date      |                  |
| fechaNacimiento | S   | M         | D       | Si    |      | Date      |                  |
| celular         | S   | M         | D       | SI    |      | VARCHAR   |                  |
| codigoID        | S   | M         | ID      | SI    |      | VARCHAR   |                  |
| fechaFin        | S   | M         | D       | no    | 0..1 | Date      |                  |
D_tipo_documento: {DNI, PASAPORTE, LIBRETA CÍVICA, LIBRETA DE ENROLAMIENTO}

6. Cliente: tipoDoc, numDoc, nombre, apellido, fechaInicio, direccion(calle, numero, depto, piso), email, fechaCumple, celular, codigoID

| Atributo      | S/C | Mono/Poli | ID/Desc | Oblig | Card | Tipo(SQL) | Dominio          |
| ------------- | --- | --------- | ------- | ----- | ---- | --------- | ---------------- |
| tipoDocumento | S   | M         | D       | SI    |      | VARCHAR   | D_tipo_documento |
| numDoc        | S   | M         | D       | SI    |      | VARCHAR   |                  |
| nombre        | S   | M         | D       | SI    |      | VARCHAR   |                  |
| apellido      | S   | M         | D       | SI    |      | VARCHAR   |                  |
| fechaInicio   | S   | M         | D       | SI    |      | Date      |                  |
| direccion     | C   | M         | D       | SI    |      |           |                  |
| -calle        | S   | M         | D       | SI    |      | VARCHAR   |                  |
| -numero       | S   | M         | D       | SI    |      | VARCHAR   |                  |
| -depto        | S   | M         | D       | SI    |      | VARCHAR   |                  |
| -piso         | S   | M         | D       | SI    |      | VARCHAR   |                  |
| email         | S   | M         | ID      | SI    |      | VARCHAR   |                  |
| fechaCumple   | S   | M         | D       | Si    |      | Date      |                  |
| celular       | S   | M         | D       | SI    |      | VARCHAR   |                  |
| codigoID      | S   | M         | ID      | SI    |      | VARCHAR   |                  |
D_tipo_documento: {DNI, PASAPORTE, LIBRETA CÍVICA, LIBRETA DE ENROLAMIENTO}