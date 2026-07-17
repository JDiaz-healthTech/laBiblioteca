# 📚 La Biblioteca

Pipeline de validación y documentación de ideas de software. Ninguna idea se construye
sin sobrevivir antes a una crítica adversarial rigurosa (mercado real, alcance,
aprendizaje, alineación estratégica).

**Objetivo dominante:** aprender construyendo. Las ideas son vehículos de aprendizaje;
el criterio principal de selección es qué se aprende y si ese aprendizaje acerca al
pivote healthtech.

## El pipeline

| Fase | Qué ocurre | Puerta de salida |
| :--- | :--- | :--- |
| 0 · Intake | La idea se reformula en una ficha | Confirmación de la ficha |
| 1 · Crítica adversarial | Ataque en 4 frentes con investigación de mercado | Veredicto: GO / PIVOTE / NO-GO |
| 2 · Decisión | Se acepta, pivota o descarta | Decisión explícita |
| 3 · Especificación | Stack, arquitectura, MVP, hitos, estimación | Aprobación de la spec |
| 4 · Documentación | Guía de construcción + doc de usuario | Documentos completos |
| 5 · Ejecución | Construcción con seguimiento y actualización de la guía | MVP funcionando |

### Los cuatro frentes de la crítica (Fase 1)
1. **Aprendizaje** — ¿qué se aprende realmente y merece las horas frente a otra idea?
2. **Alcance** — ¿es realista para una persona con horas sueltas?
3. **Valor** — ¿tiene interés mercantil o utilidad personal real, o es un juguete?
4. **Alineación** — ¿acerca al pivote healthtech o es dispersión?

Que ya exista algo mejor no es eliminatorio (se aprende reconstruyendo), pero se señala.

## Estados

🟡 Intake · 🔴 Crítica · ⚖️ Decisión · 📐 Especificación · 📗 Documentada · 🔨 En construcción · ✅ Terminada · ❌ NO-GO

## Índice de ideas

| Idea | Estado | Veredicto propuesto | Pivote healthtech | Última actualización |
| :--- | :---: | :---: | :---: | :--- |
| [Surf Skate Spot](surf-skate-spot/ficha.md) | ⚖️ Fase 1 completada — pendiente decisión de Julius | PIVOTE (cierre de portfolio con núcleo de aprendizaje) | No | 2026-07-17 |
| [Anthropofilia](anthropofilia/ficha.md) | ⚖️ Fase 1 completada — pendiente decisión de Julius | GO (cierre auditado, tope 12 sesiones) | No | 2026-07-17 |
| [ScoringNews / Prism](scoringnews/ficha.md) | ⚖️ Fase 1 completada — pendiente decisión de Julius | PIVOTE (laboratorio de esqueleto .NET, dos etapas) | Técnico | 2026-07-17 |
| [RealAudio](realaudio/ficha.md) | ⚖️ Fase 1 completada — pendiente decisión de Julius | PIVOTE (AudioLab personal, sin claims clínicos) | **Sí** | 2026-07-17 |
| [Mantenimiento vehículo v2](vehiculo-v2/ficha.md) | ⚖️ Fase 1 completada — pendiente decisión de Julius | PIVOTE (módulo OCR de tickets sobre v1) | Tangencial | 2026-07-17 |
| [Juego 2D por oleadas](juego-2d/ficha.md) | ⚖️ Fase 1 completada — pendiente decisión de Julius | NO-GO (archivo como hobby, dossier congelado) | No | 2026-07-17 |
| [App de logopedia](logopedia/ficha.md) | ⚖️ Fase 1 completada — pendiente decisión de Julius | PIVOTE (norte estratégico por peldaños; peldaño 0) | **Sí, núcleo** | 2026-07-17 |

## Estructura por idea

Cada idea vive en su propia carpeta:

​```
{nombre-idea}/
├── ficha.md               ← Fase 0 (actualizada tras cada fase)
├── tribunal.md            ← Fase 1 (4 dictámenes independientes)
├── orquestador.md         ← Fase 2a (síntesis y veredicto propuesto)
├── especificacion.md      ← Fase 3
├── guia-construccion.md   ← Fase 4
└── doc-usuario.md         ← Fase 4
​```
