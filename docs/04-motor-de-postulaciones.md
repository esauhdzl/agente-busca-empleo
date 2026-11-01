# 04 · El motor de postulaciones diarias

Esto corre cada mañana, solo. Tú recibes el resumen. Así decide el agente, en este orden, con cada vacante que encuentra:

## El embudo

```
Buscar → Dedupe (log) → Filtros duros → Ranking → Postular (1 clic) → Registrar
```

### 1. Buscar
En todos tus portales, con las búsquedas derivadas de tus criterios: puestos de tus familias, tu ciudad (si es presencial) y «remoto» en tu país (y LATAM/internacional si tu perfil lo permite).

### 2. Dedupe contra el log — antes que nada
Cada vacante se cruza con `applications-log.md` por empresa + puesto + portal:
- Si ya se postuló → es **repost**: se anota como repost, **no** se cuenta como nueva y **no** se vuelve a postular.
- Las empresas se normalizan (mayúsculas/minúsculas, razones sociales tramposas tipo «EMPRESA CONFIDENCIAL» se marcan como dudosas y solo se postula si todo lo demás encaja).

### 3. Filtros duros (un «no» en cualquiera = fuera)

| Filtro | Regla |
|---|---|
| Sueldo | Publicado o estimado ≥ tu piso. Si el sueldo es claramente menor, fuera aunque el puesto sea bonito. |
| Modalidad | Remoto, o presencial/híbrido dentro de tu zona y solo si supera tu condición (ej. «considerablemente mejor que mi empleo actual»). |
| Idioma | Si exige un nivel mayor a tu nivel **real** confirmado, fuera. (Ej.: «inglés avanzado/fluido en vivo» con B1 confirmado → fuera.) |
| Exclusiones | Tu lista del Bloque G: comisión 100%, call centers, giros excluidos, empresas marcadas. |
| Experiencia imposible | Si pide una herramienta o trayectoria que objetivamente no tienes (ej. «3 años en QuickBooks Online» y nunca lo usaste), fuera. |
| Señales de estafa | Piden dinero, «inversión», documentos por Telegram/WhatsApp personal, sueldos imposibles para el puesto, empresa imposible de verificar → fuera **y queda marcada para siempre** en el log. |
| Forma de postulación | Solo «postulación fácil / 1 clic». Si exige carta, ensayo, video, portafolio o crear cuenta en otro sistema → se salta y se anota (salvo tu excepción aprobada, ver abajo). |

### 4. Ranking de las que sí pasan
- **Track A — Paga:** sueldo mayor primero; USD antes que moneda local a igualdad de condiciones; remoto antes que presencial.
- **Track B — Crecimiento** (si lo activaste): aprendizaje, calidad del equipo, misión y futuro del sector pesan más que el sueldo (sin cruzar el piso).

### 5. Postular — solo 1 clic
- Se usa el botón oficial del portal («Postularme», «Easy Apply», «Postulación fácil»).
- Las preguntas de filtro se responden **solo** desde tu banco de respuestas veraz (doc 02).
- Pregunta sin respuesta confirmada → la vacante se salta. Sin excepciones, sin «más o menos».
- Sueldos en campos: texto libre «A convenir»; numérico local = piso o mínimo del rango publicado; numérico USD = mínimo del rango o tu último sueldo USD.
- **La única excepción típica:** un campo corto obligatorio tipo «¿Por qué te interesa trabajar en [empresa]?» (50–1000 caracteres) puede responderse con 2–3 frases **veraces** armadas desde tu perfil y tu motivación declarada, sin inventar datos de la empresa. Cualquier otra redacción (cartas completas, ensayos largos) sigue fuera.

### 6. Registrar — todo, siempre
Cada postulación (y cada repost y cada salto con motivo) entra al log el mismo día:

```markdown
| Fecha | Empresa | Puesto | Portal | Sueldo publicado | Modalidad | Estado | Notas |
```

El resumen diario que recibes: total nuevas del día, acumulado, las 3–5 notables (mejor paga/encaje), los saltos con motivo agrupado y cualquier alerta (empresa sospechosa, portal que pidió re-login).

## Volúmenes sanos (la experiencia real detrás de estos números)

- **Días 1–3:** 8–12 postulaciones/día. Estás calibrando filtros.
- **Régimen estable:** 15–25/día repartidas entre 4–5 portales (ningún portal recibe todo el volumen).
- Con ese ritmo, un sistema bien filtrado llega a **100 postulaciones en ~1 semana** y a **300+ en dos semanas** sin una sola advertencia de los portales — porque cada postulación es indistinguible de una manual bien hecha: porque, en lo que importa, *es* una manual bien hecha, solo que la hace el agente.
- Más volumen que eso no produce más entrevistas: produce peores encajes y respuestas de filtro forzadas. El cuello de botella real no es el portal, es la cantidad de vacantes **que sí encajan contigo** que existen ese día.

## Mantenimiento del sistema (5 min cuando el agente te lo pida)

- **Re-login de portales:** las sesiones caen de vez en cuando (Indeed con Google es el clásico). El agente te avisa; lo resuelves tú presente, en 1 minuto. Nunca intentes que el agente «adivine» códigos SMS.
- **Decisión del CV guardado:** si la mayoría de tus postulaciones son de una familia, evalúa cambiar el CV guardado de los portales a esa variante (doc 03).
- **Ajuste de criterios:** tu piso, tus exclusiones y tus tracks los cambias tú con una frase («a partir de hoy, también startups de IA»); el agente lo registra y aplica desde la siguiente corrida. **Cada cambio de criterio queda escrito** — el agente te lo confirma el mismo día («Registrado el cambio: …»).

## Lo que el agente hace con las respuestas

- **«Vieron tu CV» / cambios de estado sin texto:** se acumulan y se te resumen para que los revises en una sola sesión semanal en el portal.
- **Encuestas de «¿la empresa te contactó?»:** la regla es responder SÍ solo si te contactaron de verdad (correo/WhatsApp). Una vista de CV **no** es contacto.
- **Respuesta de reclutador / invitación a entrevista:** alerta inmediata por la Fase 3, con contexto y, si aplica, un borrador de respuesta listo para que lo apruebes. El agente **no** responde por ti a personas sin tu confirmación.
