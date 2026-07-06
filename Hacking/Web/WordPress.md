Tipo de CMS

| Rutas        | Descripcion                                   |
| ------------ | --------------------------------------------- |
| wp-admin.php |                                               |
| wp-login.php | Autenticarnos                                 |
| xmlrpc.php   | Permite hacer fuerza bruta si esta habilitado |

Lo que podemos ver es el código fuente
- etiqueta generator --> muestra la versión del wordpress


Se pueden enumerar usuarios por el error que da si pones un usuario incorrecto o password incorrecta


### Acceso al servidor desde panel interno de wordpress
Nos interesa mucho estar en la parte de Apariencia 
![[Pasted image 20260706232503.png|697]]
en este caso esta con el theme code editor, pero si no apareciese nada, tendremos que ir a plugins -> plugins instalados -> y subirlo de forma manual
![[Pasted image 20260706232608.png]]
tambien se puede hacer agregando un nuevo plugins (tiene que haber acceso a internet) y buscaremos theme editor
![[Pasted image 20260706232655.png]]
este seria el interesante y si vamos a el podemos editor archivos, y agregar codigo malicioso
![[Pasted image 20260706232751.png]]
le daríamos a update file y nos iríamos al navegador y escribiríamos la siguiente ruta
![[Pasted image 20260706232901.png|697]]
en este caso seria este porque si nos fijamos es la ruta anterior



### Enumeración de plugins de forma manual
Primero la instalaremos
![[Pasted image 20260706233045.png]]
Podemos encontrar usuarios con esta app, de la siguiente forma
![[Pasted image 20260706233147.png]]
-e u --> es para enumerar usuarios
esperamos a que termine y vemos que nos muestra usuarios encontrados
![[Pasted image 20260706233234.png]]
vemos que nos dice que nos a encontrado usuarios, tambien se pueden buscar usuarios usando la siguiente ruta
![[Pasted image 20260706233324.png|691]]

También se puede hacer ataque de fuerza bruta de la siguiente forma una vez encontremos los usuarios
![[Pasted image 20260706233419.png]]


### Enumerar y explotar vulnerabilidades de plugins
Una vez encontremos el plugins y la versión buscamos una PoC, nos lo descargaríamos y lo ejecutaríamos
![[Pasted image 20260706233928.png]]
si viésemos este fallo tenemos que ejecutar lo siguiente
![[Pasted image 20260706233944.png]]
y si este falla ejecutamos el siguiente
![[Pasted image 20260706234001.png]]



### Creación de plugins malicioso
Lo primero seria sacar el usuario y password del login de wordpress y acceder a el, una vez veremos si hay algún plugins malicioso, si no tendremos que crearlo nosotros
*![[Pasted image 20260706234626.png]](Se hace en php porque wordpress funciona con php)*
Usaremos el siguiente código
![[Pasted image 20260706234729.png]]
Luego lo tenemos que comprimir
![[Pasted image 20260706235112.png]]
y lo subimos en agregar plugins además de instalarlo y activarlo