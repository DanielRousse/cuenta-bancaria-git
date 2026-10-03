# Cuenta bancaria — Git y pull requests

**Autor:** Jonathan Daniel Reyes Gordillo

## Cómo correr

    ./correr.sh

## Mis pull requests

| # | Qué cambió |
|---|---|
| 1 | El estado de cuenta muestra cuántos retiros se hicieron y cuántos fueron gratis |
| 2 | README y evidencia de la práctica |

## Boleto de salida

1. ¿Qué diferencia hay entre `git add` y `git commit`?  
Respuesta: `git add` prepara los cambios colocándolos en el área de preparación (*staging area* o *index*), seleccionando qué modificaciones entrarán en el próximo snapshot. `git commit` toma todo lo que está preparado en el área de staging y lo guarda de forma permanente e inmutable en el historial local del repositorio, generando un nuevo commit con su hash único, autor, fecha y mensaje descriptivo.

2. ¿Por qué después del merge en GitHub tu `main` de Ubuntu no tenía el cambio hasta que hiciste `git pull`?  
Respuesta: Porque Git es un sistema distribuido: el merge ocurrió en el servidor remoto de GitHub (`origin/main`). Nuestra copia local de `main` en Ubuntu no se actualiza sola porque Git no sincroniza automáticamente por internet en segundo plano; para recibir los nuevos commits remotos e integrarlos en nuestra rama local, es indispensable ejecutar explícitamente `git pull`.

3. Abriste un PR y después hiciste otro commit en la misma rama. ¿Qué pasó con el PR?  
Respuesta: El Pull Request se actualizó automáticamente incorporando el nuevo commit en cuanto hicimos `git push`. En GitHub, un PR sigue dinámicamente a la rama de origen (*compare*); no representa un commit estático, por lo que cualquier nuevo commit enviado a esa rama entra directamente a la misma conversación y revisión sin necesidad de abrir un nuevo PR.

4. ¿Por qué en un equipo nadie hace cambios directamente en `main`?  
Respuesta: Porque `main` es la rama principal que representa el código estable, probado y listo para producción. Hacer cambios directos en `main` puede introducir errores no detectados, romper el entorno de los demás colaboradores y provocar conflictos difíciles de resolver. Al trabajar con ramas y Pull Requests, cada cambio se desarrolla de forma aislada, se somete a revisión de código (*code review*) y pruebas antes de integrarse de manera segura.

## Preguntas del libro — Capítulos 3 y 4

En este repositorio se incluyen las respuestas detalladas y explicaciones a las preguntas de certificación de los capítulos 3 y 4 del libro:
- 📄 Documento Markdown completo: [preguntas-capitulos-3-y-4.md](preguntas-capitulos-3-y-4.md)
- 📑 Documento PDF original en evidencia: [evidencia/Capítulo 3 y 4 - Preguntas.pdf](evidencia/Capítulo%203%20y%204%20-%20Preguntas.pdf)
- **Capítulo 3 (Making Decisions):** 29 preguntas resueltas sobre estructuras de control (`if/else`, `switch`, `for`, `for-each`, `while`, `do/while`), alcance de variables y evaluación booleana.
- **Capítulo 4 (Core APIs):** 22 preguntas resueltas sobre APIs centrales de Java (`String`, `StringBuilder`, arreglos, `Math`, `LocalDate`, `ZonedDateTime`, `Instant`).
