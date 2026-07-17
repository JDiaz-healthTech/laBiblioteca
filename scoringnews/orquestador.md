# Orquestador — ScoringNews (repo Prism)

**Fecha:** 2026-07-17
**Entrada:** 4 dictámenes independientes (tribunal.md), emitidos SIN acceso a la crítica previa de 2026-07-16. Única voz que lee ambos.
**Criterio dominante de ponderación:** aprendizaje + pivote healthtech.

---

## 1. Resumen de veredictos

| Frente | Veredicto | Núcleo |
|---|---|---|
| T1 Mercado | **NO APTO** | Nadie paga por scoring de credibilidad puro; supervivientes venden otra cosa; acceso a contenido hostil y encareciéndose; riesgo reputacional (precedente NewsGuard-FTC). "Potencialmente público general" es humo. |
| T2 Técnica | APTO CON CONDICIONES | La vía técnica existe y es barata (RSS + readability + LLM en tareas verificables + score determinista, <$15/mes). El repo actual no la implementa: esqueleto de 2 días que nunca arrancó, connection string filtrada en `/health`. Retarget obligatorio a .NET 10 (net8.0 EOL 10-nov-2026). |
| T3 Aprendizaje | APTO CON CONDICIONES | Salto .NET 3.5→moderno + cadena LLM = mejor eje de empleabilidad disponible. Alineamiento pivote ~40-45%. Redefinir como "laboratorio del esqueleto", 80 h/3 meses, núcleo a mano. Señala vía superior: logopedia con datos sintéticos (~85-90%). |
| T4 Alcance | **NO APTO** (alcance actual) | MVP completo = 17-35 sesiones vs cuota real ~0,3-0,6 sesiones/semana → 7-27 meses. Velocidad empírica: cero (11 meses parado). Única vía reconsiderable: spike de consola 6-10 sesiones con trueque de prioridades explícito. |

## 2. Contradicciones y resolución

**T3 (laboratorio de 80 h) vs T4 (solo spike de 6-10 sesiones).** No es contradicción de fondo sino de granularidad: T4 exige demostrar ejecución antes de conceder alcance; T3 define el techo si la ejecución aparece. **Resolución:** estructura en dos etapas — el spike de T4 es la puerta de entrada; el laboratorio de T3 es el techo solo si el spike se completa en plazo.

**T1 (NO APTO) vs el resto.** T1 no tumba el proyecto porque su NO APTO aplica al producto de mercado, que se elimina de la ficha. Su consecuencia es de alcance: sin ambición pública, no hay cliente que construir ni scores que publicar (converge con T2-7 y con el recorte de UI de T3).

**Tensión no resuelta por los jueces (la señalo yo):** T3 admite que la vía de mayor alineamiento sería saltar directamente a logopedia con datos sintéticos. La ficha defiende ScoringNews como paso previo de menor riesgo para aprender el esqueleto ANTES de tocar dominio clínico. Ambas son defendibles; la decisión es de Julius en 2b, y el timebox con cesión automática de horas a logopedia (T3-1) acota el coste de equivocarse.

## 3. Estrategia óptima reformulada

**"Laboratorio de esqueleto .NET moderno, en dos etapas con puerta":**

**Etapa A — Spike de consola (6-10 sesiones, puerta de entrada):**
1. Antes de la primera línea: score de 3 componentes congelado por escrito; declarar qué ideas se aparcan para liberar 2 sesiones/semana (T4).
2. Sanear repo (T2-2), retarget .NET 10, reparar `Program.cs` (endpoint muerto, DI, connection string fuera de `/health`).
3. Pipeline mínimo: 1 fuente RSS → readability → LLM solo en tareas verificables (claims con cita textual) → score determinista → Postgres. Tope de tokens/día implementado.
4. **Prueba de vida:** commits con lógica de dominio real en 14 días (T3-5) y un análisis end-to-end demostrable en 4 semanas (T2-8). Si falla, NO-GO automático y las horas pasan a logopedia.

**Etapa B — Laboratorio (solo si A supera la puerta; techo total 80 h / 3 meses):**
API mínima + migraciones + un informe generado + despliegue público. Sin scraping, sin dedupe, sin UI de lectura, sin publicación de scores de medios. Núcleo escrito a mano; la plantilla Clean Architecture se desmonta a la arquitectura mínima que el problema pida (T3-4).

## 4. Veredicto propuesto

**PIVOTE** — cambios concretos sobre la idea original:
1. Eliminar de la ficha "potencialmente público general" y toda vía de monetización (T1). Uso personal + laboratorio de aprendizaje.
2. Estructura en dos etapas con puerta de ejecución (spike → laboratorio) y decaimiento automático a NO-GO si fallan las pruebas de vida.
3. Retarget a .NET 10 LTS; RSS propio como vía primaria; prohibido scraping anti-bot y dependencia de API de pago.
4. LLM restringido a tareas verificables; score final determinista con desglose; nunca publicar scores atribuidos a medios.
5. Timebox global 80 h/3 meses con cesión automática del remanente a la app de logopedia.

## 5. Comparación con la Fase 1 previa (crítica de un solo crítico, 2026-07-16)

El veredicto previo fue PIVOTE con: (a) 1 solo cliente Blazor, (b) reencuadre portfolio/banco de pruebas sin monetización, (c) RSS propio en vez de Newscatcher, (d) saneamiento del repo, (e) definición del dominio; más la adición de pgvector para clustering/dedupe (nunca para puntuar).

**Convergencias (independientes, refuerzan la fiabilidad):** reencuadre sin monetización (T1), RSS propio frente a Newscatcher (T2-5), saneamiento del repo (T2-2), definición del dominio real (T2-4, T3-3). El nuevo tribunal llega a lo mismo sin haber leído la crítica previa.

**Divergencias (el tribunal nuevo es más duro):**
1. **El cliente Blazor desaparece.** T3 excluye la UI de lectura del alcance y T4 propone consola. La spec v2 congelada, que asume cliente Blazor, queda desautorizada en ese punto salvo decisión expresa de Julius.
2. **pgvector se retira del alcance mínimo.** T3 excluye la deduplicación explícitamente y ningún juez la considera necesaria para el laboratorio. Queda como extensión posible post-Etapa B, no como parte del MVP.
3. **Dato nuevo que la crítica previa no tenía:** .NET 8 sale de soporte el 10-nov-2026 → retarget a .NET 10 (T2-1).
4. **Mecanismos de decaimiento:** la crítica previa no imponía pruebas de vida con plazo ni cesión automática de horas a logopedia; el tribunal sí (T2-8, T3-5, T4). La diferencia clave: el crítico único evaluó la idea; el tribunal evaluó además la evidencia de ejecución (11 meses parado) y la penaliza.

**Consecuencia:** la especificación v2 en borrador debe revisarse contra este veredicto antes de descongelarse (cliente, pgvector, target framework, timebox).

**Decisión de Fase 2b: pendiente de Julius.**
