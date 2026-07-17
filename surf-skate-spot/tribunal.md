# Tribunal Fase 1 — Surf Skate Spot

> Cuatro dictámenes independientes emitidos en contextos aislados (ninguno leyó a los demás). Fecha: 2026-07-17.

---

# Dictamen T1 — MERCADO — Surf Skate Spot

**Juez:** T1 (frente exclusivo: mercado)
**Fecha del dictamen:** 2026-07-17
**Posición de partida:** no conformidad por defecto. La idea es rechazable salvo que las evidencias demuestren hueco de mercado real.
**Ámbito:** SOLO viabilidad de mercado. No juzgo valor formativo, técnico ni académico.

---

## 1. Resumen de la idea sometida a juicio

App Android que localiza spots de deporte urbano/costero (surf, skate, BMX, calistenia) por radio de km, con taxonomía de atributos por tipo de spot y geoqueries eficientes (geohashes/GeoFire sobre Firestore). Estado: repo público incompleto, geoposicionamiento anticuado.

Desde el frente de mercado, la pregunta no es si se puede construir. Es: **¿existe un usuario que hoy no tiene esto resuelto y que adoptaría una app nueva y vacía?** La respuesta, con las evidencias abajo, es no.

---

## 2. Mapa competitivo verificado (verificación: 2026-07-17)

### 2.1 Surf — vertical saturado y profesionalizado

