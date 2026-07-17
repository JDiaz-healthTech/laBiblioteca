# Ficha — Mantenimiento de vehículo (v2)

**Fase:** 1 completada — pendiente decisión de Julius (2b)
**Actualizada:** 2026-07-17 (tras tribunal; la v2 completa no sobrevivió)

## Problema
Registrar una intervención de taller a mano es tedioso; la información ya está en el ticket/factura. (El problema original de la ficha — "los conductores no saben qué toca" — quedó desacreditado en T1: apps de fabricante, CARFAX gratis y el Libro Taller Electrónico de la DGT ya lo cubren.)

## Usuario objetivo
Julius con su propio coche. El "conductor particular no técnico" murió en Fase 1: es el segmento que ni registra ni paga.

## Propuesta de valor (una frase)
Módulo quirúrgico sobre la v1 existente: fotografiar el ticket de taller → extracción estructurada (on-device por defecto) → autorrelleno de la intervención con validación contra la plantilla del propio coche — como banco de pruebas del pipeline de extracción de documentos que luego se reutilizará en healthtech.

## Relación con el pivote healthtech
Tangencial pero real (~70-75% del módulo según T3): "foto de documento semiestructurado → extraer campos → validar contra un perfil" es isomorfo a procesar informes clínicos/audiogramas escaneados. La v2 completa diluía esa transferencia al 20-25%.

## Hechos verificados por el tribunal (2026-07-17)
- El repo de la v1 NO está en la cuenta pública JDiaz-healthTech → publicarlo/auditarlo es condición previa y pieza de portfolio barata.
- VIN: NHTSA vPIC solo cubre mercado US; APIs europeas de pago (~0,20 €/consulta); VIN = dato personal (TJUE C-319/22). **Eliminado.**
- Plantillas por modelo: sin fuente abierta; solo honestas como tabla genérica editable con disclaimer. **Plantillas universales eliminadas.**
- OCR de facturas: ML Kit on-device gratis; LLM cloud fracciones de céntimo/ticket pero mete matrícula/NIF en cloud → opt-in con decisión RGPD documentada.
- Mercado: OCR+IA de tickets ya en producción en ≥4 competidores; monetización descartada.

## Veredicto del orquestador (propuesto, pendiente 2b)
**PIVOTE** — la v2 muere; sobrevive el módulo de extracción de tickets sobre la v1: 8-15 sesiones, timebox 15, dataset propio ≥30 tickets con métricas por campo, esquema/prompts/matching a mano, compuerta de precisión ("si corrige menos de lo que teclea, se cierra"). Al terminar, las horas van a healthtech reutilizando el pipeline. Detalle en `orquestador.md`; dictámenes íntegros en `tribunal.md`.

## Estado
V1 funcional en uso personal (repo privado/no localizado). Módulo sin empezar, condicionado a 2b.
