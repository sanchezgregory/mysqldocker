# Docker para Mysql 

##### Clona el repositorio: `git clone git@github.com:sanchezgregory/mysqldocker.git  mysqlDB `
##### Clona el repositorio de las apps: `git clone git@github.com:sanchezgregory/dockerphpnginx.git app`
### Los entornos locales se comunicarán a este contenedor, y todas las BD estarán  centralizadas aquí. 

#### Dentro del directorio: `cd mysqlDB && docker-compose up --build`

#### Debes crear la red del docker: `docker network create my-network`

##### *Solo si es la primera vez que levanta este entorno o si el usuario root deja de tener acceso de superusuario al servidor de Mysql **solo se ejecuta la primera vez que se construye el docker, esto creará un usuario name=store password=store  con privilegios de root**

#### ` docker exec -it mysqldb bash  /etc/user.sh `

### **Solo debe aparacer la siguiente línea si todo está OK**
##### *mysql: [Warning] Using a password on the command line interface can be insecure*

#### Luego, debe entrar con su cliente de mysql favorito e ingresar con las credenciales

##### **Host** = 127.0.0.1 **Puerto** = 3000  **User** = root  **Password** = root

===================================================================================

#### Tip: para hacer una copia de mysql de tu entorno local actual, y llevarlo al nuevo.

##### `mysql --user=root --password=root` 
###### Una vez dentro de mysql, ejecutar `show databes;`
###### Fijarse del nombre que tiene la BD a la cual se le realizará el dump
###### salir de mysql con `exit`
###### ejecutar ahora: `mysqldump --user=root --password=root bdToBackup > /var/lib/mysql/bdToRestore.sql`
###### Dirigirse a la carpeta de su antiguo proyecto y entrar en data/db/mysql/ ahí verás el dump creado "bdToRestore.sql"