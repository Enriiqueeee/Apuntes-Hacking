Desplegamos la maquina
![[Pasted image 20260514235428.png]]
Una vez desplegada, vemos la ip y le hacemos un escaneo para ver que puertos están activos
![[Pasted image 20260514235515.png]]
hacemos un escaneo mas completo
![[Pasted image 20260514235639.png]]Podemos apreciar un servicio ftp, dos http uno en el 80 y otro en el 3000 que sera un ppp y un shh, si nos fijamos bien vemos que tenemos en el ftp anonymous habilitado
![[Pasted image 20260514235752.png]]accedemos y veremos lo siguiente
![[Pasted image 20260514235835.png]]
vemos el directorio de mantenimiento que entraremos y vemos que contiene
![[Pasted image 20260515000101.png]]
Vemos que tenemos una base de datos de password de keepass, asique lo abriremos 
![[Pasted image 20260515000358.png]]
Vemos que nos pide una password asique de momento lo dejaremos de lado, veremos que contiene la web![[Pasted image 20260515000506.png]]
Vemos que es una pagina de apache por defecto, asique probamos la que estaba en el puerto 3000
![[Pasted image 20260515000533.png]]
nos redirige a un login, en el que probamos credenciales comunes
![[Pasted image 20260515222308.png]]
Vemos que accedemos con admin - admin, asique ahora miramos la configuración
![[Pasted image 20260515222347.png]]
Vemos que no tenemos nada interesante, asique miramos si tenemos algún directorio oculto en este puerto
![[Pasted image 20260515223937.png]]
Encontramos varios pero vemos este que es importante
![[Pasted image 20260518160637.png]]
Vemos que esta en mantenimiento pero vemos que el acceso esta en la siguiente ruta, asique probamos a leer los archivos
![[Pasted image 20260518161148.png]]
Vemos que tenemos un usuario freddy y podemos hacer lfi, asique probamos con la otra ruta que encontramos
![[Pasted image 20260518161226.png]]
Probamos a acceder con el usuario freddy y esta password que encontramos![[Pasted image 20260518161312.png]]
Vemos que entramos como dicho usuario asique ahora miramos si tenemos algo importante que podamos usar para escalar privilegios
![[Pasted image 20260518161431.png]]
Vemos que podemos ejecutar el python de maintenance, asique viendo que contiene un print y que lo podemos modificar, probaremos a que nos lance una shell como root
![[Pasted image 20260518161604.png]]
Lo lanzamos, nos pedira la password de dicho usuario  y veremos que somos root
![[Pasted image 20260518161649.png]]
