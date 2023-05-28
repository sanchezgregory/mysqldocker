Add this line to the service app in other docker, so you can connect to this mysql docker

    ...
    
    service-name:
        ...
        networks:
            - mysql-network
            - others networks...

networks:
    mysql-network:
        external: true


in the .env file of each project, host can be: mysql57 or mysql80, depending on the mysql version you want.
the ports are 33067 (mysql 5.7) and 33068 (mysql 8.0.31), username and password are the same for both: admin password