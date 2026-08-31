# Registro de Errores

Completar una fila por cada error detectado.

| N | Archivo | Problema encontrado | Como lo detectaron | Solucion aplicada |
|---|---------|---------------------|--------------------|-------------------|
| 1 | src/ejemplo.js | El token no se verificaba | Prueba manual de ruta protegida | Se uso jwt.verify con manejo de excepcion |

## Guia de calidad para el informe

No alcanza con escribir "habia un error y lo arreglamos".

En cada caso expliquen:

1. Que ocurria.
2. Por que ocurria.
3. Como se soluciono.
4. Como validaron que quedo funcionando.


error 1 :
no llama desde el app.js la ruta del register (la solucion fue crear la ruta y se probo en postman )
error 2 :
falta la s en el export y por eso no se creaba el token (se soluciono agregandole la s que le faltaba y me di cuenta que funcionaba cuando lo probe en postman y encotro la funcion de token )
error 3 :
compara mal la contraseña (se soluciono con invertir el compare haciendo que primero este la contraseña que este en la bd con la ingresada por el usuario y se probo en postman )
error 4: 
el error estaba en que el id cuando lo buscaba buscaba req.user en vez de req.body o en todo caso tendría que ser req.params (la solucion fue poner .body haciendo que funcione el get by id )
error 5 : 
había que poner en el update el body (misma solucion que en el anterior error )
error 6 : 
estaban puestos los corchetes en el cost para el name haciendo que realmente no se actualice (la solucion fue sacarle los corchetes haciendo que el update funcione correctamente )