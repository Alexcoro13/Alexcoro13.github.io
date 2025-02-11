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

1. Crear(si no lo habeis hecho ya) en vuestro repositorio local un documento README.md

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
	- Crearemos el fichero con `nano` y lo dejaremos vacío

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

	- Para cambiar la foto de perfil deberemos ir a configuración de github y hacer clic en cambiar foto

	![Foto sin cambiar](../../assets/images/Practica5.1/foto-sin-cambiar.png)

	Y como podemos ver ya hemos cambiado la foto

	![Foto cambiada](../../assets/images/Practica5.1/foto-cambiada.png)


2. Poner el doble factor de autentificación en vuestra cuenta de Github

	- Para añadir el doble factor de autentificación deberemos irnos al apartado de 
	contraseñas y autenticación, en donde añadiremos los métodos de autenticación de doble factor que queramos.

	![alt text](../../assets/images/Practica5.1/doble-factor.png)

## **Uso social de github**

1. Preguntar los nombres de usuario de GitHub de 2 de tus compañeros de clase, búscalos, y síguelos.

	- Buscamos los usuarios y le damos a seguir:

	![Alexcoro](../../assets/images/Practica5.1/Alexcorox.png)

	![Albluq22](../../assets/images/Practica5.1/Albluq22.png)

2. Seguir los repositorios DEAW del resto de tus compañeros.

	- Dentro del repositorio, le daremos a watch all activity y ya estaremos 
	siguiendo el repositorio

	![Seguir repositorio](../../assets/images/Practica5.1/seguir-repositorio.png)

	Y para seguir al resto seria igual.

3. Añadir una estrella a los repositorios DEAW del resto de tus compañeros.

	- Para dar una estrella haremos clic en star y así habremos dado una estrella

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

	![Merge sin conflicto](../../assets/images/Practica5.1/merge-sin-conflicto.png)

## **Merge con conflicto**

1. En la rama `master` poner `Hola` en el fichero `1.txt` y hacer commit
	![Cambios 1.txt](../../assets/images/Practica5.1/cambios-en-main.png)

2. Posicionarse en la rama v0.2 y poner Adios en el fichero "1.txt" y hacer commit.
	![Cambios v0.2](../../assets/images/Practica5.1/cambio-v0.2.png)

3. Posicionarse de nuevo en la rama master y hacer un merge con la rama v0.2

	- Una vez que hemos hecho los cambios en cada rama hacemos un merge y nos indicara que hay un conflicto.

	![merge-conflicto](../../assets/images/Practica5.1/merge-conflicto.png)

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

## **Ejercicios Git y Github II**

## **Ejercicios de creación y actualización de repositorios**

## **Ejercicio 1**

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

	- Como hemos podido ver en la anterior captura el repositorio está vacío

2. Crear un fichero `indice.txt` con el siguiente contenido:

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

	![Comprobar estado 2](../../assets/images/Practica5.1/comprobar-estado.png)

## **Ejercicio 4**

1. Realizar un commit de los últimos cambios con el mensaje “Añadido índice del libro.” y ver el estado del repositorio.

	```
	git commit -m "Añadido índice del libro"
	```

## **Ejercicio 5**

1. Cambiar el fichero `indice.txt` para que contenga lo siguiente:


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

2. Cambiar el mensaje del último commit por "Añadido capítulo 3 sobre gestión de ramas al índice"

	```
	git commit --amend -m "Añadido capítulo 3 sobre gestión de ramas al índice."
	```
	

	![ammend commit](../../assets/images/Practica5.1/ammend-commits.png)

3. Volver a mostrar los últimos cambios del repositorio.

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

2. Crear la carpeta capítulos y crear dentro de ella el fichero capitulo1.txt con el siguiente texto.

	`El flujo de trabajo básico con Git consiste en: 1- Hacer cambios en el repositorio. 2- Añadir los cambios a la zona de intercambio temporal. 3- Hacer un commit de los cambios.`

	![Imagen del capitulo](../../assets/images/Practica5.1/creacion-carpeta-capitulo.png)

3. Añadir los cambios a la zona de intercambio temporal.

	![Añadir capitulo](../../assets/images/Practica5.1/añadir-capitulo.png)

4. Hacer un commit de los cambios con el mensaje "Añadido capítulo 1." Volver a mostrar de cambios del repositorio.

	![Log capitulo](../../assets/images/Practica5.1/log-capitulo.png)

## **Ejercicio 2**

1. Crear el fichero `capitulo2.txt` en la carpeta capítulos con el siguiente texto.

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

1. Crear el fichero capitulo3.txt en la carpeta capítulos con el siguiente texto.

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

	- Y el ID que vemos a la izquierda es el ID de cada commit en este caso el número 1 es `f09939b`.

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

