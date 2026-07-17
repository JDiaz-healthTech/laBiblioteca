# Tribunal Fase 1 — Mantenimiento de vehículo (v2)

> Cuatro dictámenes independientes emitidos en contextos aislados (ninguno leyó a los demás). Fecha: 2026-07-17.

---

# Dictamen T1 — MERCADO — Mantenimiento de vehículo (v2)

**Tribunal adversarial de validación de ideas · Juez T1 (frente MERCADO exclusivamente)**
**Fecha del dictamen:** 2026-07-17
**Posición de partida:** no conformidad por defecto. La carga de la prueba recae sobre la idea. No la ha levantado.

---

## 1. Panorama competitivo 2026: categoría madura, saturada y con precios a la baja

Esto no es un nicho vacío; es una de las categorías más pobladas de las tiendas de aplicaciones desde hace más de una década:

- **Drivvo** (Brasil, ~2012): +5,2 M de descargas, ~2 M de usuarios declarados, 4,51★ con 110.000 reseñas. Freemium: versión gratuita completa para 1 vehículo; Pro desbloquea multivehículo, backup en nube y exportación. Quejas recurrentes de usuarios por subida de precio de ~6 $ a ~25 $ y anuncios pese a pagar (reseñas 2025, justuseapp/Google Play). [Similarweb, consultado 2026-07; Google Play, 2026]
- **Simply Auto**: registro de combustible, gastos, mantenimiento y kilometraje con GPS; premium para nube y tracking fiscal. [simplyauto.app, 2026]
- **Fuelio** (propiedad de Sygic): gratuita, centrada en combustible, con base de datos comunitaria de consumos. Compite a precio cero.
- **CARFAX Car Care / myCARFAX**: **gratuita**, +50 M de conductores declarados, con historial de servicio real reportado por talleres, alertas de recalls y avisos de próximos servicios. [carfax.com/Service, App Store, consultado 2026-07]
- Cola larga de entrantes 2024–2026: MyAutoLog, 1Garage, REVAULT, ServiceLog, CarCareDiary, GarageHub… La barrera de entrada es tan baja que la categoría se repuebla cada año con clones, lo que confirma dos cosas: es fácil de construir y difícil de monetizar.

**Lectura de mercado:** el precio ancla de la categoría lo fija CARFAX en **0 €** (subvencionado por su negocio de informes y captación para talleres) y Fuelio en **0 €** (subvencionado por Sygic). Un independiente compite contra productos gratuitos con más datos de los que jamás tendrá.

## 2. Demanda real: uso esporádico, abandono alto, disposición a pagar residual

- El patrón de uso de la categoría es estructuralmente hostil a la retención: un coche particular tiene 2–6 eventos de mantenimiento **al año**. No hay hábito diario que retener; la app se abre cuando algo pasa. Las apps que sobreviven (Drivvo, Fuelio) lo hacen enganchándose al repostaje (evento semanal), no al mantenimiento. La ficha de la idea prescinde justamente del gancho de frecuencia.
- No he encontrado cifras públicas de retención de la categoría (los vendors no las publican, lo cual ya es una señal), pero los proxies son consistentes: Drivvo, líder con 12+ años, acumula ~5 M de descargas totales y ~680 descargas/día — cifras de categoría de nicho, no de mercado masivo — y sus quejas más visibles son de fricción con el pago. [Similarweb/AppBrain, consultado 2026-07]
- Quien sí paga: **autónomos y flotas** (deducción fiscal del kilometraje, gestión de vehículos de empresa — Simply Auto premium, AUTOsist a 5 $/vehículo/mes con mínimo de 59 $/mes). El conductor particular no técnico —el usuario objetivo declarado— es precisamente el segmento que **no paga** y que menos registra. [autosist.com/pricing, 2026]

**Conclusión de demanda:** existe un micro-segmento entusiasta (foros tipo BobIsTheOilGuy, r/cars) que registra religiosamente y ya está servido. El "conductor particular no técnico" no ha demostrado en 12 años de categoría que quiera registrar nada: quiere que se lo registren (ver §4, apps de fabricante y DGT).

## 3. El "hueco diferencial": ya está ocupado desde 2025

La combinación propuesta —plantillas por motorización + OCR de tickets con autorrelleno— **ya existe en producción**, y en varios competidores simultáneamente:

- **1Garage** (2025–2026): foto del ticket → IA extrae taller, fecha, servicios, piezas y costes; escaneo de VIN para autorrelleno. Es literalmente la propuesta de la ficha. [1garage.ai, consultado 2026-07]
- **REVAULT**: "Scan. Track. Verify." — OCR con IA que registra taller, fecha, kilometraje y coste. [app.myrevaultapp.com, 2026]
- **MyAutoLog**: escaneo de recibos con IA para añadir múltiples servicios de una factura. [alternativeto.net, 2026]
- **Simply Fleet**: OCR de tickets de combustible y facturas de servicio + mantenimiento preventivo **por marca y modelo** (la "validación cruzada" de la ficha, en su versión flota). [simplyfleet.app, 2026]

El coste de replicar esta función en 2026 es una llamada a un LLM multimodal; no es defendible ni 6 meses. Lo que en 2023 habría sido diferencial hoy es **conveniencia de tabla de features**. La única pieza de la propuesta que nadie hace bien es la validación cruzada contra el plan de mantenimiento real del vehículo — y esa pieza choca frontalmente con §4.

## 4. El problema del dato: aquí muere la propuesta en el frente mercado

