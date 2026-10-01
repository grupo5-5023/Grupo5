Nueve preguntas: cada miembro responde tres (A: 1–3, B: 4–6, C: 7–9) en el mismo fichero, en su rama, con PR.

7. Roles: ¿qué puede hacer un Maintain que no pueda un Write? ¿Quién podría haber quitado la protección de `main`?

	Con el rol Maintainpuedes hacer todo lo que puede hacer un Write mas modificar las reglas de proteccion de ramas, cosa que el Write no puede.
	El que pudiera quitar la proteccion de main puede ser Admin o Maintain, Write no puede

8. Si mañana un miembro sube un force push a `main`, ¿qué se pierde y qué lo impide en vuestro repositorio?

	Se pierden los commits de otros que yo no tenia en local.
	Lo impide la proteccion de rama "Do not allow force pushes" que tien main
	
9. En la Fase 1 compartíais un portátil y en la Fase 2 cada uno tenía el suyo. ¿Qué diferencia práctica tiene eso para la identidad del autor de cada commit y para cómo aparecen los conflictos?

	En la fase 1 simulabamos multiusuarios con un mismo Git, y en la 2 cada uno tenia ya su propio usuario, pero ahora los conflictos ya no son locales, si no mas del remoto compartido