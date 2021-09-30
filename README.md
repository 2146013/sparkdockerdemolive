# Sparkdockerdemolive
## Taller Arep 30 de septiembre del 2021

Se crea una aplicacion web usando Spark java,esta aplicación procederemos a construir un container para docker para la
aplicación y los desplegaremos y configuraremos en nuestra máquina local. Luego, cerremos un repositorio en DockerHub
y subiremos la imagen al repositorio. Finalmente, crearemos una máquina virtual de en AWS, instalaremos Docker ,
y desplegaremos el contenedor que acabamos de crear.

## Prerrequisitos

- Git version 2.25.1
  Git es un proyecto de código abierto maduro y con un mantenimiento activo,Git, que presenta una arquitectura distribuida, 
  es un ejemplo de DVCS . En lugar de tener un único espacio para todo el historial de versiones del software, como sucede
  de manera habitual en los sistemas de control de versiones antaño populares, como CVS.la copia de trabajo del código de
  cada desarrollador es también un repositorio que puede albergar el historial completo de todos los cambios.
  ![imagengit](https://user-images.githubusercontent.com/60073527/135369933-16356d8c-d54f-4c69-9975-8545c96ea0b8.png)


- Apavhe Maven version 4.0.0
  Apache Maven es una herramienta que estandariza la configuración de un proyecto en todo su ciclo de vida, como por ejemplo
  en todas las fases de compilación y empaquetado y la instalación de mecanismos de distribución de librerías, para que puedan
  ser utilizadas por otros desarrolladores y equipos de desarrollo.
  

- Docker
  es una plataforma abierta para que desarrolladores y administradores de sistemas desarrollen, envíen y ejecuten aplicaciones
  distribuidas, ya sea en computadoras portátiles, maquinas virtuales de centros de datos o en la nube.
  ![imagendocker](https://user-images.githubusercontent.com/60073527/135370062-8dbe401c-4c97-482b-82a7-944169ac1d98.png)

  
- Aws Amazon
  Amazon Web Services (AWS) es la plataforma en la nube más adoptada y completa en el mundo, que ofrece más de 200 servicios
  integrales de centros de datos a nivel global. Millones de clientes, incluso las empresas emergentes que crecen más rápido,
  las compañías más grandes y los organismos gubernamentales líderes, están usando AWS para reducir los costos, aumentar su 
  agilidad e innovar de forma más rápida.
  ![imagenaws](https://user-images.githubusercontent.com/60073527/135370073-bd023a1b-e322-4d4c-a44f-d85a809ade63.jpg)


- Para verificar que esten instalados los programas puede usar los suguientes comandos + mvn --version + git version
- +java --version





## Instrucciones de uso

Java versión: 1.8.0
Ejecución
En el sigiente lik de Github [https://github.com/2146013/sparkdockerdemolive.git]

podras encontara la aplicacion web donde posteriormente se implemento la contruccion de un container para docker dede se
configuro en nuestra maquina local, este contenedor creado sera igualmente desplegado en la maquina virtual de AWS
mvn spring-boot:run,se abrira la ventana donde puede evidenciar "hello docker"

El tablero se corre en http://ec2-54-162-247-23.compute-1.amazonaws.com:42000/hello

## Bitacora 

1. Se creo un proyecto java usando maven,crando tambien la clase principal

<img width="957" alt="imagenbitacora1" src="https://user-images.githubusercontent.com/60073527/135370165-ade2ed38-ba28-435d-bbb1-d76f68a190f6.PNG">

2. Se crean las imagenes para docker y con Docker compose se detine la estrategia de despliegue sobre Docker y el Docker 
 permite definir los archivos como vemos en la siguiente imagen.
 
<img width="956" alt="imagenbitacora2 1" src="https://user-images.githubusercontent.com/60073527/135370198-d9a504a7-c540-47a7-b6fc-2dc5f66bdcd3.PNG">

3. Verificamos que se creen correctamente

<img width="656" alt="imagendockrer" src="https://user-images.githubusercontent.com/60073527/135370275-5664c1af-3625-423e-9b1c-dc1ff4f3ffc2.PNG">

4. Accedemos  al menu de repositorio y creamos un repositorio

<img width="946" alt="imagenbitacora3" src="https://user-images.githubusercontent.com/60073527/135370422-155a1e3b-0764-4979-927d-25f43a822c07.PNG">

6. Creamos una instancia en AWS e instalamos Docker en la maquina. 

<img width="590" alt="aws 6 punto" src="https://user-images.githubusercontent.com/60073527/135370440-76083f33-c3c1-4c2e-8ce4-137928268055.PNG">

<img width="597" alt="imagen6 1" src="https://user-images.githubusercontent.com/60073527/135370446-3958ca06-c4e0-4614-b922-5750ade242fe.PNG">

7. Creamos las reglas de entrada

<img width="891" alt="regla" src="https://user-images.githubusercontent.com/60073527/135370468-d7a30bc3-82c3-4627-bad0-4e65f852c323.PNG">

8. Creamos contenedores con el siguiente comando
   docker run -d -p 42000:6000 --name firstdockerimageaws danielapachoncuan/chispa-dockerdemolive

9.Instalamos Docker en la maquina aws

<img width="675" alt="Captura cmd" src="https://user-images.githubusercontent.com/60073527/135370527-7880f966-c5bc-4845-af54-645d5d67b6b3.PNG">


10. En nuestro motor  de docker local se creo una referencia con la imagen y el nombre que se desea subir,con el siguiente comando
   docker tag dockersparkprimer danielapachoncuan/chispa-dockerdemolive en este caso. Se verifica que la imagen exista con docker images.
   
   <img width="788" alt="Captura cmd docker" src="https://user-images.githubusercontent.com/60073527/135370545-7accc080-2c6f-4099-bc35-61d03096ce06.PNG">


11. Verificamos que las imagenes esten creadas


<img width="656" alt="imagendockrer" src="https://user-images.githubusercontent.com/60073527/135370588-21fe0497-29d7-4b59-bd5a-9b81bce86186.PNG">

12. Verificamos el funcionamiento 

<img width="960" alt="funcionamientoaws" src="https://user-images.githubusercontent.com/60073527/135370601-671ca542-4c58-426c-8d8f-92eea97a2ec8.PNG">

## Tecnologias

Maven
Java
Springboot
micro-framework de Spark java
docker
dockerhub
máquina virtual de en AWS

## Autor
Laura Daniela Pachon Cuan - Fecha: 30/09/2021

## Licencia
This project is licensed under the MIT License - see the LICENSE file for details

