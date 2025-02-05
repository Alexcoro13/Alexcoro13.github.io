# **Ejercicios de Git y Github**

## **Repositorio DEAW**

1. Crear un repositorio en vuestro Github llamado DEAW

    - Para crear un repositorio en github nos iremos al inicio y haremos clic en new:

    ![Click en new](../../assets/images/Practica5.1/crear-repo.png)

    - Tras esto nos aparecerá la página para crear el repositorio en github

    ![Crear repo 2](../../assets/images/Practica5.1/crear-repo2.png)

2. Clonar vuestro repositorio en local

    - Para clonar nuestro repositorio en local deberemos ejecutar el siguiente comando:

    ```
    git clone (url del repositorio)
    ```

    ![Clonar repositorio](../../assets/images/Practica5.1/clonar-repo.png)


## **README**

1. Crear(si no lo habeís hecho ya) en vuestro repositorio local un documento README.md

	- Para crear un archivo README.md usaremos el siguiente comando:

	```bash
	nano README.md
	```

	Y añadiremos un pequeño texto al mismo.

	![Archivo creado](../../assets/images/Practica5.1/readme-creado.png)

## **Commit Inicial**

1. Realizar un commit inicial con el comentario `Comenzamos con los ejercicios de Git`

	- Para hacer un commit primero necesitamos añadir los archivos a los que queramos incluir
	en el commit.

	```
	git add README.md
	```

	- Y así habremos preparado el archivo el README.md para el commit.

	```
	git commit -m "Comenzamos con los ejercicios de Git
	```

	![Primer commit](../../assets/images/Practica5.1/1er-commit.png)

## **Push inicial**

1. Subir los cambios al repositorio remoto

	```
	git push
	```
	
	![Push Inicial](../../assets/images/Practica5.1/primer-push.png)

## **Ignorar archivos**

1. Crear en el repositorio local un fichero llamado privado.txt.
	- Crearemos el fichero con `nano` y lo dejaremos vacio

	![Creación archivo privado](../../assets/images/Practica5.1/privado.txt.png)

2. Crear en el repositorio local una carpeta llamada privada.

	- Y para crear la carpeta lo haremos con `mkdir`

	![Creación carpeta privada](../../assets/images/Practica5.1/privada-carpeta.png)

3. Realizar los cambios oportunos para que tanto el archivo como la carpeta sean ignorados por git.

	- Una vez que tenemos los archivos creados necesitaremos crear un archivo llamado `.gitignore` 
	en donde incluiremos los archivos y directorios anteriores para excluirlos.

	![Gitignore](../../assets/images/Practica5.1/gitignore.png)

## **Añadir fichero 1.txt**

1. Añadir fichero `1.txt` al repositorio local.

	- Ahora creamos el archivo y lo añadimos con git add

	```
	git add 1.txt
	```

	![Añadir fichero 1.txt](../../assets/images/Practica5.1/Añadir-fichero-1.txt.png)

## **Crear el tag v0.1**

1. Crea un tag llamado **v0.1**

	```
	git tag V0.1
	```

	![Crear tag v0.1](../../assets/images/Practica5.1/crear-tag.png)

## **Subir el tag v0.1**

1. Subir los cambios al repositorio remoto.

	- Para subir el tag v0.1 usaremos el siguiente comando

	```
	git push --tags
	```

	![Subir tag](../../assets/images/Practica5.1/subir-tag.png)


## **Cuenta de github**

1. Poner una foto en vuestro perfil de GitHub

	- Para cambiar la foto de perfil deberemos ir a configuración de github y hacer click en cambiar foto

	![Foto sin cambiar](../../assets/images/Practica5.1/foto-sin-cambiar.png)

	Y como podemos ver ya hemos cambiado la foto

	![Foto cambiada](../../assets/images/Practica5.1/foto-cambiada.png)


2. Poner el doble factor de autentificación en vuestra cuenta de Github

	- Para añadir el doble factor de autentificación deberemos irnos al apartado de 
	contraseñas y autenticación, en donde añadiremos los metodos de auteticación de doble factor que queramos.

	![alt text](../../assets/images/Practica5.1/doble-factor.png)

## **Uso social de github**

1. Preguntar los nombres de usuario de GitHub de 2 de tus compañeros de clase, búscalos, y sigueles.

	- Buscamos los usuarios y le damos a seguir:

	![Alexcoro](../../assets/images/Practica5.1/Alexcorox.png)

	![Albluq22](../../assets/images/Practica5.1/Albluq22.png)

