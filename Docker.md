#**WEB EN APACHE DOCKER**

Primer que tot per a penjar la web en un servidor apache de docker tenim que instalar el propi Docker. Per a fer-ho utilitzarem el comando

**sudo apt-get install docker-ce**

Despues instalarem la imatge de Nginx que es una imatge de servidor apache per a Docker. Per a fero gastem el comando

**docker pull nginx**

Una vegada tenim la imatge llançem el contenedor amb el seguent comando:

**docker run -d -p 8888:80 nginx nginx\_prova nginx**

Despues ejecutem el seguent comando

**docker run -d -p 8888:80 --name nginx\_prova -v /home/alumne/public:/usr/share/nginx/html:ro nginx**

Ara ya podrem accedir a la web en la url 127.0.0.1/8888

![](/imagenes/6.jpg)