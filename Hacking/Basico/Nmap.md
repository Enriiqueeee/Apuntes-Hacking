Descubrimiento de maquinas activas:
	nmap -sn  < ip >

Escaneo de puertos básicos:
	❯ nmap -sS 10.129.63.130 -Pn -p-
![[Pasted image 20260511181826.png]]


Escaneo de puerto mas avanzado
	Este escaneo suele ser para ver versiones de los protocolos
	❯ nmap -sS 10.129.63.130 -Pn -p22,80,443,3552 -sV
![[Pasted image 20260511182001.png]]
	También se puede usar 
	❯ nmap -sS 10.129.63.130 -Pn -p22,80,443,3552 -sVC 


| Parametro       | Funcion                                                         |
| --------------- | --------------------------------------------------------------- |
| -sS             | Para que sea sutil y silencioso                                 |
| -sC             | Sacar mucha información automatizada a traves de script de nmap |
| --min-rate 5000 | Vaya mas rápido el escaneo                                      |
| -n              | No intente resolucion dns                                       |
| -vvv            | Mientras va enumerando muestre lo que encuentre                 |
| -Pn             | Para que no haga ping para ver si esta activo                   |
| -oN             | Sacar la información a un archivo                               |
