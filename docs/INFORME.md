4. Pegad el mensaje de error del push a main protegida y explicad qué regla lo ha bloqueado.
Al realizar el push desde main, GitHub mostró el siguiente mensaje de error:

remote: error: GH006: Protected branch update failed for refs/heads/main.
remote: 
remote: - Changes must be made through a pull request.
To https://github.com/grupo5-5023/grupo5.git
 ! [remote rejected] main -> main (protected branch hook declined)
error: failed to push some refs to 'https://github.com/grupo5-5023/grupo5.git'

El push fue bloqueado porque al configurar la regla sobre main obligaba a
obligaba a introducir los cambios mediante una Pull Request con una revisión
aprobada y prohibe el push directo a main. 


5. ¿Qué comando sacó .env del control de versiones sin borrarlo? ¿Por qué la contraseña sigue 
siendo un problema y qué haríais en un proyecto real? (Pista: la respuesta empieza por lo que hay 
que hacer con la contraseña, no con el historial.)

git rm --cached .env

Este comando quita el archivo .env de Git, pero no lo borra de 
nuestro ordenador.

La contraseña seguiría siendo un problema porque ya se había subido antes y 
puede seguir apareciendo en el historial del repositorio.

En un caso realista, lo primero sería cambiar esa contraseña por una nueva,
luego intentaríamos eliminarla también del historial y dejaríamos .env 
dentro de .gitignore

6. ¿Qué hace mejor GitHub Desktop que la terminal, y qué no puede hacer? ¿Con 
cuál habéis entendido mejor el conflicto?

GitHub Desktop es más fácil y visual que la terminal. Desde GitHub Desktop
permite ver mejor todo el proceso como los commits, las ramas, los cambios...
sin necesidad de escribir tantos comandos y tener que recordar de ellos.

Un comando que no sería posible realizar desde GitHub Desktop sería:
git log --oneline --graph --all

Este comando sirve para ver el historial de commits de una forma más completa

GitHub Desktop nos ayudó a entender mejor el conflicto porque podíamos ver 
de forma más clara qué archivos tenían problemas y los cambios que
habíamos hecho.

