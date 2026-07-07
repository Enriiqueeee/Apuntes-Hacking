Habilitamos el docker con la maquina victima
![[Pasted image 20260708005917.png]]
Ahora realizamos un escaneo sencillo solo para saber que puertos tenemos activos
![[Pasted image 20260708010008.png]]
Tenemos el puerto 22,80,139 y 443, suponemos que es un windows asique lo primero que hacemos es ver que web tenemos alojada en el puerto 80![[Pasted image 20260708010057.png]]
Vemos un login y debajo en negrita tenemos un registrate pero el botón no carga nada, asique vemos si tenemos subdominios detras de esta web
No vemos nada interesante asique miramos el recurso de samba a ver que hay
![[Pasted image 20260708010905.png]]
Vemos que tenemos varios recursos interesantes

| Recurso  | Comentario         |
| -------- | ------------------ |
| myshare  | carpeta compartida |
| backup24 | Privado            |
| home     | Produccion         |
El primer recursos se puede acceder de forma anónima asique vemos que tiene
![[Pasted image 20260708011102.png]]![[Pasted image 20260708011114.png]]
Vemos que es una cadena con forma de token JWT si lo descodificamos 
![[Pasted image 20260708011156.png]]
Vemos un usuario con lo que podemos probar a hacer fuerza bruta por si sacamos la password para acceder al recurso privado
![[Pasted image 20260708011442.png]]
esperamos a ver si nos saca una password
![[Pasted image 20260708011457.png]]
tenemos un usuario y password asique accedemos con dicho usuario
![[Pasted image 20260708011603.png]]
![[Pasted image 20260708011611.png]]Seguimos buscando hasta que encontramos esto
![[Pasted image 20260708011709.png]]
ahora miraremos que contiene
![[Pasted image 20260708011741.png]]
Vemos notes que es algo raro y luego unos usuarios con credenciales que los probaremos en ssh porque vemos un usuario administrador
![[Pasted image 20260708011854.png]]
Miraremos si podemos hacer algo con este usuario
![[Pasted image 20260708011945.png]]
Vemos que no asique sabiendo que tenemos una web podemos subir una revershell para acceder como www-data, modificaríamos la ip y el puerto por el que queramos, una vez lo tengamos lo intentaríamos subir a la maquina victima para ejecutarlo, asique vamos a la web y ponemos la ruta de la revershell y en la terminal en la que estemos a la escucha vemos la sesion
![[Pasted image 20260708012249.png|555]]
teniendo esto vemos si podemos ejecutar algo como root
![[Pasted image 20260708012502.png]]
Vemos que teníamos el /service y mirando gtfobins nos dio una shell como root