### 4a. VIN: la vía gratuita no sirve para España
- **NHTSA vPIC** es gratuita y sin registro, pero solo cubre vehículos destinados a venta/importación en EE. UU. (desde 1981). Un Seat León, un Peugeot 208 o un Dacia Sandero matriculados en Santander devuelven resultado vacío o basura. [vpic.nhtsa.dot.gov, consultado 2026-07]
- Los decodificadores europeos son **de pago por consulta**: Matrícula API ~0,20 €/búsqueda (matrícula española), Vincario ~54 €/200 informes, más CarsXE/Zyla en rangos similares. Coste variable desde el usuario 1, contra un producto que el mercado espera gratis. [matriculaapi.com; vindecoder.eu, consultado 2026-07]
- Agravante regulatorio: el **TJUE dictaminó (enero 2024)** que el VIN es dato personal bajo RGPD cuando es vinculable al titular. Tratar VINs de terceros en la UE añade obligaciones de cumplimiento que los competidores estadounidenses simplemente ignoran. [Sentencia C-319/22, ecarstrade.com/blog, 2024]

### 4b. Intervalos "por motorización": simplificación sin valor defendible
- Los intervalos reales son por **fabricante/modelo/año/motor y condiciones de uso** (normal vs severo), y muchos vehículos post-2010 llevan **mantenimiento flexible por sensor** (longlife VAG, condition-based de BMW/Mercedes): el propio coche calcula cuándo toca. Una tabla genérica "diésel: aceite cada 15.000 km" es, en el mejor caso, redundante con el manual y, en el peor, contradice lo que el salpicadero del usuario le dice — destruyendo la confianza, que es el único activo de una app de registro.
- Los datos OEM estructurados existen pero son **de pago y US-céntricos**: Vehicle Databases (1999–2023, mercado USA), DataOne, CarScan (vehículos vendidos en EE. UU. desde 1996). No hay fuente gratuita y legal de planes de mantenimiento OEM para el parque europeo. Construirla a mano ("intervalos investigados") es un trabajo de curación permanente, sin licencia, con responsabilidad implícita si alguien alarga un intervalo por fiarse de la app. [vehicledatabases.com; dataonesoftware.com, consultado 2026-07]

### 4c. El cerco institucional: fabricantes y DGT
- **Apps oficiales de fabricante** (MyPeugeot, We Connect, My BMW, Mercedes me…): gratuitas, con telemetría real del coche, avisos de mantenimiento calculados por el propio vehículo, **libro de servicio digital automático** y cita en taller. Para el parque post-≈2018, hacen de serie y con datos reales lo que esta idea haría a mano y con datos aproximados. [peugeot.co.uk/owners/digital-service-record, consultado 2026-07]
- **España, tiro de gracia:** la DGT y Ganvam operan el **Libro Taller Electrónico / Libro Electrónico de Mantenimiento**: es el **taller** quien anota fecha, kilómetros, operación y piezas en una base de datos nacional consultable. El registro fiable "para que no se pierda el historial" está siendo resuelto institucionalmente, sin que el conductor teclee nada — que es exactamente lo que el conductor no técnico quería. [sede.dgt.gob.es, dgt.es; Infotaller, consultado 2026-07]
- Queda fuera del cerco el parque antiguo sin conectividad y el mantenimiento DIY — es decir, el entusiasta que cambia su propio aceite: el segmento ya servido por Drivvo/Fuelio/foros y el menos dispuesto a pagar por plantillas que él conoce mejor que la app.

## 5. Monetización: descarte explícito

- **Suscripción B2C:** contra CARFAX gratis, Fuelio gratis, apps de fabricante gratis y DGT gratis, con 2–6 eventos/año de uso. Los líderes con millones de usuarios monetizan mal (quejas por subir de 6 $ a 25 $/año en Drivvo). Un entrante sin distribución no captura nada. **Descartada.**
- **Compra única:** incompatible con costes variables recurrentes (VIN de pago por consulta ~0,20 €, LLM por ticket escaneado, licencias de datos OEM). Cada usuario activo genera coste perpetuo. **Descartada.**
- **Publicidad:** requiere volumen que un desarrollador a horas sueltas en un mercado saturado no alcanzará. **Descartada.**
- **B2B (talleres/flotas):** es donde hay dinero (AUTOsist, Fleetio, Simply Fleet), pero es otro producto, otro usuario, otra venta, y en España colisiona con la plataforma DGT/Ganvam para talleres. Fuera del alcance de la ficha. **No aplicable.**

No existe ruta de monetización creíble para esta ficha tal como está definida (B2C, conductor particular, España/UE).

---

## Veredicto T1

**NO APTO** (frente MERCADO).

Fundamentos: (1) categoría saturada con ancla de precio en 0 € fijada por actores subvencionados (CARFAX, Sygic, fabricantes); (2) el usuario objetivo declarado —conductor particular no técnico— es el segmento con menor registro y nula disposición a pagar, y su necesidad está siendo absorbida por apps de fabricante y, en España, por el Libro Taller Electrónico de la DGT; (3) el supuesto diferencial (OCR de tickets con IA + plantillas) ya está en producción en al menos cuatro competidores en 2026 y su coste de réplica es trivial; (4) el dato necesario para la única pieza valiosa (planes OEM reales, VIN europeo) es de pago, US-céntrico o inexistente en abierto, con carga RGPD añadida (VIN = dato personal, TJUE 2024); (5) ninguna vía de monetización sobrevive al análisis.

Este veredicto se pronuncia exclusivamente sobre el frente mercado. El valor de la idea como vehículo de aprendizaje (objetivo dominante declarado del proponente) no es competencia de este tribunal y no queda afectado por este dictamen; lo que queda descartado es cualquier expectativa mercantil sobre la v2 tal y como está formulada.

---

