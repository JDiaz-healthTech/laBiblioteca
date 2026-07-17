# Tribunal Fase 1 — ScoringNews (repo Prism)

> Cuatro dictámenes independientes emitidos en contextos aislados, SIN acceso a la crítica previa de 2026-07-16. Fecha: 2026-07-17.

---

# Dictamen T1 — MERCADO — ScoringNews (repo Prism)

> [!warning] Posición de partida
> Juez T1 (frente MERCADO). Evaluación desde cero, contexto aislado, no conformidad por defecto. Fecha del dictamen: **2026-07-17**. Todas las fuentes verificadas por búsqueda web en esa fecha.

---

## 1. Estado del mercado de credibilidad/calidad de noticias (2026)

### 1.1 Quién sigue en pie y de qué vive

| Actor | Modelo | Estado verificado (2026-07-17) |
|---|---|---|
| **Ground News** | B2C suscripción. Tres niveles: Pro (~9,99 $/año), Premium (~29,99 $/año), Vantage (~99,99 $/año). | Vivo. El líder B2C del nicho. Ojo: **no vende "credibilidad", vende comparación de sesgo** (izquierda/centro/derecha, "blindspots"). Su producto es meta-cobertura, no un score de veracidad por artículo. |
| **NewsGuard** | B2B (licencias a anunciantes, plataformas, empresas de IA) + nuevo chatbot a 6 $/mes (jun-2026). | Vivo pero tocado. Investigación de la FTC cerrada en abr-2026 tras acuerdo con agencias de publicidad para **no usar colusoriamente ratings como NewsGuard** en compra de anuncios. Acusado públicamente de sesgo contra medios conservadores. Es el caso de estudio del riesgo reputacional del nicho. |
| **AllSides** | Híbrido: membresías, formación, publicidad; pivotando a B2B (">90% de ingresos de clientes", estilo Bloomberg). | Vivo, **no rentable a 2025**, financiándose por crowdfunding (Wefunder/RegCF) en 2026. Más de una década operando y aún sin rentabilidad. |
| **Otherweb** | "Nutrition labels" por IA sobre artículos. ~7,26 M$ levantados (incl. ronda de 1,7 M$ oct-2024). | Vivo, pero financiándose también vía **Wefunder (crowdfunding minorista)** — señal de que el capital riesgo institucional no acompaña. Es el competidor que hace *exactamente* lo que propone Prism, con años de ventaja y modelos propios. |
| **Media Bias/Fact Check** | Donaciones + publicidad. | Vivo como proyecto artesanal, no como negocio escalable. |
| **Particle** | Agregador IA con resúmenes multi-fuente. 10,9 M$ Serie A (Lightspeed + Axel Springer). Android mundial en feb-2026. | Vivo y creciendo. Su gancho no es "score de credibilidad" sino resumen + contraste de fuentes. |

### 1.2 Cementerio y contracción (verificado 2026-07-17)

- **Artifact** (fundadores de Instagram, con todo el capital y talento imaginables): cerrado en 2024; la tecnología se la quedó Yahoo. Si ellos no encontraron negocio en "noticias con IA para consumidor", la vara está clarísima.
- **Logically Facts** (Irlanda): cesó publicación en 2025 tras perder ingresos de Meta y TikTok.
- **Meta** terminó su programa de fact-checking en EE. UU. a principios de 2025; el **Washington Post** abandonó su columna Fact Checker tras ~20 años.
- Censo Duke/Poynter (jun-2026): en 2025 nacieron 10 proyectos de fact-checking y **más de 30 dejaron de publicar**; ~75% de los fact-checkers encuestados por la IFCN se declaran financieramente vulnerables o en crisis.
- Los agregadores nativos absorben la función: Google desplegó en 2026 insignias **"Highly Cited"** y **"Preferred Sources"** dentro de Search/AI Overviews. La señal de credibilidad se está convirtiendo en *feature gratuita de plataforma*, no en producto.

**Conclusión del panorama:** el nicho existe pero está en contracción del lado "veracidad/credibilidad" y solo respira del lado "comparación de sesgo" (Ground) o "datos B2B" (NewsGuard, AllSides pivotando). Nadie está construyendo un negocio B2C sano sobre "un score de credibilidad por artículo".

---

## 2. ¿Paga alguien por scoring de credibilidad?

- Reuters Institute Digital News Report 2026 (jun-2026): solo el **17%** paga por noticias online (estancado), y la confianza en las noticias está en **37%, mínimo histórico** desde 2015. El consumidor que ya no paga ni por las noticias no va a pagar por un metadato sobre las noticias.
- Los que cobran, cobran por otra cosa: Ground News cobra por *comparación de cobertura*; NewsGuard cobra a *empresas* (y ahora prueba un chatbot a 6 $/mes cuyo gancho es "respuestas de fuentes fiables", no un score); AllSides pivota a B2B porque el B2C no le dio rentabilidad en más de diez años.
- **El scoring de credibilidad puro es una feature, no un producto.** Nadie ha demostrado disposición a pagar por él de forma aislada. Los muertos del nicho (Artifact, Logically Facts, 30+ proyectos de fact-checking en 2025) lo confirman.

---

## 3. Problemas de mercado específicos de Prism

### 3.1 Acceso al contenido (el problema estructural, y va a peor)

- **APIs de noticias con licencia comercial** (verificado 2026-07-17): NewsAPI.org exige ~449 $/mes para uso comercial (el tier gratuito es solo desarrollo/localhost); GNews desde ~84 $/mes; alternativas baratas entre 11 y 40 $/mes (Mediastack, NewsData.io) con límites serios de volumen/histórico. Cualquier modelo de negocio carga con este coste fijo antes del primer usuario.
- **El scraping está muriendo**: Cloudflare bloquea por defecto crawlers de IA "de uso mixto" en páginas con publicidad a partir del **15-sep-2026**, y empuja "Pay Per Crawl"/"Pay Per Use" (TechCrunch, 2026-07-01). El 52% del tráfico de crawl de junio-2026 ya era IA y los publishers están cerrando la puerta. Un producto que necesita leer el texto completo de artículos ajenos para puntuarlos nace contra la corriente regulatoria y técnica de 2026, con exposición legal (paywalls, ToS, copyright) incluida.

### 3.2 Coste LLM por artículo vs. disposición a pagar

- Precios API Claude (verificado 2026-07-17): Haiku 4.5 a 1 $/5 $ por Mtok; Sonnet 5 a 3 $/15 $ (intro 2/10 hasta ago-2026). Un análisis de artículo (~2.000-4.000 tokens entrada + ~500 salida) cuesta del orden de **0,005-0,02 $ por artículo** con Haiku/Sonnet; con batch y caching, menos.
- Para uso personal: trivial (decenas de artículos/día ≈ céntimos). **El coste LLM no es el cuello de botella; el acceso al contenido y la demanda sí.** Para escala consumidor: 100 artículos/día × 10.000 usuarios ya son miles de $/mes de inferencia + licencia de contenido, contra un usuario que estadísticamente no paga (17%).

### 3.3 El problema reputacional: "un algoritmo me dice qué es creíble"

