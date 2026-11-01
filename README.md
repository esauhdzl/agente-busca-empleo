# Agente Busca-Empleo 🤖💼

**Un agente de IA que busca empleo por ti todos los días y postula automáticamente — configurado en una sola sesión de preguntas.**

Este repositorio es el paso a paso completo, con los prompts listos para copiar y pegar, para montar tu propio sistema de búsqueda de empleo automática con un agente de IA (recomendado: **Muse**, porque su plan gratuito alcanza para operar el sistema; cualquier agente con memoria, navegación web y tareas programadas sirve).

No es un bot de spam. Es el sistema real con el que se han enviado **300+ postulaciones reales en menos de dos semanas** sin un solo bloqueo de cuenta, y funciona por una razón simple: el agente postula como lo haría una persona cuidadosa — solo a vacantes que encajan, solo por la vía oficial de cada portal, a ritmo humano, con un CV hecho a la medida de cada familia de puestos y sin inventar **nada**.

---

## Cómo funciona (en 4 fases)

| Fase | Qué pasa | Archivo |
|---|---|---|
| **0. Entrevista inicial** | El agente te hace todas las preguntas necesarias —una sola vez— y con tus respuestas construye tu perfil, tu banco de respuestas y tu CV. Tú no redactas nada. | [docs/02-cuestionario-inicial.md](docs/02-cuestionario-inicial.md) |
| **1. CV profesional ATS** | El agente genera un CV maestro de 1 página que pasa los filtros automáticos (ATS) y variantes enriquecidas por familia de puesto (ej. contabilidad, operaciones, ventas). | [docs/03-cv-profesional-ats.md](docs/03-cv-profesional-ats.md) |
| **2. Corrida diaria automática** | Cada mañana el agente busca en los portales, filtra con TUS criterios, ordena por mejor paga/encaje y postula solo con «postulación fácil / 1 clic». Todo queda registrado en un log para no duplicar jamás. | [docs/04-motor-de-postulaciones.md](docs/04-motor-de-postulaciones.md) |
| **3. Vigilancia de entrevistas** | El agente revisa tu correo cada 12 horas y te avisa **al momento** si un reclutador responde o te invita a entrevista. Silencio si no hay nada. | [prompts/03-vigilancia-de-entrevistas.md](prompts/03-vigilancia-de-entrevistas.md) |

## Paso a paso

1. **[Instalación y configuración](docs/01-instalacion-y-configuracion.md)** — cuentas, portales, credenciales seguras y la tarea programada diaria (≈20 min, una sola vez).
2. **[La entrevista inicial](docs/02-cuestionario-inicial.md)** — pega el prompt, responde las preguntas del agente y deja que él construya tu CV y tu perfil.
3. **[CV profesional que pasa filtros](docs/03-cv-profesional-ats.md)** — las reglas ATS y el sistema de variantes por tipo de empleo.
4. **[El motor de postulaciones](docs/04-motor-de-postulaciones.md)** — criterios, ranking, reglas de sueldo, qué se salta y qué jamás se inventa.
5. **[El máximo de propuestas sin bloqueos](docs/05-maximo-sin-bloqueos.md)** — la parte honesta: no existe un truco para «que no te detecten». Existe un método que no necesita truco.

## Los prompts (copiar y pegar)

- [`prompts/00-agente-principal.md`](prompts/00-agente-principal.md) — la instrucción permanente del agente.
- [`prompts/01-entrevista-inicial-y-cv.md`](prompts/01-entrevista-inicial-y-cv.md) — la Fase 0: preguntas + construcción del CV.
- [`prompts/02-corrida-diaria.md`](prompts/02-corrida-diaria.md) — la tarea de cada mañana.
- [`prompts/03-vigilancia-de-entrevistas.md`](prompts/03-vigilancia-de-entrevistas.md) — la alerta de respuestas de reclutadores.

## Plantillas

- [`templates/perfil.yaml`](templates/perfil.yaml) — tu perfil estructurado (lo llena el agente, no tú).
- [`templates/criterios-de-busqueda.md`](templates/criterios-de-busqueda.md) — tus reglas: piso salarial, modalidad, exclusiones.
- [`templates/banco-de-respuestas.md`](templates/banco-de-respuestas.md) — respuestas veraces para las preguntas de filtro de los portales.
- [`templates/applications-log.md`](templates/applications-log.md) — el registro anti-duplicados.
- [`templates/cv-base.md`](templates/cv-base.md) — la estructura del CV maestro.
- [`ejemplos/perfil-ejemplo.md`](ejemplos/perfil-ejemplo.md) — un perfil ficticio ya llenado, para que veas el resultado esperado.

## Las 5 reglas que hacen que funcione

1. **Nada se inventa.** Si el agente no sabe un dato tuyo con certeza, esa vacante se salta. Un dato falso te quema en la primera entrevista.
2. **Solo postulación de 1 clic.** Cartas de presentación, ensayos, videos y portafolios quedan fuera (salvo una excepción corta y veraz que tú apruebes).
3. **Log o no pasó.** Cada postulación se registra con empresa, puesto, portal y fecha. Antes de postular, el agente revisa el log: si ya está, es *repost*, no se cuenta ni se duplica.
4. **Ritmo humano, horario humano.** El máximo sostenible sin bloqueos no se logra postulando 200 en una hora, sino 15–25 bien elegidas al día, distribuidas entre portales, todos los días. La constancia le gana al volumen bruto (ver [docs/05](docs/05-maximo-sin-bloqueos.md)).
5. **Tú decides los criterios; el agente ejecuta.** Piso salarial, modalidad, exclusiones y disponibilidad se fijan en la entrevista inicial y el agente no los cruza sin tu palabra.

## Aviso honesto

- Ningún método garantiza que un portal nunca te pida una verificación (SMS, captcha, re-login). Este sistema está diseñado para que eso sea raro y para resolverlo contigo en minutos cuando pase — no para evadirlo.
- Respeta los términos de cada portal: usa siempre su botón oficial de postulación. Este repo no contiene ni recomienda técnicas de evasión de captchas, huellas de navegador falsas ni cuentas múltiples.
- Tus datos reales (CURP, teléfono, CV con datos) **nunca** se suben a este repositorio: vive en las plantillas vacías y cada quien llena las suyas en privado.

## Licencia

MIT — úsalo, adáptalo y compártelo. Si te consigue empleo, cuenta la historia.
