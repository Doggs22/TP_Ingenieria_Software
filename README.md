# TP Ingeniería de Software

Este proyecto consiste en una página HTML simple desplegada en un contenedor Docker utilizando la imagen oficial de `nginx`.

A continuación se detallan los pasos seguidos para contenerizar el proyecto y ejecutarlo localmente.

---

##  Contenido del Proyecto

El proyecto contiene:

- `index.html`: Página web principal.
- `Dockerfile`: Archivo de configuración para crear la imagen Docker.

---

##  Pasos realizados

1. Ingresé a la carpeta del proyecto previamente creado.

2. Creé el archivo `Dockerfile` dentro de esa carpeta:
   - Primero creé un archivo de texto (`.txt`).
   - Luego lo renombré como `Dockerfile` (sin extensión).
   - Verifiqué su creación y edición con Visual Studio Code.

3. Consulté a ChatGPT para obtener el contenido correcto del `Dockerfile` y pegué lo siguiente:

    ```Dockerfile
    FROM nginx:alpine

    COPY . /usr/share/nginx/html

    EXPOSE 80
    ```

4. Abrí la terminal y construí la imagen Docker con el siguiente comando:

    ```bash
    docker build -t tp_ingenieria_software .
    ```

5. Ejecuté el contenedor con el siguiente comando:

    ```bash
    docker run -p 80:80 tp_ingenieria_software
    ```

6. Finalmente, abrí el navegador y visité:

    ```
    http://localhost
    ```

    para comprobar que la página se está sirviendo correctamente desde el contenedor.

---

## Recursos utilizados

- [Docker Hub – nginx](https://hub.docker.com/_/nginx)
- ChatGPT para consultas técnicas
- Visual Studio Code como editor

---

##  Estado

 Proyecto funcional  
 Imagen Docker construida correctamente  
 Página HTML visible en navegador usando contenedor
