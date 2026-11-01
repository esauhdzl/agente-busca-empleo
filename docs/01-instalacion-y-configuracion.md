# 01 · Instalación y configuración

Tiempo total: ~20 minutos, una sola vez. Al terminar, el sistema corre solo.

## 1. El agente

Recomendado: **Muse** (app o web). Su plan gratuito es suficiente para operar este sistema porque el trabajo pesado —buscar, leer vacantes, postular— lo hace el agente en sesiones cortas y programadas, no en un chat infinito.

Lo que el agente necesita poder hacer (cualquier agente que cumpla sirve):

- ✅ Memoria persistente entre sesiones (recordar tu perfil y tu log).
- ✅ Navegador web real (entrar a los portales con tu sesión iniciada).
- ✅ Tareas programadas (correr solo cada mañana y revisar tu correo).
- ✅ Leer tu correo (para detectar respuestas de reclutadores).

> Si tu agente no tiene alguna de estas piezas, el sistema funciona en «modo manual asistido»: tú le pegas el prompt de la corrida diaria cada mañana. El resto de esta guía aplica igual.

## 2. Tus cuentas en portales de empleo

Crea o prepara tus cuentas **antes** de la entrevista inicial. El agente postula con tus cuentas reales, a tu nombre — eso es parte de por qué no hay bloqueos.

Portales base (México / LATAM; adapta a tu país):

| Portal | Nota |
|---|---|
| OCC Mundial | Guarda tu CV en el perfil: será el que use la mayoría de las postulaciones. |
| Indeed | La sesión con Google puede caducar; el re-login se hace contigo presente. |
| LinkedIn | Completa el perfil al 100%: muchas postulaciones «Easy Apply» jalan los datos de ahí. |
| Computrabajo | Igual que OCC: el CV guardado en el perfil manda. |
| Get on Board | Ideal para startups/tech. Login por enlace mágico al correo. |

Reglas de cuentas:

- **Un solo correo para todo** el sistema (crea uno dedicado si quieres separar tu vida: ej. `tunombre.buscaempleo@gmail.com`).
- Guarda cada credencial en el gestor seguro de tu agente/navegador. **Nunca** en un archivo de texto del repo ni en el chat sin cifrar.
- Sube a cada portal el **CV maestro** que el agente genere en la Fase 0 (ver doc 03). Ese CV guardado es el que realmente viaja en casi todas las postulaciones automáticas — por eso tiene que ser el bueno desde el día 1.

## 3. Conecta tu correo

El agente necesita leer (solo leer) el correo donde llegan las respuestas de los portales:

- Alertas de «tu CV fue visto», cambios de estado y cierres: útiles, pero ruido.
- Lo que importa: **respuestas de reclutadores e invitaciones a entrevista** → alerta inmediata (Fase 3).

## 4. Crea tu carpeta de trabajo

```
mi-busqueda/
├── perfil.yaml              ← lo llena el agente en la Fase 0
├── criterios-de-busqueda.md ← tus reglas
├── banco-de-respuestas.md   ← respuestas veraces para filtros
├── applications-log.md      ← el registro anti-duplicados
└── cv/
    ├── CV_Maestro.pdf       ← 1 página, ATS
    ├── CV_<Familia1>.pdf    ← variante por familia de puesto
    └── CV_<Familia1>_EN.pdf ← variante en inglés, si aplica
```

Copia las plantillas de [`templates/`](../templates) y renómbralas así. No las llenes tú: eso lo hace el agente preguntándote (doc 02).

## 5. Programa las dos tareas

En tu agente, crea dos tareas programadas:

| Tarea | Horario sugerido | Prompt |
|---|---|---|
| Corrida diaria de postulaciones | Diario ~08:30 (hora local), antes de que los reclutadores revisen su día | [`prompts/02-corrida-diaria.md`](../prompts/02-corrida-diaria.md) |
| Vigilancia de entrevistas | Cada 12 horas | [`prompts/03-vigilancia-de-entrevistas.md`](../prompts/03-vigilancia-de-entrevistas.md) |

Y pega **una vez**, en la conversación principal con tu agente, la instrucción permanente de [`prompts/00-agente-principal.md`](../prompts/00-agente-principal.md).

## 6. La primera corrida, supervisada

La corrida del día 1 hazla **contigo presente**:

- Revisa las primeras 5 postulaciones que el agente envíe: ¿los datos son correctos? ¿el CV es el correcto?
- Corrige en el momento cualquier dato mal interpretado y pídele que lo guarde en el perfil.
- A partir del día 2, el sistema corre solo y solo te llega el resumen diario y las alertas de entrevista.

## Checklist final

- [ ] Agente elegido y con memoria/navegador/tareas (o modo manual asumido)
- [ ] Cuentas creadas en los portales, credenciales guardadas de forma segura
- [ ] Correo conectado
- [ ] Carpeta de trabajo creada con las plantillas
- [ ] Prompt principal pegado
- [ ] Dos tareas programadas creadas
- [ ] Entrevista inicial realizada (doc 02) y CV maestro generado (doc 03)
- [ ] CV maestro subido como CV guardado en **cada** portal
- [ ] Primera corrida supervisada ✅
