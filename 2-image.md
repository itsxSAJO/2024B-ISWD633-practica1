# Imagen
Es un archivo único que contiene todos los programas, librerías, dependencias y configuraciones necesarias para instalar y/o ejecutar una aplicación o un conjunto de aplicaciones.
![Imagen](img/imagen.PNG)


## ¿Cuál es la relación entre una imagen y un contenedor? 
Una imagen es un archivo único que contiene todo el entorno necesario para instalar y/o ejecutar una aplicación o un conjunto de aplicaciones, mientras que un contenedor es una instancia independiente ejecutable de esa imagen.
# COMPLETAR 

![Imagen y contenedores](img/imagenContenedores.JPG)
## Comandos para imágenes

### Descargar imagen
Descarga la última versión de la imagen disponible en el registro de Docker.

```
docker pull hello-world
```

Descarga una versión específica de la imagen, cada imagen tiene etiquetas (tags) para diferentes versiones.
Una imagen puede tener la etiqueta latest para representar la última versión, si no se especifica una etiqueta se hará referencia a la versión latest.

```
docker pull hello-world:latest
```

Descargar la imagen **hello-world**

# COMPLETAR

**¿Qué es nginx?**

Nginx es un servidor web y proxy inverso de código abierto, optimizado para gestionar solicitudes HTTP/HTTPS de forma eficiente. Es conocido por su capacidad de balanceo de carga, manejo de alto tráfico y configuración flexible. Además, es ideal para servir contenido estático y soporta módulos para agregar funcionalidades como autenticación, compresión y seguridad.

[1] F.Brutti. (2023, November 21). ¿Qué es Nginx y cómo funciona? Entérate de todo ahora [Online]. Available: https://thepower.education/blog/que-es-nginx
# COMPLETAR 

Descargar la imagen  **nginx** en la versión **alpine**
```
docker pull nginx:alpine
```
# COMPLETAR

### Listar imágenes

```
docker images
```

# COLOCAR UNA CAPTURA DE PANTALLA DEL RESULTADO 

**Identificadores**

En Docker, se utilizan varios identificadores para diferenciar de manera única los elementos del sistema, como imágenes, contenedores, volúmenes y redes. Estos identificadores son generados automáticamente por Docker y son únicos dentro del contexto del sistema Docker en el que se encuentran. 

### Inspeccionar una imagen
El comando docker inspect se utiliza para obtener información detallada sobre un objeto de Docker específico, como un contenedor, una imagen, un volumen o una red.  Proporciona información en formato JSON sobre el objeto especificado.

```
docker inspect hello:world
docker inspect hello-world:latest
```

Inspeccionar la imagen hello-world 
# COMPLETAR

**¿Con qué algoritmo se está generando el ID de la imagen?**

El ID de una imagen en Docker se genera utilizando un algoritmo basado en SHA-256, que es una función hash criptográfica. Este algoritmo toma el contenido de la imagen (incluyendo todos sus archivos, capas y metadatos) y genera un hash único de 256 bits (32 bytes).
# COMPLETAR

### Filtrar imágenes

Al intentar ejecutar el comando docker images | grep nginx, obtuve un error porque grep es un comando de Unix/Linux y no está disponible de forma predeterminada en PowerShell de Windows. Para solucionar esto, utilicé el comando Select-String para filtrar la salida en PowerShell, de la siguiente manera:
```
docker images | Select-String nginx
```

### Para eliminar una imagen
Eliminar permanentemente la imagen de tu sistema Docker.

```
docker rmi hello-world:latest
```

Eliminar la imagen hello-world 
# COMPLETAR

-f: Es la opción para forzar la eliminación de la imagen incluso si hay contenedores en ejecución que utilizan esa imagen.
Cuando eliminas una imagen Docker, Docker no elimina automáticamente los contenedores que se han creado a partir de esa imagen. Esto significa que, aunque hayas eliminado la imagen, el contenedor seguirá ejecutándose normalmente.  
**Considerar**
Eliminar una imagen no afecta a los contenedores que se han creado a partir de esa imagen, a menos que esos contenedores dependan de archivos o configuraciones específicas de la imagen eliminada. En ese caso, es posible que los contenedores se comporten de manera inesperada después de eliminar la imagen.
Es una buena práctica detener y eliminar todos los contenedores que dependan de una imagen antes de eliminar la imagen en sí.

```
docker rmi -f nginx:alpine
```

