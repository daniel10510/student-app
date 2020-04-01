# Proyecto PersonList con Docker

Proyecto final para el curso de Docker de Mitocode

## Comenzando 🚀

Estas instrucciones te permitirán obtener una copia del proyecto en funcionamiento en tu máquina local para propósitos de desarrollo y pruebas.

### Pre-requisitos 📋

* Cuenta en dockerhub
* (EQUIPO-A) Computador físico o virtual en el cual debe estar instalado la herramienta docker. (Necesario para compilar la aplicación),
    - Procesador i3 o superior, ó en su defecto al menos 2 nucleos.
    - RAM de al menos 2GB
    - Espacio en disco de 10 GB
    - Conexión a internet.
* (EQUIPO-B) Computador físico o virtual en el cual debe estar instalado la herramienta docker swarm
    - Procesador i5 o superior, ó en su defecto al menos 4 nucleos.
    - RAM de al menos 4GB
    - Espacio en disco de 10 GB
    - Conexión a internet.

### Instalación 🔧

* En el EQUIPO-A, realizar lo siguiente:
	- Clonar el repositorio.
	- Abrir una terminal y situarse en la raiz del proyecto clonado.
	- Ejecutar los siguientes comandos en el orden que precede:
		- $docker build -t daniel10510/student-api:1 .
		- $docker build -t daniel10510/student-frontend:1 ./frontend/
		- $docker login -u {LOGIN_DOCKERHUB} -p {PASSWORD_DOCKERHUB}
		- $docker push daniel10510/student-api:1
		- $docker push daniel10510/student-frontend:1
	
	(Nota: Reemplazar los valores {LOGIN_DOCKERHUB} y {PASSWORD_DOCKERHUB} con los valores respectivos a la cuenta dockerhub)
	
## Despliegue 📦

* En el EQUIPO-B, realizar lo siguiente:
	- Ejecutar los siguientes comandos en el orden que precede:
		$sudo docker stack deploy --compose-file docker-compose.yml student-app
	- Para verificar el correcto despliegue de la aplicación, ejecute el siguiente comando:
		- $sudo docker service ls
	(Nota: Espere aproximadamente 5 minutos a que se levanten los servicios)

## Construido con 🛠️

* [Maven](https://maven.apache.org/) - Manejador de dependencias backend
* [NPM](https://www.npmjs.com/) - Manejador de dependencias frontend

## Versionado 📌

Usamos [SemVer](http://semver.org/) para el versionado.

## Licencia 📄

Este proyecto está bajo la Licencia MIT.

## Expresiones de Gratitud 🎁

* Mitocode
