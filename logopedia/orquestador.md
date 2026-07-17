# Orquestador — App de logopedia

**Fecha:** 2026-07-17
**Entrada:** 4 dictámenes independientes (tribunal.md). Única voz que los lee juntos.
**Criterio dominante de ponderación:** aprendizaje + pivote healthtech.

---

## 1. Resumen de veredictos

| Frente | Veredicto | Núcleo |
|---|---|---|
| T1 Mercado | **NO APTO** (formulación actual) | Dolor real (1 logopeda/122.800 hab. en Madrid, listas de espera duplicadas), pero 3 productos españoles ya atacan el hueco (LogopediaApp con convenios de colegios, Logopedy APS, SandiApp). TAM B2B minúsculo (~8.000 colegiados). El modelo dual sin cliente definido es el patrón que el mercado castiga; colegios en modo anti-intrusismo ante informes de un dev individual. |
| T2 Técnica | **NO APTO** | Evaluación + terapia adaptativa + informes clínicos = producto sanitario clase IIa (MDR regla 11) sin lectura alternativa: €60k-150k iniciales + €20k-50k/año, inviable para un individuo. RGPD: datos de salud de MENORES + LLM = punto radiactivo. ASR infantil patológico en español: no honesto en 2026. ARASAAC prohíbe uso comercial. Julius no es logopeda: colaborador clínico = requisito estructural. Existe descope defendible (práctica sin evaluación + registro bruto on-device). |
| T3 Aprendizaje | APTO CON CONDICIONES | Alineamiento 90% — el paquete completo del pivote. Pero ejecutada HOY: 4 incógnitas simultáneas → riesgo de no-entrega 75-80%, densidad 5/10. Orden vinculante: (1) esqueleto técnico en proyecto menor, (2) RealAudio para regulación en dominio propio, (3) esta como capstone (densidad 8,5/10, riesgo ~35%). |
| T4 Alcance | **NO APTO** (MVP dual) | El "MVP" son 6 productos: 235-575 sesiones ≈ 9-23 años a cuota real. Pesa más que el resto de la cartera junta. Vía admisible: peldaño 0 (documento de dominio validado con UN logopeda, 0 código, 6-10 sesiones); techo a 12 meses = peldaño 2 (registro de actividad exportable, nunca "informe clínico"). |

## 2. Contradicciones y resolución

**Tres NO APTO contra el 90% de alineamiento de T3.** Igual que en RealAudio pero más extremo: nadie niega el valor del destino; los tres NO APTO describen el coste del camino directo. T3 mismo dice que ejecutarla hoy sería NO APTO. La síntesis es unánime aunque los veredictos no lo parezcan: **esta idea no se ejecuta ahora como producto; se convierte en el norte de la cartera y se recorre por peldaños.**

**Convergencia independiente decisiva:** T3 ("orden vinculante: esqueleto → RealAudio → capstone") y T4 ("norte estratégico por peldaños, esqueleto entrenado en otra idea menor") proponen la MISMA secuencia sin haberse leído. T2 aporta la línea regulatoria que hace posible cada peldaño sin certificación; T1 aporta el requisito de socio clínico que T2 también exige por vía técnica (contenido terapéutico no autovalidable por un audiólogo).

**Palabras prohibidas (T2+T4 coinciden):** "informe clínico", "evaluación", "terapia adaptativa" — mientras no haya empresa, capital y certificación. El vocabulario superviviente: "ejercicios de práctica", "registro de actividad exportable", "sin interpretación clínica".

## 3. Estrategia óptima reformulada

**"Norte estratégico por peldaños"** — la idea no se mata: se convierte en la columna vertebral de la cartera, con esta escalera:

- **Peldaño 0 — AHORA (6-10 sesiones, 0 código):** documento de dominio + modelo de datos clínico de la logopedia digitalizada, **validado con UN logopeda real** (Julius tiene red clínica de 10 años para encontrarlo). Test de vida o muerte: si no consigue un logopeda interesado, la idea se archiva sin gastar más. Este documento es además pieza de portfolio healthtech inmediata.
- **Peldaños intermedios (fuera de esta ficha):** esqueleto .NET moderno + Postgres + informes en el laboratorio ScoringNews; decisión regulatoria y disciplina metrológica en RealAudio (dominio propio).
- **Peldaño 1 (cuando el esqueleto exista):** prototipo de UN tipo de ejercicio con progresión, datos sintéticos, cara del clínico primero (sesión→datos→registro exportable). Sin ASR, sin LLM sobre datos reales, sin menores reales, on-device/seudonimizado.
- **Peldaño 2 (techo a 12 meses):** registro de actividad exportable para el logopeda colaborador — nunca denominado "informe clínico".
- **Peldaño 3+ (otra vida de la idea):** si hay tracción clínica real, la vía es B2B-first con cofundador clínico y empresa — decisión empresarial, no de side-project; exigiría tribunal nuevo.

## 4. Veredicto propuesto

**PIVOTE** — cambios concretos sobre la idea original:
1. De "app dual ejecutable" a **norte estratégico por peldaños**: solo el peldaño 0 se autoriza ahora; cada peldaño posterior exige el anterior cerrado + puertas del pipeline.
2. Requisito estructural no negociable: **un logopeda colaborador real desde el peldaño 0**. Sin él, archivo automático.
3. Vocabulario y alcance fuera de MDR mientras no haya empresa: ejercicios de práctica + registro de actividad exportable; prohibido "evaluación", "terapia adaptativa" e "informe clínico" (T2).
4. Sin ASR de habla infantil, sin LLM sobre datos de pacientes reales, sin menores reales en ninguna prueba de los peldaños 0-2.
5. La secuencia de cartera queda vinculada: esqueleto (ScoringNews) y regulación (RealAudio) son prerequisitos declarados del peldaño 1 (T3/T4 convergentes).

**Decisión de Fase 2b: pendiente de Julius.**
