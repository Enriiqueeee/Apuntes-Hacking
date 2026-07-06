
## Hacking Web
Cookies --> para cambiar las cookies seria:
- Clic derecho -- abrir dev-tools -- storage -- y cambiamos las cookies
	Si vemos que no funciona lo mejor es hacerlo en ventana de incógnito

En wordpress si acedemos  al panel de admin, podemos agregar un plugin llamado file manager para gestionar archivos


## FTP
Para habilitar el servicio seria primero instalarlo
![[Pasted image 20260705154724.png]]
Luego le iniciamos e habilitamos
![[Pasted image 20260705154752.png]]
Para cambiar el puerto por el que corre nos iremos al archivo 
	/etc/vsftpd.conf
![[Pasted image 20260705155720.png]]
bajamos y agregamos la siguiente linea si no existe
![[Pasted image 20260705155810.png]]
guardamos salimos y reiniciamos el servicio



## SSH
Primero tenemos que instalarlo
![[Pasted image 20260705160443.png]]
Luego lo iniciamos y vemos que esta activo
![[Pasted image 20260705160516.png]]



###  Navegador parámetros
Si en un navegador por ejemplo en una academia agregamos el parámetro /?s=" lo que sea "
	Serviría para hacer búsquedas
Lo que podríamos hacer es por ejemplo copiar el nombre de una lección
![[Pasted image 20260706235822.png]]
y usamos el parámetro /s="nombre de la lección" veremos todas las entradas
![[Pasted image 20260706235913.png]]
y vemos que nos encuentra varias y si entramos podemos ver el contenido de la lección huérfanas
Para corregirlo en WordPress tendremos que elegir en Temas los huérfanos y eliminar la correcta

