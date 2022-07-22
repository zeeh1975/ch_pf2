## **Segunda entrega del Proyecto Final**

*Consigna:* Basándose en los contenedores ya desarrollados (memoria, archivos) desarrollar dos contenedores más (que cumplan con la misma interfaz) que permitan realizar las operaciones básicas de CRUD en MongoDb (ya sea local o remoto) y en Firebase. Luego, para cada contenedor, crear dos clases derivadas, una para trabajar con Productos, y otra para trabajar con Carritos.

*Aspectos a incluir en el entregable:*
a. A las clases derivadas de los contenedores se las conoce como DAOs (Data Access Objects), y pueden ir todas incluidas en una misma carpeta de ‘daos’.
b. En la carpeta de daos, incluir un archivo que importe todas las clases y exporte una instancia de dao de productos y una de dao de carritos, según corresponda. Esta decisión se tomará en base al valor de una variable de entorno cargada al momento de ejecutar el servidor (opcional: investigar el uso de imports dinámicos).
c. Incluir un archivo de configuración (config) que contenga los datos correspondientes para conectarse a las bases de datos o medio de persistencia que corresponda.

*Opcional:*
Hacer lo mismo para bases de datos relacionales: MariaDB/SQLite3.


**Notas:**
- Utilizar **npm install** para descargar las dependencias.
- Usar **node src/server.js** para ejecutar el proyec
- Para probar el punto 3 de 'Aspectos a incluir en el entregable' se puede cambiar el valor de la variable *admin* en el archivo /middleware/auth.js linea 4 y en el archivo public/assets/scripts/app.js línea 18
  Cuando admin es true en la pagina web se muestra un botón "Nuevo producto" y en cada tarjeta de producto aparecen dos botones uno para modificar el producto y otro para borrarlo ambos a la derecha del precio.
  Para probar las restricciones de autenticación del lado del servidor se puede dejar el valor de admin en true en el lado del cliente (app.js) y admin en false del lado del servidor (auth.js) y al intentar agregar, modificar o eliminar un producto mostrara un mensaje de operación no autorizada.
- Versión en vivo en Glitch: https://sustaining-shadow-myrtle.glitch.me/
