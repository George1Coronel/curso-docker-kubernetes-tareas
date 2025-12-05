# 01.Setup Ambiente - Preparacion de entorno e instalaciones requeridas

**Preparacion del entorno**

1. Caracteristicas de la maquina u ordenador:

![Informacion de la maquina u ordenador](screenshots/etapa01/00.JPG)

- El entorno con el que se cuenta para el despliegue del proyecto final, es una maquina virtual.
- Con el sistema operativo sugerido: Ubuntu Server 24.04.
- El equipo se encuentra conectado en la redi virtual con la siguiente direccion IP: 192.168.1.13

![Informacion de la maquina u ordenador](screenshots/etapa01/01.JPG)

2. Instalación `microk8s` orden de pasos seguidos:
- Ejecución de los comando de instalación: `sudo snap install microk8s --classic`
    
    Proceso de instalación

    ![Informacion de la maquina u ordenador](screenshots/etapa01/02.JPG)

    Instalación completada

    ![Informacion de la maquina u ordenador](screenshots/etapa01/03.JPG)


- Configuracion de grupos

    ![Informacion de la maquina u ordenador](screenshots/etapa01/04.JPG)

- Configuracion de alias para el comando `microk8s`

    ![Informacion de la maquina u ordenador](screenshots/etapa01/05.JPG)

- Habilitacion de Addons los comandos ejecutados son los siguientes:
    * `microk8s enable dns` Habilitación del DNS de microk8s
    * `microk8s enable storage` Habilitacion del Storage.
    * `microk8s enable ingress` Habilitacion de Ingress
    ![Informacion de la maquina u ordenador](screenshots/etapa01/06.JPG)

    * `microk8s enable metrics-server` Habilitacion de Metraicas
    ![Informacion de la maquina u ordenador](screenshots/etapa01/07.JPG)


    * `microk8s enable metallb:192.168.1.200-192.168.1.210` Habilitacion de direccion IP fuera del rango de la asignacion del DHCP de mi red local.
    ![Informacion de la maquina u ordenador](screenshots/etapa01/08.JPG)

        Por ultimo verificamos el estado del microk8s con el comando: `microk8s status`
        ![Informacion de la maquina u ordenador](screenshots/etapa01/09.JPG)


        Validamos los paquetes requeridos para los siguientes pasos ejecutando los siguienes comandos:
        - Validamos la instalacion de GIT: `git --version`
        - Validamos la instalacion de Docker: `docker --version`
        - Validamos la instalacion de docker compose: `docker composer version`

        ![Informacion de la maquina u ordenador](screenshots/etapa01/10.JPG)

        Iniciamos sesion en DockerHub con el siguiente comando: `docker login`

        ![Informacion de la maquina u ordenador](screenshots/etapa01/11.JPG)

- Obtencion y Despliegue "PROYECTO INTEGRADOR V2.0"
        - Extraemos los archivos con el siguiente comando: `unzip proyecto-integrador-docker-k8s-main`

    ![Informacion de la maquina u ordenador](screenshots/etapa01/12.JPG)

- Despliegue y verificacion Proyecto Integrador v2.0

    Siguiendo los pasos del `Proyecto-Integrador/k8s/DEPLOYMENT_GUIDE_MICROK8S`
    
    - Habilitacion de requisitos 

    <!-- ![Informacion de la maquina u ordenador](screenshots/etapa01/13.JPG)
    ![Informacion de la maquina u ordenador](screenshots/etapa01/14.JPG)
    ![Informacion de la maquina u ordenador](screenshots/etapa01/15.JPG) -->
    ![Informacion de la maquina u ordenador](screenshots/etapa01/16.JPG)

    - Preparacion de Imagenes

    ![Informacion de la maquina u ordenador](screenshots/etapa01/17.JPG)
    ![Informacion de la maquina u ordenador](screenshots/etapa01/18.JPG)

    - Uso del registry local de microk8s e importacion de imagenes desde docker 

    ![Informacion de la maquina u ordenador](screenshots/etapa01/19.JPG)

    ![Informacion de la maquina u ordenador](screenshots/etapa01/20.JPG)

    Paso: 0 - Creacion del NameSpace

    ![Informacion de la maquina u ordenador](screenshots/etapa01/21.JPG)

    Paso: 1 - Configuracion (ConfigMaps y Secrets)

    Paso: 2 - Base de Datos (PostgreSQL con StatefulSet)

    ![Informacion de la maquina u ordenador](screenshots/etapa01/22.JPG)

    ![Informacion de la maquina u ordenador](screenshots/etapa01/23.JPG)

    ![Informacion de la maquina u ordenador](screenshots/etapa01/24.JPG)

    ![Informacion de la maquina u ordenador](screenshots/etapa01/25.JPG)

    ![Informacion de la maquina u ordenador](screenshots/etapa01/26.JPG)

    Paso: 3 - Cache (Redis)

    ![Informacion de la maquina u ordenador](screenshots/etapa01/27.JPG)

    ![Informacion de la maquina u ordenador](screenshots/etapa01/28.JPG)

    Paso: 4 - Backend (Sprint Boot API)

    ![Informacion de la maquina u ordenador](screenshots/etapa01/29.JPG)

    ![Informacion de la maquina u ordenador](screenshots/etapa01/30.JPG)

    Paso: 5 Frontend (Angular)

    ![Informacion de la maquina u ordenador](screenshots/etapa01/31.JPG)

    Paso: 6 - Ingres (Routing HTTP)

    ![Informacion de la maquina u ordenador](screenshots/etapa01/32.JPG)

    ![Informacion de la maquina u ordenador](screenshots/etapa01/32.JPG)
    ![Informacion de la maquina u ordenador](screenshots/etapa01/33.JPG)
    ![Informacion de la maquina u ordenador](screenshots/etapa01/34.JPG)
    ![Informacion de la maquina u ordenador](screenshots/etapa01/35.JPG)
    ![Informacion de la maquina u ordenador](screenshots/etapa01/36.JPG)
    ![Informacion de la maquina u ordenador](screenshots/etapa01/37.JPG)
    ![Informacion de la maquina u ordenador](screenshots/etapa01/38.JPG)
    ![Informacion de la maquina u ordenador](screenshots/etapa01/39.JPG)

    Ya para la seccion de "Actualizar la aplicacion Desdepues de la modificacion de codigo", se presenta el siguiente problema:
    No se logra encontrar la imagen: alefiengo/springboot-api:v2.0 en doker-hub

    ![Informacion de la maquina u ordenador](screenshots/etapa01/40.JPG)







