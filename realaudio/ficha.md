# Ficha — RealAudio

**Fase:** 1 completada — pendiente decisión de Julius (2b)
**Actualizada:** 2026-07-17 (tras tribunal; la ficha original prometía capacidades que Android no permite)

## Problema
Personas con posible pérdida auditiva no tienen forma accesible de estimar su audición — y Julius no tiene aún ninguna pieza de portfolio que una sus 10 años de audiología con su perfil de desarrollador.

## Usuario objetivo
**Corregido por el tribunal:** Julius, su familia y los entrevistadores healthtech. El B2C Android murió en Fase 1 (T1: categoría a 0 €, absorbida por SO/firmware; Mimi abandonó este segmento en 2024).

## Propuesta de valor (una frase)
Laboratorio personal de audiología aplicada: motor de cribado psicoacústico hecho a mano (staircase adaptativo, test-retest, gate de ruido, umbrales relativos) + demo de compensación EQ en reproductor propio, con decisión regulatoria documentada.

## Relación con el pivote healthtech
SÍ, directo — la más alineada de la cartera (~90-95% según T3, densidad de aprendizaje 70-80%/hora si el núcleo se hace a mano).

## Hechos duros verificados por el tribunal (2026-07-17)
- **EQ de llamadas: imposible** para apps de terceros desde Android 10. **EQ global (sesión 0): deprecada y ruleta OEM.** **ANC: sin API pública.** Se eliminan de la ficha, no se aparcan.
- **Frontera MDR:** "estima pérdida + deriva a clínica" publicado = software producto sanitario clase IIa (MDCG 2019-11, regla 11). Certificación inviable para un individual; Mimi perdió su CE en mayo 2024. La app se mantiene como cribado orientativo no diagnóstico, uso personal, datos on-device, sin dB HL absolutos.
- Sin transductor calibrado no hay validez clínica de umbral: se trabajan umbrales relativos + cuaderno de incertidumbre validado contra el audiograma real de Julius.

## Veredicto del orquestador (propuesto, pendiente 2b)
**PIVOTE** → "AudioLab personal": Fase A motor de test a mano (con bloque regulatorio al inicio y kill criterion a 6 semanas) → Fase B demo EQ en app propia. Techo 42 sesiones, exige ≥2 sesiones/semana prioritarias o se aparca sin ejecutar. Logopedia congelada hasta cerrar Fase A. Cualquier ampliación (tienda, claims, hardware) = tribunal nuevo. Detalle en `orquestador.md`; dictámenes íntegros en `tribunal.md`.

## Estado
Idea sin repo. Full Kotlin. Sin empezar — condicionada a la decisión 2b y a la priorización de sesiones.
