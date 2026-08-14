Try Hack Me - "HTTP in Detail"
TryHackMe | 2026-08-14

Conceptos: 
-HTTP (HyperText Transfer Protocol): Protocolo de capa de aplicacion basado en arquitectura cliente-servidor.
Stateless (Sin estado): El servidor no guarda memoria de peticiones anteriores; cada solicitud es independiente.
- Puertos estandar: Puerto 80 para HTTP (texto plano) y puerto 443 para HTTPS (cifrado con TLS/SSL).
- Cookies y Sesion: Mecanismo para persistir la sesion del usuario usando cabeceras Set-Cookie (servidor) y Cookie (cliente).

Estructura de peticiones:
- Linea de peticion: Metodo, ruta y version del protocolo (ej. GET /index.html HTTP/1.1).

Códigos y metodos:

- GET: Solicitar o descargar un recurso del servidor.
- POST: Enviar informacion para crear o procesar un recurso (formularios, login).
- PUT: Reemplazar o actualizar completamente un recurso en el servidor.
- DELETE: Eliminar un recurso especifico.
- HEAD: Solicita unicamente las cabeceras de respuesta sin el cuerpo.
- OPTIONS: Consulta que metodos HTTP estan permitidos en el endpoint.

Comandos utiles:

-100-199: La primera parte del request del usuario fue aceptada y deben de seguir para mandar su request completo.
- 200-299: El request fue un éxito
- 300-399: Se va a redirecionar al usuario a otra página.
- 400-499: Informa al usuario que hubo un error en su request:
- 500-599: Hay problemas en el servidor manejando el request.

- 201 : Se creo el output con éxito
- 301 : señala que la pagina fue movida a otra dirección y que la busquen ahí.
- 400: Informa al usuario que algo esta mal con su request.
- 401 : Informa al usuario que no tiene los permisos para entrar a esa dirección, casi siempre hasta que se cree el usuario.
- 403: La página esta prohibida aunque tengas usuario.
- 404: Lá pagina no existe.

Headers Cookies: 

- get/http/1.1: Desde que http el cliente solicita la paágina.
- http/1.1  200 ok: Pregunta la página por el usuario. 
- post/ http1.1: Formato lleno con el usuario se envia a la página.
- http/1.1 200 ok: Respuesta set-cookie diciendo a la página que guarde información.
- get/ http/1.1: en los siguientes requeest el cliente envia la cookie de regreso al servidor.
- http/1.1 200 ok: el servidor ve la cookie y la información y manda de regreso un mensaje de bienvenido al cliente.