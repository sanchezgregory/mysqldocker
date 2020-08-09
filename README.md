# Docker para Mysql 

## Clona el repositorio: ` git clone https://  mysqlDB `

### Los entornos locales se comunicarán a este contenedor, y todas las BD estarán  centralizadas aquí. 

#### Dentro del directorio: `cd mysqlDB && docker-compose up --build`

#### *Solo si es la primera vez que levanta este entorno o si el usuario root deja de tener acceso de superusuario al servidor de Mysql **solo se ejecuta la primera vez que se construye el docker, esto creará un usuario name=store password=store  con privilegios de root**

#### ` docker exec -it mysqldb bash  /etc/user.sh `

### **Solo debe aparacer la siguiente línea si todo está OK**
#### *mysql: [Warning] Using a password on the command line interface can be insecure*

#### Luego, debe entrar con su cliente de mysql favorito e ingresar con las credenciales

### **Host** = 127.0.0.1 **Puerto** = 3000  **User** = root  **Password** = root