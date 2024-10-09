# Contenedores

### Crear un contenedor
Para crear un nuevo contenedor Docker a partir de una imagen específica, pero sin iniciarlo automáticamente. 

```
docker create --name srv-web nginx:alpine
```
Crear el contenedor  **srv-web** usando la imagen nginx version alpine
# COMPLETAR

Si creas un contenedor en Docker sin asignarle un nombre específico utilizando la opción --name, Docker asignará automáticamente un nombre aleatorio al contenedor. Este nombre suele consistir en una combinación de palabras y números.  
```
docker create hello-world:latest
```
Crear el contenedor usando la imagen hello-world
# COMPLETAR

### Listar los contenedores ejecutándose o no

```
docker ps -a
```

### Para iniciar un contenedor

```
docker start srv-web
```
Iniciar el contenedor srv-web 
# COMPLETAR

### Listar los contenedores ejecutándose
Al intentar ejecutar el comando docker ps | grep srv-web, obtuve un error porque grep es un comando de Unix/Linux y no está disponible de forma predeterminada en PowerShell de Windows. Para solucionar esto, utilicé el comando Select-String para filtrar la salida en PowerShell, de la siguiente manera: 
```
docker ps 
docker ps | Select-String srv-web
```

### Para detener un contenedor

```
docker stop srv-web
```

### Para crear un contenedor y ejecutarlo inmediatamente

```
docker run --name srv-web2 nginx:alpine
```
![Ecosistema de Docker](img/dockerRun.PNG)

Crear y ejecutar inmediatamente el contenedor **srv-web2** usando la imagen nginx:alpine
# COMPLETAR

**¿Qué sucede luego de la ejecución del comando?**

Después de ejecutar el comando la terminal se queda "bloqueada" porque el contenedor de Nginx está funcionando en primer plano. Esto indica que el proceso de Nginx está activo y esperando recibir solicitudes, mientras esto sucede, no puedo ingresar nuevos comandos en la terminal, ya que está ocupada ejecutando el contenedor.
# COMPLETAR  

Cuando ejecutas un contenedor en primer plano sin la opción -d (modo detach), el contenedor captura la entrada estándar (stdin) del terminal, lo que significa que el terminal queda "atrapado" y no puedes introducir más comandos hasta que detengas el contenedor.

### Para crear un contenedor y ejecutarlo inmediatamente sin estar vinculados al mismo
-d: Es la opción que indica a Docker que ejecute el contenedor en segundo plano (en modo "detach").
Cuando un contenedor se ejecuta en segundo plano, Docker devuelve el control al terminal inmediatamente después de iniciar el contenedor, lo que permite al usuario seguir ejecutando otros comandos en el mismo terminal sin que el contenedor detenga la interacción.

```
docker run -d --name srv-web3 nginx:alpine
```
Crear y ejecutar inmediatamente el contenedor **srv-web3** en modo detach usando la imagen nginx:alpine
# COMPLETAR

### Para eliminar un contenedor

```
docker rm magical_sammet
```
Eliminar el contenedor que se creó a partir de la imagen hello-world 
# COMPLETAR

Verificar que el contenedor que se eliminó
# COMPLETAR

### Para eliminar un contenedor que esté ejecutándose

```
docker rm -f srv-web3
```
Eliminar el contenedor **srv-web3** 
# COMPLETAR

Verificar que el contenedor que se eliminó
# COMPLETAR

### Para inspecionar un contenedor 

```
docker inspect srv-web
```

Inspeccionar el contenedor **srv-web** 
# COMPLETAR
