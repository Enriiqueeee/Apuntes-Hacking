## La regla de oro: Mirar antes de tocar
La enumeración web es el arte de observar pacientemente antes de actuar
- Observar la pagina principal sin prisas.
- Hacer clic en todos los enlaces visibles.
- Probar acciones simples como formularios, botones y busquedas.
- Prestar atencion a los mensajes de error.
- Tomar nota de cada comportamiento sospechoso.

Toda pagina web esta hecha de HTML, CSS y JavaScript. Ese codigo viaja hasta tu navegador y puedes verlo con clic derecho > "Ver codigo fuente de la pagina" o con **Ctrl+U**.

Los programadores a veces dejan notas para ellos mismos en forma de comentarios HTML. A veces son inofensivas, pero otras revelan cosas como "**backup** temporal en **/backup.zip**" o "el panel de **admin** esta en **/admin-dev**".

Tambien puedes encontrar enlaces a archivos internos, rutas antiguas que siguen funcionando o nombres de archivos que dan pistas sobre la estructura del servidor.

## Las cabeceras invisibles: Headers HTTP

Cuando tu navegador pide una pagina, el servidor responde con la pagina y con informacion oculta llamada cabeceras HTTP.

Puedes ver estas cabeceras con **curl -I http://192.168.1.50** en tu terminal. Busca tecnologias, cookies, versiones y redirecciones raras.

## Con que esta construida la web: Identificar tecnologias

Saber si una web usa WordPress, Drupal, PHP casero o una aplicacion Node**.js** cambia completamente lo que vas a probar despues.

La herramienta whatweb hace esto por ti: **whatweb http://192.168.1.50**. Tambien puedes fijarte en extensiones como **.php**, **.aspx** o **.js**, en el favicon, en mensajes de error o en rutas tipicas.