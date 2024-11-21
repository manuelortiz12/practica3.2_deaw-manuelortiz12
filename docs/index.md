# PRÁCTICA 3.2: DESPLIEGUE DE APLICACION CON NODE EXPRESS

En primer lugar, y tras haber usado tomcat9 en la práctica anterior deberemos desactivarlo de nuestro equipo, ya que este puede causar incompatibilidad con Node.

## Instalación de Node.js, Express y test de la primera aplicación

En primer lugar y sin extendernos mucho procederemos a instalar Node.js de la siguiente manera:

![Imagen 2](images/2.png)

Y ahora instalamos Express.js y creamos un un proyecto de prueba:

![Imagen 3](images/3.png)


![Imagen 4](images/4.png)

Y cambiamos localhost por nuestra ip:

![Imagen 5](images/5.png)


![Imagen 6](images/6.png)

Nos dirigimos a la ip con el puerto 3000 y veremos lo siguiente:

![Imagen 7](images/7.png)

## Despliegue de una nueva aplicación

Ahora desplegaremos una aplicación ya creada. Clonamos el repositorio a nuestra máquina e instalamos las librerias:

![Imagen 8](images/8.png)

Por último iniciamos la aplicación

![Imagen 9](images/9.png)

Como vemos nos ha soltado un error "sh: 1: nodemo: not found. Para solucionarlo debemos installar nodemon:

![Imagen 10](images/10.png)

E iniciamos de nuevo:

![Imagen 11](images/11.png)

Ahora podremos visualizar lo sigueinte en nuestro navegador:

![Imagen 12](images/12.png)

# PRÁCTICA 3.4: DESPLIEGUE DE UNA APLICACIÓN REACT EN NETLIFY (PaaS)

Nos logueamos con ssh en nuestra máquina debian

## Creación de nuestra aplicación

Creamos un directorio con 3 archivos: head.html, tail.html y aplicacion.js. Dentro del directorio creamos nuestra aplicación Node.js. Ejecutamos node aplicacion.js para ver que funciona correctamente:

![Imagen 16](images/16.png)

![Imagen 17](images/17.png)

![Imagen 18](images/18.png)

![Imagen 13](images/13.png)


![Imagen 15](images/15.png)

## Aplicación para Netlify

En primer lugar nos clonamos una aplicación creada con React a nuestra máquina:

![Imagen 19](images/19.png)

## Proceso de despliegue en Netlify

Antes de nada me he creado una cuenta en Netlify sin enlazar mi github.
Y a continuación instalamos el CLI de Netlify:

![Imagen 20](images/20.png)

Desde la página de Netlify generamos un token que añadimos nuestra máquina:

![Imagen 21](images/21.png)

Y a continuación nos logueamos:

![Imagen 22](images/22.png)

Como antes instalamos las dependencias y lo ejecutamos de la siguiente forma:

![Imagen 23](images/23.png)

Y lo desplegamos:

![Imagen 24](images/24.png)


![Imagen 25](images/25.png)

Ya desplegado, iremos al navegador e introduciremos la url que nos ha proporcionado:

![Imagen 26](images/26.png)

## Despliegue mediante conexión con Github.

Eliminamos el proyecto anterior tanto en local como en el servicio de Netlify:

![Imagen 27](images/27.png)

Creamos un repositorio en GitHub:

![Imagen 28](images/28.png)

Descargamos un repositorio de GitHub:

![Imagen 29](images/29.png)

Lo descomprimimos en nuestro directorio:

![Imagen 30](images/30.png)

Y a continuación enlazamos el repositorio local con el que acabamos de crear en github y hacemos un push del contenido de este:

![Imagen 31](images/31.png)


![Imagen 32](images/32.png)

Ahora desde la página de Netlify, enlazamos nuestra cuenta de GitHub, seleccionamos nuestro repositorio y lo desplegamos:

![Imagen 33](images/33.png)


![Imagen 34](images/34.png)

Ya desplegado, vamos a hacer un commit en nuestro repositorio de github y comprobaremos que se despliega el cambio automáticamente en Netlify. Para esto modificaremos el contenido del archivo robots.txt, donde añadiremos una carpeta con nuestro nombre:

![Imagen 35](images/35.png)

Ahora comprobamos Netlify, y veremos que se ha realizado un cambio con la fecha en la que hemos hecho el push del commit:

![Imagen 36](images/36.png)


![Imagen 37](images/37.png)

Y si nos dirigimos a la siguiente dirección comprobaremos que, efectivamente, se ha realizado el cambio:

![Imagen 38](images/38.png)
