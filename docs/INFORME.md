Nueve preguntas: cada miembro responde tres (A: 1–3, B: 4–6, C: 7–9) en el mismo fichero, en su rama, con PR.

<<<<<<< HEAD
1. ¿Por qué el segundo push del apartado 2.2 fue rechazado? ¿Qué dos operaciones hace `git pull` por debajo?

2. En vuestro historial, señalad un merge *fast-forward* y un *merge commit*. ¿Qué los diferencia?

3. ¿Por qué rellenar filas distintas de la tabla no dio conflicto y cambiar `Última revisión` sí?

4. Pegad el mensaje de error del push a `main` protegida y explicad qué regla lo ha bloqueado.

5. ¿Qué comando sacó `.env` del control de versiones sin borrarlo? ¿Por qué la contraseña sigue siendo un problema y qué haríais en un proyecto real? (Pista: la respuesta empieza por lo que hay que hacer con la contraseña, no con el historial.)

6. ¿Qué hace mejor GitHub Desktop que la terminal, y qué no puede hacer? ¿Con cuál habéis entendido mejor el conflicto?

7. Roles: ¿qué puede hacer un Maintain que no pueda un Write? ¿Quién podría haber quitado la protección de `main`?

8. Si mañana un miembro sube un force push a `main`, ¿qué se pierde y qué lo impide en vuestro repositorio?

9. En la Fase 1 compartíais un portátil y en la Fase 2 cada uno tenía el suyo. ¿Qué diferencia práctica tiene eso para la identidad del autor de cada commit y para cómo aparecen los conflictos?
=======
7. Roles: ¿qué puede hacer un Maintain que no pueda un Write? ¿Quién podría haber quitado la protección de `main`?

	Con el rol Maintainpuedes hacer todo lo que puede hacer un Write mas modificar las reglas de proteccion de ramas, cosa que el Write no puede.
	El que pudiera quitar la proteccion de main puede ser Admin o Maintain, Write no puede

8. Si mañana un miembro sube un force push a `main`, ¿qué se pierde y qué lo impide en vuestro repositorio?

	Se pierden los commits de otros que yo no tenia en local.
	Lo impide la proteccion de rama "Do not allow force pushes" que tien main
	
9. En la Fase 1 compartíais un portátil y en la Fase 2 cada uno tenía el suyo. ¿Qué diferencia práctica tiene eso para la identidad del autor de cada commit y para cómo aparecen los conflictos?

	En la fase 1 simulabamos multiusuarios con un mismo Git, y en la 2 cada uno tenia ya su propio usuario, pero ahora los conflictos ya no son locales, si no mas del remoto compartido
>>>>>>> 1d56ccfcacd798be60d81dd67d7727577fdedfaf
