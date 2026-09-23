
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

7. factura:(numFactura, fecha, tipoPago, montoTotal)

| Atributo   | S/C | Mono/Poli | ID/Desc | Oblig | Card | Tipo(SQL) | Dominio    |
| ---------- | --- | --------- | ------- | ----- | ---- | --------- | ---------- |
| numFactura | C   | M         | ID EXT  | SI    |      | VARCHAR   |            |
| fecha      | S   | M         | D       | SI    |      | Date      |            |
| tipoPago   | S   | M         | D       | SI    |      | VARCHAR   | t_tipoPago |
| montoTotal | S   | M         | D       | SI    |      | DOUBLE    |            |
t_tipoPago: {efectivo, transferencia, tarjeta de crédito o cuenta corriente}



8. Lineas:  numero, producto, cantidadVendida, precioUnitario, subtotal

| Atributo        | S/C | Mono/Poli | ID/Desc | Oblig | Card | Tipo(SQL) | Dominio |
| --------------- | --- | --------- | ------- | ----- | ---- | --------- | ------- |
| numero          | S   | M         | ID ext  | SI    |      | VARCHAR   |         |
| cantidadVendida | S   | M         | DESC    | SI    |      | INT       |         |
| precioUnitario  | S   | M         | DESC    | SI    |      | DOUBLE    |         |
| subtotal        | S   | M         | DESC    | SI    |      | DOUBLE    |         |


9. Proveedores: codigoID, nombre, CUIT, email, telefono

| Atributo | S/C | Mono/Poli | ID/Desc | Oblig | Card | Tipo(SQL) | Dominio |
| -------- | --- | --------- | ------- | ----- | ---- | --------- | ------- |
| codigoID | S   | M         | ID      | SI    |      | VARCHAR   |         |
| nombre   | S   | M         | DESC    | SI    |      | VARCHAR   |         |
| CUIT     | S   | M         | DESC    | SI    |      | VARCHAR   |         |
| email    | S   | M         | ID      | SI    |      | VARCHAR   |         |
| telefono | S   | M         | DESC    | SI    |      | VARCHAR   |         |


10. Compras: fecha, cantidad, precioCosto

| Atributo    | S/C | Mono/Poli | ID/Desc | Oblig | Card | Tipo(SQL) | Dominio |
| ----------- | --- | --------- | ------- | ----- | ---- | --------- | ------- |
| fecha       | S   | M         | DESC    | SI    |      | DATE      |         |
| cantidad    | S   | M         | DESC    | SI    |      | INT       |         |
| precioCosto | S   | M         | DESC    | SI    |      | DOUBLE    |         |

11. Promociones: fecha, descuento

| Atributo  | S/C | Mono/Poli | ID/Desc | Oblig | Card | Tipo(SQL) | Dominio |
| --------- | --- | --------- | ------- | ----- | ---- | --------- | ------- |
| fecha     | S   | M         | DESC    | SI    |      | DATE      |         |
| descuento | S   | M         | DESC    | SI    |      | VARCHAR   |         |
