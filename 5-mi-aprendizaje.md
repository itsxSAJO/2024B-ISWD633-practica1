# COMPLETAR  

Durante esta práctica con Docker, me di cuenta de varias cosas que antes no tenía tan claras. Lo primero fue entender bien la diferencia entre una imagen y un contenedor, antes pensaba que eran lo mismo, pero en realidad, la imagen es como un paquete que tiene todo lo necesario para que la app funcione, y el contenedor es la instancia de esa imagen que se ejecuta.

Con los comandos básicos como docker create, docker run, docker ps y docker stop, me siento mucho más cómodo. Algo que no sabía es que, si no le asigno un nombre al contenedor, Docker le pone uno raro automáticamente, aunque ya entendí que es mejor darle un nombre para no confundirme.

También aprendí cómo funciona el mapeo de puertos, lo que me permite acceder desde mi navegador al servidor que corre dentro de un contenedor.

Otro punto importante fue darme cuenta de la utilidad de la opción -d para ejecutar contenedores en segundo plano. Al principio, cuando corría un contenedor, mi terminal quedaba bloqueada y no podía hacer nada más, con -d, el contenedor corre en segundo plano y puedo seguir usando la terminal sin problemas.

Finalmente, entendí cómo gestionar mejor las imágenes. Ahora sé cómo descargarlas, inspeccionarlas y eliminarlas cuando ya no las necesito, lo que me ayuda a mantener limpio el sistema.

Quiero agradecer a la Ing. Evelyn Mosquera por el desarrollo de esta práctica, fue muy intuitiva y divertida, lo que hizo que aprender Docker se sintiera más fácil y práctico.
