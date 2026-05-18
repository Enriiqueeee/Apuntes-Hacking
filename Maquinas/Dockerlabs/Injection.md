Miramos que puerto tiene abiertos
![[Pasted image 20260518162439.png]]
Miramos mas detalladamente las versiones de cada puerto
![[Pasted image 20260518162537.png]]
Miramos que tenemos en la web
![[Pasted image 20260518162707.png]]
Apreciamos un loggin, probaremos a ver si tenemos subdirecciones ocultas
![[Pasted image 20260518162854.png]]
Vemos que no apreciamos mucho, asique probamos a mirar Vhost
![[Pasted image 20260518163120.png]]
Seguimos sin ver nada asique, siendo un login podriamos probar a acceder mediante sql injection
![[Pasted image 20260518163355.png]]
User: admin
Password: ' or '1'='1
Le daremos en login y 
![[Pasted image 20260518163438.png]]
Vemso que pudimos acceder como el usuario dylan y nos da su password, que las probaremos en ssh
![[Pasted image 20260518163551.png]]Vemos que estamos con el usuario dylan asique buscamos cosas para poder escalar privilegios
![[Pasted image 20260518163751.png]]
El que vemos mas interesante seria el de env, asique lo explotaremos
![[Pasted image 20260518163853.png]]
y ya seriamos root