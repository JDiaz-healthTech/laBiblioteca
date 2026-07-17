# Orquestador — Surf Skate Spot

**Fecha:** 2026-07-17
**Entrada:** 4 dictámenes independientes (tribunal.md). Única voz que los lee juntos.
**Criterio dominante de ponderación:** aprendizaje + pivote healthtech.

---

## 1. Resumen de veredictos

| Frente | Veredicto | Núcleo del dictamen |
|---|---|---|
| T1 Mercado | **NO APTO** | Cuatro verticales saturados (ShredSpots +100k spots, Caliplaces +25k, Surfline, etc., verificado 2026-07-17). Arranque en frío sin plan. Monetización: cero. Único valor defendible: no mercantil. |
| T2 Técnica | APTO CON CONDICIONES | El repo NO contiene la idea: geohash al 0%, taxonomía a 1/3, "Clean Architecture" invertida, clave de Maps expuesta en público, targetSdk 34 impublicable. GeoFire = librería archivada (18-11-2024). La técnica geohash manual sigue siendo válida. |
| T3 Aprendizaje | APTO CON CONDICIONES | ~60-70% de las horas serían repetición; alineamiento con el pivote ~10-12%. Valor real: cierre/higiene de portfolio + geohash/security-rules hechos a mano. Exige timebox 60 h y prueba de salida. |
| T4 Alcance | APTO CON CONDICIONES | Alcance de la ficha = 68-126 h (4-8 meses reales). MVP Play Store = 38-70 h. Recorte extremo (GitHub Release, sin Play) = 8-14 sesiones y rinde ~80% del valor. Repo parado 13 meses. |

## 2. Contradicciones entre jueces y resolución

**Contradicción principal — el geohash.**
- T2 lo exige (condición 3: sin geoconsulta "el proyecto no es la idea presentada, es otra distinta y más pequeña").
- T4 lo mata (con <500 spots, filtro de distancia en cliente da la misma UX por el 5% del coste; optimización prematura).
- T3 lo señala como el único aprendizaje nuevo denso del proyecto si se hace a mano.

**Resolución:** el criterio dominante es aprendizaje, no producto. T4 tiene razón en términos de producto (nadie notará la diferencia), pero este proyecto ya no es un producto tras el NO APTO de T1: es un ejercicio de cierre y aprendizaje. Por tanto el geohash **se mantiene, hecho a mano y en versión mínima** (encoding + query por rangos + filtro haversine, sin GeoFire, ~4-6 sesiones), porque es lo único que convierte estas horas en aprendizaje y no en repetición. Se acepta explícitamente que es "innecesario" a esta escala: se hace por lo que enseña, y así se documenta en el README del repo.

**Contradicción secundaria — tamaño del cierre.**
T2 empuja hacia publicabilidad completa en Play (condiciones 2, 6); T4 demuestra que la ruta Play añade 3-6 semanas muertas, closed testing con 12 testers, borrado de cuenta, moderación UGC y ciclos de review — para una app que T1 declara sin mercado. **Resolución:** ruta GitHub Release (recorte extremo de T4). Las condiciones de publicabilidad de T2 se reducen a las que aplican fuera de Play: toolchain moderno razonable, clave rotada, reglas de seguridad. Play Store queda descartado salvo decisión futura expresa de Julius.

**Sin contradicción pero decisivo:** T1 (NO APTO mercantil) no tumba la idea porque su valor declarado en la ficha nunca fue mercantil. Se acepta su condición implícita: prohibido disfrazarlo de producto; etiqueta oficial "portfolio/cierre académico".

## 3. Estrategia óptima reformulada (basada en la idea original)

**"Cierre digno con núcleo de aprendizaje"** — 5 bloques, presupuesto total **≤ 20 sesiones (~40 h) / 10 semanas**:

1. **Sesión 0 (hoy, 30 min):** rotar y restringir la clave de Google Maps expuesta en `strings.xml`. No espera al arranque del proyecto.
2. **Toolchain (sesiones 1-5):** targetSdk 35/36, Kotlin 2.x + KSP, Credential Manager. Disparador de archivo de T4: si tras 8 sesiones no compila modernizado, se archiva el proyecto documentando lo aprendido.
3. **Núcleo de aprendizaje a mano (sesiones 6-11):** campo `geohash` + consulta por radio manual + filtro haversine; `firestore.rules` versionadas (acumuladores bloqueados al cliente, voto único `spotId_userId`); eliminación de `getAllSpots()` en `onResume`. Todo escrito por Julius, IA solo para revisar.
4. **Cierre (sesiones 12-18):** taxonomía congelada en los 3 tipos existentes (BMX/calistenia se recortan oficialmente de la ficha); atributos por tipo descartados (la descripción libre ya existe); seed de 20-30 spots de Cantabria; QA.
5. **Release (sesiones 19-20):** APK firmada en GitHub Releases + README honesto con capturas y decisiones técnicas + nota Obsidian con la prueba de salida de T3 (explicar geohash y modelo sin mirar código).

Se descartan: Play Store, mapa dinámico de atributos de Gemini, BMX/calistenia, editar/borrar valoraciones, moderación UGC completa (basta un "reportar" que escriba en una colección si algún día hay usuarios).

## 4. Veredicto propuesto

**PIVOTE** — la idea sobrevive solo reformulada:

1. Reetiquetado: de "app para la comunidad" a **cierre de portfolio con núcleo de aprendizaje**. Sin roadmap comercial, sin Play Store, sin fantasía de tracción (T1).
2. Alcance congelado por escrito antes de la sesión 1; kill-list de T4 aceptada excepto el geohash, que se rescata como ejercicio de aprendizaje manual (resolución de la contradicción T2/T4).
3. Timebox duro: 20 sesiones o 10 semanas, lo que llegue antes. Al agotarse, release con lo que haya.
4. Acción inmediata independiente del veredicto: rotar la clave de Maps hoy.
5. Cláusula anti-desplazamiento de T3: este proyecto no bloquea ni un día el arranque del análisis de la primera idea healthtech; corre en paralelo.
6. Dato a aclarar por Julius antes de asignar horas: si el título de FP DAM depende formalmente de esta entrega (T3, condición 1).

**Decisión de Fase 2b: pendiente de Julius.**
