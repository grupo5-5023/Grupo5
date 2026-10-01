Nueve preguntas: cada miembro responde tres (A: 1–3, B: 4–6, C: 7–9) en el mismo fichero, en su rama, con PR.


4. Pegad el mensaje de error del push a main protegida y explicad qué regla lo ha bloqueado.

	remote: error: GH006: Protected branch update failed for refs/heads/main.
remote:
remote: - Changes must be made through a pull request.
! [remote rejected] main -> main (protected branch hook declined)
error: failed to push some refs

El push fue bloqueado porque configuramos una regla de protección sobre `main`. Esta regla obliga a introducir los cambios mediante una Pull Request con al menos una revisión aprobada y prohíbe el push directo a `main`. Por eso GitHub rechazó el push.


5. ¿Qué comando sacó .env del control de versiones sin borrarlo? ¿Por qué la contraseña sigue siendo un problema y qué haríais en un proyecto real? (Pista: la respuesta empieza por lo que hay que hacer con la contraseña, no con el historial.)

git rm --cached .env

Aunque después eliminemos `.env` del control de versiones y lo añadamos a `.gitignore`, la contraseña sigue siendo un problema porque ya apareció en un commit anterior y, por tanto, queda guardada en el historial de Git.

En un proyecto real, lo primero sería revocar o cambiar inmediatamente la contraseña comprometida y generar una nueva. Después se podría eliminar el secreto del historial del repositorio para evitar que siga siendo
accesible. Finalmente, mantendríamos `.env` en `.gitignore` para evitar volver a subirlo por accidente.

6. ¿Qué hace mejor GitHub Desktop que la terminal, y qué no puede hacer? ¿Con cuál habéis entendido mejor el conflicto?

Pero GitHub Desktop no puede hacer todo lo que podemos hacer desde la terminal. Por ejemplo, en la terminal podemos usar comandos como git log --oneline --graph --all para ver el historial de commits de una forma más completa

7. Roles: ¿qué puede hacer un Maintain que no pueda un Write? ¿Quién podría haber quitado la protección de `main`?

	Con el rol Maintainpuedes hacer todo lo que puede hacer un Write mas modificar las reglas de proteccion de ramas, cosa que el Write no puede.
	El que pudiera quitar la proteccion de main puede ser Admin o Maintain, Write no puede


8. Si mañana un miembro sube un force push a `main`, ¿qué se pierde y qué lo impide en vuestro repositorio?

	Se pierden los commits de otros que yo no tenia en local.
	Lo impide la proteccion de rama "Do not allow force pushes" que tien main
	

9. En la Fase 1 compartíais un portátil y en la Fase 2 cada uno tenía el suyo. ¿Qué diferencia práctica tiene eso para la identidad del autor de cada commit y para cómo aparecen los conflictos?

	En la fase 1 simulabamos multiusuarios con un mismo Git, y en la 2 cada uno tenia ya su propio usuario, pero ahora los conflictos ya no son locales, si no mas del remoto compartido