- NewsGuard —con periodistas humanos, metodología publicada y años de trayectoria— acabó investigado por la FTC y señalado como árbitro sesgado; el cierre de la investigación (abr-2026) vino acompañado de un acuerdo para limitar el uso colusorio de sus ratings. Si eso le pasa al actor más serio del nicho, un score compuesto generado por LLM de un desarrollador individual no tiene ninguna defensa: los LLM tienen sesgos documentados, no son auditables por el usuario y la mitad del espectro político desconfiará del veredicto por defecto (confianza en noticias al 37%). El producto vende confianza y no puede fabricarla.

---

## 4. Como app personal (usuario = Julius)

Aquí el mercado deja de ser objeción: coste marginal ridículo, sin licencias (uso personal de feeds RSS), sin problema reputacional. Como banco de pruebas de .NET 8 + Postgres + LLM + informes, el ejercicio es coherente con el esqueleto que Julius quiere para healthtech.

**Pero la ficha no es honesta en un punto:** "potencialmente público general" es humo. No hay ningún camino verosímil de la app personal al público general que no choque con todo lo anterior (contenido, coste fijo de APIs, competidores financiados haciendo lo mismo, demanda de pago inexistente, riesgo reputacional). Esa coletilla debe eliminarse de la ficha: mantenerla contamina decisiones de diseño (multi-tenant, auth, escalado) que consumen las "horas sueltas" sin devolver aprendizaje relevante para el pivote healthtech. Nota adicional de coherencia: el estado real del repo (2 commits de ago-2025, entidades vacías, stubs) indica que ni siquiera la versión personal ha superado la fase de esqueleto en 11 meses; cualquier discurso de mercado sobre esta base es ciencia ficción.

---

## 5. Monetización

**Descarte explícito.** No hay hipótesis de monetización defendible:
- B2C suscripción: compite contra Ground News (desde ~9,99 $/año) y contra features gratuitas de Google; el usuario no paga por noticias (17%), menos por meta-noticias.
- B2B datos/ratings: exige credibilidad institucional, metodología auditable y equipo; es el terreno de NewsGuard/AllSides, y ni AllSides es rentable.
- Publicidad: requiere volúmenes de audiencia inalcanzables para un side-project de horas sueltas.
- API de scoring para terceros: los terceros con esa necesidad (plataformas, empresas de IA) compran a NewsGuard o lo hacen in-house.

---

## Fuentes (verificadas 2026-07-17)

