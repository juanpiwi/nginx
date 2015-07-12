# nginx

Nginx tiene un proceso maestro y varios procesos de trabajo. El propósito principal del proceso principal es a leer y evaluar configuración, y mantener los procesos de trabajo. Los procesos de trabajo hacen procesamiento real de solicitudes. nginx emplea mecanismos de modelo y sistema operativo dependiente basado en eventos para distribuir eficientemente las solicitudes entre los procesos de trabajo. El número de procesos de trabajo se define en el archivo de configuración y puede fijarse para una configuración determinada o automáticamente ajusta al número de núcleos de CPU disponibles (ver [worker_processes]).

## Instalación (Ubuntu)

1. Para autentificar la firma de repositorio ngnix y eliminar advertencia de falta de clave PGP durante la instalación,
es necesario añadir la firma. Para ello se debe descargar la clave desde [key] y se debe agregar con el siguiente comando:

```sh
$ sudo apt-key add nginx_signing.key
``` 

2. Añadir a sources.list las siguientes lineas:

```sh
deb http://nginx.org/packages/ubuntu/ codename nginx
deb-src http://nginx.org/packages/ubuntu/ codename nginx
```

3. Ejecutar los siguientes comandos:

```sh
$ apt-get update
$ apt-get install nginx
```

## Configuración

El archivo de configuración **nginx.conf** se encuentra en el directorio  */etc/nginx*

### Starting, Stopping, and Reloading Configuration

```sh
nginx -s signal
```

Donde *signal* son alguna de la siguientes:

- stop
- quit 
- reload 
- reopen 

Lista de procesos que ejecuta nginx

```sh
ps -ax | grep nginx
```




[key]: http://nginx.org/keys/nginx_signing.key
[worker_processes]: http://nginx.org/en/docs/ngx_core_module.html#worker_processes