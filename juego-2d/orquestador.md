# Orquestador — Juego 2D por oleadas

**Fecha:** 2026-07-17
**Entrada:** 4 dictámenes independientes (tribunal.md). Caso especial: T1 propuso los conceptos; el orquestador elige uno para el veredicto.
**Criterio dominante de ponderación:** aprendizaje + pivote healthtech.

---

## 1. Resumen de veredictos

| Frente | Veredicto | Núcleo |
|---|---|---|
| T1 Mercado | APTO CON CONDICIONES | Mercado demoledor (mediana Steam 2025: 249 USD brutos/año sobre 20.017 lanzamientos; bullet heaven saturado). Único canal con esperanza: portales web (Poki 100M jugadores/mes; techo realista 500-3.000 USD/mes). Propone 3 conceptos: **Faro** (bullet heaven + tower defense día/noche), **Última Parada** (tower defense de carril con héroe), **Nidos** (survivors score-attack de 3 min). |
| T2 Técnica | APTO CON CONDICIONES | El brief literal no es ejecutable: C# choca con el requisito móvil/web (Godot C# no exporta a web; Unity = mayor riesgo de abandono). Recomienda **Phaser 4 + TypeScript web-first (PWA)**. "Backend fuerte escalable" = sobre-ingeniería impugnada (v1 sin backend). El bloqueo real son los assets, no el código. |
| T3 Aprendizaje | **NO APTO** | Alineamiento pivote ~5-10%, mínimo de la cartera. La excepción "gamificación clínica" se desmonta: se aprende mejor dentro de la propia app de logopedia, y el diseño de engagement comercial es en parte transferencia NEGATIVA a contexto terapéutico pediátrico. Recomienda archivar como hobby, sin reactivación automática. |
| T4 Alcance | **NO APTO** | Brief completo: 73-152 sesiones = 70-150% de su presupuesto anual TOTAL para las 7 ideas. MVP honesto: 26-41 sesiones (1-2 años a cadencia real). Tasa de abandono de primeros juegos ~90%. Aparcamiento ratificado con números. Única re-entrada admisible: game jam de un fin de semana. |

## 2. Contradicciones y resolución

**T1/T2 (aptos condicionados) vs T3/T4 (no aptos).** No es contradicción: T1 y T2 responden "¿se puede?" (sí, como aprendizaje web-first con expectativa de ingresos ~0) y T3/T4 responden "¿debe, este proponente, ahora?" (no: mínimo alineamiento de la cartera y coste máximo). Con el criterio dominante del pipeline, T3+T4 pesan más.

**El matiz de T3 que cierra el debate:** la única justificación estratégica posible (aprender gamificación para la app de logopedia) es exactamente al revés — la gamificación terapéutica se diseña con lógica clínica (progresión por objetivos terapéuticos, refuerzo sin adicción), no con lógica de retención comercial. El juego no es un atajo hacia la logopedia; es un desvío.

**Elección de concepto (obligación del encargo):** **"Faro"** (T1-A). Es el único con gancho diferencial defendible (híbrido día/noche torretas/acción) frente a un género etiquetado y saturado, y encaja con el stack web-first de T2. "Última Parada" queda como plan B documentado y "Nidos" como posible pieza de game jam.

## 3. Estrategia (para el dossier, no para ejecución)

Si algún día se activa como hobby: **Faro — Phaser 4 + TypeScript, web-first (itch.io → CrazyGames; prohibida la exclusividad de 5 años de Poki), sin backend en v1, assets de packs coherentes + game feel por código, MVP de 26-41 sesiones, hito de corte: prototipo jugable en ≤20 h o se abandona.** Monetización: expectativa honesta 0-500 €/mes como techo, nunca justificación del proyecto.

**Puerta de re-entrada única (T4):** una game jam de un fin de semana (~15 h, concepto "Nidos" reducido). Si tras ella Julius no quiere seguir por puro disfrute, el expediente se cierra definitivamente.

## 4. Veredicto propuesto

**NO-GO** — con dossier completo para el futuro:
1. Se ratifica el aparcamiento de Julius, pero se corrige su formulación: no "hasta ver el rendimiento de las otras apps" (condición ambigua que deja la puerta abierta y drena atención), sino **archivado como hobby potencial**, fuera de La Biblioteca como proyecto de aprendizaje. Reactivarlo requiere la game jam de prueba + decisión expresa.
2. Alternativa que cubre el objetivo real (aprender diseño de progresión/engagement): diseñar el sistema de niveles y refuerzos DENTRO de la app de logopedia, con lógica clínica — donde ese aprendizaje vale ~10× más para su pivote.
3. El dossier (conceptos de T1, stack de T2, MVP de T4) queda congelado en esta carpeta, listo si el contexto vital de Julius cambia.

**Decisión de Fase 2b: pendiente de Julius.**