2. Seguir los repositorios DEAW del resto de tus compañeros.

	- Dentro del repositorio, le daremos a watch all activity y ya estaremos 
	siguiendo el repositorio

	![Seguir repositorio](../../assets/images/Practica5.1/seguir-repositorio.png)

	Y para seguir al resto seria igual.

3. Añadir una estrella a los repositorios DEAW del resto de tus compañeros.

	- Para dar un estrella haremos clic en star y así habremos dado una estrella

	![Estrella](../../assets/images/Practica5.1/estrella.png)


## **Crear una tabla**

1. Crear una tabla en el fichero README.md con la información de varios de tus compañeros de clase:

	![Tabla](../../assets/images/Practica5.1/tabla.png)

## **Colaboradores**

1. Poner a un compañero como colaborador en el repositorio **DEAW**

	- Para añadir un colaborador deberemos ir a `settings` dentro del repositorio.
	Una vez dentro iremos a colaboradores y haremos clic en añadir personas

	![Añadir colaboradores](../../assets/images/Practica5.1/colaboradores.png)

	![Añadir colaboradores](../../assets/images/Practica5.1/añadir-colaborador.png)

	![Colaborador añadido](../../assets/images/Practica5.1/colaborador-añadido.png)

## **Crear una rama v0.2**

1. Crear una rama `v0.2`.

	- Para crear una rama nueva lo haremos con la siguiente rama

	```
	git branch v0.2
	```

2. Posiciona tu carpeta de trabajo en esta rama.

	!!! warning "Atención"
		Antes de hacer un cambio de rama deberemos tener todos los cambios 
		confirmados en el repositorio.

	- Para cambiar de rama deberemos usar el siguiente comando:

	```
	git checkout nombre_rama
	```

	![Cambio a v0.2](../../assets/images/Practica5.1/cambio-v0.2.png)

## **Añadir fichero 2.txt**

1. Añadir un fichero 2.txt en la rama v0.2

	![2.txt](../../assets/images/Practica5.1/crear-2.txt.png)

## **Crear rama remota v0.2**

1. Subir los cambios al repositorio remoto

	- Para subir la rama v0.2 usaremos el siguiente comando.

	```
	git push --set-upstream origin v0.2
	```

	![Subir cambios v0.2](../../assets/images/Practica5.1/subir-cambios-v0.2.png)

## **Merge directo**

1. Posicionarse en la rama `main`
2. Hacer un merge de la rama v0.2 en la rama master

	![Mege sin conflicto](../../assets/images/Practica5.1/merge-sin-conflicto.png)

## **Merge con conflicto**

1. En la rama `master` poner `Hola` en el fichero `1.txt` y hacer commit
	![Cambios 1.txt](../../assets/images/Practica5.1/cambios-en-main.png)

2. Posicionarse en la rama v0.2 y poner Adios en el fichero "1.txt" y hacer commit.
	![Cambios v0.2](../../assets/images/Practica5.1/cambio-v0.2.png)

3. Posicionarse de nuevo en la rama master y hacer un merge con la rama v0.2

	- Una vez que hemos hecho los cambios en cada rama hacemos un merge y nos indicara que hay un conflicto.

	![mege-conflicto](../../assets/images/Practica5.1/merge-conflicto.png)

	- Para resolverlo nos iremos al archivo y nos quedaremos con los cambios de la rama que queramos	

	![resolver-cambios](../../assets/images/Practica5.1/resolver-cambios.png)

	![Resolver cambios](../../assets/images/Practica5.1/resolver-cambios2.png)

	- Una vez que hemos dejado el archivo con los cambios correctos y realizamos un commit

	![Cambios confirmados](../../assets/images/Practica5.1/merge-conflictivo-exitoso.png)

## **Listado de ramas**

1. Listar las ramas con merge y las ramas sin merge.

	- Para listar las ramas con merge usaremos el siguiente comando:

	```
	git branch --merged
	```

	- Para listar las ramas sin merge usaremos el siguiente comando:

	```
	git branch --no-merged
	```

	![Listar ramas](../../assets/images/Practica5.1/listar-ramas.png)

## **Arreglar conflicto**

	- El conflicto anterior ha sido arreglado en el 3 apartado de `Merge con conflicto`

## **Borrar rama**

1. Crear un tag v0.2
2. Borrar la rama v0.2

	![Borrar rama v0.2 y tag v0.2 ](../../assets/images/Practica5.1/crear-tag02-borrar-rama.png)

## **Listado de cambios**

1. Listar los distintos commits con sus ramas y sus tags.

	- Para listar los cambios usaremos el comando:

	```
	git log --oneline --graph --decorate --all
	```

	- Y nos mostrará algo así

	![Listado de cambios](../../assets/images/Practica5.1/listado-de-cambios.png)