1. Eliminar la última línea del fichero `indice.txt` y guardarlo.

	![Borrar-UltimaLinea](../../assets/images/Practica5.1/borrar-ultima-linea.png)

2. Comprobar el estado del repositorio.

	![Comprobación de estado](../../assets/images/Practica5.1/comprobar-estado5.png)

3. Deshacer los cambios realizados en el fichero `indice.txt` para volver a la versión anterior del fichero.

	- Para deshacer los cambios usaremos el siguiente comando:

	```
	git restore indice.txt
	```

	![Git restore](../../assets/images/Practica5.1/restore-git.png)

4. Volver a comprobar el estado del repositorio.

	![Comprobar estado 6](../../assets/images/Practica5.1/Comprobar-Estado-6.png)

## **Ejercicio 2**

1. Eliminar la última línea del fichero `indice.txt` y guardarlo.

	![Borrar-ultima linea Indice](../../assets/images/Practica5.1/Borrar-Ultima-LineaIndice.png)

2. Añadir los cambios a la zona de intercambio temporal.

3. Comprobar de nuevo el estado del repositorio.

	![Comprobar estado 7](../../assets/images/Practica5.1/comprobar-estado7.png)

4. Quitar los cambios de la zona de intercambio temporal, pero mantenerlos en el directorio de trabajo.

	- Para quitar los cambios de la zona de intercambio, pero mantenerlos en el directorio de trabajo usaremos el siguiente comando:

	![Git reset](../../assets/images/Practica5.1/git-reset.png)

5. Comprobar de nuevo el estado del repositorio.

	![Comprobar estado 5](../../assets/images/Practica5.1/Comprobar%20estado%205.png)

6. Deshacer los cambios realizados en el fichero `indice.txt` para volver a la versión anterior del fichero.

	```
	git restore indice.txt
	```

7. Volver a comprobar el estado del repositorio.

	![Deshacer cambios](../../assets/images/Practica5.1/deshacer-cambios.png)

## **Ejercicio 3**

1. Eliminar la última línea del fichero `indice.txt` y guardarlo.

	![Borrar última línea de índice](../../assets/images/Practica5.1/borrar-ultima.png)

2. Eliminar el fichero `capitulos/capitulo3.txt`.

3. Añadir un fichero nuevo `capitulos/capitulo4.txt` vacío.

4. Añadir los cambios a la zona de intercambio temporal.

5. Comprobar de nuevo el estado del repositorio.

	![Estado repo ejercicio 3](../../assets/images/Practica5.1/Estado-repo-ejercicio3.png)

6. Quitar los cambios de la zona de intercambio temporal, pero mantenerlos en el directorio de trabajo.

	- Para hacer esto usaremos los siguientes comandos:

	```git
	git restore --staged indice.txt
	git restore --staged capitulos/capitulo4.txt
	git restore --staged capitulos/capitulo3.txt
	```

	![Restore Ejercicio 3](../../assets/images/Practica5.1/restore-ejercicio3.png)

7. Comprobar de nuevo el estado del repositorio.

8. Deshacer los cambios realizados para volver a la versión del repositorio.

	- Aquí usaremos el mismo comando que en el apartado 6 pero sin la opción `--staged`. Y para deshacer los cambios del capitulo4 usaremos este comando.

	```
	rm capitulos/capitulo4.txt
	```

	- Usamos rm en vez de git rm o restore, porque este archivo no está guardado en ningún commit de git.

9. Volver a comprobar el estado del repositorio.

	![Estado git ejercicio3](../../assets/images/Practica5.1/estado-ejercicio3.png)

## **Ejercicio 4**

1. Eliminar la última línea del fichero `indice.txt` y guardarlo.

	![Borrar ejercicio 4](../../assets/images/Practica5.1/Borrar-Ejercicio4.png)

2. Eliminar el fichero `capitulos/capitulo3.txt`.

	```
	rm capitulos/capitulo3.txt
	```

	![Estado ejercicio 4 1](../../assets/images/Practica5.1/status-ej4-1.png)

3. Añadir los cambios a la zona de intercambio temporal y hacer un commit con el mensaje “Borrado accidental.”

	![Borrado Accidental](../../assets/images/Practica5.1/commit-borrado-accidental.png)

4. Comprobar el historial del repositorio.

	![Log ej4](../../assets/images/Practica5.1/Log-Ej4.png)

5. Deshacer el último commit pero mantener los cambios anteriores en el directorio de trabajo y la zona de intercambio temporal.

	- Para mantener los cambios y borrar el commit, deberemos usar el siguiente comando:

	```
	git reset --soft HEAD~1
	```

	- El parámetro soft nos permite mantener los cambios y solo deshace el commit.

	![Reset soft](../../assets/images/Practica5.1/soft-reset.png)

