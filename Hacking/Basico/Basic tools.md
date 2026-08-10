
## Enumeración local: El ritual que debes repetir siempre

Ya tienes **shell**. Ahora toca **enumeración local**: mirar desde dentro del sistema igual que mirabas desde fuera con **Nmap**.

Antes de explotar nada, responde preguntas: qué **usuario** soy, a qué **grupos** pertenezco, qué comandos puedo ejecutar como **root**, qué **procesos** corren y dónde puede haber **credenciales**.

La **enumeración local** no es memorizar comandos. Es una actitud de detective: entender el sistema antes de tocarlo.

- Identidad: whoami, id, groups.
- Usuarios: cat /etc/passwd, ls /home.
- Procesos: ps aux.
- Conexiones: netstat -tulpn o ss -tulpn.
- Capacidades: getcap -r / 2>/dev/null.
- Buscar binarios con SUID: find / -perm -4000 -type f 2>/dev/null | xargs ls -la


Existe una webshell en el propio kali que lo veremos de la siguiente forma
![[Pasted image 20260705143330.png|350]]
También existe binario de netcat
![[Pasted image 20260705143428.png|404]]


| **Command**                    | **Description**                       | **Uso**         |
| ------------------------------ | ------------------------------------- | --------------- |
| Ping                           | Ver si un sistema esta levantado o no | ping -c1 < IP > |
| whoami                         | Ver mi usuario                        | whoami          |
| cat                            | Ver el contenido de un fichero        | cat < fichero > |
| find / -perm -4000 2>/dev/null | Para escalada de privilegios          |                 |




### Directorios

| ruta | descripcion                                                        |
| ---- | ------------------------------------------------------------------ |
| /opt | destinado a la instalación de **paquetes de software adicionales** |


### Puertos

| Nombre | puerto | descripcion                                                                                |
| ------ | ------ | ------------------------------------------------------------------------------------------ |
| ppp    | 3000   | utilizado en el desarrollo de software para ejecutar servidores web y aplicaciones locales |
|        |        |                                                                                            |


#### CMS
Gestor de contenidos para la creación y administración de contenidos digitales.
Ejemplo seria WordPress



#### Shell
Si estamos en una shell de meterpreter con el siguiente comando podremos ver una shell interactiva
![[Pasted image 20260707004438.png]]


#### Samba
Para poder acceder como anonymous usamos el siguiente comando
└─$ smbclient -L //172.17.0.2 -N
![[Pasted image 20260708010834.png]]
Enumerar usuarios de samba
```
enum4linux -a 172.17.0.2
```

