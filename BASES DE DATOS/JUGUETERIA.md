
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

| Atributo        | S/C | Mono/Poli | ID/Desc | Oblig | Card | Tipo(SQL) | Dominio |
| --------------- | --- | --------- | ------- | ----- | ---- | --------- | ------- |