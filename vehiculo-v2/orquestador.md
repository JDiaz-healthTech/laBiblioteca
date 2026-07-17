# Orquestador — Mantenimiento de vehículo (v2)

**Fecha:** 2026-07-17
**Entrada:** 4 dictámenes independientes (tribunal.md). Única voz que los lee juntos.
**Criterio dominante de ponderación:** aprendizaje + pivote healthtech.

---

## 1. Resumen de veredictos

| Frente | Veredicto | Núcleo |
|---|---|---|
| T1 Mercado | **NO APTO** | Categoría anclada en 0 € (CARFAX 50M+ gratis, apps de fabricante, Libro Taller Electrónico DGT+Ganvam en España). El "diferencial" OCR+IA ya está en producción en ≥4 competidores (2025-2026). Datos OEM/VIN europeos: de pago o inexistentes en abierto; VIN = dato personal (TJUE C-319/22). |
| T2 Técnica | APTO CON CONDICIONES | La v1 NO está en la cuenta pública (verificado 2026-07-17) → no auditable. NHTSA vPIC inservible para parque europeo → VIN degradado a gadget opcional. Plantillas solo genéricas y editables con disclaimer. OCR viable: ML Kit on-device por defecto, LLM cloud solo opt-in (RGPD: matrícula/NIF en facturas). Sin backend. |
| T3 Aprendizaje | **NO APTO** (v2 completa) | 75-80% re-ejecución de terreno conocido (densidad 2-3/10) que congela el pivote. Vía de rescate explícita: spike quirúrgico OCR/LLM sobre la v1 (30-40 h) = APTO CON CONDICIONES, con ~70-75% de transferencia a healthtech (extracción de documentos ≈ informes clínicos escaneados). |
| T4 Alcance | APTO CON CONDICIONES | Reconstrucción: 49-96 sesiones (2-8 años reales) → no apto. V2 incremental completa: 36-71 sesiones → no apto. Solo defendible el escenario mínimo: módulo foto-ticket→autorrelleno sobre v1, 8-15 sesiones, timebox 15 con compuerta de precisión. |

## 2. Contradicciones y resolución

**No hay contradicciones de fondo: hay una convergencia inusual.** T3 y T4, desde frentes distintos y sin leerse, proponen EXACTAMENTE el mismo rescate: abandonar la v2 como proyecto y quedarse con el módulo de extracción de tickets injertado en la v1. T2 aporta los límites técnicos del módulo (on-device por defecto, taxonomía cerrada primero, set de facturas reales antes del matcher) y T1 confirma que no hay razón mercantil para nada más ambicioso.

**Única tensión formal:** T3 declara la v2 NO APTO y exige que el spike se "re-presente" como idea distinta. Resolución idéntica al criterio general del pipeline: el veredicto PIVOTE existe precisamente para esto — la reformulación se compone solo de elementos ya juzgados por los cuatro frentes (módulo de T3-rescate, escenario 3 de T4, condiciones técnicas de T2), así que la ficha reescrita queda cubierta por este tribunal. Cualquier ampliación posterior (VIN, plantillas universales, backend, publicación) exigiría tribunal nuevo.

**Hallazgo lateral de T2 que se eleva a condición:** la v1 no está publicada. Para un perfil que necesita portfolio, una app completa invisible es valor desperdiciado — publicar el repo v1 (tras revisar que no contenga datos personales) es una tarea de ~1 sesión con retorno inmediato.

## 3. Estrategia óptima reformulada

**"Módulo de extracción de tickets sobre la v1"** — 8-15 sesiones, timebox duro 15:

1. **Sesión 0-1:** publicar/auditar el repo de la v1 (sin datos personales dentro). Congelar la v1: prohibida toda reconstrucción.
2. **Sesiones 1-3 — Diseño a mano:** taxonomía cerrada de conceptos de factura (aceite, filtros, frenos...), esquema de extracción, dataset propio de ≥30 tickets reales anotados (T3-3, T2-6). Esto es lo que transfiere a healthtech: es el mismo problema que extraer datos de un informe clínico escaneado.
3. **Sesiones 4-9 — Pipeline:** cámara → ML Kit on-device por defecto (LLM cloud solo opt-in explícito con aviso) → extracción estructurada → pantalla de corrección manual → validación contra la plantilla de SU coche (genérica, editable, con disclaimer).
4. **Sesiones 10-13 — Evaluación:** métricas por campo sobre el dataset, comparando al menos dos enfoques de extracción. **Compuerta de T4:** si corrige menos de lo que teclea, el módulo se cierra y la v1 queda como estaba.
5. **Sesiones 14-15 — Cierre:** README con métricas y decisiones. Las horas siguientes van a la cartera healthtech aplicando este mismo pipeline a un documento clínico (T3-4).

**Fuera, sin excepción:** VIN, plantillas universales por modelo, backend, notificaciones nuevas, exportación, multi-vehículo, nube, cualquier expectativa mercantil.

## 4. Veredicto propuesto

**PIVOTE** — la v2 muere; sobrevive el módulo:
1. De "v2/reconstrucción" a **spike quirúrgico de extracción de documentos sobre la v1** (8-15 sesiones, timebox 15, compuerta de precisión).
2. Eliminar VIN y plantillas por modelo (datos inexistentes en abierto para el parque europeo; T1/T2 coinciden).
3. On-device por defecto; cloud solo opt-in; decisión RGPD documentada antes de cualquier publicación.
4. Esquema, prompts, matching y evaluación escritos a mano; dataset ≥30 tickets con métricas por campo (el núcleo de aprendizaje).
5. Publicar la v1 auditada como pieza de portfolio (~1 sesión).
6. Al cierre, las horas liberadas se redirigen a la cartera healthtech reutilizando el pipeline aprendido.

**Decisión de Fase 2b: pendiente de Julius.**
