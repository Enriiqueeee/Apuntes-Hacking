
Lo primero seria hacer un escaneo básico para saber que puertos están abiertos
![[Pasted image 20260817150431.png]]
Vemos que tenemos el puerto 22 ssh y el puerto 80 http, vemos que tiene la web
![[Pasted image 20260817150513.png]]
si no asociamos el host con la ip no nos dejaria
![[Pasted image 20260817150610.png]]
ahora si recargamos la web vemos el siguiente contenido
![[Pasted image 20260817150632.png]]
No vemos nada interesante asique miramos si tiene algún subdominio importante
![[Pasted image 20260817151359.png]]
no nos dice nada interesante asique nos vamos a ver vhost
![[Pasted image 20260817151656.png]]
encontramos un git, asique lo agregamos a hosts de nuestro kali
![[Pasted image 20260817151948.png]]
y vemos que contiene
![[Pasted image 20260817151958.png]]
Vemos que es como una especia de github en el que si le damos a explore podemos ver el proyecto![[Pasted image 20260817152029.png]]
Abrimos el unico que esta y vemos los siguientes ficheros
![[Pasted image 20260817152048.png]]Vemos cada uno a ver que contiene, lo que podemos hacer es descargar el proyecto y verlo
![[Pasted image 20260817152223.png]]
miramos commits
![[Pasted image 20260817155741.png]]
y vemos lo siguiente
![[Pasted image 20260817155752.png]]
una password asique probamos a entrar con esa
![[Pasted image 20260817155829.png]]
Vemos que accedemos a la web
![[Pasted image 20260817155846.png]]Aqui ahora miramos lo que podemos hacer