- Ground News — [Suscripción Vantage](https://ground.news/subscribe) · [Comparativa Pro/Premium/Vantage](https://factually.co/product-reviews/electronics-tech/ground-news-premium-vs-pro-vantage-feature-price-comparison-9dd5ab) · [Ground News Pricing](https://inspiretothrive.com/ground-news-pricing/)
- NewsGuard — [CNN Business, chatbot 6 $/mes (2026-06-22)](https://www.cnn.com/2026/06/22/media/newsguard-ai-chatbot-news-atlantic-publisher) · [Washington Times, cierre investigación FTC (2026-04-17)](https://www.washingtontimes.com/news/2026/apr/17/federal-trade-commission-shuts-investigation-newsguard/)
- AllSides — [Wefunder/RegCF](https://wefunder.com/allsides/) · [Perfil AIN](https://angelinvestorsnetwork.com/startups/allsides-regcf-crowdfunding-13k-media-bias-platform) · [Wikipedia](https://en.wikipedia.org/wiki/AllSides)
- Otherweb — [Wefunder](https://wefunder.com/otherweb) · [Axios, ronda 1,7 M$ (2024-10-17)](https://www.axios.com/pro/media-deals/2024/10/17/otherweb-news-filter-app) · [Crunchbase](https://www.crunchbase.com/organization/otherweb)
- Contracción fact-checking — [Poynter, censo Duke (2026)](https://www.poynter.org/fact-checking/2026/fact-checking-projects-survive-funding-cuts-duke-census/) · [Editor & Publisher (2026)](https://www.editorandpublisher.com/stories/2026-census-fact-checking-losses-continue-amid-funding-pressure-but-most-projects-persist,262121)
- Artifact/Particle — [TechCrunch, Artifact (2024-03-26)](https://techcrunch.com/2024/03/26/instagram-co-founders-ai-powered-news-app-artifact-may-not-be-shutting-down-after-all/) · [TechCrunch, Particle web (2025-05-06)](https://techcrunch.com/2025/05/06/particle-brings-its-ai-powered-news-reader-to-the-web/) · [Readless, agregadores IA 2026](https://www.readless.app/blog/best-ai-news-aggregators-2026)
- Google credibilidad nativa — [Blog de Google, Highly Cited / Preferred Sources](https://blog.google/products-and-platforms/products/search/original-high-quality-content-search/) · [Android Central (2026)](https://www.androidcentral.com/apps-software/google-is-giving-a-big-credibility-upgrade-to-ai-overviews-in-search)
- Acceso a contenido — [TechCrunch, Cloudflare pay-per-crawl/pay-per-use (2026-07-01)](https://techcrunch.com/2026/07/01/cloudflares-new-policy-pushes-ai-companies-to-pay-for-publishers-content/) · [The Register (2026-07-01)](https://www.theregister.com/ai-and-ml/2026/07/01/cloudflare-to-block-cynical-search-and-scrape-bots-from-ad-supported-web-pages/5264727) · [NewsAPI pricing](https://newsapi.org/pricing) · [NewsData.io pricing](https://newsdata.io/pricing) · [APITube, desglose precios 2026](https://apitube.io/blog/post/news-api-pricing-breakdown-2026)
- Demanda — [Reuters Institute Digital News Report 2026, resumen ejecutivo (2026-06)](https://reutersinstitute.politics.ox.ac.uk/digital-news-report/2026/dnr-executive-summary)
- Coste LLM — [Claude Platform Docs, pricing](https://platform.claude.com/docs/en/about-claude/pricing)

---

## Veredicto T1

**NO APTO** (frente MERCADO).

Razones nucleares:
1. **Demanda de pago inexistente** para scoring de credibilidad puro: el 17% que paga por noticias no paga por meta-noticias; los supervivientes del nicho venden otra cosa (comparación de sesgo, datos B2B) y aun así AllSides no es rentable y Otherweb/AllSides mendigan crowdfunding.
2. **Acceso al contenido estructuralmente hostil y encareciéndose** (APIs comerciales desde ~40-449 $/mes; Cloudflare bloqueando crawlers IA por defecto desde sep-2026): el insumo básico del producto tiene coste fijo y riesgo legal antes del primer usuario.
3. **Riesgo reputacional insalvable**: el precedente NewsGuard-FTC demuestra que "un algoritmo que dicta credibilidad" es un pararrayos de acusaciones de sesgo; un score LLM unipersonal no tiene defensa posible en un entorno con la confianza en noticias en mínimo histórico (37%).
4. **La ficha contiene humo**: "potencialmente público general" debe eliminarse. Como app personal y andamio de aprendizaje .NET 8/LLM/Postgres, el mercado no aplica y este tribunal no lo obstaculiza — pero eso no es un veredicto de mercado favorable, es la constatación de que no hay mercado que evaluar.

Este veredicto se limita al frente MERCADO; no juzga el valor del proyecto como vehículo de aprendizaje (fuera de mi competencia).

---

# Dictamen T2 — TÉCNICA — ScoringNews (repo Prism)

**Juez:** T2 (frente técnico, exclusivamente)
**Fecha:** 2026-07-17
**Posición de partida:** no conformidad por defecto. Todo lo afirmado abajo está respaldado por lectura directa del código (`git clone --depth 100 https://github.com/JDiaz-healthTech/Prism.git`) o por fuentes verificadas hoy.

---

## 1. Auditoría del repositorio: lo que hay de verdad

**Historial:** 2 commits, ambos del **2025-08-12** (`f4a51c0` "Estructura inicial", `851de43` "primer dia de trabajo concluido. Estructura basica hecha. Siguiente paso postgres"). **11 meses sin actividad.** El "siguiente paso postgres" del mensaje de commit nunca llegó a ejecutarse contra una BD real más allá de generar la migración.

### 1.1 Higiene del repo: deficiente

- **No hay `.gitignore`.** Están commiteados `.vs/` completo (índices de Copilot, `CodeChunks.db`, incluso **sesiones de chat de Copilot**: `.vs/Prism/copilot-chat/0052a775/sessions/...`), `bin/` y `obj/` de los 4 proyectos, y un `Domain/NewsAgent.Domain.csproj.Backup.tmp`.
- **`NewsAgent.Api/.env` está commiteado.** Contiene solo placeholders (`Newscatcher__ApiKey=PEGA_TU_APIKEY`) y credenciales locales de Postgres (`Password=postgres`), así que no hay fuga real de secretos, pero el patrón (`.env` versionado + `DotNetEnv`) es exactamente el que produce fugas cuando se pega la clave de verdad.
- No hay README, ni tests, ni CI, ni Dockerfile, ni `docker-compose` para el Postgres que la app exige.

### 1.2 Estructura: Clean Architecture de nombre, con el dominio en el sitio equivocado

`Prism.sln` define 4 proyectos con las dependencias correctas (Domain ← Application ← Infrastructure ← Api). Hasta ahí, bien. Pero:

- **Las entidades "oficiales" están vacías.** `Domain/Entities/Analysis.cs`, `AnalysisItem.cs` y `DomainReputation.cs` son clases `internal` sin un solo miembro.
- **Las entidades reales viven en el archivo del enum**: `Domain/Enum/Classification.cs` contiene `Analysis`, `AnalysisItem` y `DomainReputation` completas bajo el namespace `NewsAgent.Domain.Enum`. Todo el resto del código (`DbContext`, repositorio, endpoints) hace `using NewsAgent.Domain.Enum;` para importar *entidades*. Compila porque las stubs de `Entities` son `internal` y no colisionan desde otros ensamblados — es decir, compila por accidente.

### 1.3 Bugs de bloqueo en `NewsAgent.Api/Program.cs` (el pipeline no funciona)

Esto es lo determinante: **la API, tal como está, no expone la funcionalidad principal.**

1. **Endpoint de análisis muerto.** El final del archivo es:
   ```csharp
   app.Run();
   app.MapAnalyzeEndpoints();   // nunca se ejecuta: Run() bloquea
   builder.Services.AddHttpClient<INewsSearchProvider, NewscatcherProvider>(...) // registro tras Build(): lanzaría excepción
   ```
   El único endpoint vivo es `/health`. `/api/v1/analyze/url` no existe en tiempo de ejecución.
2. **`AnalyzeUrlHandler` no está registrado en DI.** Aunque se moviera el `MapAnalyzeEndpoints()` antes de `Run()`, el endpoint fallaría al resolver el handler.
3. **`/health` filtra la connection string de Postgres en la respuesta HTTP** (`Postgres = builder.Configuration.GetConnectionString("Postgres")`). Vulnerabilidad de manual si esto se despliega.
4. **Rate limiter configurado pero no aplicado**: se define la política `"fixed"` y se llama `app.UseRateLimiter()`, pero ningún endpoint hace `RequireRateLimiting("fixed")`.
5. **Registro duplicado y contradictorio del HttpClient de Newscatcher** (uno con nombre `"newscatcher"`, otro typed client tras `Run()`), y `NewscatcherProvider` se registra además como `AddScoped` suelto, con lo que el `HttpClient` inyectado no lleva las políticas Polly. Además `Polly.Extensions.Http` 3.0.0 está en modo legacy (lo actual en .NET 8+ es `Microsoft.Extensions.Http.Resilience`).

### 1.4 El núcleo de valor es 100% stub

- `Infrastructure/StubClaimExtractor.cs`: `ExtractFactsAsync` devuelve lista vacía. `StubComparerAgent.CompareAndScoreAsync` devuelve **`Score: 78` hardcodeado** con citas inventadas ("Fragmento relevante encontrado."). **No hay una sola línea de integración LLM en el repo**: ni SDK de Anthropic/OpenAI en los `.csproj`, ni cliente HTTP hacia ningún modelo, ni prompt.
- Bug latente en `Application/UseCases/AnalyzeUrl.cs`: `Summary1020s = string.Join(" • ", comp.Summary1020s)` donde `Summary1020s` es un `string` — `string.Join` sobre un string itera **caracteres**, produciendo `"H • e • c • h • o …"`.
- `AnalyzeUrlHandler` lanza 12 `FetchAsync` en paralelo con `Task.WhenAll` **sin manejo de errores**: un solo 403/timeout de cualquier medio tumba el análisis completo.
- Las ponderaciones del score compuesto existen solo como configuración (`Application/Options.cs`: `C=.40, K=.25, F=.15, S=.15, L=.05`; `appsettings.json` `Scoring:Weights`). No hay código que las consuma.

### 1.5 Lo que sí está decidido en el código (respuestas a "¿qué fuente? ¿qué LLM? ¿qué BD?")

| Decisión | Evidencia | Estado |
|---|---|---|
| Fuente de noticias: **Newscatcher v2** | `Infrastructure/Providers/NewsSearch/NewscatcherProvider.cs`, `BaseUrl = "https://api.newscatcherapi.com/v2"` | Implementado pero apunta a la **API v2, hoy obsoleta** (la oferta actual es v3) |
| Extracción de texto: **SmartReader (readability) + HtmlAgilityPack** | `Infrastructure/Providers/Fetchers/HtmlArticleFetcher.cs` | Funciona, pero descarga cada URL **dos veces** (SmartReader y luego `HtmlWeb.LoadFromWebAsync` para metadatos), sin User-Agent propio, sin robots.txt, sin caché |
| BD: **Postgres + EF Core (Npgsql)** | `Infrastructure/Persistence/NewsAgentDbContext.cs`, migración `20250812123625_InitialCreate` | Migración generada, modelo razonable (índices, FK, precisión en `Weight`) |
| LLM | — | **Sin decidir, sin código** |
| Mismatch de versiones | `.csproj`: TFM `net8.0` con paquetes EF Core/Extensions **9.0.x** | Funciona (EF 9 soporta net8.0) pero es una mezcla incoherente |

**Diseño conceptual subyacente (a favor del proponente):** las interfaces de `Application/Abstractions/Abstractions.cs` (`INewsSearchProvider`, `IArticleFetcher`, `IClaimExtractor`, `IComparerAgent`) describen **corroboración cruzada** — buscar artículos relacionados, clasificarlos confirm/contradict/context y componer un score con señales medibles (similaridad, frescura, peso de dominio) — no un "LLM, puntúa credibilidad" ingenuo. El diseño es más defendible que la ficha; el problema es que está implementado al 0%.

---

## 2. Ingesta de contenido: vías reales en 2026

Verificado hoy con búsqueda web:

- **Newscatcher (la decisión actual del repo):** free tier limitado (~21 llamadas/hora), planes desde **$50/mes (Starter, ~6.000 créditos)** y **$500/mes (Scale)**; la v2 que usa el código está descatalogada frente a v3. Fuentes: [pricing Newscatcher](https://www.newscatcherapi.com/pricing), [planes v3](https://www.newscatcherapi.com/docs/v3/documentation/get-started/news-api-v3-subscription-plans).
- **NewsAPI.org:** tier Developer gratuito pero **solo no comercial, con retraso de 24 h y 100 req/día**; el primer plan comercial es **$449/mes**. Fuentes: [newsapi.org/pricing](https://newsapi.org/pricing), [comparativa 2026](https://apitube.io/blog/post/news-api-pricing-breakdown-2026).
- **RSS + extracción readability (SmartReader, que ya está en el repo):** coste cero, sin API key, legalmente la vía menos conflictiva para *descubrimiento* (el feed lo publica el propio medio). La extracción del texto completo sigue siendo una descarga de la página (ver §5), pero para uso personal y sin republicar el texto es la opción de menor riesgo.
- **Scraping directo / bypass de paywalls:** anti-bot (Cloudflare, fingerprinting) convierte esto en una guerra de mantenimiento continuo, incompatible con "horas sueltas", y es la vía con mayor exposición legal (CFAA-equivalentes, condiciones de uso, art. 4 DSM con opt-out). **No defendible.**
- Alternativas gratuitas razonables para descubrimiento: **GDELT** (gratuito, metadatos y URLs) y los propios sitemaps/feeds de medios. Los antiguos atajos (Bing News Search API) fueron retirados en 2025.

**Conclusión del frente ingesta:** para un proyecto personal con horas sueltas, la única vía defendible es **RSS/feeds + SmartReader con caché y respeto de robots.txt**, con Newscatcher free tier como complemento opcional de búsqueda. La dependencia actual del código (Newscatcher v2 como *única* fuente de descubrimiento) es un callejón: o pagas $50–500/mes o el pipeline no arranca.

---

## 3. El scoring LLM

### 3.1 Fiabilidad

Pedir a un LLM "puntúa la credibilidad de este artículo 0–100" produce números **no calibrados** (el mismo artículo da scores distintos entre ejecuciones y modelos), con sesgos conocidos (favorece registro formal y medios famosos, penaliza opinión legítima) y sin trazabilidad. Como producto que muestra "credibilidad 78" sin descomposición, es indefendible técnicamente.

Lo que sí es defendible — y coincide con lo que las interfaces del repo ya esbozan — es un **score compuesto donde el LLM solo hace tareas verificables**:
- Extraer afirmaciones fácticas (`IClaimExtractor`) — tarea acotada, auditable.
- Clasificar pares (afirmación, artículo relacionado) en confirm/contradict/context con **cita textual obligatoria** (`Quote` ya existe en el modelo) — la cita permite verificar la alucinación.
- El score final se calcula **determinísticamente** con las señales: corroboración entre fuentes independientes, frescura, reputación de dominio (`DomainReputation` ya modelada), similaridad. Los pesos C/K/F/S/L de `Options.cs` van en esa línea.

Condición técnica irrenunciable: presentar siempre el desglose (qué fuentes confirman, qué contradicen, con citas), nunca solo el número.

### 3.2 Coste por análisis (precios verificados jul-2026)

Pipeline según el diseño del repo: 1 artículo principal + hasta 12 relacionados ≈ 25–35k tokens de entrada + 1–2k de salida por análisis.

- **Claude Haiku 4.5** ($1 in / $5 out por millón de tokens): **~$0,03–0,05 por análisis**. Con 10 análisis/día ≈ **$10–15/mes**.
- **Claude Sonnet** ($2/$10 introductorio hasta 31-08-2026, luego $3/$15): ~$0,07–0,12 por análisis. Fuente: [pricing Anthropic](https://platform.claude.com/docs/en/about-claude/pricing), [referencia 2026](https://benchlm.ai/blog/posts/claude-api-pricing).
- Batch API (−50%) y prompt caching reducen esto más si se procesa en lotes nocturnos, que es el patrón natural para un lector personal.

**El coste LLM no es el problema del proyecto.** Es un gasto de nivel "suscripción a un periódico". El riesgo está en la fiabilidad del juicio, no en la factura.

---

## 4. Stack .NET 8 + Postgres

- **.NET 8 muere el 10 de noviembre de 2026** — a menos de 4 meses de hoy. .NET 9 muere el mismo día. **.NET 10 es el LTS vigente (GA nov-2025, soporte hasta nov-2028).** Empezar hoy sobre net8.0 es empezar sobre un runtime con fecha de defunción inmediata. Fuentes: [.NET Blog: 8 y 9 EOL 10-nov-2026](https://devblogs.microsoft.com/dotnet/dotnet-8-9-end-of-support/), [política de soporte](https://dotnet.microsoft.com/en-us/platform/support/policy/dotnet-core).
- **Condición:** retarget a `net10.0` y alinear paquetes a 10.x (el repo ya mezcla net8.0 con EF Core 9.x — la incoherencia se resuelve de paso). Para el objetivo de aprendizaje de Julius (salir de .NET 3.5/WinForms), aprender sobre el LTS actual es estrictamente mejor.
- **Postgres + EF Core + Npgsql: idóneo.** Es el estándar de facto para este perfil de app, gratuito, y coherente con el pivote declarado hacia healthtech (Postgres es habitual en clínica). Sin objeción.
- **Minimal APIs + Clean Architecture en 4 proyectos:** para un pipeline personal de un solo caso de uso es sobre-arquitectura leve, pero como vehículo de aprendizaje es una elección razonable y ya está pagada.
- **¿Reparar o rehacer?** El esqueleto **se conserva en lo conceptual** (interfaces de `Application/Abstractions`, modelo de datos, migración) pero **`Program.cs` y la organización del Domain hay que rehacerlos**: mover entidades a `Domain/Entities`, eliminar stubs vacíos, reordenar el arranque (mapear endpoints antes de `Run()`, registrar el handler, quitar la connection string de `/health`), añadir `.gitignore` y purgar `bin/obj/.vs/.env` del historial. Es ~1–2 sesiones de trabajo, no una reescritura total: el valor rescatable es el diseño, no el código.

---

## 5. Riesgos regulatorios (frente técnico-legal del artefacto)

1. **Copyright / almacenamiento del texto.** El pipeline actual guarda `Quote` (fragmento) pero el diseño implica descargar y procesar el texto completo de 13 artículos por análisis. Para **uso personal sin republicación**, el riesgo práctico es bajo. Si se publica el servicio, almacenar/mostrar texto completo de terceros infringe; además en la UE existe el **derecho conexo de los editores de prensa (art. 15 DSM)**, que cubre incluso snippets no triviales. Mitigación técnica: almacenar solo URL, título, cita corta y señales derivadas; TTL de caché (ya previsto en `CacheTtlHours`).
2. **TDM en la UE.** El art. 4 de la Directiva 2019/790 permite minería de textos con fines comerciales **solo si el titular no ha hecho opt-out machine-readable** (robots.txt/TDM signals, hoy con peso reforzado: desde el **2 de agosto de 2026** el AI Act exige a proveedores GPAI políticas de copyright que respeten esas reservas). Un agregador personal no es un GPAI, pero la dirección regulatoria es clara: **el fetcher debe respetar robots.txt y señales TDM**, cosa que `HtmlArticleFetcher.cs` hoy no hace en absoluto. Fuentes: [Morrison Foerster: primera sentencia TDM (LAION, Alemania)](https://www.mofo.com/resources/insights/241004-to-scrape-or-not-to-scrape-first-court-decision), [CMS: excepciones TDM](https://cms.law/en/bel/legal-updates/ai-and-copyright-exploring-exceptions-for-text-and-data-mining), [AI Act y copyright](https://iapp.org/news/a/the-eu-ai-act-and-copyrights-compliance).
3. **Difamación / derecho al honor.** Publicar "El Medio X: credibilidad 32/100" generado por LLM es una afirmación de hecho sobre una persona jurídica. En España (art. 7.7 LO 1/1982, derecho al honor) y en general en la UE, un score erróneo y no fundamentado publicado es demandable; la defensa exige metodología documentada, señales verificables y lenguaje de opinión ("según estas N fuentes, no encontramos corroboración de..."). **Mientras el uso sea personal (Julius como único lector), este riesgo es nulo.** La condición es no publicar rankings de medios sin ese blindaje metodológico.

---

## Veredicto T2

**APTO CON CONDICIONES** (frente técnico exclusivamente; no me pronuncio sobre mercado, dedicación ni encaje con el pivote healthtech).

La vía técnica existe y es barata: RSS + readability + LLM barato en tareas acotadas + score compuesto determinista sobre .NET LTS + Postgres. Pero el artefacto actual **no la implementa**: es un esqueleto de 2 días, roto en su arranque, con el núcleo de valor al 0%. Condiciones vinculantes:

1. **Retarget a .NET 10 LTS** y alineación de paquetes 10.x. .NET 8 muere el 10-nov-2026; no se acepta empezar sobre él.
2. **Sanear el repo antes de escribir features:** `.gitignore`, purga de `.vs/`, `bin/`, `obj/`, `.env` y `*.Backup.tmp` del historial; README mínimo; `docker-compose` para Postgres.
3. **Reparar `Program.cs`:** `MapAnalyzeEndpoints()` antes de `Run()`, registrar `AnalyzeUrlHandler` en DI, eliminar el código muerto tras `Run()`, **quitar la connection string de `/health`**, unificar el registro del HttpClient (una sola vía, con `Microsoft.Extensions.Http.Resilience`).
4. **Reubicar el dominio:** entidades reales en `Domain/Entities`, eliminar las stubs `internal` vacías y el contrabando de clases en `Domain/Enum/Classification.cs`. Corregir el bug de `string.Join` sobre `Summary1020s` y envolver los fetch paralelos en manejo de errores por ítem.
5. **Ingesta: RSS/feeds como vía primaria** con respeto de robots.txt/señales TDM y caché; Newscatcher (v3, no v2) solo como complemento opcional dentro de su free tier. Prohibido el scraping anti-bot/paywall como dependencia del pipeline.
6. **Scoring: LLM solo en tareas verificables** (extracción de claims y clasificación con cita textual obligatoria); score final calculado determinísticamente con los pesos ya definidos; salida siempre con desglose de fuentes, nunca el número a secas. Presupuesto de referencia: Haiku 4.5, <$15/mes a 10 análisis/día.
7. **Ámbito de publicación restringido:** mientras no exista metodología documentada y almacenamiento limitado a URL+cita corta+señales, el sistema es de uso personal; no se publican scores de credibilidad atribuidos a medios concretos.
8. **Prueba de vida en 4 semanas:** un (1) análisis end-to-end real — URL → fetch → claims → corroboración → score persistido en Postgres — demostrable. Sin esa prueba, este dictamen decae a NO APTO: el historial (2 commits en 11 meses) es la principal evidencia en contra y solo se refuta con ejecución.

---

# Dictamen T3 — Frente APRENDIZAJE
**Idea:** ScoringNews (repo Prism) · **Fecha:** 2026-07-17 · **Juez:** T3 (Aprendizaje) · **Posición de partida:** no conformidad por defecto

---

## 0. Hecho previo que condiciona todo el dictamen

El repo Prism tiene **2 commits de agosto de 2025, entidades vacías y stubs**. Hoy es julio de 2026. Son **once meses de inactividad** sobre un esqueleto de plantilla. Antes de discutir qué se aprendería, hay que registrar qué se ha aprendido hasta ahora con esta idea: **nada**. Un esqueleto Clean Architecture generado y no rellenado no es aprendizaje; es la ilusión de haber empezado. Este dictamen evalúa el potencial, pero el potencial lleva un año caducando.

---

## 1. ¿Qué aprende Julius REALMENTE? Desglose por bloque

### 1.1 .NET moderno (8/10) — salto real: GRANDE, pero no exclusivo de esta idea
El salto .NET 3.5 → .NET 8 es de ~15 años de plataforma: `async/await`, DI nativa con generic host, minimal APIs, EF Core, nullable reference types, records, `IConfiguration`/`ILogger`, top-level statements, publicación self-contained. Para alguien que trabaja a diario en WinForms + VS2008, esto no es "ponerse al día": es aprender una plataforma distinta que comparte sintaxis. **Densidad de aprendizaje alta en las primeras 40–60 horas.**

Objeción de fondo: este aprendizaje lo da **cualquier** proyecto backend .NET 8 no trivial. No es mérito de ScoringNews; es mérito del stack. La idea solo lo justifica si el resto del proyecto no diluye esas horas (ver 1.5).

### 1.2 Postgres (vs SQL Server) — salto real: PEQUEÑO
EF Core abstrae el 90% de la diferencia. Julius ya piensa en relacional. Lo genuinamente nuevo (jsonb, índices GIN, `EXPLAIN ANALYZE`, migraciones con Npgsql) solo aparece si el proyecto lo fuerza, y un scoring de noticias apenas lo fuerza. **Aprendizaje marginal salvo diseño deliberado.** Valor real: poder escribir "Postgres" en el CV sin mentir, que en el mercado español tiene peso creciente frente a SQL Server-only.

### 1.3 Integración LLM seria en backend — salto real: GRANDE y diferencial (con matiz)
Prompting estructurado, salidas tipadas y validadas (JSON schema / structured outputs), gestión de costes por token, reintentos con backoff, idempotencia, colas para procesado asíncrono, evaluación de calidad del scoring. Esto **no lo tiene** (su experimento React+Claude fue frontend llamando a una API, que es otra cosa) y **es exactamente lo que la app de logopedia necesitará** para generar informes. Es el bloque de mayor valor del proyecto.

Matiz adversarial: ya hizo un experimento de scoring de noticias con Claude. Repetir el mismo dominio temático tiene rendimiento decreciente en la parte de producto; el rendimiento nuevo está solo en la ingeniería backend de esa integración. Si la IA le escribe esa ingeniería, el bloque entero se evapora.

### 1.4 Clean Architecture "de verdad" — riesgo: aprendizaje NEGATIVO tal como está planteado
El esqueleto actual es plantilla: capas antes que problema. Para un proyecto de una persona con horas sueltas, Clean Architecture de 4 proyectos es sobreingeniería que **retrasa el contacto con lo difícil** (dominio, LLM, datos) y produce la sensación de progreso sin progreso — exactamente lo que muestran los 2 commits. Aprender arquitectura es tomar decisiones de separación cuando duelen, no rellenar carpetas `Domain/Application/Infrastructure` vacías. Tal como está, este bloque resta.

### 1.5 Despliegue — solo cuenta si ocurre
Docker, un VPS o un PaaS, migraciones en despliegue, secretos, logs. Aprendizaje real y muy vendible, pero históricamente es lo primero que se cae de los proyectos personales. Sin despliegue, "ScoringNews" es un repo más; con despliegue es una línea de CV defendible en entrevista.

### 1.6 Lo que NO enseña y consumirá horas
Ingesta de feeds/RSS, scraping, deduplicación de artículos, heurísticas del score compuesto de credibilidad, UI de lectura de noticias. Nada de esto transfiere a la app de logopedia ni al pivote healthtech. Es **peso muerto de dominio**: horas de un presupuesto ya escaso invertidas en un problema (credibilidad de noticias) que Julius ni va a explotar ni le acerca a audiología.

---

## 2. La tesis del "esqueleto" para la app de logopedia — juicio crítico

**Lo que la tesis acierta:** el fontanería sí transfiere. Backend .NET 8 + Postgres + EF Core + pipeline LLM con salidas validadas + generación de informes es, efectivamente, el chasis de la app clínica. Y hay un argumento de gestión de riesgo legítimo: **equivocarse con noticias es gratis; equivocarse con datos de menores en contexto sanitario no.** Aprender async, migraciones y validación de salidas LLM sobre datos triviales antes de tocar datos de salud es una secuencia sensata.

**Lo que la tesis oculta (y es lo esencial):**
1. **El esqueleto no es la parte difícil de la app clínica.** Lo difícil será: modelado del dominio logopédico/audiológico (donde Julius tiene 10 años de ventaja que ScoringNews no ejercita en absoluto), RGPD con datos de categoría especial (art. 9), consentimiento, pseudonimización, trazabilidad/auditoría, y validación clínica de lo que un LLM escribe en un informe que leerá un especialista. **Nada de eso lo enseña ScoringNews.** El esqueleto cubre quizá el 40–50% técnico de la app clínica y el 0% de lo que la hará viable o inviable.
2. **Existe una vía más corta que la ficha no considera:** construir directamente la app de logopedia **con datos sintéticos/ficticios**. Misma fontanería (.NET 8 + Postgres + LLM + informes), riesgo cero de datos reales, y además ejercita el dominio clínico y el diseño de informes para especialistas — donde está su ventaja competitiva real. La única función que ScoringNews cumple y esa vía no es "proyecto sin carga emocional para calentar". Eso vale unas semanas, no un proyecto entero.
3. **Riesgo de esqueleto fantasma:** si Prism sigue al ritmo actual, la app de logopedia heredará un esqueleto vacío, no un esqueleto probado. Un chasis solo transfiere conocimiento si se ha conducido con él.

**Conclusión del frente:** la tesis del esqueleto es *parcialmente verdadera y estratégicamente cómoda*. Es la vía de menor riesgo, pero no la de menor coste: la vía de menor coste con riesgo igualmente bajo es la app clínica con datos sintéticos. ScoringNews solo se justifica como **laboratorio acotado y breve** del esqueleto, no como producto.

---

## 3. Empleabilidad (mercado español)

- **".NET 8 + Postgres + API REST + LLM en producción"** es de lo más eficiente que puede hacer para salir del pozo .NET 3.5. .NET sigue siendo de los stacks más demandados en España (banca, seguros, salud, consultoría), y la brecha 3.5 → 8 es exactamente lo que un entrevistador va a sondear. Un proyecto desplegado, con tests y CI, le da respuestas concretas ("usé DI nativa, EF Core con migraciones, structured outputs con reintentos") que ninguna certificación da.
- **La pieza LLM-backend es el diferenciador de 2026:** perfiles .NET que sepan integrar LLMs con validación y control de costes escasean; perfiles .NET a secas no.
- **Frente a sus alternativas:** más Android/Kotlin no mueve la aguja (ya lo tiene demostrado y no es su vía de pivote); su React pequeño tampoco. En términos de empleabilidad pura, este es su mejor eje de aprendizaje disponible. **Pero:** un repo con stubs de 2025 en el perfil de GitHub resta, no suma. Empleabilidad exige artefacto terminado y desplegado, o el efecto es contrario.

---

## 4. Riesgo de vaciado por IA

El esqueleto de plantilla ya es el primer síntoma: estructura generada, contenido cero. Si la IA rellena los stubs, Julius terminará con un proyecto ".NET 8" en el CV y sin poder explicar en entrevista por qué un `DbContext` es scoped o qué hace `ConfigureAwait`. Aprenderá a mirar, y el pozo .NET 3.5 seguirá intacto por dentro.

**A MANO obligatoriamente (es el temario):**
- Entidades de dominio y reglas del score compuesto (es SU lógica; si la escribe la IA, el proyecto no tiene autor).
- Toda la cadena LLM: prompts, esquemas de salida, validación, manejo de fallos/reintentos, control de coste. Es el bloque que transfiere a informes clínicos; delegarlo anula el proyecto.
- Configuración de DI, pipeline de la API y decisiones de arquitectura (incluida la decisión de **simplificar** la plantilla: menos capas escritas por él > más capas generadas).
- Migraciones EF Core: escribirlas, romperlas, revertirlas.
- Al menos un despliegue completo hecho paso a paso, no con script mágico.

**Delegable a IA sin pérdida:**
- DTOs y mapeos repetitivos, scaffolding de tests (no los asserts de dominio), Dockerfile base, YAML de CI, parsers de feeds RSS, frontend si lo hubiera, y explicaciones bajo demanda ("por qué esto es así en .NET 8") — IA como tutor, no como autor.

**Regla operativa:** IA explica y revisa; Julius escribe el núcleo. Si un commit del core no lo puede reescribir de memoria en pizarra, ese commit no le pertenece.

---

## 5. Cuantificación

| Métrica | Valor | Justificación |
|---|---|---|
| Alineamiento técnico con el esqueleto de la app clínica | ~60% | Fontanería transfiere; ingesta/scraping/score de noticias e informes de credibilidad, no |
| Alineamiento con el pivote healthtech (dominio + regulación + producto) | ~0% | Ni datos sanitarios, ni RGPD art. 9, ni dominio clínico, ni usuario especialista |
| **Alineamiento total con el pivote** | **~40–45%** | Media ponderada: el pivote es dominio+técnica, y esto solo aporta técnica parcial |
| Densidad de aprendizaje nuevo, horas 0–60 | Alta (~70–80% del tiempo es material nuevo) | .NET moderno + cadena LLM backend, ambos vírgenes para él |
| Densidad de aprendizaje nuevo, a partir de ~hora 60–80 | Baja (<25%) | Lo que queda es dominio-noticias y pulido de producto que no transfiere |
| Comparativa: app de logopedia con datos sintéticos | ~85–90% de alineamiento | Mismo esqueleto + dominio clínico + informes reales para especialista |
| Riesgo de vaciado por IA | Alto | Plantilla ya generada + horas sueltas + presión por "avanzar" = relleno automático |
| Evidencia de ejecución hasta la fecha | 2 commits / 11 meses | El mayor riesgo no es aprender mal: es no aprender |

Lectura: ScoringNews tiene una **ventana de alto rendimiento de unas 60–80 horas** (el esqueleto y la cadena LLM). Todo lo que exceda esa ventana es coste de oportunidad contra la app clínica.

---

## Veredicto T3

**APTO CON CONDICIONES** — exclusivamente en el frente de aprendizaje, y solo bajo TODAS las siguientes:

1. **Timebox duro: 80 horas o 3 meses naturales, lo que llegue antes.** ScoringNews se redefine como *laboratorio del esqueleto*, no como producto. Al vencer el plazo, se congela y las horas pasan a la app de logopedia con datos sintéticos, herede lo que herede.
2. **Recorte de alcance:** fuera scraping/ingesta sofisticada, deduplicación y UI de lectura. Alcance mínimo: API .NET 8 + Postgres con migraciones + pipeline LLM con salida estructurada y validada + un informe generado + desplegado en un entorno público. Nada más.
3. **Núcleo escrito a mano** (sección 4): dominio, cadena LLM completa, DI/pipeline, migraciones, despliegue. IA solo como tutor y para lo delegable listado. Condición verificable: poder explicar cada pieza del core sin mirar el código.
4. **Desmontar la plantilla:** reducir el esqueleto Clean Architecture a la arquitectura mínima que el problema pida, decidida y escrita por Julius. Rellenar la plantilla tal cual invalida el objetivo de aprendizaje.
5. **Prueba de vida en 14 días:** si en dos semanas desde la reactivación no hay commits con lógica de dominio real (no estructura), el expediente pasa a NO APTO por evidencia de ejecución, y la vía correcta es saltar directamente a la app clínica con datos sintéticos.

---

# Dictamen T4 — ALCANCE / REALISMO — ScoringNews (repo Prism)

**Juez:** T4 (Alcance/Realismo) · **Fecha:** 2026-07-17 · **Posición de partida:** no conformidad por defecto.
**Evidencia:** clonado `JDiaz-healthTech/Prism` y auditado archivo a archivo. Sin dictámenes previos.

---

## 1. Calibración del punto de partida real (auditoría del repo)

**Historia git completa: 2 commits, ambos del 2025-08-12.** "Estructura inicial" y "primer dia de trabajo concluido. Estructura basica hecha. Siguiente paso postgres". Es decir: **un (1) día de trabajo hace 11 meses**, y el "siguiente paso" anunciado nunca ocurrió. Velocidad empírica demostrada en este proyecto: **cero**.

### Lo que hay de verdad (~600-700 LOC de código fuente propio)

| Pieza | Estado real |
|---|---|
| Entidades de dominio (`Domain/Entities/*.cs`) | **Clases `internal` VACÍAS.** Las entidades "reales" están pegadas dentro de `Domain/Enum/Classification.cs`, en el namespace equivocado. Duplicación que hay que deshacer. |
| Interfaces (`Application/Abstractions`) | Firmas razonables pero basadas en **tuplas de 8 elementos** en vez de DTOs — habrá que refactorizar en cuanto se toque algo. |
| Caso de uso `AnalyzeUrl` | Escrito pero **nunca ejecutado**: contiene el bug `string.Join(" • ", comp.Summary1020s)` sobre un `string` (une carácter a carácter). Código sin probar. |
| Pipeline LLM | **No existe.** `StubClaimExtractor` devuelve lista vacía; `StubComparerAgent` devuelve un 78 hardcodeado con citas inventadas. Cero prompts, cero proveedor LLM, cero validación. |
| Score compuesto | **No existe.** Hay pesos C/K/F/S/L en `appsettings.json` sin ninguna línea de código que los lea ni los aplique. Configuración sin implementación: sensación de avance, no avance. |
| API (`Program.cs`) | **Rota por construcción:** `app.MapAnalyzeEndpoints()` está DESPUÉS de `app.Run()` (código muerto: el único endpoint de negocio jamás se registra), hay registros de DI duplicados también tras `Run()`, y `AnalyzeUrlHandler` nunca se registra en el contenedor. La API nunca ha funcionado end-to-end. Además `/health` devuelve la connection string de Postgres en la respuesta. |
| Ingesta | `NewscatcherProvider` contra **Newscatcher API v2: producto B2B de pago** (sin free tier real; cientos de $/mes). La única vía de ingesta implementada es económicamente inviable para un proyecto personal. `HtmlArticleFetcher` (SmartReader + HtmlAgilityPack) sí es aprovechable. |
| BD | Migración `InitialCreate` + `DbContext` con índices: **la única pieza genuinamente terminada.** |
| Higiene del repo | `.vs/`, `bin/`, `obj/`, cachés de Copilot y un `.env` **commiteados**. Sin `.gitignore` efectivo, sin tests, sin README, sin CI. |

**Conclusión de calibración:** el esqueleto es el output típico de una tarde de scaffolding asistido por IA, sin haber arrancado nunca la aplicación (los bugs de `Program.cs` lo prueban: nadie que ejecute eso deja el endpoint tras `Run()`). Aprovechable de verdad: migración/DbContext, fetcher, forma general de la solución — equivale a **2-4 sesiones de ahorro**, parcialmente anulado por **1-2 sesiones de limpieza y reparación** obligatorias. Avance neto real: ~1-2 sesiones sobre cero.

---

## 2. Estimación honesta por bloques (sesiones de ~2h)

Contexto: Julius viene de .NET 3.5; minimal APIs, DI moderno, EF Core, `IOptions`, Polly y consumo de LLMs son **aprendizaje, no ejecución**. Las horquillas lo incluyen.

| Bloque | Mín | Máx | Notas |
|---|---:|---:|---|
| Limpieza repo + reparar `Program.cs` + build verde + entidades en su sitio | 2 | 3 | Deuda heredada del "día 1". Obligatorio antes de nada. |
| Dominio real + definición cerrada del score (3-5 componentes, por escrito) | 1 | 3 | El máx asume disciplina; sin ella, es infinito (ver §4). |
| Ingesta: UNA vía (RSS de 1 fuente; descartar Newscatcher) | 2 | 4 | Sustituir el proveedor de pago por lector RSS + fetcher existente. |
| Pipeline LLM: prompt, salida estructurada, validación, reintentos, presupuesto tokens | 4 | 8 | El bloque gordo. Hoy hay CERO. Iteración de prompts consume sesiones enteras. |
| Score compuesto: cálculo real conectado a la salida del LLM | 2 | 4 | Los pesos en config no cuentan como nada. |
| API mínima funcional (wiring DI, endpoint, DTOs) | 1 | 2 | |
| Cliente mínimo para leer (HTML plano servido o consola) | 1 | 3 | Máx si cede a la tentación de frontend (ver §4). |
| Migraciones/BD: ajustes tras rediseño de entidades | 1 | 2 | |
| Despliegue (Railway/Fly/VPS ~5-10 €/mes + Postgres gestionado) | 2 | 4 | Primera vez desplegando .NET 8 + Postgres: no será 1 sesión. |
| Observabilidad mínima (Serilog + log de coste LLM por análisis) | 1 | 2 | |
| **TOTAL** | **17** | **35** | **34-70 horas** |

---

## 3. Confrontación con la disponibilidad real

- Disponibilidad total: 2-4 sesiones/semana **repartidas entre 7 ideas** → cuota realista para ScoringNews: **~0,3-0,6 sesiones/semana**.
- 17-35 sesiones a ese ritmo: **entre 7 y 27 meses de calendario.**
- Incluso con dedicación EXCLUSIVA (las 7 ideas paradas): 4-17 semanas, es decir, 1-4 meses solo para el MVP completo.
- **Evidencia empírica contra proyección:** este proyecto ya tuvo su oportunidad y produjo 1 día de trabajo seguido de 11 meses de silencio. La carga de la prueba de que "esta vez será distinto" recae en el proponente, y no hay nada en el repo que la sostenga.
- Coste de oportunidad: cada sesión aquí es una sesión que no va a las 2 ideas alineadas con el pivote healthtech. ScoringNews no aporta al pivote (el scoring de credibilidad de noticias generalistas no es healthtech por estar en una cuenta llamada healthTech).

---

## 4. Sumideros ocultos identificados

1. **El score es un rabbit hole sin fondo.** Ya hay 5 pesos (C/K/F/S/L) + reputación de dominio + frescura + similitud definidos en config sin una sola línea de cálculo. Es el patrón clásico: diseñar criterios es placentero e infinito; implementarlos y validarlos, no. Riesgo: 10+ sesiones "afinando" un score que nadie ha usado.
2. **Ingesta = objetivo móvil.** HTML de medios cambia sin avisar; SmartReader falla en sitios con paywall/JS. Cada fuente nueva es mantenimiento perpetuo. Newscatcher (la vía ya elegida) es de pago B2B: hay que tirarla.
3. **Coste recurrente LLM.** 10 artículos/día × análisis con contexto de artículos relacionados = miles de tokens/artículo. Asumible (~5-20 €/mes) SOLO si hay presupuesto de tokens y tope diario implementados desde el día 1; el diseño actual (12 artículos relacionados por análisis) multiplica ×13 el coste por consulta.
4. **Tentación de cliente bonito.** "Algún cliente para leer (por definir)" es la puerta a 10 sesiones de Blazor/React antes de que exista un solo análisis real. El backend hoy no produce nada que valga la pena mostrar.
5. **Gold plating preventivo "para la app clínica futura".** Clean Architecture de 4 proyectos, rate limiting, Polly, feature flags de Redis y caché por ventanas temporales... para una app que nunca ha arrancado. El repo YA exhibe este patrón. Es el sumidero más peligroso porque se disfraza de profesionalidad.
6. **Higiene pendiente que morderá:** `.env` y cachés de IDE en el historial git; `/health` filtrando la connection string.

---

## 5. Recorte: el MVP mínimo digno

Lo MÍNIMO que valida la idea ("¿un score LLM de credibilidad me resulta útil como lector?") no necesita API, ni Postgres, ni despliegue, ni cliente:

**Spike de validación (consola):**
- 1 fuente RSS fija (p. ej. portada de un medio) · 10 artículos/día ejecutado a mano.
- 1 llamada LLM por artículo con salida JSON validada.
- Score de **3 componentes** (p. ej. verificabilidad de afirmaciones, señales de lenguaje, consistencia interna) — congelado por escrito antes de codificar.
- Salida: un HTML plano estático (o texto en consola) con título, score y justificación.
- Persistencia: SQLite o un JSON por día. Postgres puede esperar.
- Presupuesto duro: tope de tokens/día en código.

**Coste del spike: 6-10 sesiones (12-20 h).** Con dedicación preferente (2 sesiones/semana a ESTA idea, aparcando otras): **3-5 semanas.** Con el reparto actual entre 7 ideas: 3-8 meses incluso para esto — lo cual es en sí el dato que condena el alcance propuesto.

Todo lo demás del pitch (API pública, Postgres, cliente, despliegue, "público general", reutilización clínica) es post-validación y hoy es humo.

---

## Veredicto T4

**NO APTO** — en su alcance actual (backend .NET 8 + Postgres + pipeline LLM + score compuesto + API + cliente + despliegue).

Fundamentos, exclusivamente en el frente alcance/realismo:
1. **Desajuste esfuerzo/disponibilidad de un orden de magnitud:** 17-35 sesiones de MVP contra una cuota real de ~0,3-0,6 sesiones/semana para esta idea → 7-27 meses de calendario.
2. **Velocidad empírica en este proyecto: cero.** Un día de trabajo (2 commits, 2025-08-12) y 11 meses de abandono; el propio "siguiente paso" anunciado en el commit nunca se dio.
3. **El esqueleto no es avance, es atrezzo:** aplicación que nunca ha arrancado (endpoint tras `app.Run()`, handler sin registrar en DI), entidades vacías duplicadas, score inexistente, LLM inexistente, y la única vía de ingesta implementada depende de una API B2B de pago.
4. **Perfil de sumideros máximo:** score infinitamente afinable + ingesta frágil + coste LLM recurrente + gold plating ya presente en el repo.

Condición única bajo la cual T4 reconsideraría (como propuesta NUEVA, no como esta): el **spike de consola de 6-10 sesiones** del §5, con score de 3 componentes congelado por escrito antes de la primera línea de código, tope de tokens/día implementado, y compromiso explícito de qué otras ideas se aparcan para liberar 2 sesiones/semana. Sin ese trueque de prioridades declarado, ni siquiera el spike es realista.
