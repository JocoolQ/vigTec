# 21
Aplicación de herramientas de automatización para pruebas de comportamiento a partir de cucumber

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

## Quickstart

This section assumes you want to get started quickly, the following sections explain the
steps in more detail. So let's start.

Just start up a new database container:

```bash
$ docker run -d --name ttrssdb nornagon/postgres
```

And because this docker image is available as a [trusted build on the docker index](https://index.docker.io/u/clue/ttrss/),
using it is as simple as launching this Tiny Tiny RSS installation linked to your fresh database:

```bash
$ docker run -d --link ttrssdb:db -p 80:80 clue/ttrss
```

Running this command for the first time will download the image automatically.
