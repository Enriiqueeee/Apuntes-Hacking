## ¿Qué es Nmap?
**Nmap** es la **herramienta de reconocimiento** por excelencia. Convierte algo abstracto como "la máquina **192.168.1.50**" en una **lista concreta** de cosas que puedes investigar
### Los dos tipos de "llamada": TCP (educado) vs. UDP (directo)
**TCP** (Protocolo de Control de Transmisión): Es el método educado. Nmap dice "Hola, ¿estás ahí?" y espera un apretón de manos. Si la máquina responde, sabes que hay alguien. Es rápido y fiable para la mayoría de servicios como páginas web (**HTTP**) o terminales remotas (**SSH**).

**UDP** (Protocolo de Datagramas de Usuario): Es más brusco. Nmap lanza un paquete y se queda esperando... y esperando. Muchos servicios **UDP** no responden a menos que les digas la frase exacta. Por eso escanear **UDP** es más lento y frustrante. Pero algunos servicios cruciales como **DNS** (el que traduce nombres a **IPs**) viven aquí. Ignorar **UDP** es como no mirar el sótano.


Cuando Nmap termina, verás algo como "**22/tcp open ssh**". Respira hondo. Esto no significa que puedas entrar. Significa que hay una puerta con un cartel que dice "**SSH**". Ahora toca la parte de detective:


| Parametro              | Funcion                                                         |
| ---------------------- | --------------------------------------------------------------- |
| -sS                    | Para que sea sutil y silencioso                                 |
| -sC                    | Sacar mucha información automatizada a traves de script de nmap |
| --min-rate 5000        | Vaya mas rápido el escaneo                                      |
| -n                     | No intente resolucion dns                                       |
| -vvv                   | Mientras va enumerando muestre lo que encuentre                 |
| -Pn                    | Para que no haga ping para ver si esta activo                   |
| -oN                    | Sacar la información a un archivo                               |
| -sV                    | Detectar versiones de servicios                                 |
| -SVC                   | Combina el anterior con script basicos seguros                  |
| -p-                    | Mira todos los puertos TCP                                      |
| <br>-sU --top-ports 20 | Prueba los UDP mas comunes                                      |

## Timing y Performance

|Plantilla|Opción|Descripción|Velocidad|
|---|---|---|---|
|**Paranoid**|-T0|Muy lento, evasión máxima|🐌 5min+|
|**Sneaky**|-T1|Lento, buena evasión|🐢 15s|
|**Polite**|-T2|Normal, bajo ancho de banda|🚶 5s|
|**Normal**|-T3|Default, equilibrado|🏃 1s|
|**Aggressive**|-T4|Rápido, red confiable|🚗 300ms|
|**Insane**|-T5|Muy rápido, puede perder paquetes|✈️ 100ms|
## Interpretación de Resultados

|Estado|Descripción|Significado|
|---|---|---|
|**open**|Puerto abierto y aceptando conexiones|Servicio activo y accesible|
|**closed**|Puerto accesible pero no hay servicio|Host vivo pero puerto no usado|
|**filtered**|Firewall/IPS bloqueando el puerto|No se pudo determinar estado|
|**unfiltered**|Puerto accesible pero estado indeterminado|Generalmente en escaneos ACK|
|**open\|filtered**|No se pudo determinar si está abierto o filtrado|Común en escaneos UDP o IP|
|**closed\|filtered**|No se pudo determinar si está cerrado o filtrado|Muy raro|