6. Comprobar el historial y el estado del repositorio.

	![Log 2 ej4](../../assets/images/Practica5.1/log2-ej4.png)

7. Volver a hacer el commit con el mismo mensaje de antes.

	![Borrado accidental2](../../assets/images/Practica5.1/borrado-accidental2.png)

8. Deshacer el último commit y los cambios anteriores del directorio de trabajo volviendo a la versión anterior del repositorio.

	- Ahora usaremos el parámetro `--hard`en vez de `--soft` para que el directorio vuelve a estar como el último commit antes de borrado accidental.

	```
	git reset --hard HEAD~1
	```

	![Hard reset](../../assets/images/Practica5.1/reset-hard.png)

9. Comprobar de nuevo el historial y el estado del repositorio.

	![Log ejercicio 4 2](../../assets/images/Practica5.1/log-ej4-2.png)

## **Ejercicios de gestión de ramas**

## **Ejercicio 1**

1. Crear una nueva rama bibliografía y mostrar las ramas del repositorio.

	-	Para crear una usaremos el comando `git branch` como se muestra abajo

	```
	git branch bibliografia
	```

	- Y para mostrar las ramas actuales usaremos:

	```
	git branch
	```


	![Rama bibliografia](../../assets/images/Practica5.1/rama-bibliografia.png)

## **Ejercicio 2**

1. Crear el fichero `capitulos/capitulo4.txt` y añadir el texto siguiente

	`En este capítulo veremos cómo usar GitHub para alojar repositorios en remoto.`

3. Añadir los cambios a la zona de intercambio temporal.

	![EJ1-ramas.1](../../assets/images/Practica5.1/Ej1-ramas.1.png)

4. Hacer un commit con el mensaje “Añadido capítulo 4.”

5. Mostrar la historia del repositorio incluyendo todas las ramas.

	- Para que en log salgan todas las ramas deberemos usar el parámetro `--all`.

	```
	git log --all
	```

	![Ejercicio 1 ramas 2](../../assets/images/Practica5.1/Ej1-ramas.2.png)

## **Ejercicio 3**

1. Cambiar a la rama bibliografía.

	- Para cambiar a la rama bibliografía lo haremos con `git checkout`

	!!! warning "Aviso"
		Para cambiar de rama deberemos tener todos los cambios confirmados en el repositorio, si no podrían ocurrir errores.

	```
	git checkout bibliografia
	```

2. Crear el fichero `bibliografia.txt` y añadir la siguiente referencia

`Chacon, S. and Straub, B. Pro Git. Apress.`

4. Añadir los cambios a la zona de intercambio temporal.

5. Hacer un commit con el mensaje “Añadida primera referencia bibliográfica.”

	![Ej3 ramas 1](../../assets/images/Practica5.1/Ej3-ramas.1.png)

6. Mostrar la historia del repositorio incluyendo todas las ramas.

	![Ej 3 ramas 2](../../assets/images/Practica5.1/Ej3-ramas.2.png)

## **Ejercicio 4**

1. Fusionar la rama bibliografía con la rama master.

	- Para fusionar la rama bibliografía con la rama master primero debemos de situarnos en la rama master y luego hacer un `merge` 

	- Para cambiarnos de rama usaremos `git checkout` como anteriormente

	![Merge rama bibliografía](../../assets/images/Practica5.1/Ej4-ramas.1.png)

2. Mostrar la historia del repositorio incluyendo todas las ramas.

	![Log ejercicio 4](../../assets/images/Practica5.1/Ej4-ramas.2.png)


3. Eliminar la rama bibliografía.

	- Para borrar la rama bibliografía usaremos el siguiente comando

	```
	git branch -d bibliografia
	```

	![Log Ejercicio 4](../../assets/images/Practica5.1/Ej4-ramas.3.png)

4. Mostrar de nuevo la historia del repositorio incluyendo todas las ramas.
	
	![Log ejercicio4](../../assets/images/Practica5.1/Ei4-ramas.4.png)

## **Ejercicio 5**

1. Crear la rama bibliografía.

2. Cambiar a la rama bibliografía.

3. Cambiar el fichero `bibliografia.txt` para que contenga las siguientes referencias:

	```
	Scott Chacon and Ben Straub. Pro Git. Apress.
	Ryan Hodson. Ry’s Git Tutorial. Smashwords (2014)
	```

5. Añadir los cambios a la zona de intercambio temporal y hacer un commit con el mensaje “Añadida nueva referencia bibliográfica.”

	![Ej5 ramas 1](../../assets/images/Practica5.1/Ej5-ramas.1.png)

6. Cambiar a la rama master.

7. Cambiar el fichero `bibliografia.txt` para que contenga las siguientes referencias:

```
Chacon, S. and Straub, B. Pro Git. Apress.
Loeliger, J. and McCullough, M. Version control with Git. O’Reilly.
```

