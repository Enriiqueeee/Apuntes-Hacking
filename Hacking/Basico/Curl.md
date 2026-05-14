Imprime el código fuente de la web
- curl http://info.cern.ch/

| **Opciones** | Descripcion                          | Comando                                                                                                                                      |
| ------------ | ------------------------------------ | -------------------------------------------------------------------------------------------------------------------------------------------- |
| -O           | Descarga el código fuente de la web  | curl -O http://info.cern.ch/index.html                                                                                                       |
| -S           | Silenciar el estado                  | curl -s -O http://info.cern.ch/index.html                                                                                                    |
| -k           | Omitimos comprobación de certificado | curl -K http://info.cern.ch/index.html                                                                                                       |
| -I           | Ver versión del servidor web         | curl -I http://info.cern.ch/index.html                                                                                                       |
| -U           | Proporcionar credenciales            | curl -u admin:admin http://<SERVER_IP>:<PORT>/                                                                                               |
| -X           | se usaria como metodos POST/DELETE   | curl -X POST http://<SERVER_IP>:<PORT>/api.php/city/ -d '{"city_name":"HTB_City", "country_name":"HTB"}' -H 'Content-Type: application/json' |
