
## Creando un usuario
 RUN useradd bVasquez

### Usando ese usuario
 USER bVasquez

## Comando para crear una imagen
RUN apt -y update && apt install iputils-ping

## Variable de entorno 
CMD echo $DEMO World

## Cada vez que se hace un cambio, se debe actualizar la imagen y cambiar su version.

## Ver todas los contenedores o instancias:
 docker ps -a

# Modificar la variable de entorno en el comando
 docker run -e DEMO=Yazmin my demo:v1.0.2

# Creando un container
   docker run --name container-1 mydemo:3.0 sh

# Usar Docker Compose para componer los dockers que creamos
  1. hay que ir al directorio donde esta el .yaml
  2. Ejecutar el siguiente comando: 
    - docker-compose up