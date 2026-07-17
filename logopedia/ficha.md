# Ficha — App de logopedia

**Fase:** 1 completada — pendiente decisión de Julius (2b)
**Actualizada:** 2026-07-17 (tras tribunal; de producto ejecutable a norte estratégico por peldaños)

## Problema
Pacientes con dificultades de comunicación necesitan entrenamiento progresivo entre sesiones clínicas, y los especialistas datos objetivos de ese entrenamiento. El dolor es real y verificado (escasez pública: 1 logopeda/122.800 hab. en Madrid; listas de espera duplicadas — 2026-07-17).

## Usuario objetivo
Largo plazo: dual (paciente + logopeda). **Ahora mismo: UN logopeda colaborador real** — requisito estructural desde el peldaño 0 (Julius es audiólogo, no logopeda; el contenido terapéutico no es autovalidable).

## Propuesta de valor (una frase)
Norte estratégico del pivote healthtech, construido por peldaños: primero el documento de dominio clínico validado con un logopeda real, después prototipos con datos sintéticos sobre el esqueleto técnico entrenado en otras ideas de la cartera.

## Relación con el pivote healthtech
SÍ, núcleo (~90% según T3) — pero con riesgo de no-entrega del 75-80% si se ejecuta hoy como producto dual.

## Hechos duros verificados por el tribunal (2026-07-17)
- **MDR:** evaluación + terapia adaptativa + informes clínicos = producto sanitario clase IIa sin lectura alternativa. Certificación: €60k-150k iniciales + €20k-50k/año. Inviable para un individuo.
- **RGPD:** datos de salud de menores (art. 9) + LLM = radiactivo. Peldaños 0-2: sin menores reales, sin LLM sobre datos de pacientes, on-device/seudonimizado.
- **Mercado:** 3 productos españoles ya en el hueco (LogopediaApp, Logopedy APS, SandiApp); TAM B2B ~8.000 colegiados; colegios en modo anti-intrusismo. El modelo que sobrevive en terapia digital es B2B con prescriptor.
- **Técnica:** ASR de habla infantil patológica en español no es honesto en 2026; ARASAAC prohíbe uso comercial.
- **Alcance:** el "MVP" dual real son 6 productos: 235-575 sesiones (9-23 años a cadencia real) — más que el resto de la cartera junta.

## Veredicto del orquestador (propuesto, pendiente 2b)
**PIVOTE** → escalera de peldaños: **Peldaño 0 autorizado ya** (documento de dominio + modelo de datos validado con UN logopeda, 6-10 sesiones, 0 código; si no aparece logopeda → archivo). Prerequisitos del peldaño 1: esqueleto .NET (ScoringNews) + regulación (RealAudio). Techo a 12 meses: registro de actividad exportable — prohibido llamarlo "informe clínico". Peldaño 3+ (producto real) = empresa + cofundador clínico + tribunal nuevo. Detalle en `orquestador.md`; dictámenes íntegros en `tribunal.md`.

## Estado
Sin repo, sin código — por diseño. Peldaño 0 pendiente de decisión 2b.
