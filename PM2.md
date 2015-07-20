# PM2

Gestor de procesos de producción de Node.js / io.js

## Instalación (Ubuntu)

```sh
$ sudo npm install pm2 -g
```

## Script de inicio (Ubuntu) --- Startup script generation

```sh
$ pm2 startup ubuntu
```

## Start an application

```sh
$ pm2 start [app.js] --name [example]
```

## Save process list

```sh
$ pm2 save
```

## Gestión de procesos

```sh
$ pm2 stop     <app_name|id|'all'|json_conf>
$ pm2 restart  <app_name|id|'all'|json_conf>
$ pm2 delete   <app_name|id|'all'|json_conf>
```

## Listado de procesos

```sh
$ pm2 list
```

## Monitoreo de procesos

```sh
$ pm2 monit
```

## Descripción de procesos

```sh
$ pm2 describe [id|name]
```