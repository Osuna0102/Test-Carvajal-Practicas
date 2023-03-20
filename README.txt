Test para practicas en carvajal. 
app simple que haga uso de API REST con metodos consumibles.

Extraer API REST.rar y Library-app.rar
Crear una carpeta donde dejar ambas carpetas. 
Abrir API REST y copiar y pegar los contenidos hacia la carpeta creada
La carpeta Library-app se deja en la carpeta creada.

Usar Visual Studio Code para abrir la carpeta creada.
Buscar en las extensiones de Visual Studio Code por "REST Client" e instalarla.

Al abrir la carpeta, acceder a la terminal y usar los siguientes comandos:
1) npm install express
2) npm install nodemon --save-dev
3) npm install mysql express-myconnection
4) node server.js

En mySQL WorkBench se usó: 

    host: 'localhost',
    port: 3307,
    user: 'root',
    password: '1234',
    database: 'library'

CREATE TABLE `libreta`.`libretas` (
  `id` INT NOT NULL AUTO_INCREMENT,
  `Nombre` VARCHAR(45) NOT NULL,
  `Apellido` VARCHAR(45) NOT NULL,
  `Correo` VARCHAR(45) NOT NULL,
  `Telefono` INT NOT NULL,
  `Direccion` VARCHAR(45) NOT NULL,
  `Cc` INT NULL,
  PRIMARY KEY (`id`));

CREATE TABLE `library`.`administrador` (
  `id_administrador` INT NOT NULL AUTO_INCREMENT,
  `usuario_administrador` VARCHAR(45) NULL,
  `contrasena_administrador` VARCHAR(45) NULL,
  PRIMARY KEY (`id_administrador`));


Abrir otra ventana en VS CODE y abrir la carpeta Library-app
En Library-app usar:

1) npm install
Para instalar los modulos de node
2) npm start 
Si no te redirige despues de usar npm start, asegurarse de que el proyecto de VS Code se abrió desde la carpeta library-app
Esto nos redirige a la puerta donde inicio la app. Hay un formulario y una lista de los datos que existen.
Si no hay datos en la lista, revisar la integridad de la base de datos y asegurar que se uso node server.js en el API REST

Usar el Formulario de Clientes arriba de el boton crear para usar el metodo CREAR
La lista de Clientes que hay abajo es un READ de la base de datos
Usa el boton Actualizar para UPDATE el dato junto al boton. El contenido que quieres actualizar se hace desde el formulario, pero en vez de dar crear, le das a actualizar
Usa el boton Eliminar para DELETE el dato junto al boton. 