### Fuentes (consultadas 2026-07-17)
- Drivvo — Google Play / Similarweb / AppBrain: https://www.similarweb.com/app/google-play/br.com.ctncardoso.ctncar/statistics/ ; https://play.google.com/store/apps/details?id=br.com.ctncardoso.ctncar
- Reseñas Drivvo (quejas de precio/suscripción, 2025): https://justuseapp.com/en/app/1206041425/drivvo-car-management/reviews
- Simply Auto: https://simplyauto.app/
- CARFAX Car Care (gratuita, 50 M+ conductores): https://www.carfax.com/Service/
- Comparativas de categoría 2026: https://carmaintenance.app/best-car-maintenance-tracking-apps/ ; https://www.carcarediary.com/blog/best-car-maintenance-apps
- NHTSA vPIC (gratuita, solo mercado USA): https://vpic.nhtsa.dot.gov/api/
- Comparativa de decodificadores VIN gratuitos 2026: https://cardog.app/blog/free-vin-decoder-api-comparison
- Matrícula API España (~0,20 €/consulta): https://www.matriculaapi.com/
- Vindecoder.eu / Vincario (precios UE): https://vindecoder.eu/api/
- VIN como dato personal, TJUE C-319/22 (enero 2024): https://ecarstrade.com/blog/best-vin-decoders-for-car-history
- APIs de planes de mantenimiento OEM (de pago, US-céntricas): https://vehicledatabases.com/vehicle-maintenance-api ; https://www.dataonesoftware.com/vehicle-data-vin-decoding/vehicle-service-data
- AUTOsist precios flota (5 $/vehículo/mes, mín. 59 $/mes): https://autosist.com/pricing/
- MyPeugeot / Digital Service Record: https://play.google.com/store/apps/details?id=com.psa.mym.mypeugeot ; https://www.peugeot.co.uk/owners/digital-service-record.html
- DGT — Libro Taller Electrónico / Libro Electrónico de Mantenimiento: https://sede.dgt.gob.es/es/vehiculos/tramites-para-empresas/libro-taller-electronico/ ; https://www.dgt.es/nuestros-servicios/tu-vehiculo/tus-vehiculos/libro-electronico-de-mantenimiento/
- Plataforma Ganvam+DGT (Infotaller): https://www.infotaller.tv/concesionarios/Ganvam-DGT-plataforma-Libro-Mantenimiento_0_1386161380.html
- Competidores con OCR+IA ya en producción: https://1garage.ai/ ; https://app.myrevaultapp.com/ ; https://alternativeto.net/software/myautolog-vehicle-maintenance/about/ ; https://www.simplyfleet.app/solutions/ai-fleet-management

---

# Dictamen T2 — Frente TÉCNICA
**Idea:** Mantenimiento de vehículo v2 (VIN + plantillas por motorización + OCR/LLM de facturas + validación cruzada)
**Juez:** T2 (Técnica) — tribunal adversarial, contexto aislado
**Fecha del dictamen:** 2026-07-17
**Posición de partida:** NO CONFORMIDAD POR DEFECTO. La carga de la prueba recae en la idea.

---

## 0. Verificación del activo declarado: la v1

**Comprobación realizada el 2026-07-17** contra la cuenta pública `JDiaz-healthTech` vía API de GitHub (`api.github.com/users/JDiaz-healthTech/repos`, HTTP 200) y `git ls-remote` sobre 8+ nombres plausibles (`vehicle-maintenance`, `CarMaintenance`, `MantenimientoVehiculo`, `CarLog`, `MyCar`, etc.).

