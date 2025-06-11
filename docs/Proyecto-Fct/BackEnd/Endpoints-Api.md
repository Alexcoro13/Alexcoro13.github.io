# 2. Rutas para peticiónes

Para el sistema de autenticación se ha usado [Laravel Sactum](https://laravel.com/docs/12.x/sanctum) el cual provee un sistema de autenticación simple para aplicaciones móviles, y APIS basadas en el uso de tokens simples.

## Obtener un token de autenticación (Auth)

### Registro - /api/register
Para obtener un token de autenticación necesitamos habernos registrado previamente en el sistema. Para esto accederemos al Endpoint mediante una petición `POST` a `/api/register` en donde deberemos introducir los siguientes campos para crear una solicitud válida.

```json
{

"nombre": "tunombre",

"apellidos": "tuapellido",

"email": "correo@gmail.com",

"password": "tucontraseña",

"nombre_usuario": "tunombredeusuario"

}
```

Una vez hecha esta petición el servidor nos devolverá una respuesta con estado 201 Created, si todo ha ido bien y la siguiente información:

```json
{
"data": {

	"nombre": "tunombre",
	
	"apellidos": "tuapellido",
	
	"email": "correo@gmail.com",
	
	"nombre_usuario": "tunombredeusuario"
	
	"updated_at": "2025-06-11T08:13:06.000000Z",
	
	"created_at": "2025-06-11T08:13:06.000000Z",
	
	"id": 63

	}
}
```

En caso de haber cualquier problema con los campos en la petición nos devolverá una respuesta con estado 422 Unprocesable Entity y la siguiente información:

```json
{

"message": "The email has already been taken. (and 2 more errors)",

"errors": {

	"email": [
	
		"The email has already been taken."
	
	],
	
	"password": [
	
		"La contraseña es un dato obligatorio"
	
	],
	
	"nombre_usuario": [
	
		"El nombre de usuario ya existe"
	
	]
	
	}
}
```

Una vez registrados, el servidor generará un token de verificación de correo electrónico el cual se mandara en un enlace al correo electrónico que se registró. 

![[Pasted image 20250611105437.png]]

Una vez aquí el usuario solo tendrá que hacer clic en el enlace de verificar correo el cual mandará al usuario a través de una página del servidor en donde se marca el proceso de verificar correo como completado y redirige al usuario hacia el frontEnd de la página.

Una vez completados estos 2 pasos, ya habríamos conseguido registrar un usuario de manera exitosa en el sistema.

> [!warning] Atención
> Si se intentase acceder a cualquier otro Endpoint sin realizar este paso el servidor no te dará acceso a ninguna ruta protegida. Lo mismo pasa si intentases entrar en alguna ruta protegida del frontend sin verificar tu Email. 

### LogIn - /api/login

Una vez tenemos un usuario registrado, deberemos mandar una petición `POST` a `/api/login` con los siguientes campos **email** y **password**

El body de la petición ser vería algo así:

```json
{

"email": "alex.coronetas@gmail.com",

"password": "usuario"

}
```

Si faltase alguno de los campos o estos, contuviesen información errónea, véase contraseña o email incorrectos, el servidor nos devolverá una respuesta con estado **401 Unauthorized**.

En caso de ir todo bien, el servidor nos devolverá 2 cosas en la repuesta: 

1. La cookie encriptada con el token de Laravel Sactum:

>[!note] Info
>Esta cookie que nos devuelve el servidor es una cookie segura, marcada como HTTPOnly, samesite none. La cual esta encriptada para que no se pueda ver el token que hay dentro de la misma.

2. Información del usuario con el cual hemos iniciado sesión:

```json
{
	"user": {
	
	"id": 61,
	
	"nombre": "alex",
	
	"apellidos": "Coronado",
	
	"email": "alex.coronetas@gmail.com",
	
	"nombre_usuario": "Alexcoro",
	
	"visibilidad": true,
	
	"estado": true,
	
	"email_verified_at": "2025-06-08T22:37:22.000000Z",
	
	"avatar": "https://res.cloudinary.com/dok6y8wwp/image/upload/v1749499625/z4vku2db7wdjxr1lqlqy.png",
	
	"created_at": "2025-06-08T22:37:00.000000Z",
	
	"updated_at": "2025-06-09T20:07:06.000000Z"
	
	}
}
```


### LogOut - /api/logout

Una vez que ya hemos iniciado sesión necesitaremos cerrarla. Para esto haremos uso de la ruta `/api/logout` y con una simple petición `GET` cerraremos sesión ya que no necesitamos pasar ningún campo para realizar esta acción ya que el servidor en base a la sesión iniciada obtendrá tu token de acceso y lo  borrará junto a las cookies de sesión del navegador.

```json
{
	"message": "Successfully logged out"
}
```

Si la petición es exitosa el servidor nos devolverá este mensaje para darnos un poco mas de contexto.

### Comprobar sesión - /api/verifySession

Esta ruta nos permite realizar una petición `GET` a `/api/verifySession` al servidor para comprobar si la sesión sigue activa el cual devuelve true o false. La razón de ser de esta ruta es meramente para comprobar que cuando accedemos a una nueva página del FrontEnd como `/workouts` tenemos una sesión activa.

```json
{
	"verified": true
}
```

>[!note] Nota
> Esta ruta no se encarga de redirigir a los usuarios en caso de que no estén verificados simplemente devuelve true o false si el usuario tiene o no una cookie de autenticación válida.


## Tabla Usuarios

Para el manejo de la tabla de usuarios tenemos 5 endpoints:

### Get-All-Users - /api/usuarios

Este Endpoint devuelve un array con todos los usuarios registrados en la base de datos.
`GET /API/USUARIOS`

Ejemplo de respuesta:

```json
{
"data": [
	{
		"id": 1,
		
		"nombre": "Cecile",
		
		"apellidos": "Gibson",
		
		"email": "vernie81@example.org",
		
		"nombre_usuario": "ariane15",
		
		"visibilidad": true,
		
		"estado": true,
		
		"email_verified_at": "2025-06-08T22:36:37.000000Z",
		
		"avatar": "https://picsum.photos/200/300?grayscale",
		
		"created_at": "2025-06-08T22:36:37.000000Z",
		
		"updated_at": "2025-06-08T22:36:37.000000Z"
	
	},
	
	{
	
		"id": 2,
		
		"nombre": "Braulio",
		
		"apellidos": "Kling",
		
		"email": "crippin@example.org",
		
		"nombre_usuario": "rozella.leannon",
		
		"visibilidad": true,
		
		"estado": true,
		
		"email_verified_at": "2025-06-08T22:36:37.000000Z",
		
		"avatar": "https://picsum.photos/200/300?grayscale",
		
		"created_at": "2025-06-08T22:36:37.000000Z",
		
		"updated_at": "2025-06-08T22:36:37.000000Z"
	
	}
    ]
}
```

### Get-User - /api/usuarios/{id}

La ruta `GET /API/USUARIOS/{ID}` devuelve un json con la información del usuario del cual se ha hecho la petición.

Ejemplo respuesta para petición `GET /API/USUARIOS/61`:

```json
{
"data": {
	
	"id": 61,
	
	"nombre": "alex",
	
	"apellidos": "Coronado",
	
	"email": "alex.coronetas@gmail.com",
	
	"nombre_usuario": "Alexcoro",
	
	"visibilidad": true,
	
	"estado": true,
	
	"email_verified_at": "2025-06-08T22:37:22.000000Z",
	
	"avatar": "https://res.cloudinary.com/dok6y8wwp/image/upload/v1749499625/z4vku2db7wdjxr1lqlqy.png",
	
	"created_at": "2025-06-08T22:37:00.000000Z",
	
	"updated_at": "2025-06-09T20:07:06.000000Z",
	
	"propietario": true
	
},

"message": "User obtained successfully"
}
```

En caso de que el id introducido no existiese en la base de datos el servidor devolvería una respuesta con un código **404 Not Found** y la siguiente información:

```json
{

"error": "No query results for model [App\\Models\\Usuario] 80",

"message": "User not found"

}
```

### Update-User - /api/usuarios/update/61

Para actualizar de la información de un usuario lo haremos mediante una petición **POST** pues para poder mandar una imagen para actualizar el campo avatar, la petición debe incluir la cabecera **Content-Type: multipart/form-data** la cual no funciona en peticiones *PUT y PATCH*.
