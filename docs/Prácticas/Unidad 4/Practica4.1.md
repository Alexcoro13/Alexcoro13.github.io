# **Práctica 4.1 - Configuración de un servidor DNS**


## **Instalación de servidor DNS**

Para esta práctica usaremos Bind una herramienta de software libre que se distribuye con la mayoria de plataformas Unix y Linux.
La version que usaremos será Bind9 la cual es la versión recomendada para usarse y es la que usaremos.

Para instalar el servidor DNS, usaremos el siguiente comando:

```
sudo apt-get install bind9 bind9utils bind9-doc 
```

## **Configuración del servidor**

En esta práctica solo usuaremos IPv4, por lo tanto debemos indícarselo a Bind, para esto deberemos irnos al su archivo general de Configuración.
Este archivo se encuentra en el siguiente directorio:

```
/etc/default/named
```

Y una vez que estemos dentro editandolo con `nano` debemos modificar siguiente línea:

```
OPTIONS = "-u bind -4"
```

![Imagen de configuracion ipv4](../../assets/images/Practica4.1/ipv4-bind.png)

A continuación nos dirigiremos al archivo principal de configuración `named.conf` el cual está en el directorio


```
/etc/bind
```

Y al consultarlo deberá salir lo siguiente:

![Imagen configuracion de bind](../../assets/images/Practica4.1/cat-namedconf.png)

Este archivo sirve para agrupar los diferentes directorios de configuración que usaremos a lo largo de práctica.

## **Configuración named.conf.options**

Acontinuación realizaremos una copia de seguridad del archivo `named.conf.options` antes de editarlo a nuestro gusto

```
sudo cp /etc/bind/named.conf.options /etc/bind/named.conf.options.backup
```

![alt text](../../assets/images/Practica4.1/copia-seguridad.png)

Una vez que hemos hecho la copia de seguridad del archivo
editaremos el archivo `named.conf.options` e incluiremos los siguientes contenidos:

- Por razones de seguridad, incluiremos una lista de acceso para que sólo puedan acceder ip's 
autorizadas a ello, es decir vamos a limitar el acceso a nuestro servidor DNS.

Para esto, crearemos un boque con los host autorizados que seran los de la red `192.168.X.0/24` (la X depende de nuesra red). El bloque
de configuracion deberia de quedarnos algo así

```
acl confiables{
  192.168.X.0/24;
}
```

![Configuracion Hosts autorizados](../../assets/images/Practica4.1/hosts-autorizados.png)

Tras realizar esta configuración, nos daremós cuenta que el servidor ya viene configurado para ser un DNS cache. 
```/var/cache/bind``` es donde se guardaran las zonas.

Por lo tanto realizaremos las siguiente configuraciones.

- Que sólo se permitan consultas recursivas a los host autorizados
- No permitir la transferencia de zonas.
- Configurar el servidor para que escuche consultas DNS en el puerto 53(puerto por defecto) y en la IP de la maquina virtual.
- Además, comentaremos la línea que pone `listen-on-v6`{ any; };` puesto que no vamos a responder a consultas de IPV6

![Configuracion extra](../../assets/images/Practica4.1/configuracion-2.png)

Ahora comprobaremos si nuestra configuración es correcta con el comando:

```
sudo named-checkconf
```

![comprobacion configuracion](../../assets/images/Practica4.1/comprobacion-configuracion.png)

Si hay algun error, nos saldra si no nos devolvera la linea de comandos limpia,

Reiniciamos el servidor y comprobamos sus estado.

![Reinicio de servidor](../../assets/images/Practica4.1/estado-servidor.png)

