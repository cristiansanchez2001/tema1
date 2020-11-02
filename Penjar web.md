#Carta en servidor Apache i Hosting

El primer que tot, necesitem instalar el servidor web Apache, per a instalarlo utilizarem el comando apt-get install apache2. Una vegada estiga instalat tindrem que modificar uns arxius de la nostra web en hugo, en concret la forma de accedir per a que siga accesible desde el servidor.
Per a fer-ho entrarem en el archiu config.yaml i modificarem la linea de la captura per la direccio web del servidor apache.

![](/imagenes/1.jpg)

Una vegada tenim modificat el archiu fem un hugo -D dins de la carpeta de la nostra pagina. Se generara la carpeta public, aquesta carpeta conte els fichers de la web en HTML. Hem de copiarla en la ruta /var/www/html del servidor Apache per a que funcione.

![](/imagenes/2.jpg)

Pero abans de que funcione hem de cambiar el grup de la carpeta html, per a fero utilitzem el comando chgrp -R www-data /var/www/html i afegim permisos de clase 775. I per a finalitzar ens afegim com a propietaris de la carpeta fent

**sudo chown -R eljust /var/www/html**

![](/imagenes/3.jpg)

Per a penjar la web en un hosting seria molt paregut, fiquem la URL del link que ens han donat. Modifiquem el arxiu config.yaml i introduim la direccio web del noste host. Despres copiem els arxius de la carpeta public a la carpeta public\_html i ja estaria funcionant la web.

![](/imagenes/4.jpg)

![](/imagenes/5.jpg)




