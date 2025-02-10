# **Práctica 5.1 - Ejercicios de Git y Github**

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

# **Ejercicios Git y Github II**

## **Ejercicios de creación y actualización de repositorios**

## **Ejercio 1**

1. Configurar Git definiendo el nombre del usuario, el correo electrónico y activar el coloreado de salida.

	- Para configurar el nombre de usuario usaremos el comando:

	```
	git config user.name nombre_usuario
	```

	- Para configurar el email de usuario usaremos el comando:

	```
	git config user.email email_usuario
	```

	- Y por último configuraremos el coloreado de salida.

	```
	git config color.ui auto
	```

	![Configuración de git](../../assets/images/Practica5.1/Configuracion-git.png)

## **Ejercicio 2**

1. Crear un repositorio nuevo con el nombre libro y mostrar su contenido

	- Usaremos los siguientes comandos para crear el repositorio libro:

	```
	mkdir libro
	cd libro
	git init
	```

	![Contenido del repositorio libro](../../assets/images/Practica5.1/contenido-libro.png)

## **Ejercicio 3**

1. Comprobar el estado del repositorio.

	- Como hemos podido ver en la anterior captura el repositorio esta vácio

2. Crear un fichero indice.txt con el siguiente contenido:

	![Indice.txt](../../assets/images/Practica5.1/indice.txt.png)

3. Comprobar de nuevo el estado del repositorio.

	```
	git status
	```

	![Estado Repositorio](../../assets/images/Practica5.1/estado_repositorio.png)

4. Añadir el fichero a la zona de intercambio temporal.

 	```
	git add indice.txt
	```

5. Volver a comprobar una vez más el estado del repositorio.

	![Comrpobar estado 2](../../assets/images/Practica5.1/comprobar-estado.png)

## **Ejercicio 4**

1. Realizar un commit de los últimos cambios con el mensaje “Añadido índice del libro.” y ver el estado del repositorio.

	```
	git commit -m "Añadido índice del libro"
	```

## **Ejercicio 5**

1. Cambiar el fichero indice.txt para que contega lo siguiente:


2. Mostrar los cambios con respecto a la última versión guardada en el repositorio.

	```
	git diff indice.txt
	```

	![Diferencia de indice](../../assets/images/Practica5.1/diferencias-indice.png)

3. Hacer un commit de los cambios con el mensaje "Añadido capítulo 3 sobre gestión de ramas"

	![Commit diff](../../assets/images/Practica5.1/Commit-diff.png)

## **Ejercicio 6**

1. Mostrar los cambios de la última versión del repositorio con respecto a la anterior.

	```
	git diff HEAD~1 HEAD
	```

	![diff commits](../../assets/images/Practica5.1/diff-commits.png)

2. Cambiar el mensaje del último cmmit por "Añadido capitulo 3 sobre gestion de ramas al indice"

	```
	git commit --amend -m "Añadido capítulo 3 sobre gestión de ramas al índice."
	```
	

	![ammend commit](../../assets/images/Practica5.1/ammend-commits.png)

3. Volver a mostrar los ultimos cambios del repositorio.

	- Esto lo haremos con el mismo comando que en el primer apartado

	![Diff 2](../../assets/images/Practica5.1/diff2.png)

## **Ejercicios de manejo del historial de cambios**

## **Ejercicio 1**

1. Mostrar el historial de cambios del repositorio.

	- Para mostrar el historial de cambios del repositorio lo haremos con el siguiente comando

	```
	git log
	```

	![Imagen del historial del repositorio](../../assets/images/Practica5.1/log-repo.png)

2. Crear la carpeta capitulos y crear dentro de ella el fichero capitulo1.txt con el siguiente texto.

	`El flujo de trabajo básico con Git consiste en: 1- Hacer cambios en el repositorio. 2- Añadir los cambios a la zona de intercambio temporal. 3- Hacer un commit de los cambios.`

	![Imagen del capitulo](../../assets/images/Practica5.1/creacion-carpeta-capitulo.png)

