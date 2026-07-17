# Ficha — Surf Skate Spot

**Fase:** 1 completada — pendiente decisión de Julius (2b)
**Actualizada:** 2026-07-17 (tras tribunal; ficha original de Fase 0 corregida con lo aprendido)

## Problema
Localizar spots de deporte urbano/costero cercanos (surf, skate, BMX, calistenia) con recomendaciones geográficas por radio de km.

## Usuario objetivo
Comunidad de esos deportes — **corrección del tribunal:** ese mercado está servido por incumbentes con 25k-100k spots por vertical (verificado 2026-07-17). El usuario real es Julius: es su app de fin de ciclo FP DAM, pendiente de cerrar.

## Propuesta de valor (una frase)
Cerrar con dignidad la app de fin de ciclo convirtiéndola en activo de portfolio, con un núcleo de aprendizaje real (geohash manual + security rules) en lugar de un repo zombi público.

## Relación con el pivote healthtech
No. Alineamiento estimado por el tribunal: ~10-12%. Se compensa con timebox duro y cláusula anti-desplazamiento (no bloquea el arranque de la primera idea healthtech).

## Estado real del repo (verificado 2026-07-17, clon de `JDiaz-healthTech/SurfSkateSpot`)
- Último commit: 2025-06-13 (13 meses parado). Funciona: auth, mapa, CRUD de spots, fotos, favoritos, transacción de ratings.
- La feature estrella (geohash/radio) está al **0%**; taxonomía 3/4+ tipos sin atributos; "Clean Architecture" declarada pero invertida.
- **Clave de Google Maps expuesta en `strings.xml` (repo público) — rotar hoy.**
- targetSdk 34: impublicable en Play (exige 35 ya, 36 desde 31-08-2026). GeoFire = librería archivada (18-11-2024); la técnica geohash sigue válida a mano.

## Diseño previo de Gemini — resultado de la crítica
- Mapa dinámico de atributos: **rechazado** (no consultable con el rango geohash, sin validación posible razonable en reglas).
- Acumuladores de rating: **ya existían implementados** en el repo; falta blindarlos en `firestore.rules`.
- Enum SportType: insuficiente (ids no estables, acoplado a drawable, display en castellano como dato).

## Veredicto del orquestador (propuesto, pendiente 2b)
**PIVOTE** → "cierre digno con núcleo de aprendizaje": ruta GitHub Release (sin Play Store), geohash hecho a mano como ejercicio, taxonomía congelada en 3 tipos, ≤ 20 sesiones / 10 semanas, rotación de clave inmediata. Detalle en `orquestador.md`; dictámenes íntegros en `tribunal.md`.

## Pregunta abierta para Julius
¿El título de FP DAM depende formalmente de entregar esta app? (condiciona el timebox y la prioridad).
