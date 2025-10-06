# SXE-PIERO-2-DAM
Utilizaremos la imagen de Alpine. Sigue las instrucciones:

## Descarga la imagen "alpine" SIN ARRANCARLA y comprueba que está en tu equipo

- Primero lo que tenemos que hacer es que debemos abrir la aplicación de docker de manera manual y posteriormente abrir la termina.
- Posteriormente, para descargar la imagen "alpine" sin arrancarla debemos hacerla a través un "pull" de manera que quedaría así: `docker image pull alpine`. 

<img width="650" height="300" alt="imagen" src="https://github.com/user-attachments/assets/99d7a75d-6267-4467-9c9b-fc5067c022ef" />

- Comprombamos que está en nuestro equipo:
  <img width="726" height="277" alt="imagen" src="https://github.com/user-attachments/assets/598c4029-c4f8-4f80-9d04-b4582c6611b6" />

## Crea un contenedor sin ponerle nombre. ¿está arrancado? Obtén el nombre

Al crear la imagen "alpine" se crea automáticamente un contenedor, como en este caso no le asignamos un nombre, se le crea uno por defecto.
 
Con el comando `docker ps -a` podemos ver el nombre aleatorio asignado: **zen_noyce** 

<img width="650" height="300" alt="imagen" src="https://github.com/user-attachments/assets/cb058fd1-21f6-42f1-9b7f-56918f788d01" />

## Crea un contenedor con el nombre 'dam_alp1'. ¿Como puedes acceder a él?

docker container create -it --name dam_alp1 alpine
<img width="973" height="508" alt="imagen" src="https://github.com/user-attachments/assets/719d372a-4905-4dbc-880b-f05d935ca333" />

<img width="1076" height="126" alt="imagen" src="https://github.com/user-attachments/assets/87652be9-c4e6-4008-8d72-0e4a3e3b0ae7" />

## Comprueba que ip tiene y si puedes hacer un ping a google.com

<img width="1775" height="1002" alt="imagen" src="https://github.com/user-attachments/assets/983df3e5-f883-47b2-bdd1-4939f9e5f6ce" />
mensaje 
<img width="1890" height="992" alt="Archivo_000" src="https://github.com/user-attachments/assets/0f6abb0c-6823-4779-82c9-5193f2096513" />

## Crea un contenedor con el nombre 'dam_alp2'. ¿Puedes hacer ping entre los contenedores?

<img width="1890" height="992" alt="Archivo_000" src="https://github.com/user-attachments/assets/218e028b-f536-4d26-86ba-dcf09476e8a7" />

<img width="2047" height="1181" alt="Archivo_000 (1)" src="https://github.com/user-attachments/assets/7d324ad1-9975-4f5b-953c-b2ed61202163" />

<img width="1992" height="1173" alt="Archivo_000 (2)" src="https://github.com/user-attachments/assets/45c882d0-2ce5-45da-b584-09bcdc40dd45" />


## Sal del terminal, ¿que ocurrió con el contenedor?

<img width="1994" height="1036" alt="Archivo_000 (3)" src="https://github.com/user-attachments/assets/21751477-e08d-4dea-bb89-51aab436dbf6" />

## ¿Cuanta memoria en el disco duro ocupaste?

<img width="1994" height="1088" alt="Archivo_000 (4)" src="https://github.com/user-attachments/assets/cc95db6d-3407-457f-b66c-fdad44c0444e" />

## ¿Cuanta RAM ocupan los contenedores? ¿Hay algún comando docker para saber esto?.

<img width="1956" height="920" alt="Archivo_000 (5)" src="https://github.com/user-attachments/assets/39deacfb-698b-4b37-8d09-9f29e8b7e61a" />


