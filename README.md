# nginx

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

[key]: http://nginx.org/keys/nginx_signing.key