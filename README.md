# Ejecuta docker-compose como siempre

# step 1

docker-compose up --build


# step 2 (solo se ejecuta la primera vez que se construye el docker, esto creará un usuario name=store password=store  con privilegios de root)

## Una vez el docker esté Up, ejecutar: 

docker exec -it mysqldb bash  /etc/user.sh

## Solo debe aparacer la siguiente línea si todo está OK
# "mysql: [Warning] Using a password on the command line interface can be insecure."

## Luego, debe entrar con su cliente de mysql favorito e ingresar con las credenciales

# Host = 127.0.0.1
# Puerto = 3000
# User = root
# Password = root