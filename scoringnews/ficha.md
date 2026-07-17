# Ficha — ScoringNews (repo Prism)

**Fase:** 1 completada (tribunal completo, reevaluación desde cero) — pendiente decisión de Julius (2b)
**Actualizada:** 2026-07-17

## Problema
Consumir noticias con un scoring de credibilidad que filtre el ruido — para Julius como lector. **Corrección del tribunal:** se elimina "potencialmente público general" (T1: no existe demanda de pago por scoring puro; riesgo reputacional de publicar scores; acceso a contenido hostil y encareciéndose. Verificado 2026-07-17).

## Usuario objetivo
Julius, exclusivamente. Uso personal + laboratorio de aprendizaje.

## Propuesta de valor (una frase)
Laboratorio del esqueleto .NET moderno (API + Postgres + pipeline LLM + informes) que Julius necesita para su futura app clínica, ejercitado sobre un dominio sin riesgo (noticias) y con un producto personal utilizable como subproducto.

## Relación con el pivote healthtech
No temáticamente; sí técnicamente (~40-45% según T3): fontanería completa del stack previsto para logopedia, sin el dominio clínico ni RGPD sanitario. T3 deja constancia de la vía alternativa superior en alineamiento (logopedia con datos sintéticos, ~85-90%); la decisión entre ambas es de Julius.

## Estado real (verificado 2026-07-17, clon de `JDiaz-healthTech/Prism`)
- 2 commits del 12-ago-2025 (11 meses parado). El esqueleto Clean Architecture es atrezzo: la app nunca arrancó (endpoint mapeado tras `app.Run()`, handler sin registrar en DI), entidades vacías, score hardcodeado a 78, integración LLM al 0%.
- `/health` filtra la connection string; `bin/obj/.vs/.env` commiteados, sin `.gitignore`.
- Ingesta prevista atada a Newscatcher (API B2B de pago, v2 obsoleta) — se sustituye por RSS propio.
- .NET 8 sale de soporte el 10-nov-2026 → retarget a .NET 10 LTS.

## Veredicto del orquestador (propuesto, pendiente 2b)
**PIVOTE** — dos etapas con puerta: spike de consola (6-10 sesiones, score congelado por escrito, pruebas de vida a 14 días y 4 semanas con decaimiento automático a NO-GO) → laboratorio (techo global 80 h/3 meses: API + migraciones + un informe + despliegue). Sin cliente de lectura, sin dedupe/pgvector, sin publicación de scores. Cesión automática del remanente de horas a logopedia. Detalle y comparación con la crítica previa de 2026-07-16 en `orquestador.md`; dictámenes íntegros en `tribunal.md`.

## Nota sobre la Fase 1 previa
El tribunal (sin leer la crítica previa) convergió en 4 de sus 5 condiciones. Divergencias: elimina el cliente Blazor, retira pgvector del MVP, añade retarget .NET 10 y mecanismos de decaimiento. La especificación v2 congelada debe revisarse antes de descongelarse.