3. Añadir los cambios a la zona de intercambio temporal.

	![Añadir capitulo](../../assets/images/Practica5.1/añadir-capitulo.png)

4. Hacer un commit de los cambios con el mensaje "Añadido capítulo 1." Volver a mostrar de cambios del repositorio.

	![Log capitulo](../../assets/images/Practica5.1/log-capitulo.png)

## **Ejercicio 2**

1. Crear el fichero `capitulo2.txt` en la carpeta capitulos con el siguiente texto.

	`El flujo de trabajo básico con Git consiste en: 1- Hacer cambios en el repositorio. 2- Añadir los cambios a la zona de intercambio temporal. 3- Hacer un commit de los cambios.`

	![Capitulo 2.txt](../../assets/images/Practica5.1/capitulo2.png)

2. Añadir los cambios a la zona de intercambio temporal.

	![Capitulo2.txt add](../../assets/images/Practica5.1/add-capitulo2.png)

3. Hacer un commit de los cambios con el mensaje “Añadido capítulo 2.”

	![Capitulo2.txt commit](../../assets/images/Practica5.1/commit-capitulo.png)

4. Mostrar las diferencias entre la última versión y dos versiones anteriores.

	- Para mostrar las diferencias entre la última versión y dos versiones anteriores lo haremos con el siguiente comando:

	```
	git diff HEAD~2 HEAD
	```

	![Diferencia con los 2 commits anteriores](../../assets/images/Practica5.1/diferencia-2-commits.png)

## **Ejercicio 3**

1. Crear el fichero capitulo3.txt en la carpeta capitulos con el siguiente texto.

	`	Git permite la creación de ramas lo que permite tener distintas versiones del mismo proyecto y trabajar de manera simultanea en ellas.`

	![Capitulo 3](../../assets/images/Practica5.1/capitulo3.png)

2. Añadir los cambios a la zona de intercambio temporal.

	![Status Capitulo3](../../assets/images/Practica5.1/Status-Capitulo3.png)

3. Hacer un commit de los cambios con el mensaje “Añadido capítulo 3.”

	![Commit capitulo3](../../assets/images/Practica5.1/commit-capitulo3.png)

4. Mostrar las diferencias entre la primera y la última versión del repositorio.

	- Para hacer esto necesitamos primero tenemos que saber el ID del primer commit:

	```
	git log
	```

	![Id primer commit](../../assets/images/Practica5.1/id-primer-commit.png)

	- Y el id que vemos a la izquierda es el id de cada commit en este caso el numero 1 es `f09939b`.

	- Ahora hacemos la diferencia con este comando:

	```
	git diff f09939b HEAD
	```

	![Diff primer commit](../../assets/images/Practica5.1/diff-primer-commit.png)

## **Ejercicio 4**

1. Añadir al final del fichero `indice.txt` la siguiente línea:

	`Capítulo 5: Conceptos avanzados`

	![indice.txt-capitulo5](../../assets/images/Practica5.1/indice.txt-capitulo.png)

2. Añadir los cambios a la zona de intercambio temporal.

	![Git status](../../assets/images/Practica5.1/git-status-indice.png)

3. Hacer un commit de los cambios con el mensaje “Añadido capítulo 5 al índice.”.

	![Commit indice capitulo5](../../assets/images/Practica5.1/commit-capitulo5-indice.png)

4. Mostrar quién ha hecho cambios sobre el fichero `indice.txt`.

	- Para mostrar quién ha hecho los cambios usaremos

	```
	git blame indice.txt
	```

	![Git blame](../../assets/images/Practica5.1/blame-indice.png)

## **Ejercicios de deshacer cambios**

## **Ejercicio 1**

Eliminar la última línea del fichero indice.txt y guardarlo.

Comprobar el estado del repositorio.

Deshacer los cambios realizados en el fichero indice.txt para volver a la versión anterior del fichero.

Volver a comprobar el estado del repositorio.