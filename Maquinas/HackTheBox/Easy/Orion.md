Primero realizamos un escaneo para saber que puertos tenemos activos
![[Pasted image 20260707002352.png]]
Ahora sabiendo que tenemos el 22 y 80 realizo un escaneo mas detallado para tener mas informacion
![[Pasted image 20260707002450.png]]
Vemos que web tenemos detrás del puerto 80
![[Pasted image 20260707002546.png]]
Miramos si existe algún subdirectorio oculto detrás de esta web
![[Pasted image 20260707002859.png]]
apreciamos un admin y assets con código 301 asique comprobamos
![[Pasted image 20260707002936.png]]
vemos que tenemos un login al acceder al /admin, vemos que nos da una version
![[Pasted image 20260707003309.png]]
asique vemos si existe en la msfconsole algun exploit
![[Pasted image 20260707003415.png]]
vemos que tenemos uno asique lo usamos
![[Pasted image 20260707003441.png]]
configuramos lo necesario y lanzamos
![[Pasted image 20260707003701.png]]
esperamos a que termine y nos diga que funciono para lanzar una shell
![[Pasted image 20260707003911.png]]
ahora miramos para buscar usuarios futuros
![[Pasted image 20260707003940.png]]
vemos que existe el usuario adam, seguimos a ver si vemos algo mas interesante
![[Pasted image 20260707004124.png]]
apreciamos un .env asique vemos que contiene
![[Pasted image 20260707004153.png]]
apreciamos un db_user y db_password, asique accedemos a la base de datos
![[Pasted image 20260707004342.png]]
creamos una shell que podamos ver donde estamos y accedemos a la base de datos
![[Pasted image 20260707004515.png]]
ahora miramos que tablas existen
![[Pasted image 20260707004616.png]]
Vemos un montón pero buscamos la de users y vemos que tiene
![[Pasted image 20260707004933.png]]
nos interesara el id - email - password asique vemos esas 3
![[Pasted image 20260707005130.png]]
vemos que tenemos la password crackeada asique la copiamos y la probamos a descifrar
![[Pasted image 20260707005234.png]]
![[Pasted image 20260707005635.png]]
ahora con la password nos intentamos conectar por el ssh
![[Pasted image 20260707005710.png]]
vemos que si funciona asique sacamos la flag de este usuario y vemos como hacer la explotación de privilegios
![[Pasted image 20260707005917.png]]
vemos que tiene telnet, asique probamos a realizar el **CVE-2026-24061**
![[Pasted image 20260707005954.png]]
y nos da una sesión como root, asique sacamos la flag