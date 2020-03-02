# Aplicación Vigilancia Tecnológica - RSS

Gestión Tecnológica - 2019-3
Integrantes: 
<ol>
<li>Thomas Daniel Avila Blenkey  -  20151020012</li> 
<li>Jonathan Steven Capera Quintana - 20151020001</li> 
<li>Daniel David Leal Lara - 20151020057</li>
</ol>

Es necesario tener instalado docker, por lo tanto si no lo tiene instalado dentro de su maquina y usa ubuntu, es recomendable seguir las siguientes instrucciones: </br>
https://docs.docker.com/install/linux/docker-ce/ubuntu/ </br>

</br>
</br>
Para ejecutar la aplicación dockerizada es necesario seguir los siguientes pasos dentro de la terminal:
<ol>

# docker-ttrss

Esta imagen de docker permite ejecutar el lector de noticias "Tiny Tiny RSS"
This [Docker](https://www.docker.com) image allows you to run the [Tiny Tiny RSS](http://tt-rss.org) feed reader.
Keep your feed history to yourself and access your RSS and atom feeds from everywhere.
You can access it through an easy to use webinterface on your desktop, your mobile browser
or using one of the available apps.

## About Tiny Tiny RSS

> *From [the official readme](http://tt-rss.org/redmine/projects/tt-rss/wiki):*

Tiny Tiny RSS is an open source web-based news feed (RSS/Atom) reader and aggregator,
designed to allow you to read news from any location,
while feeling as close to a real desktop application as possible.

![](http://tt-rss.org/images/1.9/1.jpg)

## INSTALACIÓN

Primero se inicializa un nuevo contenedor de la base de datos postgres:

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
