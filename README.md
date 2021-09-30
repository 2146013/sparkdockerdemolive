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

- Apavhe Maven version 4.0.0
  Apache Maven es una herramienta que estandariza la configuración de un proyecto en todo su ciclo de vida, como por ejemplo
  en todas las fases de compilación y empaquetado y la instalación de mecanismos de distribución de librerías, para que puedan
  ser utilizadas por otros desarrolladores y equipos de desarrollo.

- Docker
  es una plataforma abierta para que desarrolladores y administradores de sistemas desarrollen, envíen y ejecuten aplicaciones
  distribuidas, ya sea en computadoras portátiles, maquinas virtuales de centros de datos o en la nube.
- Aws Amazon
  Amazon Web Services (AWS) es la plataforma en la nube más adoptada y completa en el mundo, que ofrece más de 200 servicios
  integrales de centros de datos a nivel global. Millones de clientes, incluso las empresas emergentes que crecen más rápido,
  las compañías más grandes y los organismos gubernamentales líderes, están usando AWS para reducir los costos, aumentar su 
  agilidad e innovar de forma más rápida.

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

2. Se crean las imagenes para docker y con Docker compose se detine la estrategia de despliegue sobre Docker y el Docker 
 permite definir los archivos como vemos en la siguiente imagen.

3. Verificamos que se creen correctamente

4. Accedemos  al menu de repositorio y creamos un repositorio

5. Creamos una instancia en AWS e instalamos Docker en la maquina. 

6. Creamos contenedores con el siguiente comando
   docker run -d -p 42000:6000 --name firstdockerimageaws danielapachoncuan/chispa-dockerdemolive

7.Instalamos Docker en la maquina aws

8. En nuestro motor  de docker local se creo una referencia con la imagen y el nombre que se desea subir,con el siguiente comando
   docker tag dockersparkprimer danielapachoncuan/chispa-dockerdemolive en este caso. Se verifica que la imagen exista con docker images.

9. Verificamos que las imagenes esten creadas

10. Verificamos el funcionamiento 

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

