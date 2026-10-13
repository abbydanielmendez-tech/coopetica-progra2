# Documentación del Conflicto de Fusión - CONFLICTO.md

## 1. ¿Qué archivo entró en conflicto y por qué?
El conflicto se generó en el archivo `README.md`. Ocurrió porque ambos integrantes modificamos el documento en nuestras ramas (`trabajo-jeremy` y `trabajo-abby`) e intentamos hacer la fusión con la rama principal.

## 2. ¿Qué mostraba Git exactamente?
Al intentar fusionar las ramas mediante la Pull Request, Git detuvo el proceso mostrando los marcadores de conflicto:

<<<<<<< trabajo-jeremy
CoopeTica R.L. es una cooperativa de ahorro y crédito que administra cuentas, asociados y movimientos financieros.
=======
El sistema para CoopeTica R.L. busca automatizar el registro de asociados, movimientos y cuentas.
>>>>>>> trabajo-abby

## 3. ¿Cómo decidieron cuál versión conservar, o cómo combinaron ambas?
Se combinaron ambas redacciones conservando la descripción del dominio, la lista de integrantes, los diagramas UML y la bitácora de IA. Se eliminaron los marcadores `<<<<<<<`, `=======` y `>>>>>>>` y se hizo el commit de resolución.

## 4. ¿Qué harían distinto para evitar ese conflicto la próxima vez?
Nos asignaremos secciones independientes del trabajo y haremos `git pull` constante de la rama principal antes de abrir una solicitud de incorporación.
