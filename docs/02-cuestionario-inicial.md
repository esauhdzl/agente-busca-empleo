# 02 · La entrevista inicial: el agente pregunta, tú solo respondes

La idea central del sistema: **tú no llenas formularios ni redactas tu CV**. Al principio, el agente se dedica a hacerte preguntas —en bloques cortos, en lenguaje normal— y con tus respuestas construye solo:

1. Tu **perfil estructurado** (`perfil.yaml`)
2. Tu **banco de respuestas** para las preguntas de filtro de los portales
3. Tu **CV maestro** y sus variantes por familia de puesto

El prompt exacto para arrancar esta fase está en [`prompts/01-entrevista-inicial-y-cv.md`](../prompts/01-entrevista-inicial-y-cv.md).

## Los bloques de preguntas

El agente pregunta por bloques (puedes responder por partes, incluso por notas de voz):

### Bloque A · Datos base
- Nombre completo tal como va en documentos oficiales
- Ciudad y colonia/zona donde vives; ¿hasta dónde te desplazarías?
- Teléfono y correo de contacto (el que va impreso en el CV)
- Fecha de disponibilidad: ¿inmediata? ¿15 días? ¿otra?

### Bloque B · Educación
- Nivel y carrera exactos (ej. «PTB en Contabilidad, CONALEP») — **como dice tu documento**
- Institución y año de término **solo si estás seguro**; si dudas, el agente lo deja fuera antes que inventarlo
- Cursos, certificaturas y sistemas que sí dominas (con nombre exacto: CONTPAQi, SAP, Excel…)

### Bloque C · Experiencia (empleo por empleo)
Para cada empleo, el agente pregunta:
- Empresa, puesto, fechas (mes/año)
- ¿Qué hacías en 3–5 verbos? ¿Qué **números** movías? (montos, volumen, personas, % de mejora)
- ¿Qué herramientas usabas ahí?

> Los números son el oro del CV: «conciliaciones de $30M+/mes» vale diez veces más que «responsable y proactivo». Si no recuerdas una cifra exacta, se usa un rango honesto o se omite.

### Bloque D · Idiomas (con honestidad calibrada)
- Nivel real por idioma, con referencia: A2 / B1 / B2 / C1.
- Si tienes examen (EF SET, TOEFL…), el resultado manda.
- **Regla dura:** el nivel declarado es el real. Postular a vacantes que exigen un nivel mayor con un nivel inflado solo produce rechazos y quemones; el sistema las filtra, no las disfraza.

### Bloque E · Dinero
- Sueldo mínimo aceptable (piso duro: por debajo, no se postula)
- Último sueldo (solo se usa cuando un portal lo exige como campo obligatorio)
- ¿Aceptas sueldo en USD / pago desde el extranjero?

### Bloque F · Forma de trabajo
- Modalidad: ¿remoto? ¿presencial? ¿híbrido? ¿presencial solo si paga cuánto más?
- Zona/horario: turnos que sí y que no
- Disponibilidad para viajar o reubicarte: sí/no/depende

### Bloque G · Exclusiones (lo que jamás)
Ejemplos reales que la gente pone:
- Ventas 100% a comisión
- Call centers / atención telefónica intensiva
- Esquemas que pidan dinero, documentos por canales no oficiales (¡bandera de estafa!) o «inversión inicial»
- Giros o empresas específicas que no quieres

### Bloque H · Datos sensibles, solo bajo demanda
- CURP / RFC / documento de identidad: se guardan cifrados y **solo** se usan cuando una postulación los exige como campo obligatorio. Nunca van en el CV impreso ni en este repo.
- Referencias: solo si decides darlas; por defecto el sistema **salta** las vacantes que las exigen.

### Bloque I · Tu «track B» (opcional pero poderoso)
Además del track «mejor paga», mucha gente tiene un segundo criterio: startups, empresas de tecnología, trabajo con misión, aprender algo nuevo. El agente lo registra como track separado con su propio ranking (aprendizaje/equipo/misión), manteniendo el mismo piso salarial.

## Qué hace el agente con tus respuestas

1. **Llena `perfil.yaml`** y te lo muestra para que confirmes cada dato. Lo que no confirmes, no se usa.
2. **Detecta huecos y contradicciones** y te pregunta solo eso («dijiste 2021–2024 en un empleo y 2022 en otro, ¿cuál es el bueno?»).
3. **Redacta tu banco de respuestas** ([plantilla](../templates/banco-de-respuestas.md)): las 20–30 preguntas de filtro que los portales repiten (años de experiencia por tema, herramientas, disponibilidad, pretensión salarial con la regla de abajo…).
4. **Construye tu CV** siguiendo el [doc 03](03-cv-profesional-ats.md) y te lo entrega para una revisión de 5 minutos.

## La regla de oro de esta fase

> **Lo que el agente no sepa con certeza, no lo usa.**
> En la corrida diaria, una vacante cuya pregunta de filtro no pueda responderse con datos confirmados **se salta y se anota** — jamás se rellena con un dato plausible. Esta regla es la que mantiene tu cuenta limpia y tu reputación intacta.

## Reglas de sueldo en campos de filtro (las fija esta entrevista)

- Campo de texto libre → «A convenir»
- Campo numérico en tu moneda → tu piso, o el mínimo del rango publicado si es mayor
- Campo numérico en USD → el mínimo del rango publicado; si no hay rango, tu último sueldo en USD
