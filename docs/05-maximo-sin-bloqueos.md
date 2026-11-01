# 05 · El máximo de propuestas al día, sin bloqueos (la versión honesta)

Empecemos por lo que este documento **no** es: no hay un truco para postular como bot «sin que te detecten». Los portales detectan patrones, no intenciones — y cualquier sistema que intente *esconder* que automatiza (rotar IPs, falsear huellas de navegador, resolver captchas con servicios de terceros, crear cuentas espejo) está violando los términos del portal y termina igual: cuenta muerta, y a veces datos quemados con los reclutadores.

La buena noticia: **no necesitas ningún truco**. El sistema de este repo ha sostenido 15–25 postulaciones diarias, 300+ acumuladas, con **cero bloqueos**, porque cada postulación cumple, en sustancia, todo lo que el portal quiere ver. Esto es lo que en la práctica marca la diferencia:

## 1. Cuenta real, sesión real, datos reales
- Una sola cuenta por portal, a tu nombre, con tu correo y tu teléfono.
- La sesión se mantiene viva como la de cualquier usuario (el navegador del agente conserva tu login). Los re-logins se hacen contigo presente.
- Nada de granjas de cuentas ni correos desechables: los portales cruzan esos datos y los reclutadores también.

## 2. Solo la vía oficial de postulación
- El botón del portal («Postularme», «Easy Apply») y nada más. Nada de scripts que envíen formularios por fuera, nada de APIs no oficiales.
- Si el portal muestra un captcha o una verificación, **se detiene y te avisa**. Resolverlo tú tarda 20 segundos; «resolverlo» con un servicio externo es exactamente el comportamiento que los sistemas anti-bot están diseñados para castigar.

## 3. Ritmo humano (aquí está el «máximo» real)
Los bloqueos y verificaciones llegan por *patrón*, no por total acumulado:

| Patrón que dispara alertas | El ritmo de este sistema |
|---|---|
| 60 postulaciones en 20 minutos | 15–25 **en todo el día**, en una corrida matutina con pausas naturales entre vacante y vacante |
| Todo el volumen a un solo portal | Repartido entre 4–5 portales según dónde esté el encaje |
| Postular a todo, sin leer | Cada postulación pasa 7 filtros; la tasa de «postula lo que ve» es bajísima |
| Respuestas de filtro idénticas y falsas | Respuestas veraces de un banco de datos confirmado, que varían porque las vacantes varían |
| Horarios imposibles (3:00 am en ráfaga) | Corrida ~08:30 hora local, como cualquier persona que busca empleo en serio |

Conclusión práctica: **el máximo sostenible no es un número mágico, es un ritmo**. 20 buenas postulaciones diarias durante 15 días (300) consiguen más entrevistas que 200 en un fin de semana seguidas de una cuenta restringida.

## 4. Calidad como camuflaje perfecto (porque no es camuflaje)
La señal más fuerte de «bot» para un portal no es técnica: es un usuario que postula a puestos absurdos para su perfil. Un contador postulando a chofer, cocinero y programador senior en la misma hora parece automatización descuidada *incluso si lo hizo a mano*. El embudo del doc 04 —piso salarial, modalidad, idioma real, experiencia posible— mantiene tu patrón de postulación indistinguible del de un profesional enfocado. Porque lo es.

## 5. Si un portal te pide verificación (pasará algún día)
Es normal y no es un bloqueo:

1. El agente se detiene en ese portal (sigue con los demás) y te lo reporta en el resumen.
2. Tú inicias sesión presente en pantalla; resuelves SMS/captcha en el momento.
3. La siguiente corrida retoma ese portal con normalidad.
4. **Jamás** se reintenta en bucle contra una verificación: insistir convierte una verificación de rutina en una restricción de verdad.

## 6. Señales de que debes bajar el ritmo (y hacerle caso al agente)
- Dos verificaciones en la misma semana en el mismo portal → baja ese portal a la mitad de volumen por 7 días.
- Mensajes del portal sobre «actividad inusual» → pausa total de ese portal 72 h y revisión manual contigo.
- Rechazo masivo (>80%) en una familia de puestos → el problema no es el portal: es el encaje o el CV de esa variante. Se ajusta el filtro, no se postula más fuerte.

## En resumen

```
Máximo de propuestas sin bloqueos =
  cuenta real + vía oficial + 15–25/día repartidas
  + filtros que solo dejan pasar encajes reales
  + respuestas 100% veraces + log anti-duplicados
  + verificaciones resueltas por ti, sin insistir
```

Eso es todo. Es aburrido, es legal, respeta los términos de cada portal — y es exactamente lo que ha funcionado en producción.
