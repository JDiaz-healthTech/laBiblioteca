# Orquestador — RealAudio

**Fecha:** 2026-07-17
**Entrada:** 4 dictámenes independientes (tribunal.md). Única voz que los lee juntos.
**Criterio dominante de ponderación:** aprendizaje + pivote healthtech.

---

## 1. Resumen de veredictos

| Frente | Veredicto | Núcleo |
|---|---|---|
| T1 Mercado | **NO APTO** | Categoría con precio de referencia 0 € absorbida por el SO y el firmware (Apple test+modo audífono en 100+ países; Samsung Adapt Sound; Mimi en SoCs). Mimi abandonó exactamente este segmento B2C Android (mayo 2024). Sin hueco para un individual. |
| T2 Técnica | **NO APTO** (tal como está formulada) | Dos pilares independientes: (1) EQ global con llamadas = imposible sin root (llamadas bloqueadas desde Android 10; sesión-0 deprecada y ruleta OEM; sin API pública de ANC); umbral sin transductor calibrado sin validez clínica. (2) "Estima pérdida + deriva a clínica" publicada = software producto sanitario clase IIa (MDR, MDCG 2019-11 regla 11), certificación inviable para un individual — Mimi perdió su CE en 2024. |
| T3 Aprendizaje | APTO CON CONDICIONES | Única idea de la cartera que une audiología + código: alineamiento pivote ~90-95%, densidad de aprendizaje 70-80%/hora si el núcleo se hace a mano. Exige fasear (Fase 1 = solo motor de test), cuaderno de calibración, decisión regulatoria documentada, kill criterion 6 semanas. |
| T4 Alcance | APTO CON CONDICIONES | Ficha promete imposibles → reescritura obligatoria (fuera llamadas y ANC). MVP realista: 24-42 sesiones (3-5 meses) SOLO con ≥2 sesiones/semana prioritarias; con la cuota actual entre 7 ideas serían 1-3,5 años → NO APTO automático sin priorización. |

## 2. Contradicciones y resolución

**La aparente contradicción central — dos NO APTO frente al mayor alineamiento de la cartera.** T1 y T2 tumban la idea *tal como está escrita*; T3 la declara el vehículo de pivote más valioso que Julius tiene. No es contradicción: los cuatro jueces coinciden en los hechos y difieren en el objeto. Lo que muere es el **producto** ("imitar un audífono" global + informe clínico publicado). Lo que sobrevive es el **laboratorio de audiología aplicada**: motor de test psicoacústico hecho a mano, gestión de incertidumbre, decisión regulatoria documentada. Como el criterio dominante del pipeline es aprendizaje + pivote, el orquestador reformula hacia lo que T3 valora, dentro de los límites duros que T1/T2/T4 han demostrado.

**T2 exige re-sometimiento.** T2 advierte que la versión superviviente (sin claims clínicos, audio propio, on-device) "es una idea materialmente distinta y debería re-someterse al tribunal". Formalmente tiene razón; operativamente, la reformulación de abajo se construye EXCLUSIVAMENTE con elementos ya juzgados por los cuatro frentes (motor de test de T3-1, MVP de T4-6, límites de claims de T4-4). No hay materia nueva sin dictamen. Si Julius acepta el PIVOTE en 2b, la ficha reescrita queda cubierta; si añade cualquier elemento nuevo (publicación en tienda, claims, hardware), entonces sí: tribunal nuevo.

**Llamadas y ANC:** T2 y T4 coinciden de forma independiente — se ELIMINAN de la ficha, no se aparcan. La frase "imitando un audífono básico" no sobrevive en ningún material.

## 3. Estrategia óptima reformulada

**"AudioLab personal: motor de cribado psicoacústico + demo de compensación"** — para Julius, su familia y su portfolio; sin tienda, sin claims, datos on-device:

**Fase A — Motor de test (el corazón; sesiones 1-16):**
1. Bloque regulatorio PRIMERO (2 sesiones): documento de 1-2 páginas fijando claims permitidos ("entrenamiento/cribado orientativo no diagnóstico, uso personal") y lenguaje prohibido (diagnóstico, audífono, dB HL absolutos). Es entregable de portfolio en sí mismo: nadie más en una entrevista healthtech tiene esto.
2. Spike de 2 sesiones máx. sobre EQ global en SU dispositivo (T4-2) — para cerrar la puerta con evidencia propia, no para abrirla.
3. Estímulos + staircase adaptativo + test-retest con criterio de concordancia + gate de ruido: **escrito a mano por Julius**, con su criterio clínico como especificación. Umbrales RELATIVOS (perfil de audibilidad), jamás dB HL sin calibración.
4. Cuaderno de calibración/incertidumbre en el repo, validado contra su propio audiograma real (T3-3).
5. Kill criterion: staircase funcional presentando tonos por oído en 6 semanas o vuelta al tribunal (T3-5).

**Fase B — Compensación demo (solo si A cierra; sesiones 17-30):**
EQ de 4-6 bandas derivada del perfil, aplicada al reproductor PROPIO de la app (música/archivos locales). Comparación A/B audible. Informe personal sin lenguaje clínico.

**Condiciones de contorno:** ≥2 sesiones/semana prioritarias o no se arranca (T4-3, con NO APTO automático); logopedia congelada hasta cerrar Fase A (T3-6); techo total 42 sesiones.

## 4. Veredicto propuesto

**PIVOTE** — cambios concretos sobre la idea original:
1. Eliminar de la ficha: EQ de llamadas, EQ global del sistema, uso de ANC, "imitando un audífono", informe de estimación de pérdida con derivación clínica publicable. (T1, T2, T4.)
2. Reencuadre: de producto B2C Android a **laboratorio personal de audiología aplicada + pieza central de portfolio healthtech**. Sin Play Store en v1; datos on-device; monetización descartada explícitamente.
3. El motor de test se convierte en el producto real: protocolo adaptativo con test-retest hecho a mano, umbrales relativos, cuaderno de incertidumbre, decisión regulatoria documentada al inicio.
4. Estructura A→B con puerta, kill criterion de 6 semanas y exigencia de ≥2 sesiones/semana; si la priorización no es posible ahora, la idea se aparca SIN ejecutar (no se degrada a ritmo homeopático).
5. Cualquier ampliación futura (tienda, claims, calibración por auricular, hardware) exige tribunal nuevo (cláusula T2).

**Decisión de Fase 2b: pendiente de Julius.**