**Resultado: el repo de la v1 NO existe públicamente.** La cuenta tiene 8 repos públicos: Anthropofilia (PHP), Escape_Room, JDiaz-healthTech (perfil), JuliusScheduler (C#), laBiblioteca (docs), Prism (C#), RestApiCourse (C#), SurfSkateSpot (Kotlin). Ninguno es la app de mantenimiento de vehículos.

**Consecuencia técnica:** la "v1 ya hecha" es **inauditables desde este tribunal**. No puedo evaluar deuda técnica real, calidad del esquema Room, ni si el MVVM/Clean declarado es real o aspiracional. A efectos de este dictamen, la v2 se evalúa como **reconstrucción parcial con base no verificada**. El único Kotlin público (SurfSkateSpot, último push 2025-06-13) acredita familiaridad con el stack, no la existencia del activo. Nota: el perfil declara desarrollador .NET + SQL Server; Kotlin/Compose es competencia lateral, relevante para estimar velocidad en "horas sueltas".

---

## 1. Decodificación VIN: gadget, no esencial

- **NHTSA vPIC (gratuita):** su propia FAQ es explícita: los datos representan vehículos destinados a venta o importación en EE. UU.; VINs de vehículos no destinados al mercado US devuelven **resultado limitado**. Solo se decodifican WMIs registrados en vPIC (proceso 49 CFR Part 565). Un SEAT León (WMI `VSS`), un Renault Clio (`VF1`) o un Dacia Sandero — el parque real español — devolverán datos parciales o nulos. Los europeos que sí exportan a US (VW `WVW`, BMW `WBA`) decodifican mejor, pero **la variante/motorización europea concreta no está**. (Fuente: [vPIC FAQ](https://vpic.nhtsa.dot.gov/api/home/index/faq), verificado 2026-07-17.)
- **Agravante estructural:** el estándar ISO 3779 (VIN europeo) **no obliga a codificar año-modelo ni acabado**; la posición 10 = año es convención norteamericana. De un VIN europeo, sin base de datos privada, no se extrae con fiabilidad la motorización — que es justo lo que la idea necesita para elegir plantilla.
- **APIs comerciales (Vincario/vindecoder.eu y similares):** cobertura europea real, pero **de pago, orientadas B2B, precio de API no publicado** (requiere registro/contacto; el lado consumidor parte de ~8,90 €/informe). Modelo de créditos por consulta. Para una app de hobby sin ingresos, es un coste recurrente y una dependencia externa injustificada. (Fuentes: [vindecoder.eu](https://vindecoder.eu/), [Vincario pricing blog](https://vincario.com/blog/vin-decoder-api-pricing/), verificado 2026-07-17.)
- **Alternativa manual:** un selector marca/modelo/año/combustible son 4 campos que el usuario rellena **una vez por vehículo**. El VIN ahorra ~30 segundos una única vez en la vida del registro, a cambio de una dependencia poco fiable para el mercado objetivo (España).

**Conclusión T2.1:** el VIN es un **gadget de demo**, no una capacidad esencial. Para VINs europeos, la vía gratuita (vPIC) es insuficiente y la de pago es desproporcionada. NO CONFORME como feature troncal; tolerable solo como autorrelleno opcional best-effort.

## 2. Plantillas de intervalos por motorización: el dato no existe en abierto

- **No hay API pública gratuita de calendarios de mantenimiento OEM.** Lo que existe es comercial y US-céntrico: [Vehicle Databases](https://vehicledatabases.com/api/vehicle-maintenance), [DataOne](https://www.dataonesoftware.com/vehicle-data-vin-decoding/vehicle-service-data), Edmunds (US). Cobertura del parque europeo/español: no acreditada; precio: B2B. (Verificado 2026-07-17.)
- **"Intervalos investigados" = tabla curada a mano por Julius** desde manuales de propietario no estructurados. Hay que decirlo con esa crudeza. Coste real: horas por modelo (localizar manual, extraer, normalizar), multiplicado por la matriz marca × modelo × motor × año. Mantenimiento: los fabricantes cambian intervalos entre generaciones (p. ej. longlife vs. fijo en el grupo VAG).
- **Riesgo de fiabilidad con consecuencias físicas:** un intervalo de correa de distribución erróneo destroza un motor. Una tabla artesanal presentada como "perfil de mantenimiento del coche" transmite una autoridad que no tiene.
- **Vía honesta:** plantillas **genéricas por tipo de motorización** (diésel/gasolina/eléctrico/híbrido), claramente etiquetadas como orientativas, **editables por el usuario**, con disclaimer de "consulta tu manual". Eso es una tabla de ~20 filas, curable en una tarde, y técnicamente defendible. Todo lo que exceda eso (por modelo concreto) es deuda de datos perpetua.

**Conclusión T2.2:** NO CONFORME como "plantillas por modelo con intervalos investigados". CONFORME solo degradado a plantillas genéricas por motorización, editables, con descargo de responsabilidad.

## 3. OCR/LLM de tickets: viable, pero el problema no es el OCR

- **ML Kit Text Recognition v2 (on-device, gratis):** buen reconocimiento latino (85–100 % según calidad de imagen; mínimo ~16×16 px por carácter; sensible a tickets térmicos arrugados y mala luz). Pero **devuelve texto plano, no estructura**: extraer marca/pieza/precio de facturas de taller españolas heterogéneas exige un parser propio — trabajo considerable y frágil. (Fuentes: [ML Kit v2 docs](https://developers.google.com/ml-kit/vision/text-recognition/v2), verificado 2026-07-17.)
- **LLM multimodal cloud (2026):** el coste NO es el obstáculo. Precios verificados 2026-07-17: GPT-4o mini $0,15/M tokens entrada; Gemini 2.5 Flash $0,30/M entrada; Claude Haiku 4.5 $1/M entrada; una imagen consume del orden de cientos a ~2.000 tokens → **fracciones de céntimo por ticket**. Para uso personal o cientos de usuarios, coste despreciable. Fiabilidad de estructuración sobre facturas variadas: sustancialmente superior a cualquier parser artesanal. (Fuentes: [Gemini API pricing](https://ai.google.dev/gemini-api/docs/pricing), [comparativas 2026](https://www.aipricing.guru/blog/ai-api-pricing-comparison-2026/).)
- **RGPD — aquí está el problema real:** una factura de taller española lleva **matrícula (dato personal según la propia [AEPD](https://www.aepd.es/preguntas-frecuentes/0-conceptos-basicos/FAQ-0002-sobre-la-matricula-de-un-coche), verificado 2026-07-17)**, NIF, y a menudo nombre y dirección del cliente. Si la app la envía a una API cloud **con la clave de API del desarrollador**, Julius pasa de "app local" a **responsable/encargado de tratamiento**, con obligaciones: política de privacidad, DPA con el proveedor, base jurídica, transferencias internacionales (EE. UU./DPF), y declaración en Google Play Data Safety. Para una app de horas sueltas, eso es carga real.
- **Mitigaciones defendibles:** (a) pipeline por defecto **on-device** (ML Kit + heurísticas), cloud solo **opt-in explícito** con aviso claro; (b) recorte/redacción local de zonas con matrícula/datos antes del envío (añade complejidad no trivial); (c) que el usuario aporte su propia API key (elimina a Julius de la cadena de tratamiento, pero mata la UX para no-técnicos).
- **Validación cruzada factura ↔ plantilla:** mapear texto libre de taller ("sust. filtro habitáculo", "aceite 5W30 longlife", "kit distribución + bba. agua") contra una taxonomía de conceptos de mantenimiento **es un problema de NLP no trivial**. Con LLM y una taxonomía cerrada bien diseñada es abordable (clasificación forzada a enum); sin LLM, on-device, queda reducido a matching por palabras clave, frágil. Requiere además diseño previo de la taxonomía y un set de facturas reales de evaluación que hoy no existe.

**Conclusión T2.3:** técnicamente viable con LLM cloud barato, pero la propuesta tal cual (fotos de facturas → API cloud) es **NO CONFORME en RGPD sin mitigaciones**, y la validación cruzada es la parte de más riesgo de ingeniería de toda la v2 — no un "extra".

## 4. Arquitectura: incremental, sin backend

- **¿Backend? No.** Ninguna feature propuesta lo exige: VIN y LLM son llamadas API directas desde el cliente; plantillas son datos estáticos empaquetados o descargables; el registro es local. Un backend añade coste (hosting, auth, seguridad, RGPD ampliado) y mantenimiento perpetuo que "horas sueltas" no puede sostener. NO CONFORME cualquier variante v2 con backend propio.
- **v2 incremental sobre Room:** es la única vía compatible con el tiempo disponible — condicionada a que la v1 exista y su esquema lo permita (no verificable, ver §0). Si la v1 real no está en condiciones, la reconstrucción consume el presupuesto de la v2.
- **Sincronización/backup:** export/import a fichero + copia en Drive del usuario (o el backup automático de Android) cubre el 95 % de la necesidad sin backend. Sincronización multi-dispositivo en tiempo real: fuera de alcance para este perfil de proyecto; si algún día hace falta, Firebase/Supabase antes que backend propio.
- **Riesgo de alcance:** VIN + plantillas + OCR/LLM + validación cruzada son **cuatro features grandes** para un desarrollador cuyo día a día es .NET, en horas sueltas. Sin recorte, la v2 es una lista de deseos, no un plan.

## 5. Riesgos regulatorios

- **RGPD: confirmado como el riesgo principal**, y es mayor de lo que sugiere la ficha ("menor") en cuanto se activa el envío de facturas a cloud (§3). En modo 100 % local, riesgo casi nulo (tratamiento doméstico).
- **Añadidos que la ficha omite:** requisitos de Google Play (Data Safety, política de privacidad obligatoria si trata datos personales); si usa LLM cloud, condiciones de encargado del proveedor. **AI Act (UE):** uso de un modelo de propósito general vía API para extracción de datos propios — no es sistema de alto riesgo; obligaciones para Julius: ninguna significativa a fecha de hoy. 
- **Corrección al enunciado:** correcto que no hay regulación sectorial automotriz aplicable a un registro personal de mantenimiento. El único matiz: **no prescribir intervalos como si fueran del fabricante** (§2) — no es riesgo regulatorio, es riesgo de responsabilidad por información defectuosa, y se neutraliza con disclaimers y editabilidad.

---

## Veredicto T2

**APTO CON CONDICIONES** (frente técnica, exclusivamente):

1. **Verificabilidad de la v1:** publicar el repo o someterlo a auditoría antes de planificar la v2 como "incremental". Sin v1 verificable, replanificar como reconstrucción (verificado 2026-07-17: no existe en la cuenta pública).
2. **VIN degradado a opcional best-effort** con entrada manual marca/modelo/año/combustible como vía primaria. Prohibido depender de vPIC para vehículos europeos o contratar API comercial de VIN en esta fase.
3. **Plantillas solo genéricas por motorización**, editables por el usuario, con disclaimer explícito. Prohibido presentar intervalos por modelo como "investigados"/oficiales.
4. **OCR: on-device (ML Kit) por defecto; LLM cloud solo opt-in explícito** con aviso de privacidad, y decisión documentada sobre el tratamiento de matrícula/datos del cliente antes de publicar en Play Store.
5. **Sin backend propio en v2.** Backup vía export/Drive.
6. **La validación cruzada factura↔plantilla se trata como la feature de mayor riesgo**: taxonomía cerrada diseñada primero y un set de facturas reales de prueba antes de escribir una línea del matcher; si no cabe en el presupuesto de horas, se recorta ella, no el registro básico.

Incumplidas las condiciones 2–4, el dictamen pasa a **NO APTO** por dependencia de datos que no existen en abierto y exposición RGPD no mitigada.

---
*Fuentes principales (todas verificadas 2026-07-17): [GitHub API JDiaz-healthTech](https://api.github.com/users/JDiaz-healthTech/repos) · [NHTSA vPIC FAQ](https://vpic.nhtsa.dot.gov/api/home/index/faq) · [vindecoder.eu](https://vindecoder.eu/) · [Vincario — VIN API pricing](https://vincario.com/blog/vin-decoder-api-pricing/) · [ML Kit Text Recognition v2](https://developers.google.com/ml-kit/vision/text-recognition/v2) · [Gemini API pricing](https://ai.google.dev/gemini-api/docs/pricing) · [AI API pricing comparison 2026](https://www.aipricing.guru/blog/ai-api-pricing-comparison-2026/) · [Vehicle Databases maintenance API](https://vehicledatabases.com/api/vehicle-maintenance) · [DataOne service data](https://www.dataonesoftware.com/vehicle-data-vin-decoding/vehicle-service-data) · [AEPD — matrícula como dato personal](https://www.aepd.es/preguntas-frecuentes/0-conceptos-basicos/FAQ-0002-sobre-la-matricula-de-un-coche)*

---

# Dictamen T3 — Frente APRENDIZAJE
**Idea:** Mantenimiento de vehículo (v2) · **Fecha:** 2026-07-17 · **Posición de partida:** No conformidad por defecto

---

## 1. Inventario de aprendizaje: lo nuevo vs. lo repetido

El proponente declara la idea como "iteración sobre terreno conocido". Eso es una confesión, no un atenuante. Descomposición del proyecto por componente:

| Componente | Peso estimado del proyecto | Aprendizaje nuevo | Transferencia al pivote |
|---|---|---|---|
| CRUD de intervenciones, Room, Compose, MVVM/Clean | ~55-65% | **Cero.** Ya lo hizo en la v1, completa y funcionando. Repetirlo es mecanografía con arquitectura. | Nula |
| Decodificación VIN (llamada a API + parseo) | ~5% | Marginal: consumir una API REST. Julius trabaja en .NET; consumir APIs no es aprendizaje, es rutina. | Nula |
| Plantillas de intervalos por motorización | ~10% | Modelado de datos algo más rico. Bajo. | Marginal |
| **Pipeline OCR/LLM: foto de ticket → extracción estructurada → autorrelleno → validación cruzada** | **~20-25%** | **Alto.** Extracción multimodal (on-device vs. cloud), salida estructurada con esquema, matching semántico de conceptos ("cambio aceite 5W30" ↔ intervención "aceite motor"), evaluación de precisión. Esto no lo ha hecho nunca. | **Alta** |
| Backend (si lo añade) | 0% en la ficha | No está en la ficha. No se juzga humo. | — |

Conclusión parcial: **el único bloque con aprendizaje real ocupa como mucho un cuarto del proyecto**. El resto es re-ejecución de habilidades ya demostradas en la v1. Una v2 completa es un proyecto de 100 horas donde ~75 son calistenia de lo que ya sabe.

## 2. La transferencia real al pivote

El patrón "fotografiar documento semiestructurado → extraer campos tipados → validar contra un perfil conocido" **sí es isomorfo** a problemas healthtech reales:

- Ticket de taller ≈ informe de audiometría escaneado, volante de derivación, factura clínica.
- Validación cruzada contra el perfil del vehículo (¿este aceite corresponde a esta motorización?) ≈ validación contra el historial del paciente (¿este umbral es coherente con la audiometría previa?).
- El matching semántico de conceptos de taller es estructuralmente idéntico al mapeo de terminología clínica libre a vocabularios controlados.

Esa transferencia vale mucho. Es de las pocas competencias donde su perfil dual (dominio clínico + código) le da ventaja competitiva real: sabe *qué* campos importan en un documento clínico y puede construir *cómo* extraerlos.

**Pero el problema es de densidad, no de dirección.** La transferencia vive en el 20-25% del proyecto. El 75-80% restante (CRUD, pantallas, navegación, Room) la diluye hasta hacerla anecdótica. Con "horas sueltas" como presupuesto temporal, la dilución no es un matiz: es la diferencia entre tener el pipeline funcionando en 6 semanas o en 6 meses. Y en 6 meses el pivote sigue congelado.

Agravante: la v2 compite en cartera contra ideas que son healthtech directas (RealAudio, logopedia). Cada hora en CRUD de coches es una hora que ninguna de esas ideas recibe.

## 3. Alternativa quirúrgica: el spike sobre la v1

Extraer SOLO el módulo de extracción de documentos e injertarlo en la v1 existente:

**Qué se gana:**
- El 100% del aprendizaje valioso (pipeline multimodal, esquema, matching, evaluación) sin pagar el peaje de reconstrucción.
- Integrar en código existente propio: eso también es una habilidad (evolucionar sin reescribir), y es más realista profesionalmente que el eterno greenfield.
- Un artefacto portfolio-compatible: "módulo de extracción estructurada de documentos con LLM, con métricas de precisión sobre dataset propio" — eso se cuenta igual en una entrevista healthtech venga de tickets o de audiogramas.
- Tiempo liberado para la cartera healthtech.

**Qué se pierde respecto a la v2 completa:**
- Práctica repetida de Compose/Room/arquitectura → valor de aprendizaje cero, pérdida nominal.
- La "satisfacción" de una app rehecha y pulida → irrelevante para el frente aprendizaje.
- Posible fricción si la v1 tiene deuda técnica que estorbe al injerto → esa fricción es, en sí, aprendizaje (trabajar sobre legacy propio).

Balance: **la pérdida real de aprendizaje del spike frente a la v2 es ~0-5%. El ahorro de tiempo es ~70-75%.** No hay debate técnico aquí; solo hay debate emocional ("me apetece rehacerla bonita"), y este tribunal no puntúa apetencias.

## 4. Riesgo de vaciado por IA

Si delega el pipeline a un asistente de código, el proyecto queda hueco: habrá "hecho" extracción de documentos sin poder explicarla en una entrevista. Reparto obligatorio:

**A mano (innegociable):**
1. **Esquema de extracción**: diseñar los tipos/campos (fecha, kilometraje, conceptos, importes, taller) y sus reglas de validación. Es la parte que codifica criterio de dominio.
2. **Prompts estructurados**: diseño iterativo de prompts con salida JSON validada (schema/function calling), manejo de campos ausentes y de alucinaciones. Iterar él, no el asistente.
3. **Matching semántico**: la lógica que mapea texto libre del ticket a conceptos del catálogo de intervenciones (exacto vs. embedding vs. LLM-as-matcher: que pruebe y compare).
4. **Evaluación**: dataset propio de 30-50 tickets reales anotados a mano, métricas por campo (precisión/exhaustividad), comparación entre al menos dos enfoques (p. ej. ML Kit on-device vs. LLM cloud multimodal). Sin este punto, no hay aprendizaje: hay demo.

**Delegable sin pérdida:**
- Boilerplate de cámara/permisos, pantallas de revisión del autorrelleno, serialización, plumbing de Room para los campos nuevos, tests repetitivos.

## 5. Cuantificación

| Métrica | v2 completa | Módulo OCR/LLM sobre v1 |
|---|---|---|
| % del esfuerzo con aprendizaje nuevo | ~20-25% | ~85-90% |
| % alineamiento con pivote healthtech | **~15-20%** (el pipeline, diluido) | **~70-75%** (pipeline casi puro; el 25 restante es dominio automoción no transferible) |
| Densidad de aprendizaje/hora (0-10) | **2-3** | **7-8** |
| Coste de oportunidad sobre cartera healthtech | Alto (meses de horas sueltas) | Bajo (semanas) |
| Riesgo de abandono a medias | Alto (reconstrucciones largas + horas sueltas) | Bajo (alcance acotado, app base ya funciona) |

---

## Veredicto T3

**NO APTO** — la v2 completa, tal como está formulada, en el frente de aprendizaje.

Motivo: el 75-80% del proyecto es re-ejecución declarada de terreno conocido (densidad de aprendizaje 2-3/10) y su coste temporal congela el pivote que el propio proponente define como criterio dominante. El único bloque defendible es el pipeline de extracción de documentos, y ese bloque **no necesita la v2 para existir**.

Vía de rescate (fuera del alcance de esta ficha, exigiría re-presentación): el **spike quirúrgico** — módulo OCR/LLM injertado en la v1 — sería APTO CON CONDICIONES en este frente, con estas condiciones mínimas:
1. Prohibida toda reconstrucción de la v1; solo el módulo.
2. Esquema, prompts, matching y evaluación escritos a mano (punto 4).
3. Dataset propio de ≥30 tickets anotados y métricas por campo, comparando al menos dos enfoques de extracción.
4. Presupuesto cerrado (~30-40 h); al terminar, la siguiente inversión de horas va a la cartera healthtech aplicando este mismo pipeline a un documento clínico.

---

# Dictamen T4 — ALCANCE / REALISMO
**Idea:** Mantenimiento de vehículo (v2) · **Fecha:** 2026-07-17 · **Juez:** T4 (alcance/realismo, contexto aislado)
**Posición de partida:** no conformidad por defecto. La carga de la prueba recae en la idea, no en el juez.

---

## 0. Marco de cálculo

- 1 sesión = ~2h de trabajo real (descontado arranque de contexto, quedan ~1,5h netas por sesión; las horquillas ya lo incorporan).
- Disponibilidad total declarada: 2-4 sesiones/semana **para las 7 ideas juntas**.
- Prioridad declarada: healthtech (2 ideas). Esta idea es, en el mejor de los casos, la 3ª-7ª en cola.
- Cuota realista para ESTA idea: **1-2 sesiones/mes** (escenario honesto), **4 sesiones/mes** (escenario en el que las healthtech se abandonan, lo cual contradice la prioridad declarada).

Toda cifra de calendario de este dictamen usa la cuota honesta de 1-2 sesiones/mes salvo indicación contraria.

---

## 1. Estimación por bloques (sesiones de ~2h, mín-máx)

### (a) Decisión v2-incremental vs reconstrucción

| Concepto | Mín | Máx | Notas |
|---|---|---|---|
| Auditoría de la v1 + decisión documentada | 1 | 2 | Leer el propio código, listar deuda real vs percibida |
| **Coste oculto de reconstruir:** reponer TODO lo que la v1 ya hace (modelo de datos, Room, CRUD de intervenciones, pantallas, navegación, ajustes) antes de añadir NADA nuevo | 15 | 30 | Es reescribir una app completa. 30-60h para volver al punto de partida funcional. Cero valor nuevo entregado durante meses. |

La ficha no decide entre incremental y reconstrucción. Eso ya es una no conformidad: una idea que no sabe si empieza en la casilla 0 o en la casilla 40 no tiene alcance definido. La reconstrucción "limpia" de algo que **ya funciona y ya se usa a diario** es el clásico proyecto-trampa del desarrollador: 15-30 sesiones de gratificación arquitectónica con valor de usuario nulo.

### (b) Decodificación VIN

| Concepto | Mín | Máx | Notas |
|---|---|---|---|
| Integración API (p. ej. NHTSA vPIC gratuita) | 2 | 3 | La API gratuita es de mercado **estadounidense**: los VIN de vehículos europeos (el parque real de un usuario en Santander) devuelven datos pobres o incompletos. Las APIs con buena cobertura europea son de pago. |
| Mapeo de respuesta → perfil de coche (motorización, modelo) | 1 | 3 | Normalizar taxonomías ajenas es siempre más caro de lo previsto |
| Fallback manual (formulario) | 1 | 2 | Irónicamente, esto es lo único que funcionará de forma fiable en Europa |
| Casos raros y pruebas | 1 | 2 | |
| **Subtotal** | **5** | **10** | **Riesgo alto de que el resultado final sea "casi siempre fallback manual", es decir, 5-10 sesiones para un formulario que ya podría existir sin VIN.** |

### (c) Plantillas de intervalos por motorización + motor de recordatorios

| Concepto | Mín | Máx | Notas |
|---|---|---|---|
| Investigación documental: leer manuales, foros, cuadros de mantenimiento; curar tablas fiables para diésel/gasolina/eléctrico **genéricas** | 6 | 12 | Esto NO es código. Son 12-24h de lectura y estructuración. Y una plantilla "genérica por motorización" es de fiabilidad dudosa por definición: los intervalos reales varían por fabricante, motor concreto, año y condiciones de uso. |
| Curación **por modelo** (si se aspira a datos "investigados" de verdad) | ∞ | ∞ | Sumidero sin fondo. Cada modelo es una investigación nueva. No estimable; solo acotable por decreto. |
| Modelo de datos de plantillas + asignación al perfil | 2 | 3 | |
| Motor de recordatorios km/tiempo (entrada de odómetro, cálculo, notificaciones, WorkManager, permisos de notificación Android) | 3 | 6 | Las notificaciones fiables en Android moderno (Doze, permisos POST_NOTIFICATIONS, exact alarms) son más caras de lo que parecen |
| **Subtotal (solo la versión genérica acotada)** | **11** | **21** | |

### (d) Pipeline OCR/LLM de tickets

| Concepto | Mín | Máx | Notas |
|---|---|---|---|
| Captura de cámara + galería | 1 | 2 | |
| Preprocesado de imagen (recorte, contraste) | 1 | 3 | |
| Extracción estructurada vía LLM (prompting, esquema JSON, gestión de API key, coste por llamada, errores de red) | 3 | 5 | Decidir además quién paga las llamadas si la app deja de ser personal |
| UI de corrección manual del usuario | 2 | 4 | Imprescindible: la extracción nunca será perfecta |
| Validación cruzada contra plantilla/perfil del coche | 2 | 3 | Depende de que (c) exista, acoplamiento de alcance |
| Evaluación de precisión con tickets reales (reunir 30-50 tickets, medir, iterar prompts) | 3 | 6 | Los tickets térmicos borrosos, abreviaturas de taller ("cbio filt hab"), facturas manuscritas y formatos por taller son un pozo: cada taller nuevo es un caso nuevo |
| **Subtotal** | **12** | **23** | |

### (e) UI de todo lo anterior

| Concepto | Mín | Máx |
|---|---|---|
| Pantallas de perfil/VIN, plantillas, recordatorios, flujo de ticket, estados de error/carga, pulido | 6 | 12 |

### (f) Migración de datos v1 (si incremental)

| Concepto | Mín | Máx |
|---|---|---|
| Migraciones de esquema Room + adaptación de datos existentes | 1 | 3 |

---

## 2. Los tres escenarios contra el calendario real

| Escenario | Sesiones (mín-máx) | Horas | Calendario a 1-2 ses./mes | Calendario a 4 ses./mes (irreal: mata la prioridad healthtech) |
|---|---|---|---|---|
| **1. Reconstrucción completa** (a-paridad + b + c + d + e) | **49 - 96** | 98-192h | **2 a 8 años** | 12-24 meses |
| **2. v2 incremental completa** (a-decisión + b + c + d + e + f) | **36 - 71** | 72-142h | **1,5 a 6 años** | 9-18 meses |
| **3. Módulo mínimo sobre v1** (detalle abajo) | **8 - 15** | 16-30h | **4 a 12 meses** | 2-4 meses |

Lectura sin anestesia: con la disponibilidad declarada y la prioridad declarada, los escenarios 1 y 2 **no son planes, son fantasías con hoja de cálculo**. Un proyecto secundario de 36-96 sesiones compitiendo contra 6 ideas más y contra un pivote healthtech prioritario no termina; se abandona a mitad, típicamente con la v1 funcional ya rota por una migración a medias.

### Detalle del escenario 3 (el único con calendario defendible)

Mantener la v1 tal cual + añadir SOLO foto-de-ticket→autorrelleno. Sin VIN. Sin plantillas universales. Plantilla codificada **solo para SU coche** (los intervalos de su propio manual: 1 sesión de leer un manual que ya tiene en la guantera).

| Bloque | Mín | Máx |
|---|---|---|
| Captura cámara/galería | 1 | 2 |
| Extracción LLM estructurada | 3 | 5 |
| UI de corrección + guardado como intervención v1 | 2 | 3 |
| Plantilla de su coche (datos + validación cruzada simple) | 1 | 2 |
| Evaluación con sus propios tickets reales | 1 | 3 |
| **Total** | **8** | **15** |

Además: valida la hipótesis técnica más arriesgada de toda la v2 (¿el LLM extrae bien tickets de taller españoles reales?) por ~10% del coste del escenario 2. Si la extracción no alcanza precisión útil con SUS tickets, toda la v2 queda invalidada habiendo quemado 8-15 sesiones en vez de 70.

---

## 3. Sumideros ocultos (riesgo de desbordamiento)

1. **Curación de intervalos: no termina nunca.** "Datos investigados por motorización" es una promesa editorial, no una feature. Cada modelo, motor y año es distinto; la alternativa (plantilla genérica) es vagamente incorrecta para casi todo el mundo. O se acota por decreto (solo su coche) o es un pozo infinito.
2. **OCR de tickets reales: pozo de casos raros.** Térmicos desvaídos, fotos torcidas, abreviaturas crípticas de taller, IVA desglosado de mil formas, facturas de varias páginas. La precisión sube rápido al 70% y luego cada punto adicional cuesta sesiones.
3. **Perfeccionismo de reconstrucción.** Reescribir "limpio" lo que ya funciona es el sumidero con mejor coartada: se siente productivo y entrega cero. 15-30 sesiones de coste oculto ya cuantificado.
4. **Scope creep satelital:** recordatorios → notificaciones → widgets → exportación CSV/PDF → copia en la nube → multi-vehículo. Cada uno "solo son un par de tardes". Suman otras 10-20 sesiones fantasma no presupuestadas.
5. **VIN europeo:** riesgo real de invertir 5-10 sesiones para acabar en el fallback manual como camino principal.
6. **Coste de contexto:** con 7 ideas en paralelo, cada sesión suelta paga un impuesto de re-arranque mental; a 1-2 sesiones/mes por idea, ese impuesto puede comerse el 20-30% del tiempo neto.

---

## 4. Recortes: el MVP honesto

El MVP honesto NO es "la v2 con menos pulido". Es el **escenario 3**: v1 intacta + módulo foto→autorrelleno + plantilla de un solo coche. Todo lo demás (VIN, plantillas universales, reconstrucción) es alcance especulativo sin usuario que lo pida — el único usuario conocido es el propio proponente, y su coche ya se sabe cuál es sin decodificar ningún VIN.

---

## Veredicto T4

**APTO CON CONDICIONES** — exclusivamente en el frente alcance/realismo, y solo bajo TODAS estas condiciones:

1. **Prohibida la reconstrucción.** La v1 funcional se conserva; cualquier v2 es incremental. La decisión que la ficha deja abierta queda cerrada aquí por realismo puro: 15-30 sesiones de coste de paridad son incompatibles con 1-2 sesiones/mes.
2. **Alcance limitado al escenario 3** (8-15 sesiones): módulo foto-de-ticket→autorrelleno + plantilla solo para su coche. VIN y plantillas universales quedan fuera, sin excepción.
3. **Timebox duro de 15 sesiones y compuerta de precisión:** si tras evaluar con sus propios tickets reales la extracción no alcanza utilidad práctica (corrige menos de lo que teclea), el módulo se cierra y la idea vuelve a v1 congelada.
4. **Sin satélites:** nada de notificaciones nuevas, exportación, nube ni multi-vehículo dentro de este timebox.

Los escenarios "reconstrucción completa" y "v2 incremental completa" son, con la disponibilidad y prioridades declaradas, **NO APTOS**: 1,5-8 años de calendario para una idea de cola contra un pivote healthtech prioritario no es un plan, es una deuda de atención.
