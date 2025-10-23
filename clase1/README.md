# Clase #1 - Introducción a Containers y Docker

**Despliegue de un servidor web**

1. Apache HTTP Server (httpd)
2. Comandos ejecutados

    ` # docker run -d -p 8081:80 --name mi-apache httpd` (Comando de despliegue - Creación)

    ` # docker logs mi-apache` (Comando de verificacion)

    `# docker rm my-apache` (Comando de limpieza)

3. Explicación breve - Qué hace cada flag del comando `docker run` que usaste:
    - `-d` Ejecuta un contenedor en segundo plano.
    - `-p` Mapea los puertos del host al contenedor. 
    - `--name` Asigna un nombre personalizado a nuestro contenedor.
    - `--rm` Elimina el contenedor automaticamente al detenerse.

4. Evidencia
    - Screenshots 01 (Estado)
    ![Containers corriendo](screenshots/Opcion1/Descarga&Despliegue%20imagen%20httpd%20(apache)%20-%2001.JPG)

    - Screenshots 02 (Verificación)
    ![Container corriendo y exponiendo resultado en navegarores](screenshots/Opcion1/Verificacion%2001.JPG)

    - Screenshots 03 (Eliminacion)
    ![Screenshot o salida mostrando que el container fue eliminado correctamente](screenshots/Opcion1/Eliminacion%20contenedor.JPG)
    
5. Conclusiones
    - *Qué se aprendio*, para esta primera clase se logro aprender acerca de los comandos basico para crear (correr), verificar y eliminar contenedores. Ademas de logramos usar diferentes tags que nos permiten personalizar el "funcionamiento" de nuestros contenedores.

    - *Dificultades*, la dificultad que puedo mesionar es el uso de comandos, al ser una persona que viene del entorno windows. 