9. Añadir los cambios a la zona de intercambio temporal y hacer un commit con el mensaje “Añadida nueva referencia bibliográfica.”

	![Ej5 ramas 2](../../assets/images/Practica5.1/Ej5%20ramas%202.png)

10. Fusionar la rama bibliografía con la rama master.



11. Resolver el conflicto dejando el fichero `bibliografia.txt` con las referencias:

```
Chacon, S. and Straub, B. Pro Git. Apress.
Loeliger, J. and McCullough, M. Version control with Git. O’Reilly.
Hodson, R. Ry’s Git Tutorial. Smashwords (2014)
```

12. Añadir los cambios a la zona de intercambio temporal y hacer un commit con el mensaje “Resuelto conflicto de bibliografía.”

	![Ej5 ramas 3](../../assets/images/Practica5.1/Ej5-ramas.3.png)

13. Mostrar la historia del repositorio incluyendo todas las ramas.

	![Ej5 ramas 4](../../assets/images/Practica5.1/Ej5-ramas.4.png)

## **Ejercicios de repositorios remotos**

## **Ejercicio 1**

1. Crear un nuevo repositorio público en GitHub con el nombre libro-git.

	![Ej1 remoto 1](../../assets/images/Practica5.1/Ej1-remoto.1.png)

2. Añadirlo al repositorio local del libro.

3. Mostrar todos los repositorios remotos configurados

	![Ej1 remoto 2](../../assets/images/Practica5.1/Ej1-remoto.2.png)

## **Ejercicio 2**

1. Añadir los cambios del repositorio local al repositorio remoto de Github.
	
	- Para submit los cambios a git deberemos usar el siguiente comando:

	```
	git push -u origin master
	```

2. Acceder a Github y comprobar que se han subido los cambios mostrando el historial de versiones.

	- Y como podemos ver, se han subido los cambios

	![Ej5-remoto 1](../../assets/images/Practica5.1/Ej2-remoto.1.png)

## **Ejercicio 3**

1. Colaborar en el repositorio remoto libro-git de otro usuario.

2. Clonar su repositorio libro-git.

	- Para clonar un repositorio usaremos `git clone`

	![Clonar](../../assets/images/Practica5.1/Ej3-remoto.1.png)

3. Añadir el fichero autores.txt que contenga el nombre del usuario y su correo electrónico.

4. Añadir los cambios a la zona de intercambio temporal.

5. Hacer un commit con el mensaje “Añadido autor.”

	![Autores](../../assets/images/Practica5.1/Ej3-remoto.2.png)

6. Subir los cambios al repositorio remoto.

	- Esta vez, como la rama en el remoto ya está creada obviaremos el parámetro `-u` en `git push`

	```
	git push
	```

	![PUSH](../../assets/images/Practica5.1/Ej3-remoto.3.png)

## **Ejercicio 4**

1. Hacer una bifurcación del repositorio remoto `asalber/libro-git` en GitHub.
	
	- Para lograr esto nos iremos al repositorio en github y haremos clic sobre Fork

	![Ejercicio 4](../../assets/images/Practica5.1/Ej4-remoto.1.png)

	![Ejercicio 4](../../assets/images/Practica5.1/Ej4-remoto.2.png)

2. Clonar el repositorio creado en la cuenta de GitHub del usuario.

	```
	git clone https://github.com/Alexcorox/libro-git.git
	```

3. Crear una nueva rama autoría y activarla.

	![Ejercicio 4](../../assets/images/Practica5.1/Ej4-remoto.3.png)

4. Añadir el nombre del usuario y su correo al fichero autores.txt.

5. Añadir los cambios a la zona de intercambio temporal.

6. Hacer un commit con el mensaje “Añadido nuevo autor.”

7. Subir los cambios de la rama autoría al repositorio remoto en GitHub.

	![alt text](../../assets/images/Practica5.1/Ej4-remoto.4.png)

8. Hacer un Pull Request de los cambios en la rama autoría. 

	- Para crear un pull request deberemos ir al apartado pull request dentro de github y haremos clic en `create a pull request`

	![Pull request 1](../../assets/images/Practica5.1/Ej4-remoto.5.png)

	- Seleccionamos las ramas que queremos que compare para hacer el pull request. Y como podemos observar detecta las diferencias que hay entre ellas.

	![Pull request 2](../../assets/images/Practica5.1/Ej4-remoto.6.png)

	- Le asignamos un nombre y le damos a `create pull request`.

	![Pull request 3](../../assets/images/Practica5.1/Ej4-remoto.7.png)

	- Una vez que hayamos completado estos pasos, habremos creado nuestro pull request

	![Pull request 4](../../assets/images/Practica5.1/Ej4-remoto.8.png)
