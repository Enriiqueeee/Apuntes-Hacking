Inyectar revershell:
- https://www.revshells.com/ 
	![[Pasted image 20260514233644.png]]
	Aqui podemos cambiar nuestra ip, puerto por el que queramos para hacer la shell inversa, si vemos que no funciona lo podemos encodear con burpsuite para que funcione



Código en php que si se ejecuta de forma automática recibimos la shell
	![[Pasted image 20260705144710.png|654]]
	Primero lo tenemos que descargar
	![[Pasted image 20260705144932.png]]
	Le tenemos que modificar y cambiar lo siguiente
	![[Pasted image 20260705144816.png]]
	modificaríamos la ip y el puerto por el que queramos, una vez lo tengamos lo intentaríamos subir a la maquina victima para ejecutarlo