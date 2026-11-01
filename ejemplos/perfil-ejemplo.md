# Ejemplo de perfil llenado (ficticio)

> «María Ejemplo» no existe. Este ejemplo muestra cómo se ve el resultado de la
> Fase 0 cuando el agente termina la entrevista: datos concretos, cifras reales
> y honestidad en lo que no está confirmado.

## Perfil (extracto)
```yaml
datos_base:
  nombre_completo: "María Ejemplo Torres"
  ciudad: "Guadalajara, Jalisco"
  telefono: "+52 33 0000 0000"
  disponibilidad: "15 días; inmediata si se requiere"
educacion:
  - grado: "Lic. en Administración"
    institucion: "Universidad Ejemplo"
    anio_termino: ""            # María no estaba segura del año → NO se usa
    estado: "no_confirmado"
experiencia:
  - empresa: "Distribuidora Ejemplo SA"
    puesto: "Auxiliar contable"
    inicio: "03/2023"
    fin: "actualidad"
    cifras: ["Conciliaciones bancarias de $8M/mes", "200+ CFDI emitidos al mes"]
    herramientas: ["CONTPAQi", "Excel avanzado"]
    estado: "confirmado"
idiomas:
  - idioma: "Inglés"
    nivel_real: "B1"
    examen: "EF SET"
    estado: "confirmado"
dinero:
  piso_mxn_mes: 12000
  ultimo_sueldo: { monto: 10500, moneda: "MXN" }
```

## Criterios (extracto)
- **Piso:** $12,000/mes. **Remoto:** sí, todo México. **Presencial:** solo ZMG y solo si supera $18,000.
- **Track A:** contabilidad/finanzas/tesorería. **Track B:** startups y fintech.
- **Exclusiones:** ventas a comisión, call centers, empresas que pidan dinero o documentos por WhatsApp personal.
- **No usar:** año de graduación (no confirmado), «inglés avanzado» (su nivel es B1 y así se declara).

## Lo que esto produce en la práctica
- El CV maestro de María lidera con «Conciliaciones bancarias de $8M/mes» — no con «responsable y proactiva».
- Una vacante que pida QuickBooks Online se salta: María nunca lo ha usado, y el sistema prefiere perder esa vacante a quemar su credibilidad.
- Una vacante en inglés «advanced» se salta igual: su B1 está confirmado y se declara como B1.
