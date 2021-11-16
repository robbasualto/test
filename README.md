1. Creamos directorio en el cual vamos a trabajar

mkdir Zippylab

2. Entramos al directorio

cd Zippylab/

3. Creamos nuestro archivo index.html

touch index.html

4. Editamos nuestro archivo index.html agregando lo solicitado “¡Hello Zippy!” 

vim index.html

5. Generamos nuestro archivo Dockerfile 

touch Dockerfile

6. Editamos nuestro Dockerfile, este utiliza nginx:alpine

vim Dockerfile

7. Levamtamos nuestra imagen apartir del Dockerfile

$ docker build -t html-zippy:v1 .

8. Levantamos nuestro contenedor via puerto 8080

$ docker run -d -p 8080:80 html-zippy:v1

9. Mediante el browser consultamos hacia localhost:8080 donde podemos ver nuestro servidor nginx operativo con su respectivo “¡Hello Zippy!” 

https://prnt.sc/1zt40qx

10. Otra forma de verlo sin ir direcamente al browser es usando el comando 

$ curl localhost:8080 
