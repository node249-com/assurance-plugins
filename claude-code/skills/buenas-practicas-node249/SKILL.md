---
name: buenas-practicas-node249
description: Aplica los manuales de buenas prácticas de NODE249 Assurance al escribir, revisar o refactorizar código en cualquier lenguaje o tecnología (TypeScript, Python, C#, Java, Go, SQL, React, PostgreSQL, Docker, nginx, Git, CI/CD, IA…). Úsala antes de empezar a programar y antes de dar un trabajo por terminado.
---

# Buenas prácticas NODE249 Assurance

Los manuales están en el servidor MCP `node249-assurance` (herramientas `listar_manuales`, `leer`, `buscar` y
`lista_comprobacion`). Si no está disponible, avisa al usuario: necesita un token de
https://assurance.node249.com/app/seguridad en la variable `NODE249_ASSURANCE_TOKEN`.

## Al empezar un trabajo
1. Identifica las tecnologías implicadas (lenguaje, framework, base de datos, infraestructura).
2. `listar_manuales` y localiza el manual de cada una. Aplica **siempre** también el `01` (ciclo de desarrollo seguro y de calidad).
3. `leer` el procedimiento de cada tecnología (sin capítulo). Para dudas concretas, `buscar` o `leer` un capítulo del libro.
4. Si el proyecto ya tiene reglas propias que contradicen un manual, señala el conflicto en lugar de elegir en silencio.

## Mientras trabajas
- Sigue las reglas del manual (estilo, seguridad, pruebas, dependencias, secretos). Cita el manual cuando una decisión dependa de él.
- No cargues libros enteros: pide solo el capítulo o la búsqueda que necesites.

## Antes de dar algo por terminado
1. `lista_comprobacion` de cada tecnología implicada y del `01`.
2. Revisa punto por punto y di cuáles se cumplen, cuáles no y por qué.
3. Una excepción a una regla se documenta con su motivo (no se omite).
