# Prompt 01 · Entrevista inicial + construcción del CV (Fase 0)

Pega esto al inicio, en una conversación nueva con tu agente. A partir de ahí, **él pregunta y tú respondes** — puede tomar 15–30 minutos, o hacerlo por partes.

---

Vamos a montar mi sistema de búsqueda de empleo automática. Hoy es la Fase 0: tú me entrevistas y construyes todo. No voy a llenar formularios: hazme las preguntas tú, por bloques cortos, en lenguaje normal, y espera mis respuestas antes de seguir.

**Bloques que debes cubrir** (detalle en `docs/02-cuestionario-inicial.md`):
A. Datos base (nombre oficial, ciudad, contacto, disponibilidad)
B. Educación (grado exacto e institución; años solo si estoy seguro)
C. Experiencia empleo por empleo (empresa, puesto, fechas, funciones y **cifras**: montos, volúmenes, resultados; herramientas por empleo)
D. Idiomas con nivel real A2–C1 y examen si tengo
E. Dinero (piso salarial duro, último sueldo, ¿USD sí/no?)
F. Forma de trabajo (remoto/presencial/híbrido y bajo qué condiciones, turnos, viajes)
G. Exclusiones (lo que jamás: comisión 100%, call centers, giros y empresas vetadas)
H. Datos sensibles solo si acepto darlos (documento de identidad: se guarda seguro y solo se usa si un portal lo exige; referencias: por defecto NO)
I. Mi track B opcional (startups/tech/misión/aprendizaje, con el mismo piso salarial)

**Reglas durante la entrevista:**
- Si una respuesta mía es ambigua o se contradice con otra, pregúntame solo eso hasta que quede confirmado. Lo no confirmado queda marcado como NO USAR.
- No des por bueno ningún dato que yo no haya dicho. Nada de autocompletar fechas, empresas ni cifras «típicas».

**Al terminar la entrevista, construye y entrégame:**
1. `perfil.yaml` llenado (plantilla en `templates/perfil.yaml`) para mi confirmación dato por dato.
2. `criterios-de-busqueda.md` con mis reglas, mis tracks y mi piso.
3. `banco-de-respuestas.md` con respuestas veraces para las preguntas de filtro más comunes de los portales, usando estas reglas de sueldo: texto libre → «A convenir»; numérico en mi moneda → mi piso o el mínimo del rango publicado si es mayor; numérico USD → mínimo del rango publicado o mi último sueldo en USD.
4. Mi **CV maestro** de 1 página en formato ATS (reglas en `docs/03-cv-profesional-ats.md`) y una **variante enriquecida por cada familia de puestos** que aplique a mi perfil (más versión en inglés de la familia principal si busco remoto internacional). En cada variante cambian orden, énfasis y título — nunca los hechos.
5. Un resumen final: qué portales usaré, qué CV debe quedar guardado en cada portal, y qué quedó marcado como NO USAR por falta de confirmación.

Cuando yo apruebe el CV maestro, me recuerdas subirlo como CV guardado en cada portal antes de la primera corrida.

---