| Competidor | Qué ofrece | Estado |
|---|---|---|
| **Surfline** | Mapa global de spots + reports + forecast humano + cámaras en vivo + boyas y estaciones de viento. Modelo de suscripción consolidado (Premium ~70 $/año con anuncios; Premium+ compartible; subida de precios abril 2025). | Líder activo, verificado 2026-07-17 ([surfline.com](https://www.surfline.com/surf-reports-forecasts-cams-map), [soporte precios](https://support.surfline.com/hc/en-us/articles/35208905809051-US-Price-Tier-Updates)) |
| **Surf-Forecast.com** | Forecast y reports de **+7.000 spots** mundiales, app Android, alertas por email. | Activo ([surf-forecast.com](https://www.surf-forecast.com/), [Google Play](https://play.google.com/store/apps/details?id=com.snowfore.surfforecast.com)) |
| **Windy / Windy.app** | Visualización de swell y viento en mapa, multi-modelo, gratis. | Activo ([windy.app](https://windy.app/surfing-forecasts)) |
| Windguru, Windfinder, SwellInfo, LazySurfer, NDBC | Ecosistema adicional de forecast, incluidos free tiers y comparativas "best of 2026" hechas por indie devs del propio nicho. | Activo ([lazysurfer.app](https://lazysurfer.app/compare/best-surf-forecasting-app-2026.html)) |

**Lectura de mercado:** en surf el "dónde" está resuelto desde hace años (Wannasurf, Surfline, Surf-Forecast). El valor competitivo actual es el **"cuándo"** (forecast, cámaras, datos de boyas), que exige infraestructura de datos meteorológicos que la idea propuesta ni contempla. Una app de surf que solo dice dónde está la playa no compite: llega ~20 años tarde y sin la capa que sí paga el usuario.

### 2.2 Skate/BMX — vertical saturado con contenido comunitario ya acumulado

| Competidor | Contenido acumulado | Estado |
|---|---|---|
| **ShredSpots** | **+100.000 spots**, comunidad declarada de +200k skaters, filtros por 20 tipos de obstáculo. | Activo en Google Play ([ficha](https://play.google.com/store/apps/details?id=com.freeto.free2shred)) |
| **Smap** | **+34.000 spots verificados** (skateparks, street, bowls, pumptracks), verificación de altas en 24 h, más módulo de aprendizaje de trucos. | Activo Android/iOS ([Google Play](https://play.google.com/store/apps/details?id=org.nativescript.rideNRoll)) |
| **Ride My Park** | **+30.000** skateparks, street spots y pumptracks; sesiones, eventos, tiendas. | Activo ([Google Play](https://play.google.com/store/apps/details?id=com.andrieutom.rmp)) |
| **RidersMap, Ramp Map, Skatehive, goskate.com** | Más mapas sociales y directorios con fotos y reseñas. | Activos ([ridersmap.app](https://ridersmap.app/), [skatehive.app](https://skatehive.app/map)) |
| **España específico:** Guía del Skate (app), directorio Fillow por comunidades/disciplina/nivel, mapas locales tipo BCN Roll. | Cobertura nacional ya existente, incluida taxonomía por disciplina y nivel. | Activos ([fillow.net](https://fillow.net/en/skateparks)) |

**Lectura de mercado:** el atributo diferencial propuesto (taxonomía por tipo: suelo, luces, obstáculos) **ya existe** — ShredSpots filtra por 20 tipos de obstáculo y Fillow clasifica por disciplina y nivel en España. No hay diferenciación ni en dato ni en función.

### 2.3 Calistenia — vertical cubierto incluso en su micro-nicho

| Competidor | Contenido | Estado |
|---|---|---|
| **Caliplaces** | **+25.000 parques**, +5.000 reseñas, eventos; gratis iOS/Android. | Activo ([caliplaces.com](https://www.caliplaces.com/)) |
| **Calisthenics Parks** | Mapa mundial con categorías, filtro por distancia y ranking, navegación por brújula — exactamente la "recomendación por radio" propuesta. | Activo ([calisthenics-parks.com](https://calisthenics-parks.com/mobile-app)) |
| **Workout Places** | Localiza el parque y **genera el entrenamiento según el equipamiento exacto del spot** — el atributo-por-tipo llevado un paso más allá. | Activo ([workout-places.com](https://workout-places.com/)) |
| **Park Atlas** | Miles de parques con detalle de equipamiento (barras, paralelas, fondos), fotos reales de la comunidad. | Activo ([Google Play](https://play.google.com/store/apps/details?id=com.benedikt.calisthenicsparkfinder)) |

**Lectura de mercado:** hasta el detalle "estado de las instalaciones y equipamiento específico" está implementado y con años de reseñas acumuladas.

### 2.4 El competidor por defecto: Google Maps

Skateparks, parques de calistenia y playas están indexados en Google Maps con fotos, reseñas, horarios y navegación, con coste de cambio cero para el usuario. Cualquier app de spots compite primero contra el hábito "lo busco en Maps", y solo gana si aporta datos que Maps no tiene (condiciones de ola, tipo de suelo, crowd en tiempo real). La idea propuesta no incluye ninguna fuente de datos propia.

---

## 3. Demanda, hueco y saturación

- **Demanda del problema: real pero ya servida.** La gente sí busca spots; por eso existen 4-8 apps activas *por vertical* con decenas de miles de spots cada una. Demanda servida no es hueco.
- **Hueco diferencial: no acreditado.** Cada elemento de la propuesta (radio de km, taxonomía por tipo, atributos de instalación, comunidad) tiene al menos dos implementaciones activas y pobladas, verificadas a 2026-07-17. La única combinación no cubierta es "las cuatro disciplinas en una sola app", y eso es un anti-feature de mercado: el surfista, el skater y el atleta de calistenia son comunidades distintas con necesidades distintas (forecast vs. obstáculos vs. equipamiento); agregarlas diluye la propuesta frente a especialistas mejores en cada frente.
- **Ventaja técnica irrelevante para el usuario:** "geoqueries eficientes con geohashes" es una decisión de implementación interna. Ningún usuario elige app por cómo consulta Firestore. GeoFire/geohashing es además el patrón estándar documentado por la propia Firebase: no es diferenciación, es deber mínimo.

## 4. Efecto red y arranque en frío

Este es el punto letal del frente de mercado:

1. **Una app de spots vale lo que su base de datos.** Los incumbentes parten de 25.000–100.000 spots y años de fotos/reseñas. Surf Skate Spot parte de cero.
2. **El contenido lo aporta la comunidad, y la comunidad ya está en otro sitio.** Un skater de Santander que quiera añadir un spot lo hará donde ya hay usuarios que lo vean (ShredSpots, Smap, Guía del Skate) o directamente en Google Maps. No hay incentivo racional para sembrar una app vacía.
3. **No hay estrategia de seeding declarada** (scraping legal de fuentes abiertas, importación OSM, alianza con comunidad local). Sin ella, el problema del huevo-y-gallina no tiene ni plan de mitigación. La literatura sobre plataformas es unánime: la mayoría de plataformas UGC mueren antes de alcanzar masa crítica ([SoftwareSeni sobre la platform trap](https://www.softwareseni.com/the-platform-trap-why-most-platforms-fail-before-reaching-critical-mass-and-how-to-overcome-the-cold-start-problem/), verificado 2026-07-17).
4. **Recursos del proponente:** horas sueltas y fines de semana no permiten hacer community management, que es el trabajo real de una app de spots (el código es la parte pequeña).

## 5. Monetización

**Descarte explícito.** Los únicos modelos que funcionan en el nicho exigen activos que esta idea no tendrá:

- **Suscripción (modelo Surfline, ~70 $/año):** requiere datos propietarios caros (cámaras, forecast humano, boyas). Fuera de alcance absoluto.
- **Publicidad:** requiere volumen de usuarios que el arranque en frío impide; los incumbentes gratuitos ya capturan ese inventario.
- **Freemium sobre spots:** cobrar por datos que la comunidad aporta gratis y que Google Maps da gratis no sostiene conversión.

Ingresos esperables realistas: **cero.** Esto no descalifica el proyecto como ejercicio, pero cierra la vía mercantil.

## 6. Matiz fuera de mi frente (constancia, no juicio)

El único valor defendible de este proyecto es no mercantil: cierre del proyecto FP DAM y aprendizaje de Firebase/geoqueries. Ese valor lo juzgará quien corresponda; consigno aquí que **no debe disfrazarse de oportunidad de mercado**, porque no lo es. Si el proyecto sigue adelante, que sea con la etiqueta correcta: portfolio/ejercicio académico, sin roadmap comercial, sin gasto en infraestructura escalable y sin la fantasía de "lanzarla luego a producción y ver qué pasa".

## 7. Fuentes (todas verificadas 2026-07-17)

- [Surfline — mapa global de spots](https://www.surfline.com/surf-reports-forecasts-cams-map) · [Precios Surfline 2025-2026](https://support.surfline.com/hc/en-us/articles/35208905809051-US-Price-Tier-Updates)
- [Surf-Forecast.com (+7.000 spots)](https://www.surf-forecast.com/) · [Windy.app surf](https://windy.app/surfing-forecasts) · [Comparativa apps surf 2026](https://lazysurfer.app/compare/best-surf-forecasting-app-2026.html)
- [ShredSpots (+100k spots)](https://play.google.com/store/apps/details?id=com.freeto.free2shred) · [Smap (+34k spots)](https://play.google.com/store/apps/details?id=org.nativescript.rideNRoll) · [Ride My Park (+30k)](https://play.google.com/store/apps/details?id=com.andrieutom.rmp) · [RidersMap](https://ridersmap.app/) · [Skatehive](https://skatehive.app/map)
- España: [Fillow — directorio skateparks](https://fillow.net/en/skateparks) · [Guía del Skate (app)](https://www.intermundial.es/blog/consulta-tu-skatepark-mas-cercano-con-la-app-guia-del-skate)
- Calistenia: [Caliplaces (+25k parques)](https://www.caliplaces.com/) · [Calisthenics Parks — app con filtro por distancia](https://calisthenics-parks.com/mobile-app) · [Workout Places](https://workout-places.com/) · [Park Atlas](https://play.google.com/store/apps/details?id=com.benedikt.calisthenicsparkfinder)
- Arranque en frío en plataformas UGC: [SoftwareSeni — The Platform Trap](https://www.softwareseni.com/the-platform-trap-why-most-platforms-fail-before-reaching-critical-mass-and-how-to-overcome-the-cold-start-problem/)

---

## Veredicto T1

**NO APTO**

Referido exclusivamente al frente de mercado: los cuatro verticales (surf, skate, BMX, calistenia) están cubiertos por múltiples apps activas y pobladas (25.000–100.000+ spots cada una, incluidas soluciones específicas para España), la taxonomía de atributos por tipo de spot ya existe en los incumbentes, el arranque en frío no tiene plan de mitigación y no hay ruta de monetización realista. No existe hueco de mercado defendible; el único valor del proyecto es no mercantil (académico/formativo), lo cual queda fuera de este frente.

---

# Dictamen T2 — Frente TÉCNICA — Surf Skate Spot

> **Tribunal adversarial de validación. Posición de partida: NO CONFORMIDAD.**
> Juez: T2 (Técnica). Fecha del dictamen: 2026-07-17.
> Evidencia primaria: clon real del repo `https://github.com/JDiaz-healthTech/SurfSkateSpot.git` (HEAD `47c7fd5`, último commit 2025-06-13, es decir, **13 meses sin actividad**). Verificaciones de librerías con fecha explícita.

---

## 1. Método

Se clonó y examinó el repositorio completo: historial (`git log`), Gradle (`build.gradle.kts`, `gradle/libs.versions.toml`), manifest, los 4 modelos de dominio, los 5 repositorios, los 13 fragments y 7 ViewModels (2.587 líneas de Kotlin de presentación). Toda afirmación sobre el estado del código lleva ruta de archivo. Toda afirmación sobre el estado de librerías lleva fecha de verificación.

---

## 2. Estado real del repositorio (lo que hay, no lo que dice la ficha)

### 2.1 La funcionalidad núcleo de la idea NO existe en el código

La ficha vende "recomendaciones por radio de km con geohashes/GeoFire para no saturar la BBDD". El repo dice otra cosa:

- **Cero geohashes.** `grep -ri "geohash|geofire|GeoQuery"` sobre todo el código: **0 resultados**. Ni dependencia, ni campo en el modelo, ni cálculo.
- El modelo `Spot` (`app/src/main/java/com/bioridelabs/surfskatespot/domain/model/Spot.kt`) guarda `latitud: Double` y `longitud: Double` planos. Ni `GeoPoint` de Firestore (aunque el README lo afirma), ni campo `geohash`.
- **La carga de spots es el anti-patrón exacto que la idea dice resolver.** `SpotRepository.getAllSpots()` (`domain/repository/SpotRepository.kt`) hace `spotsCollection.get()` — descarga la colección entera. Y `MapFragment.onResume()` (línea 84) lo relanza **cada vez que el mapa vuelve a ser visible**, con el comentario literal: *"Forzamos la recarga de spots cada vez que el mapa se vuelve visible"*. Coste: N lecturas facturadas × cada apertura de mapa × cada usuario.
- **No hay ningún filtro por radio, distancia ni "recomendación" en todo el repo.** `grep "distance|radio|radius"` en `MapFragment.kt`: 0 resultados. La feature diferencial de la idea está implementada al 0 %.

### 2.2 La taxonomía de la ficha tampoco existe

- `SportType.kt`: enum con **3 valores** (`SURF`, `SURFSKATE`, `SKATEPARK`). La ficha promete surf, skate, **BMX y calistenia**: la mitad de la taxonomía no está.
- **No hay atributos por tipo** (fondo/ola, suelo/luces, estado de instalaciones). `Spot` solo tiene nombre, descripción, fotos, coordenadas y rating. El "mapa dinámico de atributos" de Gemini es papel, no código.
- Defecto de diseño adicional: el enum guarda en Firestore el **string de presentación en castellano** (`"Surf"`, `"Skatepark"`) como dato (`tiposDeporte: List<String>`), y acopla el dominio a Android (`iconResId: Int = R.drawable...`). Datos = texto de UI en un idioma: hostil a i18n y frágil ante cualquier renombrado.

### 2.3 La "Clean Architecture" declarada está invertida

- `data/repository/SpotRepositoryImplementation.kt` es **una clase vacía** (2 líneas: `class SpotRepositoryImplementation {}`). Igual de decorativa que `UserRepositoryImplementation.kt`.
- Los repositorios reales viven en `domain/repository/` y son **clases concretas que importan `com.google.firebase.firestore.FirebaseFirestore` directamente** (`SpotRepository.kt`, `ValuationRepository.kt`, `UserRepository.kt`). El dominio depende del SDK de Firebase: es exactamente lo contrario de Clean Architecture. El commit `c757996` ("Refactorizado para cumplir con MVVM y Clean Architecture") reclama algo que el código no cumple.
- Sin capa de casos de uso, sin interfaces de repositorio, sin mapeo entidad/DTO: los modelos de dominio llevan anotaciones de Firestore (`@DocumentId`, `@ServerTimestamp`).

### 2.4 Incidencia de seguridad activa: clave de API pública en el repo

`app/src/main/res/values/strings.xml`, línea 14:

```xml
<string name="google_maps_key">AIzaSyCwnKUTZM-iGUeZtMRYttp5qK-oEpYdt3U</string>
```

Clave de Google Maps **commiteada en un repo público** (y en el historial). Si no está restringida por huella SHA-1 + package name, es facturable por terceros. Con independencia del veredicto: **revocar/rotar hoy**. El `.gitignore` excluye `google-services.json` (bien), pero la clave de Maps se coló por la vía de `strings.xml`.

### 2.5 Sin reglas de seguridad, sin tests, con binarios en el repo

- **No hay `firestore.rules` ni `storage.rules` en el repo.** Las reglas viven (si viven) solo en la consola. Consecuencia directa: nada impide en el cliente que un usuario escriba `averageRating` a mano, vote 20 veces o borre spots ajenos (ver §4.2).
- Tests: únicamente los de plantilla (`ExampleUnitTest.kt` con `assertEquals(4, 2+2)`, `ExampleInstrumentedTest.kt`). **Cobertura real: 0.**
- El repo arrastra `Documentos Asociados/` con `.docx`, `.pptx`, `.psd` y un **APK de debug** (`APK_DEBUG/SurfSkateSpot_V1.apk`) versionados en git.
- `libs.volley` declarada en `app/build.gradle.kts` y **no usada en ningún archivo Kotlin** (grep: 0 usos): dependencia muerta. `viewBinding` y `dataBinding` habilitados a la vez sin justificación.

### 2.6 Deuda de plataforma: hoy no es publicable en Google Play

- `compileSdk = 34`, `targetSdk = 34` (`app/build.gradle.kts`). **Verificado 2026-07-17:** desde el 31-08-2025 Google Play exige target API 35 para apps nuevas y actualizaciones, y desde el **31-08-2026 exigirá API 36**. Tal cual está, el proyecto no puede ni subirse; con el requisito de agosto, la diana es 36.
- `Kotlin 1.9.22` + **kapt** (Hilt y Glide por kapt). Kapt está en modo mantenimiento según JetBrains; el ecosistema 2026 es Kotlin 2.x + KSP (Hilt soporta KSP desde 2.48). Esto no rompe, pero encarece cada actualización.
- **Login con la API legacy `GoogleSignIn`** (`presentation/view/LoginFragment.kt`, líneas 21-98: `GoogleSignInClient`, `GoogleSignInOptions`). Google la declaró obsoleta en favor de **Credential Manager** (deprecación anunciada en 2023-2024, con retirada progresiva de Play Services; estado según conocimiento a 01/2026 — reverificar antes de tocar). El historial ya delata fragilidad aquí: commit `09cb06a` *"registro y autenticacion con google vuelve a funcionar. Conseguido!"*.
- Artefactos `firebase-*-ktx` (BoM 33.1.1): los módulos `-ktx` fueron deprecados por Firebase y sus APIs migradas a los módulos principales; los `-ktx` quedaron retirados del BoM en la serie 34 (2025, según conocimiento a 01/2026 — reverificar al subir el BoM). Actualizar el BoM implicará tocar imports en todo el proyecto.
- UI en **XML + Fragments + LiveData**, no Compose. No es deuda per se, pero contradice el perfil que Julius quiere señalizar (su otra app es Compose) y duplica el coste de cualquier rediseño de pantalla.

**Conclusión de sección:** el repo es un TFG presentado en junio de 2025 con esfuerzo real y visible (auth, mapa, favoritos, subida de fotos con compresión, transacción de valoraciones), pero **la distancia entre la ficha y el código es la feature principal entera**, más una migración de plataforma obligatoria antes de poder publicar.

---

## 3. Viabilidad del enfoque geohash/GeoFire + Firestore en 2026

### 3.1 GeoFire, la librería: abandonware confirmado

- **Verificado 2026-07-17 en GitHub:** `firebase/geofire-android` fue **archivado el 18-11-2024** (read-only). Última release: v3.2.0. No habrá parches.
- Matiz que la ficha confunde: GeoFire "clásico" trabaja sobre **Realtime Database**, no Firestore. Para Firestore, la documentación oficial de Firebase ("Geo queries", firebase.google.com/docs/firestore/solutions/geoqueries) propone la técnica de geohash manual apoyada en `GeoFireUtils` (`com.firebase:geofire-android-common`) — **que vive en ese mismo repo archivado**. La alternativa comunitaria `imperiumlabs/GeoFirestore-Android` lleva años sin mantenimiento.
- Veredicto parcial: **la técnica (geohash + consultas de rango) sigue siendo válida; la librería está muerta.** El camino defendible es implementar el geohash a mano (el encoding son ~100-200 líneas bien testeadas) o vendorizar `GeoFireUtils` asumiendo su código. Presentar "GeoFire" como pilar técnico en 2026 es citar una dependencia archivada: no conforme tal cual está formulado.

### 3.2 Limitaciones estructurales del geohash sobre Firestore (esto no lo cuenta el análisis de Gemini)

1. **Falsos positivos facturados.** La consulta por radio se traduce en 5-9 consultas de rango sobre celdas geohash que cubren el círculo; los documentos fuera del radio pero dentro de las celdas **se leen y se pagan**, y se descartan en cliente. En bordes de celda el sobrecoste es notable.
2. **No se puede componer con otros filtros de forma general.** El rango sobre `geohash` consume la desigualdad de la consulta. "Skateparks con luces a menos de 5 km ordenados por rating" **no es expresable como una sola consulta Firestore**: exige filtrar/ordenar en cliente tras traerse el superconjunto, con su coste de lecturas.
3. **Sin orden por distancia nativo ni paginación por distancia.** Todo post-proceso en cliente.
4. **Costes.** Lecturas a ~$0.03–0.06/100k según región. Con el diseño actual (`getAllSpots` en cada `onResume`): 2.000 spots × 1.000 usuarios × 3 aperturas/día = 6M lecturas/día — muy por encima de la cuota gratuita (50k lecturas/día) y ~$60-110/mes solo en lecturas de mapa. Con geohash bien hecho (~30-80 docs por consulta de radio) la misma carga son ~90-240k lecturas/día: en el borde de lo gratuito. **El geohash no es una optimización opcional: es la diferencia entre coste cero y factura.**

### 3.3 Alternativas (para un desarrollador solo, con horas sueltas)

| Opción | Pros | Contras | Juicio |
|---|---|---|---|
| **Geohash manual + Firestore** | Sin backend; encaja con lo ya hecho; gratis a escala TFG/beta | Limitaciones §3.2; reglas de seguridad complejas | **Razonable para cerrar el proyecto** |
| **Supabase (Postgres + PostGIS)** | `ST_DWithin` real: radio + filtros + orden por distancia en una consulta SQL; plan gratuito; RLS | Migración total desde Firebase (auth, storage, datos); curva SQL/PostGIS | La opción técnicamente superior **si se empezara de cero**; como migración, mata el cierre del TFG |
| **PostGIS + backend propio (ASP.NET Core)** | Sinergia con su perfil C#/.NET; control total | Servidor que operar y pagar; el doble de superficie para horas sueltas | Sobredimensionado para esta fase |

**Juicio T2:** para *cerrar* este proyecto, geohash manual sobre Firestore es defendible. Para la versión "producto serio con filtros ricos por atributo + radio", Firestore es la herramienta equivocada y lo honesto es decirlo en la documentación del proyecto.

---

## 4. Crítica al diseño propuesto por Gemini (sometido, no asumido)

### 4.1 Mapa dinámico de atributos por tipo — RECHAZADO tal cual

- Un `Map<String, Any>` en Firestore no es consultable de forma genérica: cada filtro `atributos.luces == true` necesita índice, y combinado con el rango de geohash cae en la limitación §3.2.2. Resultado real: **los atributos serían solo texto de ficha, no criterios de búsqueda** — y entonces el mapa dinámico no aporta nada sobre campos tipados.
- `Any` sin esquema = cero validación: cada cliente puede escribir claves distintas (`"luces"`, `"lights"`, `"iluminacion"`). Sin reglas de Firestore que validen el esquema por tipo (complejas de escribir), la colección degenera.
- Alternativa exigida: **subobjetos tipados por deporte** (`surfAttrs: {...}`, `skateAttrs: {...}`, nulos si no aplican), esquema cerrado en código + validación en reglas, e índices solo para los 2-3 atributos que de verdad se filtren.

### 4.2 Acumuladores de rating — parcialmente implementado, íntegramente falsificable

- Ya existe: `ValuationRepository.addValuation()` usa una transacción que recalcula `averageRating`/`totalRatings`. La atomicidad está bien resuelta. Pero:
- **La integridad depende del cliente.** Sin `firestore.rules` en el repo (§2.5), cualquier cliente con el SDK puede: (a) escribir `averageRating: 5.0` directamente en el spot, (b) votar N veces — el README promete "único voto/año por usuario" y **no hay una sola línea que lo aplique**, ni en código ni en reglas. Validar la aritmética del acumulador en reglas de seguridad es notoriamente difícil; la solución estándar (Cloud Function con trigger) exige plan Blaze.
- Mitigación mínima exigible sin Functions: id de valoración determinista `"${spotId}_${userId}"` (un voto por usuario aplicable por reglas) + reglas que impidan al cliente escribir los campos de acumulador salvo vía la transición validada.
- `Valuation.fechaValoracion = System.currentTimeMillis()` — timestamp de cliente, manipulable; debe ser `@ServerTimestamp` como ya hace `Spot`.

### 4.3 Enum SportType — insuficiente como está

Cerrado (añadir BMX/calistenia = release de app), acoplado a `R.drawable` en el dominio, y persiste el literal de display en español como dato (§2.2). Exigible: identificadores estables (`"surf"`, `"skatepark"`), mapeo a icono/nombre en capa de presentación, y decisión explícita de si la taxonomía es fija (enum vale) o extensible (colección `sport_types` en Firestore).

---

## 5. Riesgos técnico-regulatorios (mínimos del frente)

1. **Ubicación = dato personal (RGPD).** La app pide `ACCESS_FINE_LOCATION` (manifest) y publica coordenadas de spots creados por usuarios junto a su `userId`. Hace falta: política de privacidad publicada (obligatoria también para el formulario Data Safety de Play), base jurídica declarada, y no persistir la ubicación del usuario (hoy no se persiste — que siga así por diseño documentado).
2. **Transferencias**: Firebase/Google como encargado — aceptar el DPA de Google y citarlo en la política. Trámite, no bloqueo.
3. **UGC (fotos + comentarios).** Play exige a las apps con contenido de usuarios mecanismos de **denuncia y bloqueo**: hoy no existen (no hay "report" en ningún fragment). Fotos en skateparks = alta probabilidad de menores identificables. Mínimo viable: botón de denuncia + campo `estado` (ya existe en `Spot`) para retirada, y moderación reactiva documentada.
4. **`allowBackup="true"`** con reglas de backup por defecto: revisar qué se incluye antes de release.

Ninguno de estos es letal a escala TFG/beta; todos son bloqueantes para publicación real en Play.

---

## 6. Condiciones y veredicto

El proyecto tiene una base honesta (auth funcional, mapa, favoritos, subida de fotos optimizada, una transacción bien planteada) y un alcance realista para horas sueltas. Pero la ficha describe una app que el repo no contiene: la geoconsulta por radio —el corazón de la idea— está al 0 %, la taxonomía a un tercio, la arquitectura declarada es ficticia, hay una clave de API expuesta y el target SDK impide siquiera publicar. El enfoque "GeoFire" cita una librería archivada desde noviembre de 2024.

## Veredicto T2

**APTO CON CONDICIONES** (frente técnico exclusivamente). Condiciones vinculantes, en orden:

1. **Inmediata (hoy, antes de cualquier otra cosa):** revocar/rotar la clave de Maps expuesta en `strings.xml` (línea 14) y restringirla por SHA-1 + package; sacarla del código (secrets-gradle-plugin o `local.properties`).
2. **Publicabilidad:** subir a `targetSdk 36` / `compileSdk 36` (requisito Play desde 31-08-2026, verificado 2026-07-17), Kotlin 2.x, kapt→KSP, retirar `firebase-*-ktx` al subir el BoM, migrar `GoogleSignIn`→Credential Manager, eliminar Volley.
3. **La feature núcleo:** campo `geohash` en `Spot` + consulta por radio con geohash **manual** (o `GeoFireUtils` vendorizado, asumiendo el archivo del repo el 18-11-2024); eliminar `getAllSpots()` del flujo de mapa y la recarga en `onResume`. Prohibido presentar "GeoFire" como dependencia viva.
4. **Integridad de datos:** `firestore.rules` versionadas en el repo con: escritura de acumuladores bloqueada al cliente, valoración con id `spotId_userId`, validación de esquema por tipo de spot. Sin reglas en el repo, el sistema de ratings se considera decorativo.
5. **Diseño Gemini corregido:** sustituir el mapa dinámico `Map<String, Any>` por subobjetos tipados por deporte; `SportType` con ids estables y sin `R.drawable` en dominio; completar la taxonomía (BMX, calistenia) o recortarla oficialmente de la ficha.
6. **Mínimos regulatorios pre-release:** política de privacidad + Data Safety, mecanismo de denuncia/ocultación de spots y fotos.
7. **Honestidad arquitectónica:** o se implementan interfaces en dominio con implementaciones en data (y se borran las clases vacías `*Implementation`), o se deja de etiquetar el proyecto como Clean Architecture.

Si las condiciones 1-4 no se ejecutan, el veredicto degrada a **NO APTO**: sin geoconsulta ni reglas, el proyecto no es la idea presentada, es otra distinta y más pequeña.

---

# Dictamen T3 — Frente APRENDIZAJE
**Idea:** Surf Skate Spot (app Android de spots de deporte urbano/costero)
**Juez:** T3 — Aprendizaje
**Fecha:** 2026-07-17
**Posición de partida:** No conformidad por defecto. La carga de la prueba recae en la idea.

---

## 1. Qué aprende Julius REALMENTE (y qué ya sabe)

Desglose honesto del contenido de aprendizaje, separando lo nuevo de lo redundante:

### Ya lo sabe (redundante, ~0 aprendizaje nuevo)
- **Kotlin, Compose, MVVM/Clean, arquitectura Android**: ya entregó una app completa de mantenimiento de vehículos con Kotlin + Compose + Room. Rehacer pantallas, navegación, ViewModels y capas es repetición, no aprendizaje.
- **Persistencia local y modelado de entidades**: Room ya cubierto. Pasar de Room a Firestore cambia el paradigma (ver abajo), pero el músculo de "modelar dominio + capa de datos" ya existe.
- **Ciclo de vida Android, permisos básicos, inyección de dependencias**: cubierto en el proyecto anterior o trivialmente recuperable.

### Aprendizaje genuinamente nuevo (el núcleo real)
1. **Firestore / NoSQL documental**: modelado por documentos, desnormalización deliberada, límites de consulta (sin JOINs, sin OR arbitrarios, índices compuestos), reglas de seguridad (`security rules`), costes por lectura. Esto SÍ es nuevo respecto a Room/SQLite. Valor conceptual transferible: pensar en NoSQL es útil en general (Cosmos DB, Mongo, DynamoDB comparten la mentalidad). Valor: **medio, pero genérico**.
2. **Geoqueries con geohashes**: entender por qué Firestore no soporta consultas geoespaciales nativas, cómo un geohash codifica lat/lng en prefijos, consultas por rangos de prefijo, cajas envolventes, falsos positivos y filtrado en cliente. Es un algoritmo bonito y concreto. **Advertencia**: GeoFire/geofire-android es una librería semiabandonada; la solución canónica actual es `geofire-common` (solo utilidades de geohash) + queries manuales. El conocimiento es real pero **nicho**: fuera de apps de mapas sobre Firestore, casi nadie te preguntará por geohashes. Valor: **bajo-medio, muy nicho**.
3. **Acumuladores/agregados en NoSQL** (medias de reviews vía transacciones o Cloud Functions): patrón real de sistemas distribuidos a escala juguete. Valor: **bajo-medio**.
4. **Mapa dinámico de atributos por tipo de spot**: modelar polimorfismo en documentos (enum SportType + map de atributos). Decisión de diseño interesante, pero el análisis previo de Gemini **no debe asumirse correcto**: los mapas dinámicos en Firestore complican índices y validación en security rules. Si Julius no re-deriva este modelo él mismo, el "aprendizaje" es cero (ver §3).
5. **Cierre y publicación**: firma de APK/AAB, ficha de Play Store o al menos release en GitHub, README decente, migración del geoposicionamiento anticuado a `FusedLocationProviderClient` + permisos runtime modernos (incl. precisión aproximada/exacta de Android 12+). Aprendizaje **operativo, no conceptual**, pero es el que convierte un repo zombi en una línea de portfolio.

**Balance:** de las horas totales del proyecto, estimación razonable: ~60-70% será repetición de lo que ya sabe (UI, arquitectura, plumbing), ~20-30% aprendizaje nuevo real (Firestore + geohashes + release), ~10% pelea con deuda del repo existente. La densidad de aprendizaje por hora es **baja** para su nivel actual.

---

## 2. Valor para el pivote healthtech y la empleabilidad

### Pivote healthtech/audiología: desalineamiento casi total
- **Firebase/Firestore en healthtech**: prácticamente ausente en software sanitario serio. Los datos de salud en Europa (RGPD, datos de categoría especial art. 9) empujan a infraestructuras controladas, no a BaaS de Google. Nadie construye un HIS, un módulo Noah o un backend de audiometrías sobre Firestore.
- **Geoqueries en audiología**: irrelevancia total. No existe caso de uso significativo.
- **El stack que SÍ pesa en audiología**: el ecosistema Noah/HIMSA es históricamente **.NET/Windows** (justo lo que Julius toca a diario en su empresa), más HL7/FHIR, HIPAA/RGPD sanitario, interoperabilidad de dispositivos. Ironía incómoda: su trabajo legacy en C# está más cerca del pivote que esta app.
- Conclusión del frente: **0 puntos de transferencia directa al pivote**. Lo único que transfiere es meta-habilidad (cerrar, publicar, modelar NoSQL como concepto).

### Empleabilidad general en España
- Mercado **.NET >> Android nativo** en volumen de vacantes en España; el perfil "junior Android + Firebase + app de spots con mapa" es el portfolio-tipo de miles de egresados de FP DAM y bootcamps. No diferencia.
- Lo que SÍ diferencia a Julius es la combinación **salud (10 años clínicos) + .NET**: esta app no toca ninguna de las dos.
- Matiz a favor: **un repo público inacabado es un pasivo de portfolio**. Un recruiter que lo abra ve abandono. Cerrarlo convierte un pasivo en un activo modesto (segunda app Android terminada + una historia de "termino lo que empiezo"). Ese valor existe, pero es de **higiene de portfolio**, no de aprendizaje estratégico.
- Punto no resuelto en la ficha: si el título de FP DAM **depende formalmente** de entregar este proyecto, la discusión de aprendizaje es secundaria: sería obligación administrativa, no idea de La Biblioteca. Si el título ya está obtenido, es 100% opcional y compite con el pivote en igualdad de condiciones. **Este dato debe aclararse antes de asignar horas.**

---

## 3. Riesgo de vaciado por IA — prescripción

Riesgo alto: es exactamente el tipo de app que Claude/Gemini generan casi entera, y ya existe un análisis de Gemini listo para copiar. Si Julius pega el modelo de Gemini y deja que la IA escriba las queries, el aprendizaje neto del proyecto tiende a cero y solo queda el valor de portfolio.

### A MANO obligatoriamente (aquí vive el 100% del aprendizaje nuevo)
1. **Re-derivar el modelo de datos desde cero**, en papel/Obsidian, ANTES de releer el análisis de Gemini. Después contrastar: cada discrepancia es una decisión que debe saber defender (¿map dinámico o subcolecciones por tipo? ¿cómo se indexa? ¿cómo lo validan las security rules?). El análisis de Gemini se trata como propuesta de un becario: se audita, no se adopta.
2. **La consulta por geohash completa a mano**: calcular la caja envolvente, generar los rangos de prefijos, lanzar las N queries, fusionar resultados, filtrar falsos positivos por distancia haversine en cliente. Puede usar `geofire-common` para el encoding, pero la orquestación de la query la escribe él. Prueba de fuego: explicar sin notas por qué un radio de búsqueda necesita varias queries y qué pasa en los bordes de celda.
3. **Security rules de Firestore**: escribirlas y romperlas él mismo (intentar escrituras ilegales desde el emulador). Es lo único de Firebase con transferencia conceptual real a "pensar en autorización de datos".
4. **La transacción/agregado de reviews** (media y contador): escribir la transacción a mano y provocar una condición de carrera para ver por qué existe.

### Delegable en IA sin pérdida
- Todo el UI Compose (ya lo aprendió en la app de vehículos): pantallas, theming, componentes de mapa.
- Migración mecánica del código de localización anticuado a FusedLocationProvider (revisar el diff, no escribirlo).
- Boilerplate: DI, navegación, serialización, tests de humo, README, ficha de release, iconos.
- Depuración de la deuda del repo antiguo (que la IA explique el código legacy propio: uso legítimo).

**Regla de control**: si al terminar no puede pizarrear el flujo geohash y el modelo de datos sin mirar el código, el proyecto se ha vaciado y solo valió como portfolio.

---

## 4. Cerrar lo inacabado vs. coste de oportunidad

**A favor del cierre (real, no negociable como categoría):**
- La habilidad de **finalización** es escasa y verificable: shipping > starting. Julius ya tiene una app terminada; una segunda refuerza el patrón, y un zombi público lo contradice.
- Coste psicológico del proyecto zombi: drena atención, genera culpa de fondo y contamina la narrativa personal ("tengo cosas a medias") justo cuando el pivote exige foco. Cerrarlo tiene valor de **liberación de RAM mental**, difícil de medir pero no nulo.
- Cerrar algo empezado cuesta menos horas que el valor de portfolio equivalente empezado de cero.

**En contra (el precio real):**
- Cada hora aquí es una hora que no va al primer proyecto healthtech, que es donde su ventaja competitiva (audiólogo + dev) es única. En este proyecto compite con cualquier junior; en healthtech casi no tiene competencia de perfil.
- El cierre tiene un enemigo conocido: el **scope creep del perfeccionista**. "Cerrar" degenera en "rehacer con el modelo de Gemini + 4 deportes + fotos + moderación de reviews". Eso no es cierre, es un proyecto nuevo disfrazado.
- Con horas sueltas tras jornada completa, un cierre sin timebox puede comerse 3-4 meses de calendario del pivote.

**Síntesis del frente:** el valor de cerrar es legítimo pero **acotado y decreciente**: se captura casi entero en la versión mínima cerrable (mapa + radio + un tipo de spot bien hecho + detalle + release firmada). Todo lo que exceda eso es coste de oportunidad puro contra el pivote.

---

## 5. Cuantificación del desalineamiento (sin decidir por él)

Estimación de horas para un cierre disciplinado: **50-70 h** (horas sueltas ≈ 8-12 semanas de calendario). Sin disciplina: 120 h+.

| Componente de las horas | % estimado | Transferencia al pivote healthtech |
|---|---|---|
| UI/arquitectura Android repetida | ~45% | ~0% (ni stack ni dominio) |
| Firestore + geohashes + agregados | ~25% | ~5-10% (solo concepto NoSQL/autorización) |
| Pelea con repo legado propio | ~10% | ~0% |
| Release, firma, publicación, README | ~10% | ~30% (shipping es shipping en cualquier stack) |
| Meta-habilidad de finalización | ~10% | ~50% (transversal) |

**Índice de alineamiento ponderado con el pivote: ~10-12%.** Las mismas 50-70 h en una idea healthtech razonable (p. ej., cualquier herramienta de audiología en .NET/C# o con FHIR, aprovechando sus 10 años clínicos) rendirían un alineamiento del 80-100% y construirían el portfolio que ningún otro candidato puede copiar. El déficit es de aproximadamente **un orden de magnitud**: unas 6-8 h de valor-pivote frente a 50-60 h de valor-pivote por el mismo esfuerzo. Ese es el precio, y debe pagarse con los ojos abiertos y solo a cambio del valor de cierre/higiene de portfolio descrito en §4 — que es real pero se agota en la versión mínima.

---

## Veredicto T3

**APTO CON CONDICIONES** (exclusivamente en el frente de aprendizaje):

1. **Aclarar primero si el título de FP DAM depende de entregar este proyecto.** Si sí, deja de ser una idea evaluable y pasa a obligación con timebox aún más agresivo. Si no, aplican las condiciones siguientes en su literalidad.
2. **Timebox duro: máximo 60 horas o 10 semanas de calendario, lo que llegue antes.** Al agotarse, se publica lo que haya (release firmada + README) y se archiva. Sin prórrogas.
3. **Alcance de cierre mínimo, congelado por escrito antes de la primera hora**: mapa + búsqueda por radio + 1-2 tipos de spot + detalle + release. Prohibido añadir features no listadas.
4. **Núcleo a mano obligatorio (§3)**: re-derivación propia del modelo de datos antes de releer el análisis de Gemini, query geohash orquestada a mano, security rules y transacción de agregados escritas y rotas por él. UI y boilerplate, delegables a IA sin restricción.
5. **Prueba de salida**: explicación en pizarra (o nota de Obsidian) del flujo geohash y del modelo de datos sin mirar código. Si no la supera, el proyecto se registra en La Biblioteca como "cerrado por portfolio, aprendizaje fallido".
6. **Cláusula anti-desplazamiento**: la selección/arranque de la primera idea healthtech no se pospone a que esto termine; puede y debe correr en paralelo al menos en fase de análisis. Este proyecto no bloquea el pivote ni un solo día.

Incumplida cualquiera de las condiciones 2-4, este dictamen degrada automáticamente a **NO APTO**: el proyecto pasaría de "cierre higiénico barato" a "distracción de baja densidad de aprendizaje con ~10% de alineamiento al pivote".

---

# Dictamen T4 — Alcance / Realismo
**Idea:** Surf Skate Spot (cierre de app FP DAM)
**Fecha:** 2026-07-17
**Juez:** T4 (Alcance/Realismo) — posición de partida: no conformidad por defecto
**Fuente:** clon del repo público `JDiaz-healthTech/SurfSkateSpot` (último commit real: 2025-06-13, hace 13 meses)

---

## 1. Estado real del repositorio (calibrado, no supuesto)

Lo que la ficha no dice y el código sí:

**Ya funciona (más de lo que sugiere la ficha):**
- Auth email + Google Sign-In (Firebase Auth), CRUD de spots en Firestore, subida de fotos con compresión (Storage), favoritos, perfil, ajustes con accesibilidad, navegación completa (13 fragments), mapa Google Maps con marcadores por tipo.
- **El acumulador de ratings YA EXISTE**: `ValuationRepository.addValuation()` hace transacción Firestore con recálculo de media incremental. El plan de Gemini propone construir algo que ya está construido.

**No existe en absoluto (0%):**
- Geohashes/GeoFire: `grep` de `geohash|GeoFire|radius` devuelve **cero resultados**. No hay búsqueda por radio; el mapa carga TODOS los spots con `getAllSpots()`. El "modernizar geoposicionamiento" de la ficha es en realidad "construir desde cero la feature estrella".
- Taxonomía con atributos dinámicos: `SportType` tiene solo 3 valores (Surf, Surfskate, Skatepark). Ni BMX ni calistenia. El modelo `Spot` no tiene mapa de atributos: ni fondo de playa, ni suelo de skatepark, ni estado de instalaciones. 0%.
- Regla "un voto/año por usuario" que promete el README: no está implementada (`addValuation` no comprueba nada).
- Moderación de contenido: inexistente. Ni reportar, ni bloquear, ni retirar.
- `SpotRepositoryImplementation.kt` es un stub vacío de 3 líneas; los "repositorios de dominio" son clases concretas. Deuda arquitectónica menor, pero delata cierre apresurado.

**Obsolescencia bloqueante para publicar:**
- `targetSdk = 34`. Google Play exige API 35 desde agosto de 2025 para apps nuevas, y el listón sube a API 36 hacia agosto de 2026 — es decir, **en ~6 semanas desde hoy**. Publicar implica saltar a targetSdk 35/36 con la imposición de edge-to-edge, doloroso en una app de XML + Fragments.
- Kotlin 1.9.22 + kapt (Hilt, Glide): migración razonable a Kotlin 2.x + KSP durante el salto de AGP.
- Google Sign-In vía `play-services-auth` (API legada, deprecada): migración a Credential Manager casi obligada para una app nueva en 2026.
- `isMinifyEnabled = false` y proguard comentado: la build de release nunca se ha endurecido.
- Política de Play: app con cuentas ⇒ **borrado de cuenta obligatorio** in-app y por web (no existe); app con contenido de usuarios ⇒ política UGC (reporte/bloqueo/moderación, no existe).

---

## 2. Estimación por bloques (sesiones de ~2h)

| # | Bloque | Mín | Máx | Nota |
|---|--------|-----|-----|------|
| 1 | Toolchain: AGP + Kotlin 2.x + KSP + targetSdk 35/36 + edge-to-edge en XML | 3 | 6 | Obligatorio para publicar; riesgo alto de "una tarde se convierte en dos fines de semana" |
| 2 | Migración Google Sign-In → Credential Manager | 2 | 4 | El commit "vuelve a funcionar. ¡Conseguido!" de 2025 anticipa el dolor |
| 3 | Geohashes + GeoFire: campo geohash, query por radio, migración de docs existentes, UI de radio | 4 | 7 | Feature nueva, no "modernización" |
| 4 | Taxonomía 4+ deportes con atributos dinámicos (modelo, formulario AddSpot dinámico, detalle, filtros, iconos) | 5 | 9 | Es el bloque más gordo y toca toda la app |
| 5 | Reviews completos: listar valoraciones en detalle, regla 1 voto/periodo, editar/borrar con recálculo | 3 | 5 | El acumulador ya existe; falta todo lo demás |
| 6 | Moderación mínima UGC: reportar spot/review, bloquear usuario, flujo de retirada, reglas | 3 | 6 | Requisito de política Play, no opcional |
| 7 | Borrado de cuenta (in-app + página web) | 2 | 3 | Requisito de política Play |
| 8 | Reglas de seguridad Firestore/Storage serias + App Check en release | 2 | 3 | Hoy cualquiera puede escribir lo que las reglas permitan |
| 9 | Contenido semilla: 30–60 spots reales con fotos y atributos | 3 | 6 | Sin esto la app publicada está vacía y muere |
| 10 | Play Store: cuenta, política de privacidad, data safety, ficha, gráficos, **closed testing (12 testers × 14 días si cuenta personal nueva)**, iteraciones de review | 4 | 8 | + 3–6 semanas de calendario muerto que no cuentan como sesiones |
| 11 | QA, proguard/minify, crashes, pulido de release | 3 | 6 | Siempre existe y siempre se subestima |
| | **TOTAL alcance de la ficha** | **34** | **63** | **≈ 68–126 horas** |

---

## 3. Confrontación con la disponibilidad real

Julius rinde en sesiones de ~2h, a un ritmo declarado de 2–4 sesiones/semana **repartidas entre 7 ideas**.

| Escenario | Sesiones | A 4/sem (todo para esta idea) | A 2/sem (realista con vida) | A 1–2/sem (con 6 ideas más compitiendo) |
|---|---|---|---|---|
| Ficha completa (mín) | 34 | ~9 semanas | ~17 semanas | 6–9 meses |
| Ficha completa (máx) | 63 | ~16 semanas | ~31 semanas | **12+ meses** |

A esto hay que sumar 3–6 semanas de calendario muerto del closed testing y de la review de Play que no dependen de él. **El alcance de la ficha, tal cual está escrita (con el plan de Gemini incluido), es un proyecto de 4 a 8 meses monopolizando la totalidad de sus horas libres.** Para un side-project de cierre de portfolio, compitiendo con dos ideas alineadas con su pivote healthtech, eso no es un plan: es una hipoteca.

Agravante: el repo lleva **13 meses sin un commit**. La evidencia empírica de ritmo sostenido en este proyecto concreto es cero desde la entrega del FP.

---

## 4. Recorte necesario: el MVP que cierra con dignidad

El error de la ficha es confundir "cerrar la app" con "construir la app que Gemini imaginó". Recorte quirúrgico:

**Se elimina (kill list):**
- ❌ Geohashes/GeoFire. Con <500 spots, `getAllSpots()` + filtro de distancia en cliente (`Location.distanceTo`) da la MISMA experiencia de usuario por el 5% del coste. GeoFire es optimización prematura para una app con cero usuarios.
- ❌ BMX y calistenia. Se queda la taxonomía actual de 3 tipos que ya tiene iconos y funciona.
- ❌ Atributos dinámicos por tipo. El campo `descripcion` ya existe; que el fondo de la playa vaya en la descripción.
- ❌ Editar/borrar valoraciones. Solo añadir (ya funciona) + listar.

**Se mantiene (irrenunciable para publicar):**
- Toolchain a targetSdk 35/36 (bloqueante legal de Play), Credential Manager, borrado de cuenta, botón "Reportar" mínimo (escribe en colección `reports`, revisión manual), reglas Firestore decentes, seed de 20–30 spots de Cantabria, ficha de Play y closed testing.

| MVP recortado | Mín | Máx |
|---|---|---|
| Toolchain + Sign-In moderno | 5 | 9 |
| Filtro por radio en cliente (sin GeoFire) | 1 | 2 |
| Listar reviews en detalle + regla 1 voto | 1 | 2 |
| Reportar (mínimo viable de moderación) | 1 | 2 |
| Borrado de cuenta | 2 | 3 |
| Reglas de seguridad | 1 | 2 |
| Seed 20–30 spots (Cantabria) | 2 | 3 |
| Play Store completo | 4 | 8 |
| QA/release | 2 | 4 |
| **TOTAL MVP** | **19** | **35** | 

**≈ 38–70 horas ≈ 2–4 meses a ritmo realista.** Sigue sin ser barato, pero es un proyecto terminable.

**Recorte extremo (si Play Store no compensa):** cerrar como *release de portfolio* — toolchain mínimo, filtro por radio, README con capturas y APK firmada en GitHub Releases, vídeo demo. **~8–14 sesiones (1–1,5 meses).** Cierra la historia "tengo una app Android completa y documentada" sin pagar el peaje de Google Play. Para un portfolio orientado a healthtech, esto puede rendir el 80% del valor por el 30% del coste.

---

## 5. Sumideros de tiempo ocultos (los que esta idea esconde)

1. **Closed testing de Play (cuenta personal):** 12 testers durante 14 días antes de poder pasar a producción. Reclutar 12 personas que instalen y mantengan la app es un mini-proyecto social en sí mismo, y son semanas de calendario que no avanzan con sesiones.
2. **Edge-to-edge en SDK 35 sobre XML+Fragments:** cada pantalla puede romperse visualmente. Es trabajo aburrido, disperso y difícil de estimar.
3. **Contenido semilla:** una app de spots vacía es una app muerta el día 1. Documentar 30+ spots reales con fotos propias (derechos de imagen incluidos) son tardes de campo, no de teclado.
4. **Políticas de Play encadenadas:** privacidad + data safety + UGC + borrado de cuenta. Cada rechazo de review añade un ciclo de días.
5. **Google Sign-In legado:** la migración a Credential Manager tiene fama merecida de consumir sesiones enteras en configuración de SHA-1/OAuth.
6. **Mapas:** el SDK de Maps para Android es gratuito en dynamic maps móviles, pero exige cuenta de facturación activa y restricción de API key para release (huella SHA-1 de la firma de producción — clásico "funciona en debug, mapa gris en release").
7. **Fotos de usuarios:** Storage + moderación de imágenes. En el MVP, mitigar limitando quién puede subir o revisando manualmente.

---

## Veredicto T4

**APTO CON CONDICIONES** — exclusivamente en el frente de alcance/realismo, y solo bajo estas condiciones vinculantes:

1. **Se descarta el alcance de la ficha y el plan de Gemini.** Geohashes/GeoFire, atributos dinámicos por tipo y la ampliación a BMX/calistenia quedan fuera. Filtro por radio en cliente. Quien quiera GeoFire, que lo pida cuando haya 500 spots y usuarios que los busquen.
2. **Presupuesto cerrado: máximo 35 sesiones.** Si al llegar a 35 no hay app en producción (o release final en GitHub), el proyecto se archiva como está, con lo aprendido documentado.
3. **Decisión previa a la sesión 1:** ruta Play Store (19–35 sesiones + semanas muertas de testing) o ruta portfolio/GitHub Release (8–14 sesiones). Tomarla por escrito antes de tocar código; cambiarla a mitad duplica el coste.
4. **Las 5 primeras sesiones son solo toolchain** (targetSdk 35/36 + Kotlin 2.x/KSP + Sign-In). Si tras 8 sesiones el proyecto no compila y arranca modernizado, disparador de archivo: el coste real supera al estimado y las ideas healthtech en cola pagan la factura.
5. **Ninguna feature nueva** que no esté en la tabla del MVP. La palabra "ya que estoy" queda prohibida durante este proyecto.

Sin estas condiciones, el dictamen sería NO APTO: el alcance descrito en la ficha son 68–126 horas (4–8 meses de su calendario real) para cerrar una app de un ciclo formativo ya aprobado, con el repo parado desde hace 13 meses y seis ideas —dos de ellas alineadas con su pivote profesional— esperando las mismas horas.
