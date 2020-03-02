# Aplicación Vigilancia Tecnológica - Alertas RSS

Gestión Tecnológica - 2019-3
Integrantes: 
<ol>
<li>Thomas Daniel Avila Blenkey  -  20151020012</li> 
<li>Jonathan Steven Capera Quintana - 20151020001</li> 
<li>Daniel David Leal Lara - 20151020057</li>
</ol>

# Docker RSS

RSS es un formato XML para distribuir contenido en la web. Se utiliza para difundir información actualizada frecuentemente a usuarios que se han suscrito a la fuente de contenidos. RSS es un instrumento de vigilancia tecnológica, específicamente una Alerta, o sea, servicios personalizados de información de actualidad sobre aspectos concretos de un sector o temática.

Esta imagen de docker permite ejecutar el lector de noticias "Tiny Tiny RSS", el cual permite, por medio de una interfaz web, registrarse a una dirección RSS de una organización de interés y recibir actualizaciones de las últimas noticias disponibles.

## Instalación

Es necesario tener instalado docker, por lo tanto si no lo tiene instalado dentro de su maquina y usa ubuntu, es recomendable seguir las siguientes instrucciones: </br>
https://docs.docker.com/install/linux/docker-ce/ubuntu/ </br>

Se inicializa un nuevo contenedor de la base de datos postgres:

```bash
$ docker run -d --name ttrssdb nornagon/postgres
```

Al ser un docker verificado en el índice (https://index.docker.io/u/clue/ttrss/) se puede
ejecutar fácilmente iniciando esta instalación de RSS vinculada a la base de datos
creada anteriormente: 

```bash
$ docker run -d --link ttrssdb:db -p 80:80 clue/ttrss
```
Al ejecutar este comando por primera vez se descargará la imagen automáticamente del
índice de imágenes verificadas de docker.
