# Tribunal Fase 1 — RealAudio

> Cuatro dictámenes independientes emitidos en contextos aislados (ninguno leyó a los demás). Fecha: 2026-07-17.

---

# Dictamen T1 — Frente MERCADO — RealAudio

> **Juez:** T1 (Mercado) · **Fecha de emisión:** 2026-07-17 · **Posición de partida:** no conformidad por defecto.
> **Alcance:** exclusivamente viabilidad de mercado. No evalúo valor formativo, arquitectura técnica ni ejecución — eso corresponde a otros frentes.

---

## 1. Panorama competitivo verificado (julio 2026)

### 1.1 La plataforma ya absorbió la propuesta

**Apple.** El test de audición por audiometría de tono puro + modo audífono (Hearing Aid, pérdida leve-moderada) + acomodaciones de auriculares son funciones **nativas, gratuitas y con aval regulatorio** en AirPods Pro 2/3. En 2026 la expansión es agresiva: Filipinas en marzo de 2026, India (test) e Italia (modo audífono) anunciados el 21 de mayo de 2026; la suite de salud auditiva supera los **100 países** ([MacRumors, 12-05-2026](https://www.macrumors.com/2026/05/12/apple-health-features-more-countries/); [9to5Mac, 21-05-2026](https://9to5mac.com/2026/05/21/apple-watch-and-airpods-health-features-get-major-new-global-expansions/); [Apple, disponibilidad por región, verificado 17-07-2026](https://www.apple.com/airpods-pro/feature-availability/)). Esto es **exactamente** la ficha de RealAudio (test guiado → compensación de curva → informe → derivación), ejecutada por el actor con más recursos regulatorios del planeta y regalada con el hardware.

**Samsung.** Adapt Sound (test auditivo por frecuencias y oído → perfil personalizado aplicado a multimedia y llamadas) es nativo en One UI y se ha profundizado con One UI 7 y los Galaxy Buds3/Buds 4 Pro, incluyendo presets por edad orientados a presbiacusia ([Samsung Newsroom, verificado 17-07-2026](https://news.samsung.com/global/galaxy-buds3-series-offers-enhanced-convenience-on-the-galaxy-s25-series); [Samsung Community](https://eu.community.samsung.com/t5/tips-how-to/did-you-know-adapt-sound-personalised-audio-for-your-ears/ba-p/14442934)). Samsung es el mayor OEM Android: el usuario objetivo de RealAudio con un Galaxy **ya tiene RealAudio de fábrica**, mejor integrado de lo que una app de terceros puede lograr.

**Google/Android.** Sound Amplifier nativo, soporte ASHA desde Android 10, LE Audio + Auracast integrados en Android 16, y Hearing Wellness en Pixel Buds ([AOSP, verificado 17-07-2026](https://source.android.com/docs/core/connect/bluetooth/asha); [Google Support](https://support.google.com/googlepixelbuds/answer/14005705); [Tom's Guide](https://www.tomsguide.com/phones/android-phones/how-to-enable-sound-amplifier-on-google-pixel)). La dirección de plataforma es inequívoca: la accesibilidad auditiva se resuelve **en el sistema operativo y en el firmware del auricular**, no en apps de terceros.

### 1.2 El B2B ya está tomado y el B2C especializado se retiró

**Mimi Hearing Technologies** — el dato más incriminatorio del expediente. Mimi (Series B, $25M) opera hoy con **+80 modelos de auriculares habilitados, +8M de dispositivos, SDK integrado en SoCs de Qualcomm, Airoha, BES y otros**, con nuevos productos (Voice Clarity) llegando a mercado en Q1 2026 ([Mimi, balance 2025 del CEO, verificado 17-07-2026](https://mimi.io/blog/from-our-ceo-a-look-back-at-2025-at-mimi-hearing-technologies); [mimi.io/partners](https://mimi.io/partners)). Y el hecho clave: **Mimi retiró su app de consumo para Android el 21 de mayo de 2024 y renunció a su certificación CE clase 1**, concentrándose en B2B e iOS ([Mimi, aviso oficial](https://mimi.io/blog/mimi-hearing-test-app-no-longer-available-on-android-what-you-need-to-know)). Una empresa financiada, con equipo científico propio y años de datos, **evaluó el segmento exacto de RealAudio (app B2C de test+personalización en Android) y lo abandonó**. Eso no es un hueco: es un solar del que el anterior ocupante se marchó por algo.

**Resto del campo:**
- **SoundID (Sonarworks):** activo en Android, freemium, respaldado por una empresa de calibración profesional; su predecesor de pago (True-Fi) fue **descontinuado** ([sonarworks.com, verificado 17-07-2026](https://www.sonarworks.com/soundid); [True-Fi discontinued](https://www.sonarworks.com/truefi)).
- **Jacoti ListenApp:** vivo, pero es **dispositivo médico CE clase IIa** — ilustra la barrera regulatoria real de "imitar un audífono" en la UE ([jacoti.com, verificado 17-07-2026](https://jacoti.com/solutions/hearing-suite/listenapp/)).
- **Petralex:** vivo, mantenimiento menor, explícitamente "no es dispositivo médico certificado"; ocupa el nicho de bajo valor percibido ([Google Play, verificado 17-07-2026](https://play.google.com/store/apps/details?id=com.it4you.petralex)).
- **hearWHO (OMS):** gratuito, con marca OMS, ~3.800 descargas/mes y rating 3,6 ([AppBrain, verificado 17-07-2026](https://www.appbrain.com/app/hearwho/com.hearxgroup.hearwho)). Si el cribado auditivo gratuito con el aval de la OMS mueve menos de 4.000 descargas mensuales, la demanda orgánica de "testéate la audición con el móvil" es **débil**, no latente.
- **Wavelet:** el EQ sistémico de referencia en Android — 4,8M de descargas acumuladas, ~470.000/mes, **gratuito** con Pro opcional ([AppBrain, verificado 17-07-2026](https://www.appbrain.com/app/wavelet-headphone-specific-eq/com.pittvandewitt.wavelet)). Fija el precio de referencia de la categoría "EQ personalizado en Android" en **cero**.

### 1.3 Restricción de plataforma con efecto de mercado directo

Android **no ofrece una vía fiable para procesar el audio de otras apps**: el problema del audio session ID hace que los EQ sistémicos fallen con apps de stack propio (Wavelet no funciona con YouTube; otros recurren a hacks de captura de pantalla o requieren root) ([Esper.io, análisis técnico, verificado 17-07-2026](https://www.esper.io/blog/android-equalizer-apps-inconsistent); [RootlessJamesDSP](https://github.com/timschneeb/RootlessJamesDSP)). La promesa central de la ficha — "ecualización aplicada a multimedia, **llamadas o todo**" — es, en Android sin root, parcial en el mejor caso e imposible en llamadas en el caso general. Esto no es un detalle técnico ajeno a mi frente: **el producto no puede entregar la propuesta de valor por la que competiría**, y los competidores que sí pueden (Samsung, Mimi-en-SoC, Apple) operan por debajo de la capa de apps.

### 1.4 Contexto OTC / regulatorio

El mercado OTC de audífonos en EE. UU. (~$1.000M en 2026) crece más lento de lo previsto: solo +4 puntos porcentuales de adopción incremental, y el estudio señala que **los earbuds con funciones auditivas tuvieron más impacto que los propios OTC** ([NIH/PMC, MarkeTrak, verificado 17-07-2026](https://pmc.ncbi.nlm.nih.gov/articles/PMC12638189/)). En la UE **no existe categoría OTC equivalente**: cualquier producto que se presente como compensación auditiva cae bajo el MDR y requiere certificación para venderse ([EFHOH](https://efhoh.org/wp-content/uploads/2025/05/2022-Over-The-Counter-Hearing-Aids-EFHOH-Statement.pdf)). Una app que "imita un audífono básico" y emite "recomendación de derivación clínica", publicada por un individuo en la UE sin marcado CE, opera en zona regulatoria gris con riesgo de retirada de Play Store — y Google ha ido endureciendo los requisitos para apps de salud.

---

## 2. Demanda: grande en epidemiología, ínfima en comportamiento de pago

- La epidemiología es real y enorme: ~1.160M de personas con pérdida leve; 2.500M con algún grado de pérdida en 2050 (OMS); solo ~17% de quienes tienen pérdida incapacitante usa audífonos ([WHO vía Swift Audiology, verificado 17-07-2026](https://swiftaudiology.com/the-world-health-organization-estimates-2-5-billion-with-hearing-loss-by-2050/)).
- Pero el comportamiento observado del usuario con presbiacusia incipiente es: **negación y espera media de años antes de actuar**; y cuando actúa en el móvil, usa lo que ya viene de serie (Adapt Sound, Sound Amplifier, accesibilidad de AirPods) o lo gratuito (Wavelet, hearWHO). No hay evidencia de disposición a pagar por una app de test+EQ en Android: el único intento de cobro directo documentado en la categoría (True-Fi) fue descontinuado, Mimi abandonó el B2C Android, y la app de la OMS apenas registra tracción.
- La paradoja demográfica: el usuario con presbiacusia (60+) es precisamente el segmento con **menor propensión a descubrir, instalar, configurar y pagar** apps de nicho en Play Store. Quien sí instalaría RealAudio (audiófilo joven, curioso del self-tracking) no tiene el problema que la app resuelve.

**Conclusión de demanda:** el mercado direccionable teórico es masivo; el mercado alcanzable por un desarrollador individual en Android B2C, tras descontar lo nativo, lo gratuito y lo regulado, es residual y sin precio.

---

## 3. ¿Hueco para un desarrollador individual?

**No en la propuesta tal como está formulada.** La personalización auditiva se está absorbiendo en dos capas donde una app de terceros no puede competir:

1. **Sistema operativo** (Apple Hearing Aid/Test, Samsung Adapt Sound, Android Sound Amplifier + LE Audio/Auracast) — gratis, preinstalado, con acceso privilegiado al pipeline de audio.
2. **Firmware/SoC del auricular** (Mimi en Qualcomm/Airoha/BES; 28 modelos nuevos solo en 2025) — el procesamiento viaja con el hardware, no con el teléfono.

Entre ambas capas, la franja "app Android de terceros" está ocupada por gratuidad (Wavelet, hearWHO) y por dispositivos médicos certificados (Jacoti). Los huecos residuales que existen — p. ej. audiología pediátrica digital, herramientas para profesionales/gabinetes, seguimiento post-adaptación de audífonos, cribado escolar — son **B2B o clínicos, no la app B2C descrita en la ficha**, y ninguno es RealAudio.

---

## 4. El diferencial clínico de Julius (10 años de audiología pediátrica)

Es un activo **de credibilidad y de producto, no de mercado**, y en esta ficha ni siquiera se despliega donde vale:

- El criterio clínico mejora el diseño del test (test-retest, criterio de concordancia, gate de ruido ambiente — la ficha lo refleja). Pero el usuario de Play Store **no puede verificar ni valora** la solvencia clínica del autor; compite en un escaparate donde Apple y Samsung firman con su marca y Mimi con papers. La ventaja no es apropiable como distribución, precio ni retención.
- Peor: la experiencia es **pediátrica**, y el segmento objetivo declarado es presbiacusia adulta. El diferencial declarable no coincide con el usuario declarado.
- Donde sí se traduciría en ventaja real (empleabilidad en healthtech, consultoría, herramienta clínica B2B, contenido de autoridad) está **fuera del perímetro de esta idea como producto de mercado**.

Veredicto parcial: ventaja de credibilidad personal, **no** ventaja competitiva de mercado para RealAudio.

---

## 5. Monetización

| Vía | Evaluación |
|---|---|
| **B2C de pago (compra/suscripción)** | **Descartada.** Precio de referencia de la categoría: 0 € (Wavelet, Adapt Sound, hearWHO, accesibilidad nativa). Precedentes de cobro directos fracasados o retirados (True-Fi, Mimi Android). |
| **Freemium** | **Descartada como negocio.** El freemium exige volumen; sin presupuesto de adquisición y contra funciones nativas gratuitas, el funnel no existe. Serviría solo como formato de publicación, no como ingreso. |
| **B2B / licencia** | **Fuera de alcance.** Requiere SDK, datos de validación, certificación y equipo comercial; el hueco lo ocupa Mimi con años de ventaja y contratos de SoC. |
| **Portfolio profesional** | **Única vía con retorno positivo verificable** — pero eso es retorno de carrera, no de mercado, y queda fuera de mi frente. Lo consigno como descarte explícito de monetización. |

---

## Señales agravantes (resumen probatorio)

1. Mimi — el comparable más directo, financiado y con ciencia propia — **salió del B2C Android** (21-05-2024) y renunció al CE clase 1.
2. Apple y Samsung entregan la propuesta completa **gratis y de fábrica**, con expansión regulatoria activa durante 2026.
3. Android no permite entregar de forma fiable el núcleo de la promesa (EQ sobre "llamadas o todo") sin root.
4. La demanda orgánica observada de cribado auditivo móvil es marginal (hearWHO: ~3.800 descargas/mes con marca OMS).
5. En la UE, "imitar un audífono" + "recomendar derivación" sin marcado CE es riesgo regulatorio, no diferencial.
6. Ningún precedente de pago B2C sostenido en la categoría en Android.

---

## Veredicto T1

**NO APTO** (frente Mercado, exclusivamente).

RealAudio, como producto de mercado B2C en Android, entra en una categoría cuyo precio de referencia es cero, cuya funcionalidad está siendo absorbida por el sistema operativo (Apple, Samsung, Google) y por el firmware de los auriculares (Mimi en SoCs), cuyo comparable mejor financiado abandonó exactamente este segmento en 2024, y cuya promesa central no es técnicamente entregable en la plataforma elegida sin privilegios de sistema. No existe hueco de mercado defendible para un desarrollador individual con horas sueltas, no existe vía de monetización realista (todas descartadas de forma explícita en §5), y el diferencial clínico del proponente es de credibilidad — y además pediátrico para un target adulto —, no de ventaja competitiva.

Este veredicto **no se pronuncia** sobre el valor de RealAudio como vehículo de aprendizaje o pieza de portfolio para el pivote a healthtech: eso corresponde a otros frentes del tribunal. Como mercado: no conformidad confirmada.

---

### Fuentes principales (fecha de verificación: 2026-07-17)

- [Apple — AirPods Pro Hearing Health Feature Availability](https://www.apple.com/airpods-pro/feature-availability/)
- [MacRumors — Apple health features expand to more countries (12-05-2026)](https://www.macrumors.com/2026/05/12/apple-health-features-more-countries/)
- [9to5Mac — Global expansion of Watch/AirPods health features (21-05-2026)](https://9to5mac.com/2026/05/21/apple-watch-and-airpods-health-features-get-major-new-global-expansions/)
- [Mimi — A look back at 2025 (CEO)](https://mimi.io/blog/from-our-ceo-a-look-back-at-2025-at-mimi-hearing-technologies)
- [Mimi — Hearing Test App no longer available on Android (2024)](https://mimi.io/blog/mimi-hearing-test-app-no-longer-available-on-android-what-you-need-to-know)
- [Samsung Newsroom — Galaxy Buds3 + One UI 7 / Adapt Sound](https://news.samsung.com/global/galaxy-buds3-series-offers-enhanced-convenience-on-the-galaxy-s25-series)
- [AOSP — Hearing aid audio support (ASHA)](https://source.android.com/docs/core/connect/bluetooth/asha)
- [Google — Pixel Buds Hearing Wellness](https://support.google.com/googlepixelbuds/answer/14005705)
- [Esper.io — Why Android equalizer apps don't work with all media players](https://www.esper.io/blog/android-equalizer-apps-inconsistent)
- [AppBrain — Wavelet (4,8M descargas; ~470K/mes)](https://www.appbrain.com/app/wavelet-headphone-specific-eq/com.pittvandewitt.wavelet)
- [AppBrain — hearWHO (~3,8K descargas/mes)](https://www.appbrain.com/app/hearwho/com.hearxgroup.hearwho)
- [NIH/PMC — Hearing aid adoption in the OTC era (MarkeTrak)](https://pmc.ncbi.nlm.nih.gov/articles/PMC12638189/)
- [Jacoti — ListenApp (CE clase IIa)](https://jacoti.com/solutions/hearing-suite/listenapp/)
- [Sonarworks — SoundID / True-Fi discontinued](https://www.sonarworks.com/truefi)
- [WHO (vía Swift Audiology) — 2.500M con pérdida auditiva en 2050](https://swiftaudiology.com/the-world-health-organization-estimates-2-5-billion-with-hearing-loss-by-2050/)

---

# Dictamen T2 — TÉCNICA + REGULATORIO — RealAudio

**Juez:** T2 (frente técnico y regulatorio, exclusivamente)
**Fecha del dictamen:** 2026-07-17
**Posición de partida:** no conformidad por defecto. Todas las fuentes verificadas el 2026-07-17 salvo indicación contraria.

---

## Resumen ejecutivo

La ficha de RealAudio contiene dos promesas nucleares que este dictamen examina por separado:

1. **Salida A** — EQ personalizada aplicada "a la salida de audio del móvil (multimedia, llamadas o todo)", "imitando un audífono básico". **Infactible en Android sin root en los términos descritos.** El caso "llamadas" es directamente imposible para una app de terceros; el caso "todo el audio" depende de una API deprecada desde 2011 con comportamiento no garantizado por fabricante.
2. **Salida B** — test que "estima pérdida auditiva" y "recomienda derivación clínica". **Tal como está redactada, es la definición de libro de software producto sanitario bajo MDR 2017/745**, clase IIa mínimo por la regla 11, lo que exige organismo notificado: económicamente y temporalmente inviable para un desarrollador individual con horas sueltas.

Además, el umbral medido sin transductor calibrado no es un umbral en dB HL: es un número sin unidad clínica, con error no acotable. El propio mercado ya ha dictado sentencia sobre este camino: Mimi, empresa financiada y especializada, **abandonó su certificación CE de su test auditivo en mayo de 2024** y migró a un estándar de consumo (ANSI/CTA-2118) precisamente para salir del perímetro regulatorio.

---

## A) Capacidades reales de Android

### A.1 — ¿EQ global a todo el audio del sistema sin root? No de forma fiable, y "llamadas" no en absoluto

**`Equalizer` sobre audio session 0 (mezcla global).** Adjuntar efectos de inserción (Equalizer, BassBoost, Virtualizer) a la sesión 0 está **deprecado desde hace ~15 años** (poco después de Gingerbread, 2011) y nunca se garantizó su funcionamiento. El método no se eliminó del SDK, por lo que *algunos* dispositivos aún lo aceptan, pero el comportamiento es inconsistente entre fabricantes: las capas de audio propietarias (Samsung, Xiaomi, etc.) pueden ignorarlo, pisarlo con sus propios efectos o romperlo en cualquier actualización. No es una base sobre la que construir un producto. Fuentes: [documentación oficial de Equalizer, que marca session 0 como deprecated](https://developer.android.com/reference/android/media/audiofx/Equalizer) (verif. 2026-07-17); [issue de Google confirmando la deprecación y su no-eliminación](https://issuetracker.google.com/issues/36936557) (verif. 2026-07-17); [análisis de Esper sobre por qué los ecualizadores Android no funcionan con todos los reproductores](https://www.esper.io/blog/android-equalizer-apps-inconsistent) (verif. 2026-07-17).

**`DynamicsProcessing` (API 28+).** Es la API moderna y potente (multi-banda, pre/post-EQ, MBC, limitador) — pero **se adjunta a un audio session ID concreto** de un `AudioTrack`/`MediaPlayer`. No existe modo "sistema". Para simular globalidad hay que escuchar los broadcasts `ACTION_OPEN_AUDIO_EFFECT_CONTROL_SESSION` que las apps reproductoras emiten *voluntariamente*: Spotify lo emite, **YouTube no**, y muchas apps tampoco. Fuentes: [referencia oficial de DynamicsProcessing](https://developer.android.com/reference/android/media/audiofx/DynamicsProcessing) (verif. 2026-07-17); [Esper, ibíd.](https://www.esper.io/blog/android-equalizer-apps-inconsistent) (verif. 2026-07-17).

**Qué hace realmente Wavelet (el estado del arte sin root).** Wavelet usa DynamicsProcessing y funciona en dos modos: (1) modo por defecto, que depende de que el reproductor difunda su session ID — por eso solo funciona con algunas apps; (2) "legacy mode" = sesión 0, que su propio autor documenta como "**puede no funcionar en todos los dispositivos**", con issues abiertos de roturas en Android 13. Su "enhanced session detection" amplía cobertura pero explícitamente **no funciona con YouTube**. Es decir: la mejor app de su categoría, con años de desarrollo, no consigue lo que la ficha de RealAudio da por hecho. Fuentes: [documentación de ajustes de Wavelet](https://pittvandewitt.github.io/Wavelet/Settings/) (verif. 2026-07-17); [issue #312: legacy mode roto en Android 13](https://github.com/Pittvandewitt/Wavelet/issues/312) (verif. 2026-07-17); [hilo XDA de Wavelet](https://xdaforums.com/t/app-9-0-wavelet-headphone-specific-equalization.4097957/) (verif. 2026-07-17).

**`AudioPlaybackCapture` (API 29+) no sirve como cadena de EQ.** Limitaciones estructurales: (a) solo captura audio con usage `MEDIA`/`GAME`/`UNKNOWN`; (b) cualquier app puede excluirse con `android:allowAudioPlaybackCapture="false"` y **las apps con DRM (Spotify, Netflix...) se excluyen — producen silencio**; (c) requiere el prompt de MediaProjection (grabación de pantalla) aceptado por el usuario en cada sesión; (d) y lo decisivo: capturar **no sustituye** el audio original — para "ecualizar" habría que silenciar la reproducción original y re-emitir la copia procesada, lo cual no es posible de forma transparente (no puedes silenciar selectivamente a la otra app) y añadiría una segunda ruta de audio con latencia. No es una arquitectura de EQ; es una API de grabación. Fuentes: [documentación oficial AV capture](https://developer.android.com/media/platform/av-capture) (verif. 2026-07-17); [Android Developers Blog, Capturing Audio in Android Q](https://android-developers.googleblog.com/2019/07/capturing-audio-in-android-q.html) (verif. 2026-07-17).

**AccessibilityService.** No otorga acceso al audio de otras apps ni a la mezcla del sistema. Su único uso histórico relacionado con audio (grabación de llamadas por la vía de accesibilidad) fue **prohibido explícitamente por Google Play desde mayo de 2022**. Fuentes: [XDA sobre la política de mayo 2022](https://www.xda-developers.com/google-kill-third-party-call-recording-apps-android/) (verif. 2026-07-17); [Android Police, ibíd.](https://www.androidpolice.com/google-ends-call-recording-apps-accessibility-services/) (verif. 2026-07-17).

**Conclusión A.1:** la Salida A tal como está escrita ("multimedia, llamadas o todo, a elección del usuario") **no es implementable como producto fiable en Android sin root**. Lo máximo defendible es lo que hace Wavelet: EQ sobre las sesiones que se dejan, con huecos enormes (YouTube, DRM, llamadas) y dependencia del fabricante.

### A.2 — Audio de llamadas: imposible para terceros

- **Telefonía clásica:** el stream de voz discurre por el DSP/módem fuera del alcance de las apps. Google eliminó la API oficial de grabación de llamadas en Android 6, restringió más en Android 9 y desde Android 10 el acceso real al stream de llamada sin root está bloqueado; solo el **dialer por defecto preinstalado** tiene acceso. Insertar un EQ en esa cadena es un subconjunto del mismo problema: vetado. Fuentes: [9to5Google sobre el bloqueo](https://9to5google.com/2022/04/21/google-will-block-all-third-party-call-recording-apps-on-play-store-from-may-11/) (verif. 2026-07-17); [issue de GrapheneOS documentando que sin ser dialer preinstalado no hay acceso al stream](https://github.com/GrapheneOS/os-issue-tracker/issues/3401) (verif. 2026-07-17).
- **VoIP (WhatsApp, Teams...):** cada app VoIP gestiona su propio audio con usage `VOICE_COMMUNICATION`, excluido de AudioPlaybackCapture y sin broadcast de session ID. Una app de terceros no puede interponerse.
- **"Aprovechar la cancelación activa de ruido del dispositivo":** no existe API estándar de Android que permita a una app de terceros controlar o modular el ANC de auriculares arbitrarios; el control ANC es propietario de cada fabricante (SDKs cerrados o apps propias). Esta línea de la ficha carece de vía de implementación general (afirmación basada en el estado de la plataforma a fecha de conocimiento, ene-2026; no existe tal API en la documentación pública de AudioManager/AudioDeviceInfo verificada 2026-07-17).

### A.3 — Fiabilidad del estímulo: sin calibración no hay dB HL

Un audiómetro emite niveles en **dB HL trazables** a un transductor calibrado (RETSPL por modelo de auricular, acoplador, verificación periódica). Un móvil con "el auricular que tenga el usuario" no controla: sensibilidad del transductor (variaciones >20 dB entre modelos), curva de respuesta, DAC/amplificador del teléfono, volumen absoluto (y con Bluetooth, absolute volume y códec añaden variabilidad), ni la colocación. El "umbral" resultante es un valor relativo sin unidad clínica.

Qué dice la evidencia publicada:

- La falta de calibración de generador+auricular es la limitación central identificada en la literatura; sin ella "no puede asegurarse la comparabilidad con pruebas auditivas establecidas". Fuente: [Scientific Reports 2024, evaluación de audiometría basada en apps](https://www.nature.com/articles/s41598-024-57944-9) (verif. 2026-07-17).
- La exactitud **depende del modelo concreto de auricular**: uHear solo fue válido para cribado (>25 dB HL) con los EarPods estándar de iPhone y en frecuencias concretas; los autores concluyen que los fabricantes deben **prescribir el modelo de auricular**. Fuente: [Am J Audiol 2018](https://pubs.asha.org/doi/10.1044/2018_AJA-17-0070) (verif. 2026-07-17).
- Incluso apps serias con auriculares controlados solo consiguen que ~83-84% de los umbrales caigan dentro de ±10 dB del audiómetro clínico. Fuente: [PubMed 30461416, audiometría smartphone de alta frecuencia](https://pubmed.ncbi.nlm.nih.gov/30461416/) (verif. 2026-07-17). hearTest logra ≤10 dB HL de diferencia media **solo con auriculares calibrados de perfil conocido**. Fuente: [Frontiers in Psychology 2020](https://www.frontiersin.org/journals/psychology/articles/10.3389/fpsyg.2020.00744/full) (verif. 2026-07-17).
- Cómo lo resuelven las apps serias: (a) **perfiles de calibración por modelo de auricular** (base de datos RETSPL-equivalente, como hearTest/uHear); (b) **calibración biológica** (normalización sobre oyentes normales); o (c) **cambiar de paradigma**: la OMS en hearWHO usa **dígitos-en-ruido (DIN)**, que mide una SNR relativa y **"no requiere material calibrado"** — precisamente porque el umbral absoluto sin calibración es indefendible. Fuentes: [Frontiers Public Health 2021, DIN antifásico](https://www.frontiersin.org/journals/public-health/articles/10.3389/fpubh.2021.725080/full) (verif. 2026-07-17); [De Sousa et al., Digital Health 2022, hearWHO global](https://journals.sagepub.com/doi/full/10.1177/20552076221113204) (verif. 2026-07-17).

**Margen de error residual con la arquitectura propuesta (auricular desconocido, sin perfil, posible BT):** no acotable; realistamente ±15-20 dB o peor, que es la diferencia entre "audición normal" e "hipoacusia moderada". El criterio test-retest de la ficha mide *repetibilidad*, no *validez*: un sistema sesgado 20 dB es perfectamente repetible. Como exaudiólogo, el proponente debería reconocer que esto no es un umbral: es una preferencia de volumen.

### A.4 — Gate de ruido ambiente por micrófono: solo válido como filtro grueso

Los micrófonos de móvil sin calibrar **no miden SPL absoluto de forma fiable**, y el fallo es máximo justo donde importa: las apps de sonómetro **sobreestiman los niveles bajos (<40-50 dBA)** incluso con micrófono calibrado, y sin calibración no se recomienda su uso para valores absolutos. Un cribado auditivo serio exige ambiente ≲35-40 dBA: exactamente el rango donde el micrófono del móvil no es creíble. Fuentes: [Thieme/AJA 2020, exactitud de sonómetros smartphone con y sin calibración](https://pubmed.ncbi.nlm.nih.gov/30398549/) (verif. 2026-07-17); [JASA 2016, evaluación NIOSH de apps de medición](https://pubs.aip.org/asa/jasa/article/140/4/EL327/922541/Evaluation-of-smartphone-sound-measurement) (verif. 2026-07-17).

Veredicto parcial: el gate es implementable como **heurística de rechazo** ("hay demasiado ruido, no hagas el test ahora"), no como **verificación de condiciones audiométricas**. Venderlo como lo segundo sería una afirmación falsa.

### A.5 — Alternativas de arquitectura defendibles

| Opción | Factibilidad técnica | Comentario |
|---|---|---|
| (a) EQ solo dentro de app propia (reproductor propio) | **Alta** | `DynamicsProcessing`/`Equalizer` sobre el `audioSessionId` propio, o DSP propio con Oboe. 100% soportado. Coste: el usuario solo se beneficia dentro de tu app — propuesta de valor mínima frente a Poweramp/Wavelet. |
| (b) Perfil exportable (PEQ) a apps/hardware que lo soporten | **Alta** | Exportar parámetros paramétricos (formato AutoEq/PEQ) importables en Wavelet, Poweramp, auriculares con DSP (Qudelix, etc.). Sin fricción de plataforma; la personalización viaja con el perfil. |
| (c) LE Audio / HAP / preset control / Auracast | **Prematura** | Android 15/16 añade Auracast y aplicación de presets de audífonos a streams, pero está limitado a dispositivos concretos (Samsung One UI 7, Pixel 9+) y la gestión de presets vive en Ajustes del sistema, no como API madura de terceros. Ecosistema 2026: incipiente. Fuentes: [Google blog, Auracast en audífonos](https://blog.google/feed/auracast-hearing-aids-earbuds/) (verif. 2026-07-17); [TechCrunch 2025-03-13](https://techcrunch.com/2025/03/13/android-is-adding-auracast-support-which-allows-hearing-aids-to-connect-to-public-audio-broadcasts/) (verif. 2026-07-17). |
| (d) "Personalización de audio" sin claims clínicos | **Alta y es la única compatible con B** | Test de *preferencia/perfil sonoro* (idealmente DIN o comparativo, no umbral absoluto), resultados en escala propia sin dB HL, EQ dentro de app propia o exportable. Es exactamente el movimiento que hizo Mimi (ver B.6). |

---

## B) Frontera regulatoria (UE / España)

### B.6 — MDR 2017/745: la Salida B, tal como está escrita, es un producto sanitario

**Cualificación.** El art. 2(1) MDR define producto sanitario por su **finalidad prevista**, incluyendo "diagnóstico, prevención, seguimiento, predicción o pronóstico" de una enfermedad o deficiencia. MDCG 2019-11 (rev. 1, junio 2025) confirma que lo determinante es el propósito declarado y la función real, no la tecnología. Un software que **"estima pérdida auditiva"** (deficiencia) y **"recomienda derivación a valoración clínica si se estima pérdida"** (información para una decisión con propósito diagnóstico) cumple la definición de MDSW sin ambigüedad. Fuentes: [MDCG 2019-11, texto oficial](https://health.ec.europa.eu/system/files/2020-09/md_mdcg_2019_11_guidance_en_0.pdf) (verif. 2026-07-17); [Emergo sobre la rev. 1 de junio 2025](https://www.emergobyul.com/news/european-revision-primary-software-guidance-mdcg-2019-11-revision-1-small-changes-meaningful) (verif. 2026-07-17); [análisis de cualificación wellness vs. médico](https://www.ncbi.nlm.nih.gov/pmc/articles/PMC7381013/) (verif. 2026-07-17).

**Clasificación.** Regla 11, Anexo VIII: software que proporciona información utilizada para tomar decisiones con fines diagnósticos o terapéuticos es **clase IIa como mínimo** (IIb/III si las consecuencias son graves). La regla 11 "conduce casi inevitablemente a clase IIa como mínimo, requiriendo organismo notificado". Fuentes: [Johner Institute sobre regla 11](https://blog.johner-institute.com/regulatory-affairs/mdr-rule-11/) (verif. 2026-07-17); [Decomplix, MDSW bajo MDR](https://decomplix.com/medical-software-mdr/) (verif. 2026-07-17).

**Qué implica clase IIa para un individuo:** sistema de gestión de calidad ISO 13485, evaluación clínica (Anexo XIV), documentación técnica completa, persona responsable del cumplimiento (art. 15), registro EUDAMED/SRN, vigilancia poscomercialización, y auditoría de **organismo notificado** con coste total estimado **€32.000–€110.000** y plazos de **12-18 meses como mínimo** (habitualmente ~2 años por saturación de organismos notificados). Fuentes: [MedDeviceGuide, desglose de costes CE 2026](https://meddeviceguide.com/blog/ce-marking-cost-medical-devices-guide) (verif. 2026-07-17); [Posos, CE para software médico](https://www.posos.co/blog-articles/ce-marking-for-medical-softwares-a-comprehensive-guide) (verif. 2026-07-17). Para un desarrollador individual con horas sueltas: **inviable de facto**. En España el interlocutor sería la AEMPS como autoridad competente; nada de esto lo abarata.

**El precedente demoledor: Mimi.** El Mimi Hearing Test estaba certificado CE como clase I bajo la antigua MDD; bajo MDR esa vía de autodeclaración murió (regla 11 → IIa). Resultado: **desde mayo de 2024 Mimi dejó de ser producto sanitario certificado** y reposicionó su test bajo el estándar de consumo ANSI/CTA-2118 ("Hearing Wellness Reporting"), abandonando además la app Android. Si una empresa dedicada, financiada y con años de ventaja eligió salir del perímetro MDR, la probabilidad de que un individuo lo cruce con éxito es nula. Fuentes: [Mimi Health Update](https://mimi.io/mimi-health) (verif. 2026-07-17); [FAQ de Mimi](https://mimi.health/faq) (verif. 2026-07-17).

**Matiz de uso personal:** el MDR regula la *introducción en el mercado / puesta en servicio*. Una app que Julius compile para su propio uso no se comercializa y queda fuera. **Publicarla en Play Store — aunque sea gratis — es comercializarla** (la gratuidad no exime; lo relevante es la puesta a disposición en el mercado de la Unión, criterio recogido en MDCG 2019-11 y la Guía Azul; verif. sobre el texto de MDCG 2019-11, 2026-07-17).

**La línea operativa, con precisión (qué puede decir/hacer la app sin cruzar):**

CRUZA al MDR (cualquiera de estas):
- Expresar resultados como **umbrales en dB HL** o como **audiograma**.
- Usar los términos "pérdida auditiva", "hipoacusia", "grado leve/moderado/severo", "cribado", "detecta", "estima tu pérdida".
- **Recomendación de derivación clínica condicionada al resultado del test** (es la app tomando una decisión de triaje diagnóstico — el corazón de la regla 11).
- Emitir un "informe" con apariencia clínica pensado para entregar a un profesional.
- Presentar la EQ como **compensación de una pérdida auditiva** o "imitando un audífono": los audífonos son productos sanitarios clase IIa, y reclamar su función es reclamar finalidad terapéutica (compárese: la función de audífono de los AirPods Pro requirió autorización De Novo de la FDA en septiembre de 2024; en la UE equivaldría a producto sanitario — conocimiento a fecha de corte ene-2026).

NO cruza (formulación defendible):
- "Perfil de sonido personal" / "así prefieres oír": resultados en **escala relativa propia**, nunca dB HL.
- Test de comparación/preferencia (o DIN presentado como "reto de audición en ruido" con resultado SNR relativo **sin mapeo a categorías clínicas**).
- EQ presentada como **mejora de la experiencia de escucha** ("más claridad", "a tu gusto"), jamás como compensación de deficiencia.
- Mensaje sanitario **genérico e incondicionado** (mostrado siempre, no disparado por el resultado): "Esta app no es un producto sanitario. Si tienes cualquier preocupación sobre tu audición, consulta a un profesional".
- Advertencia: la línea la define la **función real y la presentación global** (nombre, tienda, capturas, onboarding), no un disclaimer pegado al final. Un disclaimer no descualifica una app cuya función es estimar hipoacusia (MDCG 2019-11: la cualificación depende de la finalidad prevista deducible de todos los materiales; verif. 2026-07-17). El propio nombre "RealAudio" + narrativa de audiólogo detectando pérdidas ya construye finalidad prevista médica.

### B.7 — RGPD: los umbrales auditivos son datos de salud (art. 9)

Un umbral auditivo (o cualquier resultado que "revele información sobre el estado de salud", art. 4(15) RGPD) es **categoría especial** del art. 9: tratamiento prohibido salvo excepción, en la práctica **consentimiento explícito** (art. 9(2)(a)) además de una base del art. 6 — doble test. Fuentes: [texto del art. 9](https://gdpr-info.eu/art-9-gdpr/) (verif. 2026-07-17); [guía de consentimiento para datos de salud en apps](https://www.themomentum.ai/blog/gdpr-consent-requirements-health-data) (verif. 2026-07-17).

- **App de uso estrictamente personal:** exención doméstica (art. 2(2)(c)); sin obligaciones.
- **App publicada:** el desarrollador es responsable del tratamiento si los datos salen del dispositivo (backend, analytics, backups propios). Mitigación fuerte y recomendable: **procesamiento y almacenamiento 100% on-device, cero telemetría sobre resultados**, lo que reduce el tratamiento por parte del desarrollador a prácticamente nada — pero exige disciplina (ningún SDK de analytics tocando resultados, ojo con Crashlytics y con backups en la nube). Si hubiera tratamiento a gran escala de datos art. 9, se activaría la obligación de DPIA (art. 35). Nótese la interacción con B.6: si la app se reformula como "perfil de preferencia sonora" sin semántica clínica, el argumento de que el dato no "revela estado de salud" se refuerza; si guarda "estimación de pérdida auditiva", es dato de salud sin discusión.

### B.8 — Google Play: política de salud endurecida (2025-2026)

- Desde el **28 de agosto de 2025** las apps de salud deben completar el **Health apps declaration form** en Play Console; enero 2026 añadió requisitos técnicos y de transparencia adicionales. Fuentes: [política Health Content and Services de Play](https://support.google.com/googleplay/android-developer/answer/16679511?hl=en) (verif. 2026-07-17); [resumen de los requisitos 2025/2026](https://myappmonitor.com/blog/google-play-health-apps-update-2026-requirements) (verif. 2026-07-17).
- Apps con funcionalidad médica **sin autorización regulatoria** deben incluir el disclaimer estándar ("this app is not a medical device and does not diagnose, treat, or prevent any condition") **en el primer párrafo de la descripción**, y recordar la consulta a profesionales; las que se declaren producto sanitario deben **aportar prueba de certificación a requerimiento**. Fuentes: [ídem, política oficial](https://support.google.com/googleplay/android-developer/answer/16679511?hl=en) (verif. 2026-07-17); [anuncio de política 2025-03-05 sobre funcionalidades médicas y disclaimers](https://support.google.com/googleplay/android-developer/answer/15931464?hl=en) (verif. 2026-07-17).
- **Trampa operativa:** una ficha de Play que diga "estima tu pérdida auditiva y te deriva al especialista" con el disclaimer "no diagnostica ninguna condición" es autocontradictoria: Google puede rechazarla por claim de salud engañoso, y en la UE el disclaimer no la saca del MDR (B.6). Las dos salidas coherentes son: certificarse (inviable) o no hacer el claim.

---

## Síntesis de no conformidades

| # | Elemento de la ficha | Estado |
|---|---|---|
| 1 | EQ global "multimedia, llamadas o todo" | Infactible sin root; llamadas: imposible; global: API deprecada 2011, no garantizada |
| 2 | "Aprovechar cancelación activa de ruido" | Sin API pública universal; propietario por fabricante |
| 3 | Umbral auditivo con auricular desconocido | Sin validez en dB HL; error no acotable (±15-20 dB realista); test-retest mide repetibilidad, no validez |
| 4 | Gate de ruido como verificación audiométrica | Micrófonos no fiables <40-50 dBA sin calibrar; solo vale como filtro grueso |
| 5 | "Estima pérdida + recomienda derivación" publicado | MDSW clase IIa mín. (regla 11) → organismo notificado, €32k-110k, 12-24 meses: inviable individual |
| 6 | "Imitando un audífono básico" | Claim de finalidad terapéutica (función de audífono = clase IIa); agrava el punto 5 |
| 7 | Almacenar umbrales en app publicada | Dato de salud art. 9 RGPD: consentimiento explícito o arquitectura 100% on-device |
| 8 | Publicación en Play con esos claims | Declaración de salud obligatoria + disclaimer contradictorio con la propuesta; riesgo de rechazo |

Vía de reformulación existente (constatada, no validada por este juez): app de **personalización de sonido** — test de preferencia/DIN en escala relativa, EQ dentro de reproductor propio y/o perfil PEQ exportable, mensaje sanitario genérico incondicionado, cero vocabulario clínico, datos on-device. Eso es otra idea distinta de la que figura en la ficha, y compite frontalmente con Wavelet (gratis) y con las funciones nativas de Samsung/Apple.

---

## Veredicto T2

**NO APTO** (frente técnico-regulatorio, sobre la idea tal como está formulada en la ficha).

Motivación en dos pilares independientes, cada uno suficiente por sí solo:
1. **Técnico:** la Salida A (EQ global incluyendo llamadas, "imitando un audífono") no es implementable de forma fiable en Android sin root; el componente de llamadas es imposible para una app de terceros, y el umbral sin transductor calibrado carece de validez clínica.
2. **Regulatorio:** la Salida B ("estima pérdida" + "deriva a valoración clínica"), publicada en Play Store, cualifica como software producto sanitario clase IIa mínimo bajo MDR 2017/745 / MDCG 2019-11 regla 11, cuya certificación es inviable para un desarrollador individual — como demuestra la retirada de la certificación CE de Mimi (mayo 2024).

La única versión que sobreviviría a este frente (personalización de audio en app propia, sin claims clínicos, sin dB HL, sin derivación condicionada, datos on-device) es una idea materialmente distinta de RealAudio y debería re-someterse al tribunal como tal.

---

# Dictamen T3 — Frente APRENDIZAJE — RealAudio

**Juez:** T3 (Aprendizaje / Pivote / Empleabilidad)
**Fecha:** 2026-07-17
**Posición de partida:** NO CONFORMIDAD. La idea debe ganarse cada punto. No existe repo: a día de hoy esto es una ficha, no un proyecto. Todo lo que sigue evalúa potencial de aprendizaje, no mérito acumulado (que es cero).

---

## 1. Qué aprende Julius REALMENTE (y qué no)

### 1.1 Lo que sí es territorio nuevo y denso

- **DSP/audio digital en Android.** Generación de estímulos (tonos puros / banda estrecha con rampas de subida/bajada para evitar clics espectrales), `AudioTrack` en modo estático/streaming, latencia, sample rates, y filtros IIR/biquad para la EQ. Nada de esto está en su Android previo (Kotlin/Compose/Room era CRUD con UI). Esto es matemática aplicada a buffers, no pantallas. Densidad de aprendizaje alta **solo si lo escribe él**: Android trae `DynamicsProcessing` (API 28+) con EQ multibanda ya hecha. Si tira de la API de sistema para todo, el "aprendizaje DSP" se reduce a leer documentación. La versión con valor es: biquads a mano para la EQ o, como mínimo, generación de estímulos a mano y entender por qué una rampa de 20 ms importa.
- **Psicoacústica → código.** Este es el punto diferencial y el único que ningún otro proyecto de su cartera toca. Él sabe hacer una audiometría con un paciente delante. Traducir Hughson-Westlake (o un staircase adaptativo), criterios de parada, manejo de falsos positivos del paciente y concordancia test-retest a un autómata de estados en software es *exactamente* la traducción clínica→código que el pivote necesita. Nadie sin sus 10 años puede diseñar bien esa máquina de estados. Un dev genérico copia un paper; él sabe dónde el paper miente en la práctica.
- **Pensamiento metrológico.** Aquí está la trampa y a la vez el oro. Sin auriculares calibrados, **no puede medir dB HL. Punto.** Un móvil con auriculares desconocidos produce niveles con ±10-20 dB de variabilidad entre dispositivos. Si Julius ignora esto y presenta "tu audiograma", habrá aprendido a construir un instrumento inválido — aprendizaje negativo. Si en cambio **documenta la incertidumbre**, trabaja en dB relativos, valida contra un audiómetro real (puede auto-testearse: ventaja que casi nadie tiene), y escribe el análisis de error, habrá adquirido pensamiento metrológico real. La diferencia entre ambos caminos es la diferencia entre un juguete y una pieza de portfolio seria. El gate de ruido ambiente por micrófono tiene el mismo problema (mic sin calibrar) y la misma oportunidad.
- **Frontera regulatoria MDR.** Un software que mide audición, recomienda derivación clínica Y compensa la pérdida con EQ está pisando la definición de *software as a medical device*. Las apps comerciales equivalentes (Jacoti, Mimi, Signia) van con marcado CE. Julius no va a certificar nada — pero **saber exactamente dónde está la línea, y documentar por qué su versión se queda del lado wellness/cribado no diagnóstico**, es conocimiento profesional que en una entrevista healthtech europea vale más que el código. Condición: que esa decisión exista por escrito, no en su cabeza.

### 1.2 Lo que NO aprende (que nadie le venda humo)

- Android/Kotlin per se: ya lo tiene. Cero aprendizaje nuevo en Compose, Room, arquitectura de app.
- Backend, cloud, distribución, .NET: nada. Este proyecto no refuerza su empleo actual en absoluto. Es 100 % apuesta de pivote — lo cual es coherente con su criterio declarado, pero hay que decirlo: si el pivote no cuaja, el ROI laboral inmediato de estas horas es ~0.

---

## 2. Valor para el pivote: la historia en la entrevista

Es la única idea de su cartera donde audiología y código se intersectan de forma directa. La logopedia es adyacente; esto es el centro de la diana.

**Qué historia cuenta ante Demant/WSA/Sonova/GN/Starkey/Jacoti/Mimi o una healthtech española:**

> "Implementé un protocolo audiométrico adaptativo con criterio de concordancia test-retest, analicé el error de calibración de la cadena de reproducción móvil y documenté por qué el producto se mantiene fuera del alcance MDR como herramienta de cribado."

Esa frase, sostenida con un repo, coloca a Julius en una categoría de candidato distinta. Trabajó en retail de Demant (Aural): conoce el negocio desde dentro, y este proyecto demuestra que ha cruzado al otro lado.

**Qué partes valoran esas empresas (en orden):**
1. El algoritmo del test y sus criterios de parada/concordancia — es donde su juicio clínico es visible en el código.
2. El tratamiento de la incertidumbre y la calibración — separa ingeniería de juguetería.
3. La decisión regulatoria documentada — demuestra madurez de producto sanitario.
4. La EQ "tipo audífono" — la que MENOS. Una EQ de 4-6 bandas no imita un audífono (no hay compresión WDRC, no hay prescripción NAL/DSL real, no hay salida calibrada). Que la mantenga como demo honesta ("simulación ilustrativa"), nunca como claim.

**Advertencia adversarial:** las vacantes de esas empresas están mayoritariamente en Dinamarca/Alemania/Bélgica y son escasas. El proyecto mejora la probabilidad, no la garantiza. La historia solo funciona si el núcleo está hecho a mano (ver §4) y si puede defender cada decisión en pizarra.

---

## 3. Empleabilidad: "audiólogo que programa" vs .NET genérico

- **.NET genérico legacy:** perfil commodity. Compite con miles de CVs idénticos; su década de audiología es ruido en ese mercado.
- **Audiólogo + código demostrado:** perfil raro. El mercado europeo de audio-salud (fabricantes de audífonos, apps de hearing screening, OTC hearing aids tras la ola regulatoria americana, teleaudiología) busca exactamente gente que hable ambos idiomas y casi no existe oferta de candidatos. Su dominio clínico deja de ser ruido y pasa a ser el diferenciador.
- Matiz duro: un proyecto de portfolio no sustituye experiencia profesional en el sector. Lo que hace es **convertir su pasado clínico en credencial técnica activa** — que es lo único que un proyecto personal puede lograr, y este es el único de su cola que lo logra.

---

## 4. Riesgo de vaciado por IA

Si Julius genera el núcleo con IA, el proyecto queda hueco: en la entrevista no sabrá defender por qué el staircase baja 10 y sube 5, y se nota en dos preguntas.

**Obligatorio a mano (aquí vive su ventaja clínica y el aprendizaje):**
- La máquina de estados del protocolo: staircase, criterios de parada, gestión de falsos positivos, criterio de concordancia test-retest, decisión de repetición.
- Generación de estímulos y cadena de audio: síntesis del tono/banda estrecha, rampas, ruteo, niveles.
- Análisis de error y calibración: el documento y el código que cuantifican qué NO puede afirmar la app.
- La decisión regulatoria escrita.

**Delegable a IA sin pérdida:**
- UI Compose, navegación, persistencia Room, generación del informe PDF, scaffolding, tests de fontanería.

Regla operativa: si un fichero contiene conocimiento que solo un audiólogo tendría, lo escribe él. Si lo escribiría igual un junior de bootcamp, delega.

---

## 5. Riesgo inverso: ¿demasiado grande para primera incursión?

La ficha describe **tres productos**: (a) motor de test, (b) EQ en tiempo real sobre el audio del sistema, (c) informe con derivación. Con "horas sueltas", eso es una receta de abandono al 60 %. Además (b) tiene un problema técnico serio: interceptar y ecualizar el audio global del móvil en Android es limitado/frágil (efectos por sesión de audio, restricciones de `audioSession 0` según versión/fabricante) — puede comerse semanas de frustración con bajo aprendizaje transferible.

Frente a la logopedia: esta es claramente la de tamaño más contenible y la única con alineamiento directo. La logopedia es mayor, más difusa clínicamente para él (no es su especialidad estricta) y debe esperar.

**Cuantificación:**
- Alineamiento con el pivote: **~90-95 %** (máximo posible en su cartera; solo pierde puntos por no tocar el stack de su empleo actual).
- Densidad de aprendizaje nuevo/hora: **~70-80 %** en la fase de motor de test hecho a mano; cae a **~30-40 %** si delega el DSP en APIs/IA; la fase EQ-de-sistema baja a **~40 %** (mucha hora perdida en peculiaridades de fabricantes). Comparativa: seguir haciendo .NET legacy en horas libres ≈ 5-10 %.
- Conclusión de tamaño: **es el tamaño justo SOLO si se fasea.** Como monolito de tres piezas, es demasiado para una primera incursión con horas sueltas.

---

## Veredicto T3

**APTO CON CONDICIONES** (exclusivamente en el frente APRENDIZAJE):

1. **Fasear obligatoriamente.** Fase 1 = solo motor de test (estímulos + protocolo adaptativo + test-retest + gate de ruido) con criterio de "terminado" escrito antes de empezar. La EQ y el informe no existen hasta cerrar Fase 1. La EQ se replantea como demo sobre audio propio de la app (no audio del sistema) salvo justificación técnica escrita.
2. **Núcleo a mano.** Protocolo, generación de estímulos y análisis de error escritos por Julius sin generación IA del algoritmo. IA solo para UI, persistencia, PDF y scaffolding.
3. **Cuaderno de calibración/incertidumbre.** Documento en el repo que cuantifique qué no puede medir la app (nada de dB HL sin calibración), con validación cruzada contra un audiómetro real usando su propio audiograma.
4. **Decisión regulatoria documentada** (1-2 páginas): por qué la app se mantiene como cribado no diagnóstico fuera del alcance MDR; lenguaje del informe sin pretensión diagnóstica; no publicar en tienda sin revisar ese análisis.
5. **Kill criterion:** si en 6 semanas de calendario no hay un staircase funcional presentando tonos por oído, parar y reevaluar en tribunal.
6. **La logopedia queda congelada** hasta el cierre de Fase 1.

Incumplir 1, 2 o 3 convierte el proyecto en un juguete con EQ y anula su valor de pivote: en ese caso, NO APTO.

---

# Dictamen T4 — ALCANCE / REALISMO — RealAudio

**Juez:** T4 (Alcance/Realismo) · **Fecha:** 2026-07-17 · **Posición de partida:** no conformidad por defecto.
**Perfil del proponente:** dev C#/.NET a jornada completa; una app Kotlin/Compose/Room terminada; **cero experiencia en DSP/audio digital**; exaudiólogo (el dominio clínico no cuenta como capacidad de ingeniería de audio). Disponibilidad real: sesiones de ~2h, 2-4 sesiones/semana **repartidas entre 7 ideas**.

---

## 0. Hallazgo estructural previo: la parte B de la ficha está parcialmente muerta

Antes de estimar nada, verificación de capacidades de Android (búsquedas del 2026-07-17):

1. **EQ global del sistema (sesión de audio 0):** deprecada por Google desde hace ~14 años. Sigue funcionando *a veces*, en *algunos* dispositivos, según ROM/OEM, y el framework le da prioridad a los efectos por sesión sobre los globales. Las rutas "Hi-Res", USB directo y offload la esquivan por completo. No es una API sobre la que se pueda construir un producto: es una ruleta por fabricante. ([Esper: por qué los EQ de Android no funcionan con todos los reproductores](https://www.esper.io/blog/android-equalizer-apps-inconsistent), [issue tracker de Google](https://issuetracker.google.com/issues/36936557))
2. **EQ por sesión de otras apps (broadcast `AUDIO_SESSION`):** depende de que cada reproductor emita el broadcast voluntariamente. Muchos no lo hacen. Desde Android 8 además exige servicio en primer plano permanente. ([equalizer-issue-tracker](https://github.com/pinpong/equalizer-issue-tracker/blob/master/EQUALIZER_BROADCAST.md))
3. **EQ en llamadas de voz:** **técnicamente imposible para apps de terceros** desde Android 10: el flujo de audio remoto de la llamada está bloqueado a nivel de SO, y Google Play prohibió además la vía Accessibility. No hay escenario "posible" que estimar aquí. ([Android Police](https://www.androidpolice.com/google-ends-call-recording-apps-accessibility-services/), [9to5Google](https://9to5google.com/2022/04/21/google-will-block-all-third-party-call-recording-apps-on-play-store-from-may-11/))
4. **"Aprovechar el ANC del dispositivo":** no existe API pública genérica para que una app de terceros controle o module el ANC de auriculares arbitrarios; eso vive en SDKs propietarios de cada fabricante. Es una frase de ficha, no una capacidad.
5. **EQ dentro de la propia app (su propio `AudioTrack`/sesión con `DynamicsProcessing`, API 28+):** esto sí es API soportada y estable. ([DynamicsProcessing, Android Developers](https://developer.android.com/reference/android/media/audiofx/DynamicsProcessing))

**Consecuencia para el alcance:** de las cuatro variantes de la ficha ("multimedia, llamadas o todo el sistema, a elección" + ANC), solo sobrevive con fiabilidad **el audio que la propia app reproduce**. "Llamadas" y "ANC" salen del alcance por imposibilidad, no por recorte. "Todo el sistema" queda como apuesta degradada que funcionará en una fracción no predecible del parque de dispositivos.

---

## 1. Estimación por bloques (sesiones de ~2h, horquilla mín–máx)

Las horquillas ya incluyen el **impuesto de aprendizaje DSP** (+30-50% sobre lo que tardaría alguien con experiencia en audio): Julius nunca ha generado un tono calibrado, nunca ha peleado con latencia/rutas de audio Android, nunca ha mapeado dB FS → dB HL.

| Bloque | Contenido honesto | Mín | Máx | Notas de realismo |
|---|---|---|---|---|
| (a) Investigación viabilidad Android | Spike: qué se puede en EQ global/por sesión/propia; leer, prototipar throwaway, probar en su móvil. Sesiones enteras sin código productivo. | 3 | 6 | Este dictamen ya adelanta la respuesta; aun así necesita verificarlo en SU dispositivo. **Timebox obligatorio.** |
| (b) Estímulos calibrables + cadena de audio del test | Warble tones por banda, rampas de nivel, control fino de atenuación, mapeo dB FS→nivel percibido, referencia por auricular. La palabra "calibrable" es donde muere la inocencia: sin auricular de referencia no hay dB HL, solo umbrales relativos. | 6 | 12 | El bloque más traicionero para alguien sin DSP. La calibración absoluta es imposible con auriculares de consumo variados; aceptar umbral relativo cuesta menos, pretender calibración cuesta el doble y no se consigue. |
| (c) Protocolo test-retest + concordancia + UX guiada | Secuencia RIGHT/LEFT, pausas, descenso, pulsación, repetición, criterio de concordancia, reintentos, estados de error, onboarding. | 5 | 9 | El dominio clínico lo abarata (sabe QUÉ protocolo), pero la máquina de estados + UX no se abarata. |
| (d) Gate de ruido ambiente | Permiso mic, RMS/estimación de nivel, umbral go/no-go, UI. | 2 | 4 | Trampa: el micrófono del móvil tampoco está calibrado; solo puede dar un gate aproximado. Si intenta "dB SPL reales", el bloque se triplica. |
| (e1) Motor EQ **dentro de la propia app** | `DynamicsProcessing` multibanda sobre su propio reproductor, perfiles desde el resultado del test, A/B on/off. | 4 | 8 | Viable y estable. Es el único "audífono" honesto de la v1. |
| (e2) EQ **global sistema** (solo escenario B) | Sesión 0 + broadcasts + servicio foreground + matriz de pruebas por dispositivo. | +6 | +12 | Alto riesgo de acabar en descarte tras quemar las sesiones. Ver escenarios. |
| (f) Informe + derivación | Estimación de pérdida por banda, redacción prudente, criterio de derivación, export/compartir. | 2 | 4 | Su experiencia clínica abarata el contenido; el pulido visual es sumidero clásico (cap: 1 sesión de pulido). |
| (g) Validación con sujetos reales | Él mismo + familia: sesiones de prueba, observación, iteración del protocolo y de la UX. | 4 | 8 | El coste en sesiones es lo de menos: coordinar familia son **semanas de calendario** por ronda. Mínimo 2 rondas. |
| (h) Decisión regulatoria y claims | Qué puede afirmar sin ser producto sanitario (MDR/UE): "screening orientativo / bienestar", nunca "diagnóstico" ni "audífono". Documentar disclaimers, revisar política de apps médicas de Play. | 2 | 4 | No es opcional: un exaudiólogo que publica una app que "imita un audífono" y "estima pérdida" está a dos frases de un producto sanitario clase IIa sin marcado CE. La palabra "audífono" no puede aparecer en la app ni en la ficha de Play. |

---

## 2. Los dos escenarios

### Escenario A — EQ solo en la propia app (el único fiable)

Bloques: a + b + c + d + e1 + f + g + h.

| | Mín | Máx |
|---|---|---|
| **Sesiones (~2h)** | **28** | **55** |
| **Horas** | ~56 h | ~110 h |

Alcance resultante: test de 4 bandas con test-retest, gate de ruido, informe con derivación, y EQ aplicada **al reproductor interno de la app** (el usuario escucha su música/archivos ahí con su perfil). Es un producto coherente y publicable como app de bienestar.

### Escenario B — Intentar además EQ global del sistema

Bloques: escenario A + e2 (+ el sobrecoste de fragmentación en la validación).

| | Mín | Máx |
|---|---|---|
| **Sesiones (~2h)** | **36** | **70** |
| **Horas** | ~72 h | ~140 h |

Y con la letra pequeña que la ficha no dice: de esas 8–15 sesiones extra, hay **probabilidad alta de que la mayoría acaben en "no funciona en X dispositivo/auricular" y se descarte el bloque igualmente**, porque la API está deprecada y es OEM-dependiente. El escenario B no compra funcionalidad garantizada; compra un billete de lotería con el tiempo más escaso que tiene Julius. Las llamadas **no tienen escenario**: 0 sesiones porque es imposible, y cualquier sesión gastada ahí es pérdida pura.

---

## 3. Confrontación con la disponibilidad real (calendario)

Disponibilidad declarada: 2–4 sesiones/semana **entre 7 ideas** → cuota efectiva para RealAudio de **~0,3–0,6 sesiones/semana** si reparte uniforme.

| Régimen | Escenario A (28–55 ses.) | Escenario B (36–70 ses.) |
|---|---|---|
| Reparto entre 7 ideas (0,3–0,6 ses./sem) | **≈ 11 meses – 3,5 años** | **≈ 14 meses – 4,5 años** |
| RealAudio como idea prioritaria (2 ses./sem) | ≈ 3,5 – 7 meses | ≈ 4,5 – 8 meses |
| RealAudio en exclusiva (3–4 ses./sem) | ≈ 2 – 4,5 meses | ≈ 2,5 – 6 meses |

Lectura sin anestesia: **con el reparto actual entre 7 ideas, esta app no existe**. Ni la versión recortada. Un proyecto de audio con impuesto DSP a razón de una sesión cada 2-3 semanas pierde el contexto entre sesión y sesión (re-arranque mental de 20-30 min sobre 120: ~20% de impuesto adicional que las horquillas de arriba ni siquiera incluyen). RealAudio solo es defendible como una de las 1–2 ideas priorizadas, y aun así hablamos de un semestre para el escenario A.

---

## 4. Sumideros ocultos (los que no están en la ficha)

- **Fragmentación OEM en audio:** cada fabricante rompe algo (rutas de audio, efectos preinstalados de Dolby/DTS que colisionan con los suyos, offload). Afecta incluso al escenario A en menor medida (latencias, resampling). Presupuestado parcialmente en (b) y (g); en escenario B es el sumidero dominante.
- **Auriculares sin calibrar = matriz de pruebas infinita:** cada auricular tiene su curva de respuesta. La tentación de "compensar por modelo de auricular" es un proyecto entero (AutoEq existe por algo). Recorte obligatorio: umbral **relativo** con el auricular del propio usuario, disclaimer explícito, y punto.
- **La seducción del "ya que estoy":** 6 bandas en vez de 4, ANC, perfiles múltiples, exportar audiograma bonito. Cada uno parece 1 sesión y son 3. El criterio del test-retest ya es suficiente sofisticación clínica para una v1.
- **Coordinar humanos:** cada ronda de validación con familia son 2–4 semanas de calendario aunque solo consuma 2 sesiones de trabajo. Con dos rondas, +1–2 meses de calendario que no aparecen en ninguna tabla de horas.
- **Pulido del informe:** el informe es donde el exaudiólogo va a querer brillar. Cap duro: el informe de v1 es texto + una gráfica simple.
- **Regulatorio como veto tardío:** si descubre en el mes 5 que no puede decir "imita un audífono", habrá construido marketing y UX sobre una premisa prohibida. El bloque (h) va **al principio**, no al final.

---

## 5. Recorte: MVP que valida lo esencial

**MVP propuesto (y única versión que este frente considera estimable con honestidad):**
1. Test de **4 bandas fijas** por oído, warble, descendente, con **una** repetición y criterio de concordancia simple. Umbrales **relativos** (sin pretensión de dB HL).
2. Gate de ruido ambiente **aproximado** (go/no-go, sin dB SPL reales).
3. **EQ de 4 bandas aplicada solo al reproductor interno de la app** (`DynamicsProcessing` sobre su propia sesión), con A/B on/off para que el usuario *sienta* la diferencia.
4. Informe breve: perfil relativo + recomendación de derivación, lenguaje de bienestar, disclaimers definidos en la sesión regulatoria inicial.

**Coste del MVP:** ~**24–42 sesiones** (48–84 h) — el escenario A menos los máximos de calibración y validación extendida. En régimen prioritario (2 ses./sem): **3–5 meses**.

**Se aparca a v2 (o a nunca):** 6 bandas, EQ global del sistema (re-evaluar solo si el MVP demuestra tracción), cualquier mención a llamadas (imposible; eliminar de la ficha, no aparcar), ANC (sin API; eliminar), compensación por modelo de auricular, audiograma exportable pulido.

**Qué valida el MVP:** la hipótesis nuclear de la idea — "un test de screening autoguiado bien hecho + una EQ personalizada audible generan valor percibido" — se valida entera con el MVP. El EQ global no valida nada nuevo: solo amplía la superficie donde ese valor se aplica.

---

## Veredicto T4

**APTO CON CONDICIONES** — exclusivamente en el frente de alcance/realismo, y solo bajo TODAS estas condiciones:

1. **Reescritura obligatoria de la ficha:** eliminar (no aparcar) "llamadas" y "aprovechar ANC" — la primera es técnicamente imposible para terceros desde Android 10, la segunda no tiene API pública. Una ficha que promete imposibles no es estimable.
2. **EQ global del sistema fuera de v1:** queda como spike timeboxeado de máximo 2 sesiones dentro del bloque (a), solo para confirmar en su dispositivo lo que la evidencia ya indica. Cualquier sesión adicional en sesión-0 antes de tener el MVP funcionando es no conformidad.
3. **Priorización explícita:** RealAudio debe recibir ≥2 sesiones/semana sostenidas. Con la cuota actual de reparto entre 7 ideas (~0,5 ses./sem) el proyecto tarda 1–3,5 años y el veredicto pasa automáticamente a **NO APTO** por inviabilidad de calendario.
4. **Bloque regulatorio (h) al inicio, no al final:** definición de claims permitidos ("screening orientativo", nunca "diagnóstico" ni "audífono") antes de escribir UX o textos. La frase "imitando un audífono básico" no puede sobrevivir en ningún material del producto.
5. **Umbrales relativos, no calibración absoluta:** aceptado por escrito antes del bloque (b). Si el objetivo muta a "dB HL reales con auriculares de consumo", el bloque (b) deja de tener techo y el veredicto pasa a NO APTO.
6. **Compromiso con el MVP definido en §5** (24–42 sesiones, 3–5 meses en régimen prioritario) como alcance total de v1.

---
*Fuentes de la verificación técnica: [Esper — Android equalizer apps inconsistent](https://www.esper.io/blog/android-equalizer-apps-inconsistent) · [Google Issue Tracker — Equalizer session 0](https://issuetracker.google.com/issues/36936557) · [pinpong/equalizer-issue-tracker](https://github.com/pinpong/equalizer-issue-tracker/blob/master/EQUALIZER_BROADCAST.md) · [DynamicsProcessing — Android Developers](https://developer.android.com/reference/android/media/audiofx/DynamicsProcessing) · [Android Police — fin de las apps de grabación de llamadas](https://www.androidpolice.com/google-ends-call-recording-apps-accessibility-services/) · [9to5Google — bloqueo de call recording en Play](https://9to5google.com/2022/04/21/google-will-block-all-third-party-call-recording-apps-on-play-store-from-may-11/)*
