# SXE-PIERO-2-DAM
Utilizaremos la imagen de Alpine. Sigue las instrucciones:

## Descarga la imagen "alpine" SIN ARRANCARLA y comprueba que está en tu equipo

- Primero lo que tenemos que hacer es que debemos abrir la aplicación de docker de manera manual y posteriormente abrir la termina.
- Posteriormente, para descargar la imagen "alpine" sin arrancarla debemos hacerla a través un "pull" de manera que quedaría así: `docker image pull alpine`. 

<img width="650" height="300" alt="imagen" src="https://github.com/user-attachments/assets/99d7a75d-6267-4467-9c9b-fc5067c022ef" />

- Comprombamos que está en nuestro equipo:
  <img width="650" height="300" alt="imagen" src="https://github.com/user-attachments/assets/598c4029-c4f8-4f80-9d04-b4582c6611b6" />

## Crea un contenedor sin ponerle nombre. ¿está arrancado? Obtén el nombre

- Al crear la imagen "alpine" se crea automáticamente un contenedor, como en este caso no le asignamos un nombre, se le crea uno por defecto.
 
- Con el comando `docker ps -a` podemos ver el nombre aleatorio asignado: **zen_noyce** 

<img width="650" height="300" alt="imagen" src="https://github.com/user-attachments/assets/cb058fd1-21f6-42f1-9b7f-56918f788d01" />

## Crea un contenedor con el nombre 'dam_alp1'. ¿Como puedes acceder a él?

- Para crear un contenedor debemos colocar el código `docker container create -it --name dam_alp1 alpine`. 
- Y para acceder a él, tendremos que utilizar las abreviaturas `-it`. Estas nos permitirán interactuar con el contenedor desde la terminal como si estuvieramos dentro de él.  
- Luego de crear el contenedor debemos iniciarlo con el comando `docker start dam_alp1`, para así verificar con `docker ps -a` si está activo "up".
- Finalmente, accedemos ejecutando `docker exec -it dam_alp1 sh` y podemos usar la terminal dentro de ese contenedor (probé con un ls para verificar que funcionaba). 
- Cabe resaltar que la abreviatura `exec` sirvió para ejecutar un comando dentro de un contenedor que ya está en ejecución y `sh` es el comando que se ejecuta dentro del contenedor (en este caso shell).  

<img width="650" height="300" alt="imagen" src="https://github.com/user-attachments/assets/719d372a-4905-4dbc-880b-f05d935ca333" />

<img width="650" height="100" alt="imagen" src="https://github.com/user-attachments/assets/87652be9-c4e6-4008-8d72-0e4a3e3b0ae7" />

## Comprueba que ip tiene y si puedes hacer un ping a google.com

- Una vez dentro de la terminar del contenedor, con el comando `ip a`, podemos saber nuestra ip que podemos verla resaltada en la imagen.
- Posteriormente, procedemos a hacer ping con la dirección de `google.com` y vemos que sí funciona. (cabe resaltar que para evitar que te salgan muchos mensajes en el ping, se debe poner un máximo con el comando `ping -c 4 ....`).  

<img width="650" height="300" alt="imagen" src="https://github.com/user-attachments/assets/983df3e5-f883-47b2-bdd1-4939f9e5f6ce" /> 

## Crea un contenedor con el nombre 'dam_alp2'. ¿Puedes hacer ping entre los contenedores?

- Hacemos lo mismo que con `dam_alp1`, creamos dicho contenedor y luego procedemos a iniciarlo con `start`. 

<img width="650" height="300" alt="Archivo_000" src="https://github.com/user-attachments/assets/218e028b-f536-4d26-86ba-dcf09476e8a7" />

- Una vez dentro de la terminal del contenedor (ya habiendo usado el comando `docker exec -it dam_alp2` (así como también los dos contenedores estén con la imagen "**alpine**"), procedemos a obetener la ip de este contenedor. 

<img width="650" height="300" alt="Archivo_000 (1)" src="https://github.com/user-attachments/assets/7d324ad1-9975-4f5b-953c-b2ed61202163" />

- Finalmente, accedemos a la terminal del primer contenedor, y procedemos a hacer el ping con la ip del segundo contenedor: `ping -c 4 172.17.0.3`.
- Vemos que el ping fue **exitoso** (cabe resaltar que los dos contenedores están en funcionamiento `up`).

<img width="650" height="300" alt="Archivo_000 (2)" src="https://github.com/user-attachments/assets/45c882d0-2ce5-45da-b584-09bcdc40dd45" />


## Sal del terminal, ¿que ocurrió con el contenedor?

- Saliendo con `exit` en la terminal, procedemos a ver el **status** de los contenedores con el comando `docker ps -a`. Se concluye que ambos contenedores están abiertos. 

<img width="650" height="300" alt="Archivo_000 (3)" src="https://github.com/user-attachments/assets/21751477-e08d-4dea-bb89-51aab436dbf6" />

## ¿Cuánta memoria en el disco duro ocupaste?

- Para saber la memoria ocupada, debemos utilizar el siguiente comando: `docker system df`. Con dicho comando, se puede ver la cantidad que se utilizó.  

<img width="650" height="300" alt="Archivo_000 (4)" src="https://github.com/user-attachments/assets/cc95db6d-3407-457f-b66c-fdad44c0444e" />

## ¿Cuánta RAM ocupan los contenedores? ¿Hay algún comando docker para saber esto?.

- Mediante un `docker stats`, podemos visualizar (en tiempo real) los recursos que consume cada contenedor.
- Y para la **RAM**, podemos visualizarlo en el apartado de **MEM USAGE/LIMIT**. Donde **MEM USAGE** significa la RAM que utiliza el contenedor actualmente; mientras que **LIMIT**, es el límite máximo asegurado. 

<img width="650" height="300" alt="Archivo_000 (5)" src="https://github.com/user-attachments/assets/39deacfb-698b-4b37-8d09-9f29e8b7e61a" />


