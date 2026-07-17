# Tribunal Fase 1 — Anthropofilia

> Cuatro dictámenes independientes emitidos en contextos aislados (ninguno leyó a los demás). Fecha: 2026-07-17.

---

# Dictamen T1 — Frente MERCADO — Anthropofilia

- **Tribunal**: Validación adversarial de ideas de software — La Biblioteca
- **Juez**: T1 (Mercado)
- **Fecha del dictamen**: 2026-07-17
- **Posición de partida**: NO CONFORMIDAD POR DEFECTO. La idea es rechazable hasta que las evidencias demuestren lo contrario.
- **Objeto**: Anthropofilia — miniCMS a medida (PHP/JS/HTML/CSS) para una única usuaria real (la madre del proponente). Repo público: `JDiaz-healthTech/Anthropofilia` (creado 2025-08-10, último push 2026-07-04, 0 stars, 0 forks; verificado vía API de GitHub el 2026-07-17).

---

## 1. La pregunta incómoda: ¿tiene sentido un miniCMS a medida para un solo usuario en 2026?

Respuesta directa del frente mercado: **como decisión de mercado, no**. En 2026 el problema declarado ("una persona no técnica necesita gestionar contenido web sin desarrollador ni CMS pesado") es un problema **resuelto, comoditizado y en gran parte gratuito**. Cualquier argumento de necesidad funcional insatisfecha muere contra la tabla siguiente.

### Alternativas realistas para la usuaria HOY (precios verificados 2026-07-17)

| Alternativa | Coste | Apta para no técnicos | Notas |
|---|---|---|---|
| **WordPress.com Free** | 0 €/año | Sí (editor maduro, apps móviles, recuperación de contraseña, soporte) | Subdominio `.wordpress.com` + anuncios de la plataforma |
| **WordPress.com Personal** | ~4 $/mes facturado anual (~48 $/año); 9 $/mes mensual | Sí | Dominio gratis el primer año; desde abril 2026 permite plugins en todos los planes de pago (fuente: comparativas de precios 2026, ver Fuentes) |
| **Google Sites** | 0 € | Sí (drag & drop) | Subdominio `sites.google.com`; dominio propio conectable pagando solo el registro (~10-15 €/año) |
| **Publii** (CMS estático de escritorio, open source) | 0 € + hosting estático gratuito (GitHub Pages/Netlify) | Sí, con **setup inicial técnico** | UI tipo WordPress para no técnicos; sin servidor PHP que mantener; el hijo configura una vez y desaparece la superficie de ataque |
| **Kirby** (flat-file) | 115 $/sitio, pago único | No (orientado a desarrolladores) | Irrelevante para este caso de uso |
| **Wix Light** | 17 $/mes | Sí | Caro para el caso; plan gratuito con anuncios disponible |
| **Squarespace Basic** | ~19 $/mes | Sí | Caro para el caso; sin plan gratuito |

Conclusión funcional: existen al menos **tres opciones a coste cero** que cubren el problema declarado con mejor UX de edición, mejor recuperación ante errores y soporte que no depende de la disponibilidad de un familiar. El custom solo "gana" en: ausencia de anuncios, control total, ligereza estética, y el hecho contable de que **ya está parcialmente construido** (coste hundido).

## 2. Coste total de propiedad (TCO): el custom es la opción cara disfrazada de gratuita

### TCO Anthropofilia (custom PHP)

| Partida | Coste anual estimado |
|---|---|
| Hosting PHP compartido (Hostinger desde ~1,49-2,99 €/mes promo; IONOS desde 1 €/mes promo; **renovación realista 5-10 €/mes** — las promos de entrada suben al renovar, advertencia documentada en comparativas españolas 2026) | 36-120 €/año |
| Dominio .es/.com | 10-15 €/año |
| **Mantenimiento perpetuo por Julius**: parches de seguridad de un CMS a medida expuesto a Internet (login, formularios, subida de contenido = superficie de ataque), migraciones de versión PHP (PHP 8.1 ya EOL; 8.2 sale de soporte de seguridad en dic. 2026), roturas de dependencias JS, incidencias de la usuaria | 2-4 h/mes de forma realista a lo largo de años. A coste de oportunidad sombra de un desarrollador senior (30-50 €/h), **700-2.400 €/año en tiempo** — tiempo restado precisamente a La Biblioteca y al pivote healthtech |

### El punto que la ficha no nombra: Julius ES el vendor lock-in

La ficha critica implícitamente la dependencia de "un desarrollador o un CMS pesado", pero el custom **institucionaliza exactamente esa dependencia**: bus factor = 1, sin comunidad, sin documentación de terceros, sin mercado de profesionales que puedan heredarlo. Si Julius se cansa, cambia de prioridades (que es literalmente su plan estratégico: healthtech en .NET, no PHP), o simplemente no tiene un fin de semana libre, la madre queda con software huérfano. WordPress.com o Publii tienen un vendor con SLA o una comunidad; Anthropofilia tiene un hijo con jornada completa y un proyecto formativo en otro stack.

**Comparativa TCO a 3 años** (dinero, sin contar tiempo): custom ≈ 140-400 € vs. WordPress.com Free / Google Sites ≈ 0 € vs. Publii + dominio ≈ 30-45 €. Contando el tiempo sombra de mantenimiento, el custom es la alternativa más cara del cuadro **por un orden de magnitud**.

## 3. Monetización: descartada, y con razón

Se hace explícito lo que la ficha presume:

1. **Mercado saturado y en consolidación.** WordPress mantiene ~59,8 % del mercado CMS en 2026 (en declive por primera vez en 20 años, cediendo terreno a SaaS como Wix, Shopify y Squarespace — no a micro-CMS artesanales). No hay hueco visible que un miniCMS PHP genérico pueda ocupar.
2. **El nicho "CMS ligero" ya está servido.** Gratis y maduro (Publii, Grav) o de pago consolidado con años de comunidad (Kirby a 115 $/sitio, Statamic). Un producto nuevo aquí compite contra software gratuito mantenido por comunidades, con cero diferenciación declarada.
3. **Cero señales de demanda.** El repo lleva 11 meses público: 0 stars, 0 forks, 0 issues. No hay distribución, no hay marketing, no hay segundo usuario ni intención de tenerlo.
4. **Cero capacidad de servir un mercado.** Un CMS comercial exige soporte, seguridad continua, documentación y compatibilidad — imposible con horas sueltas y fines de semana ya comprometidos con otro objetivo estratégico.

**Probabilidad de ingreso: ≈ 0. Monetización: correctamente descartable y aquí queda descartada con argumentos.**

## 4. Matiz obligado: ¿esconde la ficha autoengaño mercantil?

**No, en lo esencial.** La ficha declara "utilidad personal real", niega el pivote healthtech y define el alcance como *finalizar*, no construir. Ese descarte del argumento mercado es honesto y este tribunal lo consigna a favor del proponente. El razonamiento económico correcto no es "¿construir o comprar?" (esa batalla la ganarían las alternativas), sino "¿cuánto cuesta terminar lo ya construido frente a migrar?" — y con el coste hundido pagado, el coste marginal de cerrar puede ser defendible **desde otros frentes** (aprendizaje, finalización), que no son el mío.

Dos focos de autoengaño residual que sí señalo:

- **La justificación funcional de la ficha es falsa tal como está redactada.** "Necesita gestionar contenido sin depender de un desarrollador": el custom produce lo contrario (dependencia total de un desarrollador concreto). La necesidad real ya estaba cubierta por el mercado a coste cero. Que se reescriba la ficha: el motivo es afecto + aprendizaje + cierre, no una necesidad de mercado insatisfecha.
- **Racionalizaciones futuras.** Toda hora futura justificada con "quizá otros lo usen", "sirve de portfolio" o "podría venderse" debe considerarse humo: PHP no es ni su stack profesional (.NET) ni su dirección estratégica (healthtech), y el valor de portfolio de un miniCMS PHP para un pivote healthtech es aproximadamente nulo.

---

## Fuentes (todas consultadas el 2026-07-17)

- Precios WordPress.com 2026 (Personal 4 $/mes anual / 9 $/mes; plugins en planes de pago desde abril 2026): [comparedge.com](https://comparedge.com/tools/wordpress/pricing), [wordpress.com/pricing](https://wordpress.com/pricing/), [costbench.com](https://costbench.com/software/cms/wordpress-com/)
- Wix Light 17 $/mes, Squarespace Basic 19 $/mes, plan gratuito de Wix: [hostadvice.com](https://hostadvice.com/blog/website-builders/wix/wix-vs-squarespace-pricing/), [websitebuilderexpert.com](https://www.websitebuilderexpert.com/website-builders/comparisons/wix-vs-squarespace/)
- Publii gratuito/open source, apto para no técnicos: [getpublii.com](https://getpublii.com/), [github.com/GetPublii/Publii](https://github.com/GetPublii/Publii)
- Kirby 115 $/sitio, pago único: [getkirby.com/buy](https://getkirby.com/buy), [selecthub.com](https://www.selecthub.com/p/cms-software/kirby/)
- Google Sites gratuito, dominio propio conectable: [workspace.google.com/products/sites](https://workspace.google.com/products/sites/), [support.google.com/sites](https://support.google.com/sites/answer/9068867?hl=en)
- Hosting PHP España 2026 (Hostinger desde 1,49 €/mes, IONOS desde 1 €/mes, advertencia de precios de renovación): [ciudadano2cero.com](https://www.ciudadano2cero.com/hosting/comparativas/barato/), [hostinger.com/pricing](https://www.hostinger.com/pricing)
- Cuota de mercado CMS 2026 (WordPress ~59,8 % del mercado CMS, primer declive sostenido; auge SaaS): [gravitykit.com](https://www.gravitykit.com/wordpress-market-share-2026/), [kinsta.com](https://kinsta.com/wordpress-market-share/), [colorlib.com](https://colorlib.com/wp/cms-market-share/)
- Estado del repo (fechas, actividad, 0 stars): API pública de GitHub, `repos/JDiaz-healthTech/Anthropofilia`

---

## Veredicto T1

**APTO CON CONDICIONES** — exclusivamente en el frente de mercado, y con esta lectura estricta: como producto de mercado la idea es **NO APTA** (alternativas gratuitas superiores, TCO custom un orden de magnitud mayor, monetización con probabilidad ≈ 0); el frente no bloquea el proyecto únicamente porque la ficha **renuncia al mercado de forma explícita y honesta**. Condiciones vinculantes:

1. **Cero horas futuras justificadas por argumentos de mercado.** Ni monetización, ni "otros usuarios", ni "portfolio healthtech". Si alguno de esos argumentos reaparece, este dictamen pasa automáticamente a NO APTO.
2. **Reescribir la justificación de la ficha**: el motivo real es utilidad afectiva + finalización + aprendizaje, no una necesidad funcional insatisfecha (esa necesidad está cubierta gratis por el mercado en 2026).
3. **Presupuesto de TCO explícito y con tope**: hosting + dominio (~50-135 €/año) y un tope de horas/mes de mantenimiento post-cierre. Superado el tope, se ejecuta la condición 4.
4. **Plan de salida documentado para la usuaria**: procedimiento de migración del contenido a una alternativa sin Julius (exportación a WordPress.com o Publii), escrito antes de dar el proyecto por "finalizado". Es la única mitigación honesta del hecho de que Julius es el vendor lock-in de su madre.

---

# Dictamen T2 — TÉCNICA · Anthropofilia

> Tribunal adversarial de validación. Juez T2 (frente técnico exclusivo).
> Posición de partida: **NO CONFORMIDAD POR DEFECTO**. La carga de la prueba recae en el código, no en el proponente.
> Fecha del dictamen: **2026-07-17**.
> Repo auditado: `JDiaz-healthTech/Anthropofilia` (público), clon `--depth 100`, HEAD `d506940` (2026-05-31).

---

## 0. Método y alcance de la lectura

Se clonó el repositorio real y se examinó: estructura completa, historial (`git log --all`), `composer.json` / `composer.lock`, la capa de seguridad (`app/Security/SecurityManager.php`, 629 líneas), autenticación (`procesar_login.php`), subida de medios (`upload_image.php`, `app/Services/ImageService.php`), sanitización de contenido (HTMLPurifier), los modelos PDO, los dumps SQL versionados y el historial en busca de secretos. Todo lo que sigue está anclado a rutas y commits.

**Aviso adversarial de entrada:** el repo transmite una imagen de rigor (headers, CSP, rate-limiting, prepared statements). Esa imagen es parcialmente **real y sólida**, pero convive con **tres defectos graves** que ningún maquillaje de la capa de seguridad compensa. Un frente técnico se juzga por su eslabón más débil expuesto a internet, no por su mejor archivo.

---

## 1. Estado real del código (no el narrado)

Stack confirmado: PHP + PDO/MySQL(MariaDB), TinyMCE como editor, HTMLPurifier como saneador, PHPMailer, phpdotenv. Arquitectura procedural en `public_html/*.php` (un script por acción) con una fina capa OO en `app/` (Models + `SecurityManager` + `ImageService`).

Módulos y su estado verificado:

| Módulo | Estado | Evidencia |
|---|---|---|
| Auth / login | **Funcional y sólido** | `public_html/procesar_login.php`: prepared statement, `password_verify`, `password_needs_rehash`, `session_regenerate_id(true)`, throttle 5/15 min, CSRF. |
| Autorización por rol | **Funcional** con inconsistencia | `SecurityManager::requireRole()` mapea `admin`→`administrador`; **pero** `requireOwnershipOrRole()` (línea ~148) comprueba `hasRole('admin')` literal, rol que **nunca existe** en BD (los roles son `administrador`/`autor`). El fallback de admin queda muerto (falla en seguro, no es vuln, pero es deuda). |
| Editor / render de contenido | **Funcional y saneado** | HTMLPurifier aplicado en guardado *y* en render (`guardar_post.php:44`, `post.php:79`, `pagina.php:114`). Defensa en profundidad correcta. |
| Subida de medios | **Funcional y notablemente bien resuelto** | ver §2.4. |
| Publicación / páginas / posts / tags / categorías | Presentes y con auth+CSRF | `gestionar_*`, `guardar_*`, `eliminar_*` llevan `requireLogin`+`requireRole`+`requireValidCsrf`+ownership. |
| Registro público de usuarios | **AÑADIDO en el último commit** | `registro.php`, `procesar_registro.php`, `dashboard_usuario.php`, `seguir_pagina.php`. Ver §3 (esto contradice el alcance "finalizar"). |
| `app/Services/AuthService.php` | **Archivo VACÍO (0 bytes)** | También `app/Helpers/view.php` y `app/Services/SettingsService.php` a 0 bytes. Stubs de arquitectura nunca implementados. |

Conclusión de estado: el CMS **funciona** en su núcleo. No es una ruina. Pero "parcialmente acabado" es exacto: hay stubs vacíos, un subsistema recién añadido a medio integrar, y —crítico— **la batería de tests que la ficha presenta como hecha NO EXISTE** (§5).

---

## 2. Seguridad con lupa (CMS PHP expuesto, gestionado por persona no técnica)

### 2.1 Inyección SQL — CONFORME
Búsqueda exhaustiva de concatenación de entrada en SQL: **no se halló ninguna**. Todos los modelos usan `prepare()`/`bindValue()`. Los pocos `->query()` sin parámetros (`sitemap.php`, `feed.php`, `editar_pagina.php:38`) son **cadenas 100% estáticas** sin entrada de usuario. Los `WHERE` dinámicos (`gestionar_posts.php:28`, `gestionar_paginas.php:29`) se construyen con placeholders fijos y binding (`p.titulo LIKE :q`). `PDO::ATTR_EMULATE_PREPARES => false` en `config/database.php`. **Sin hallazgos de SQLi.**

### 2.2 XSS — CONFORME (con matiz de rendimiento)
Contenido enriquecido saneado con **HTMLPurifier v4.19.0** vía `SecurityManager::sanitizeHTML()` (línea 421), con allowlist estricta de tags/atributos e iframes restringidos por regexp a YouTube/Vimeo/Genially/Calaméo/Drive. Se aplica **al guardar y al renderizar** (doble purificación: seguro, algo costoso). Si HTMLPurifier faltara, lanza excepción en vez de guardar HTML crudo (línea 478). Títulos y campos cortos salen con `htmlspecialchars(..., ENT_QUOTES)`. **Sin hallazgos de XSS almacenado.**

### 2.3 CSRF — CONFORME
Tokens de 32 bytes (`random_bytes`), comparación con `hash_equals` (`SecurityManager::verifyCsrf`). Todas las mutaciones revisadas invocan `requireValidCsrf()`/`csrfValidate()`. **Matiz:** en `upload_image.php:23` el CSRF es **opcional** (`if ($csrf) { ... }`): si el cliente no envía token, no se valida. Está mitigado por `requireLogin()`, pero un usuario autenticado sigue siendo CSRF-eable hacia subida. Severidad baja (un solo usuario real), pero es un hueco declarado.

### 2.4 Subida de archivos — CONFORME (punto fuerte real)
Defensa en capas genuina:
- `public_html/uploads/.htaccess`: `php_flag engine off`, `Options -ExecCGI`, `<FilesMatch ...\.(php|phtml|phar|...)>Require all denied`. **La ejecución de PHP subido está bloqueada** y se hereda a subdirectorios `Y/m`.
- `SecurityManager::validateUpload()`: tamaño, MIME por `finfo` (contenido, no extensión), `getimagesize`.
- `ImageService::store()`: **re-codifica la imagen con GD** (`imagecreatefrom*` + reoutput), lo que **destruye cualquier payload PHP embebido**, y nombra el fichero con `bin2hex(random_bytes(16))`. No hay path traversal (subdir por `date('Y/m')`, nombre aleatorio).

Esto está bien hecho. Sin objeción.

### 2.5 Sesiones y contraseñas — CONFORME
Cookies `httponly`, `samesite=Lax`, `secure` bajo HTTPS; idle timeout 30 min, rotación de ID cada 10 min, `session_regenerate_id(true)` en login. Contraseñas con `password_hash`/`PASSWORD_DEFAULT` (bcrypt `$2y$`) + rehash automático. Correcto.

### 2.6 Exposición de credenciales en el repo público — **NO CONFORME (GRAVE)**
`.env` está correctamente en `.gitignore` y nunca se commiteó. `config/database.php` y `config.php` leen sólo de entorno, sin fallbacks peligrosos. **Pero:**
- `ops/docker-compose.yml` versiona credenciales: `MYSQL_ROOT_PASSWORD: root`, `MYSQL_USER: blogmaster`, `MYSQL_PASSWORD: juliusDev2025`. Son de laboratorio local, pero `juliusDev2025` es un patrón de password reutilizable y no debería estar en un repo público.
- `ops/scripts/backup.sh` / `restore.sh`: `DB_PASS="password"` hardcodeado (plantilla `usuario`/`password`). Debe leer de `.env`; riesgo real bajo pero es mala práctica versionada.

El problema mayor de "exposición" no son credenciales de servicio, sino **datos personales reales** — ver §4.

---

## 3. Viabilidad del plan "auditar → optimizar → cerrar"

### 3.1 Versión de PHP y soporte (a 2026-07-17)
- `ops/docker/Dockerfile` fija **`FROM php:8.0-apache`**. `composer.json` exige `"php": ">=8.0"` (permite correr sobre EOL).
- Fechas EOL verificadas (WebSearch):
  - **PHP 8.0 → EOL 26-nov-2023.** Sin parches de ningún tipo desde hace **>2,5 años**.
  - **PHP 8.1 → EOL 31-dic-2025.** También muerto a fecha de hoy.
  - **PHP 8.2 → sólo-seguridad hasta 31-dic-2026.**
- Veredicto: **el intérprete objetivo del proyecto está fuera de soporte de seguridad.** Un CMS expuesto a internet, gestionado por una persona no técnica, no puede correr sobre un runtime sin parches. La versión real en Hostinger (hPanel) **no consta en el repo y DEBE verificarse**; si es 8.0/8.1, es bloqueante.
- Objetivo mínimo aceptable: **migrar a PHP 8.3+** (soporte de seguridad hasta nov-2027) y elevar `composer.json` a `"php": ">=8.3"`.

### 3.2 ¿Cerrable o hay que amputar?
El núcleo es **cerrable**: la base de seguridad y datos es de calidad suficiente para un miniCMS mono-usuario. **Pero el plan tal como se declara ("finalizar, no construir") está desmentido por el propio historial:** el último commit `d506940` **construye un subsistema nuevo** de registro público de usuarios (`registro.php`, `procesar_registro.php`, roles estándar, `dashboard_usuario.php`, `seguir_pagina.php`). Eso es lo contrario de cerrar:
- Amplía superficie de ataque y **amplía el alcance RGPD** (ahora se recogen cuentas de terceros), en un producto cuya premisa es **"un único usuario real"** (la madre, `AnaLopezS1963`).
- **Amputación recomendada:** eliminar el registro público y el rol "usuario estándar" salvo que exista una necesidad de negocio explícita. Un CMS para una persona no necesita alta de cuentas por internet.

### 3.3 Deuda estructural para el cierre
- Stubs vacíos (`AuthService.php`, `view.php`, `SettingsService.php`) → decidir: implementar o borrar.
- 4 dumps SQL versionados (`blogdb.sql`, `blogdb31012026.sql`, `blogdbInicialproduccion.sql`, `blogdbv1noproduccion.sql`) → no deben estar en el repo (ver §4).
- Inconsistencia de rol en `requireOwnershipOrRole` (§1).

---

## 4. Riesgos regulatorios (RGPD) — **NO CONFORME (GRAVE / BLOQUEANTE)**

**Se ha volcado la base de datos de PRODUCCIÓN a un repositorio PÚBLICO.** No es teoría: el fichero `database/blogdb.sql` (y `blogdb31012026.sql`, `blogdbInicialproduccion.sql` en historial) contiene datos personales reales de terceros:
- Usuaria real: `(1, 'AnaLopezS1963', 'analosampedro@gmail.com', '$2y$10$dcnI3e785FHK6ycG5A8adui34KDKsO7Pb6LmJxdsb36BwlCDCgSA2', 'autor', ...)` → **email + hash bcrypt de la madre, públicos.**
- Segundo email real (`juliodl@msn.com`) en registros de formulario de contacto.
- Tabla `app_logs` con **19 direcciones IP distintas**, user-agents y contenidos de mensajes de contacto (`{"from":"juliodl@msn.com"}`), todo con timestamp.

Implicaciones:
- **Brecha de datos personales** (RGPD arts. 5, 32) por exponer datos de identificación, IPs (dato personal) y credenciales.
- El hash bcrypt, aunque no es texto plano, es **crackeable offline** una vez público. Debe considerarse comprometido.
- Acciones obligatorias antes de cualquier "APTO": (1) purgar los 4 dumps del **historial completo** (`git filter-repo`/BFG), no basta con borrar en HEAD; (2) **rotar la contraseña** de la usuaria afectada; (3) rotar credenciales de BD; (4) hacer el repo privado o eliminar todo PII; (5) valorar el deber de notificación del art. 33/34 según criterio del responsable.
- Positivo: existe checkbox de consentimiento RGPD en registro (`procesar_registro.php:38`) y páginas legales (`privacidad.php`, `cookies.php`, `aviso-legal.php`).

**Backups y hosting:** `ops/scripts/backup.sh` implementa dump+gzip+sha256 con rotación de 100 y mínimo 10 días entre snapshots — razonable **pero no se evidencia ejecución programada (cron) ni copia off-site**; un backup en el mismo servidor no protege ante pérdida del servidor. Hosting: Hostinger (autor de commit `Hostinger Version <jdl1989@live.com>`, snapshot `8902c6c`).

---

## 5. La "batería de tests hecha con Claude Code" — **NO CONFORME (GRAVE)**

**No existe ninguna prueba en el repositorio.** Verificado:
- `find` de `phpunit.xml*`, `*/tests/*`, `*Test.php`, `*_test.php` → **cero resultados**.
- `git log --all` de cualquier fichero de test → **cero commits**. Nunca se versionó un test.
- No hay bloque `require-dev` en `composer.json`. Las menciones a `phpunit` en `composer.lock` son **dependencias transitivas de dev de librerías de terceros** (yoast polyfills, etc.), no un harness del proyecto.

No es "teatro de cobertura": **es un escenario vacío.** La ficha afirma una batería de tests reciente que el repositorio no respalda. O bien los tests viven sólo en local sin versionar (⇒ no auditables, no reproducibles, valor probatorio **cero**), o la afirmación es incorrecta. En cualquier caso, **a efectos técnicos la cobertura de tests es 0** y no puede computarse como mérito. Este punto contradice directamente un pilar de la ficha y obliga a tratar todo "está probado" como no demostrado.

---

## 6. Balance adversarial

**A favor (real, no cosmético):** SQLi cerrado, XSS saneado con HTMLPurifier en doble capa, subida de ficheros bien blindada (engine off + GD re-encode + nombres aleatorios), auth con bcrypt+rehash+throttle, sesiones endurecidas, CSP con nonce, rate-limiting persistente. Para un desarrollador cuyo stack principal **no es PHP**, la capa de seguridad está por encima de la media.

**En contra (bloqueante):**
1. PII de producción (email + hash de la madre, IPs, mensajes) **volcada a repo público** — brecha RGPD.
2. Runtime **PHP 8.0/8.1 EOL** como objetivo de despliegue, sin parches de seguridad.
3. **Tests inexistentes** pese a declararse hechos — mérito no verificable, cobertura efectiva nula.

**Secundario:** CSRF opcional en upload, credenciales dev en `docker-compose`, `DB_PASS` plantilla en backup.sh, stubs vacíos, inconsistencia de rol admin, y **scope creep** (registro público añadido) que contradice el mandato de "finalizar".

El plan "auditar → optimizar → cerrar" es **viable en el núcleo**, pero **no en el estado actual**: primero hay que remediar los tres bloqueantes; sólo entonces "cerrar" tiene sentido.

---

## Veredicto T2

**APTO CON CONDICIONES** (frente técnico exclusivamente). Las condiciones son **previas y no negociables**; mientras cualquiera siga abierta, el frente técnico es **NO APTO de facto**:

1. **[BLOQUEANTE — RGPD]** Purgar del historial completo los 4 dumps SQL con PII (`git filter-repo`/BFG), hacer el repo privado o limpiar todo dato personal, **rotar la contraseña de la usuaria real** y las credenciales de BD. Verificar deber de notificación art. 33/34.
2. **[BLOQUEANTE — Runtime]** Verificar la versión de PHP real en Hostinger y **migrar a PHP 8.3+**; elevar `composer.json` a `">=8.3"`. Nada de desplegar sobre 8.0/8.1 (EOL).
3. **[BLOQUEANTE — Tests]** Versionar una batería de tests **real y auditable** (phpunit + `require-dev` + `phpunit.xml`) que cubra al menos: login/CSRF, autorización por rol/ownership, sanitización HTML y validación de subida. Sin esto, "está probado" no se acepta.
4. **[Alta]** Retirar credenciales de `docker-compose.yml` y `backup.sh` (a `.env`); hacer CSRF **obligatorio** en `upload_image.php`.
5. **[Media]** Decidir sobre el subsistema de registro público: amputarlo (coherente con "un único usuario") o justificar y asegurar su alcance RGPD. Programar backup vía cron **off-site** y probar `restore.sh`. Eliminar/implementar stubs vacíos y corregir la inconsistencia de rol en `requireOwnershipOrRole`.

Cumplidas 1–3 (bloqueantes) el frente técnico pasa a APTO estable; 4–5 son cierre de deuda para dar por "finalizado".

---

# Dictamen T3 — Frente APRENDIZAJE

**Tribunal adversarial de validación · La Biblioteca**
**Idea:** Anthropofilia (miniCMS PHP para gestión de contenido de su madre)
**Juez:** T3 (Aprendizaje)
**Fecha:** 2026-07-17
**Posición de partida:** NO CONFORMIDAD POR DEFECTO
**Repo auditado:** `JDiaz-healthTech/Anthropofilia` (98 commits, PHP 45.7% / JS 34.2% / CSS 19.5%)

---

## 0. Advertencia metodológica

No valido la idea. Someto a la carga de la prueba la afirmación implícita de que "finalizar Anthropofilia enseña algo que acerca a Julius al pivote healthtech". La carga la tiene el proyecto, no yo. La utilidad familiar (que su madre pueda publicar) es real pero **no es aprendizaje**: es entrega de un servicio. Ese eje se juzga en otro frente. Aquí solo pesa la densidad de aprendizaje nuevo por hora y su transferibilidad al pivote.

---

## 1. ¿Qué aprende REALMENTE Julius finalizando este CMS?

Desagrego, porque "aprender PHP" es una etiqueta vacía. Hay cinco componentes con valores muy distintos:

### 1.1. PHP como lenguaje — VALOR BAJO-NULO para el pivote

- El repo usa PHP 8.0+, PDO, MariaDB. Aprender más PHP idiomático en 2026 **no acerca a healthtech ni mejora la empleabilidad de un perfil .NET**. El mercado español de PHP existe (agencias, WordPress, Symfony/Laravel) pero es un mercado *distinto y en general peor pagado* que el de .NET/C#, y **ortogonal al pivote**. Julius no quiere ser dev PHP.
- Peor aún: profundizar en PHP artesanal (sin framework — aquí no hay Laravel/Symfony, es un CMS a mano con SecurityManager y ImageService propios) enseña patrones que **no son mercado**. Nadie contrata "sé hacer un CMS PHP desde cero". El mercado PHP que paga usa framework.
- **Veredicto parcial:** el aprendizaje de PHP-como-lenguaje es coste hundido. Ya lo sabe lo suficiente para terminar esto. Aprender *más* PHP es tiempo restado al pivote. **0% de alineamiento.**

### 1.2. Seguridad web aplicada — EL ÚNICO ACTIVO TRANSFERIBLE DE PRIMER ORDEN

Aquí sí hay señal, y es la que salva parcialmente al proyecto en mi frente. El repo declara: `SecurityManager` propio (CSRF, rate limiting, CSP, HTMLPurifier), validación MIME real en subidas (no por extensión), prepared statements PDO en todas las consultas, honeypot + rate limiting en el formulario de contacto.

- XSS, CSRF, SQLi y **subida de archivos segura** son conocimiento que transfiere a *cualquier* stack: .NET, healthtech, lo que sea. En sanidad la seguridad no es un extra, es requisito regulatorio (protección de datos de salud, categoría especial RGPD art. 9). Entender *por qué* HTMLPurifier y no un `strip_tags`, *por qué* validar MIME real y no la extensión, *por qué* CSP y no confiar en el escape — eso es capital que se revende en healthtech.
- **PERO** (y es un "pero" grande): declarar estos mecanismos en un README no prueba que Julius los entienda. Un `SecurityManager` que Claude ayudó a escribir puede estar "presente" sin estar "comprendido". El valor de aprendizaje aquí es **condicional a que Julius audite a mano cada vector** (ver sección 2).
- **Veredicto parcial:** máximo potencial de transferencia del proyecto. **Alineamiento con pivote: ~70% SI SE EJECUTA A MANO; ~10% si se limita a "leer lo que ya hay".**

### 1.3. Auditoría de código propio antiguo — HABILIDAD SENIOR REAL

El alcance redefinido ("auditar → optimizar → cerrar") es lo más valioso del planteamiento, más que el código en sí.

- Auditar un codebase parcialmente hecho, identificar deuda, decidir qué se optimiza y qué se cierra, es una **competencia de nivel senior** que casi ningún junior practica. Julius, con perfil dual y horas sueltas, rara vez tiene la oportunidad de hacer esto sobre algo suyo con 98 commits de historia.
- Esto **sí transfiere** al mundo laboral y al legacy .NET 3.5/WinForms de su empresa: auditar lo que otro (o tu yo pasado) dejó a medias es exactamente lo que hace en su día a día. Refuerza una habilidad de empleabilidad general, no específica de healthtech.
- **Alineamiento con pivote: ~30% (transferencia indirecta vía "seniority" y legacy).**

### 1.4. Testing sobre legacy / código existente — RELEVANTE PARA ENTORNOS SANITARIOS

- La batería de tests reciente (hecha con Claude Code — atención, esto es el punto crítico del vaciado, sección 2) toca una habilidad real: **escribir/entender tests sobre código que ya existe**, no TDD desde cero. Los entornos sanitarios y regulados viven de esto: validación, trazabilidad, cobertura sobre sistemas que ya están en producción.
- El aprendizaje aquí es **potencialmente alto pero está en riesgo máximo de vaciado**: si los tests los escribió la IA y Julius solo los ejecutó, el aprendizaje es cero. Si Julius los lee, entiende qué cubren, *encuentra qué NO cubren* y añade casos a mano, el aprendizaje es real.
- **Alineamiento con pivote: ~40% condicional.**

### 1.5. UX para usuario no técnico — TRANSFERENCIA A SALUD PARA MAYORES

- Diseñar para su madre (usuaria única, no técnica, profesora de 60+ con tres décadas de docencia) es diseñar para una población no técnica. El repo declara accesibilidad seria: alto contraste, modo oscuro, ajuste de tamaño de fuente, navegación por teclado, FAB de accesibilidad. **Esto no es decorativo: es exactamente el tipo de diseño que necesita una app de salud para poblaciones mayores o con déficits sensoriales.**
- Aquí conecta el perfil de exaudiólogo pediátrico: diseñar para quien no puede/no quiere lidiar con complejidad. La accesibilidad web aplicada (WCAG-adyacente) **es un activo real de healthtech**.
- **Alineamiento con pivote: ~50%.**

---

## 2. Riesgo de VACIADO POR IA — el punto que puede hundir el proyecto en mi frente

**La batería de tests ya la hizo Claude Code.** Esto es la bandera roja central. Si el patrón se repite en la finalización, el resultado es literal: *"Claude mantiene la web de mi madre"* — y Julius no aprende nada, solo adquiere un servicio.

El proyecto NO es apto en mi frente si se termina delegando. Es apto SOLO si Julius ejecuta y comprende a mano lo siguiente. Soy prescriptivo:

### 2.1. Auditoría de seguridad — A MANO, línea por línea

Julius debe, sin IA que escriba por él (la IA puede explicar, no ejecutar):

1. **CSRF:** abrir el `SecurityManager`, entender cómo se genera y valida el token, y **probar a romperlo**: enviar un POST sin token / con token de otra sesión y verificar que se rechaza. Si no sabe explicar el flujo token→sesión→validación de memoria, no lo ha aprendido.
2. **Subida de archivos:** este es EL vector clásico de RCE en CMS PHP. Debe verificar a mano la validación MIME real, intentar subir un `.php` renombrado a `.jpg`, un polyglot, un SVG con script. Entender por qué se valida contenido y no extensión, y dónde se almacenan los uploads (¿ejecutables desde `public_html/uploads/`? riesgo directo).
3. **SQLi:** confirmar que *todas* las consultas usan prepared statements PDO. Buscar a mano cualquier concatenación de strings en queries. Un solo `"SELECT ... " . $var` invalida el "todas las consultas parametrizadas".
4. **XSS + HTMLPurifier:** entender la diferencia entre escapar en salida y purificar en entrada, y por qué TinyMCE (que emite HTML) obliga a HTMLPurifier. Probar a inyectar `<script>` en un post y verificar que se neutraliza.
5. **CSP:** leer la política, entender qué bloquea, verificar que los embeds (Genially, Calameo, YouTube) funcionan sin abrir `unsafe-inline` de par en par. Una CSP con `unsafe-inline` en scripts es teatro.

**Entregable de aprendizaje exigible:** un documento (para él, no para portfolio) donde explique con sus palabras cada uno de los 5 vectores, qué encontró, y qué corrigió. Si no puede escribirlo sin IA, no aprendió.

### 2.2. Tests — reapropiación obligatoria

- No aceptar la batería de Claude como cerrada. Julius debe **leer cada test, identificar qué cubre y — sobre todo — qué NO cubre**, y escribir al menos los casos de borde de seguridad a mano (los del punto 2.1: token inválido, MIME falso, inyección). Los tests de seguridad escritos por él son la prueba de que entiende los vectores.
- Regla dura: **por cada test que la IA escribió, Julius debe poder explicar por qué existe y qué pasaría si fallara.** Los que no sepa explicar, los reescribe.

### 2.3. Cierre — qué ejecuta él

- La optimización (rendimiento, queries N+1, caché en `storage/cache/HTML`) la decide y ejecuta él: son decisiones de arquitectura, no de tecleo.
- El "cerrar lo que falta" debe listarlo Julius primero (auditoría propia) ANTES de pedir ayuda. La IA rellena huecos que él ha identificado, no descubre los huecos por él.

**Si Julius no puede cumplir 2.1–2.3, el proyecto en mi frente es NO APTO: sería adquirir un CMS, no aprender.**

---

## 3. Valor de finalización vs. coste de oportunidad

### A favor de terminar
- **Usuario real esperando (su madre) = presión social positiva.** Un proyecto con deadline emocional se termina; un proyecto de portfolio abstracto muere al 80%. Esto es real y tiene valor de hábito: *aprender a cerrar* es una meta-habilidad que a Julius (horas sueltas, muchos proyectos previos) probablemente le falte.
- **Feedback real:** su madre usará el panel y se quejará de lo que no entienda. Eso es UX validada por un humano no técnico — oro para el músculo de "diseño para no técnicos".
- **El proyecto está parcialmente hecho.** El coste marginal de terminar es bajo comparado con el de arrancar algo nuevo. La curva de "aprendizaje nuevo por hora" en un proyecto ya montado es *decreciente* (lo grueso ya se aprendió), pero el coste de cierre también.

### En contra (el coste de oportunidad, que es serio)
- **Cero alineamiento de dominio con healthtech.** Es un CMS de filosofía, no toca datos de salud, ni interoperabilidad (HL7/FHIR), ni nada del dominio al que Julius pivota. Las horas que van aquí NO construyen conocimiento de sanidad.
- **Riesgo de "una golondrina más":** terminar Anthropofilia da la *sensación* de progreso (dopamina de cerrar) sin mover la aguja del pivote. Es el peligro clásico — sentirse productivo lejos del objetivo.
- La mayor parte del stack (PHP artesanal, TinyMCE, feed RSS, sitemap) es **aprendizaje ya consumido o no transferible**. La densidad de *aprendizaje nuevo* por hora en el tramo final es baja: se está puliendo, no descubriendo.

**Balance:** terminar tiene valor de **hábito de cierre + entrega familiar + refuerzo de seguridad/UX SI se hace a mano**. No tiene valor de dominio healthtech. Es defendible como "proyecto de cierre acotado", **NO** como "proyecto de pivote".

---

## 4. Cuantificación honesta

### Alineamiento con el pivote healthtech (ponderado por peso de cada componente en el tramo de finalización)

| Componente | Peso en el cierre | Alineam. pivote | Contribución |
|---|---|---|---|
| PHP como lenguaje | 20% | 0% | 0 |
| Seguridad web aplicada (a mano) | 25% | 70% | 17,5 |
| Auditoría código propio | 20% | 30% | 6 |
| Testing sobre existente | 15% | 40% | 6 |
| UX / accesibilidad no técnicos | 20% | 50% | 10 |

**Alineamiento total con el pivote: ~40%** — y ese 40% es un **techo condicionado** a que Julius ejecute a mano la auditoría de seguridad y la reapropiación de tests. Si delega (patrón "Claude lo hace"), el alineamiento real cae a **~10-15%** (solo queda la UX validada por su madre).

### Densidad de aprendizaje NUEVO por hora

- **Baja-media.** El proyecto está mayormente hecho; lo grueso del aprendizaje (montar el CMS, PDO, TinyMCE) ya ocurrió. El tramo de finalización es **pulido**, no descubrimiento. La *única* bolsa de aprendizaje nuevo denso es la **auditoría de seguridad ejecutada a mano** — ahí sí hay alta densidad por hora. El resto (RSS, sitemap, cierre de features) es densidad baja.
- **Estimación honesta:** de cada 10 horas de finalización, quizá **3-4 tienen aprendizaje nuevo real** (las de seguridad y auditoría), y **6-7 son entrega/pulido** — valiosas para el compromiso familiar y el hábito de cierre, pero **no son aprendizaje**.

### La parte que NO es aprendizaje (honestidad exigida)
Buena parte del valor de este proyecto es **compromiso familiar**: hacer que su madre pueda publicar. Eso es legítimo y humano, pero **no puede contabilizarse como avance hacia el pivote ni como aprendizaje**. Confundir "terminé algo útil para mi madre" con "avancé hacia healthtech" sería el autoengaño que este tribunal existe para bloquear.

---

## 5. Síntesis del frente

El proyecto **NO es de pivote** y no debe venderse como tal. Su valor de aprendizaje se concentra en **una sola bolsa transferible** — seguridad web aplicada — que *solo existe si Julius la ejecuta a mano* en lugar de delegar (como ya hizo con los tests). La auditoría de código propio y la UX para no técnicos aportan transferencia secundaria. El PHP-como-lenguaje es coste hundido, cero pivote. La densidad de aprendizaje nuevo en el tramo final es baja salvo en el bloque de seguridad. El riesgo de vaciado por IA es **el factor decisivo**: la evidencia (tests ya hechos por Claude Code) apunta en la dirección peligrosa.

Es aprobable **solo como proyecto de cierre acotado con condiciones estrictas de ejecución manual**, no como inversión en el pivote. Sin esas condiciones, es "adquirir un servicio para mi madre" disfrazado de aprendizaje.

---

## Veredicto T3

**APTO CON CONDICIONES.**

Condiciones de obligado cumplimiento (si no se cumplen, degrada a NO APTO en mi frente):

1. **Auditoría de seguridad ejecutada a mano** sobre los 5 vectores (CSRF, subida de archivos, SQLi, XSS/HTMLPurifier, CSP), incluyendo intentos reales de romper cada uno (POST sin token, `.php` renombrado, inyección `<script>`). Sin IA que ejecute — la IA solo explica.
2. **Entregable de comprensión:** documento propio (no para portfolio) explicando con sus palabras cada vector, qué encontró y qué corrigió. Si no puede escribirlo sin IA, no aprobó.
3. **Reapropiación de la batería de tests:** leer todos los tests de Claude, saber explicar por qué existe cada uno, identificar lo que NO cubren, y escribir a mano los casos de borde de seguridad.
4. **Auditoría propia ANTES de pedir ayuda:** Julius lista qué falta y qué optimizar antes de que la IA toque nada. La IA rellena huecos identificados por él, no los descubre.
5. **Etiquetado honesto:** el proyecto se registra en La Biblioteca como "cierre acotado + compromiso familiar", con alineamiento pivote declarado ~40% (techo condicional), NO como proyecto de pivote healthtech. Prohibido contabilizar las horas de pulido/entrega como aprendizaje.
6. **Tope de horas:** acotar el tramo de finalización. Si el cierre se estira más allá de lo pactado, se está robando tiempo al pivote real — cortar y entregar.

---

# Dictamen T4 — ALCANCE / REALISMO — Anthropofilia

**Juez:** T4 (Alcance/Realismo) · **Fecha:** 2026-07-17 · **Posición de partida:** no conformidad por defecto.
**Evidencia:** clon del repo `JDiaz-healthTech/Anthropofilia` (main, develop, feature/testing-suite), API de GitHub, cabeceras HTTP de producción.

---

## 1. Estado real medido (no el declarado)

| Métrica | Valor medido |
|---|---|
| LOC total (sin vendor) | ~21.900 (PHP 9.387 · JS 5.244 · CSS 6.655 · SQL 643) |
| Puntos de entrada PHP públicos | 43 scripts en `public_html/` + 4 endpoints en `api/` |
| Commits totales | 98 |
| Último commit en `main` y `develop` | **2026-05-31** — 47 días de inactividad a fecha de hoy |
| Patrón de actividad | Ráfaga 26-ene→28-mar; parón de 7 semanas; ráfaga 17→31-may; **nada desde entonces** |
| Producción | Viva en anthropofilia.es (Hostinger, PHP 8.3, HTTPS operativo) |
| Deuda técnica documentada | C-01…C-06, I-01…I-12, m-01/02: **resuelta** según CLAUDE.md; I-13 decisión consciente |
| Ramas | `develop` == `main`; `hostinger_v1/v2` pendientes de borrar |

### Hallazgo de no conformidad n.º 1: los tests declarados no existen en el repo

La ficha afirma "batería de tests reciente hecha con Claude Code". Medido: la rama `feature/testing-suite` (push del 2026-07-04) es **idéntica a `main`**: `git diff --stat main origin/feature/testing-suite` devuelve vacío. No hay carpeta `tests/`, no hay `phpunit.xml`, no hay ninguna dependencia de test en `composer.json`. El propio CLAUDE.md lista la suite PHPUnit en *Future Work* como no empezada. Si esos tests existen, están sin commitear en una máquina local — a efectos de alcance, **no existen**.

### Hallazgo de no conformidad n.º 2: el scope creep ya ocurrió y sigue planificado

Para un CMS con **una usuaria real**, el repo contiene: registro público de usuarios con RGPD, login por email, tres roles, `dashboard_usuario.php`, páginas de seguimiento de posts (último commit de mayo). Y en *Future Work*: sistema de comentarios, analíticas propias, remember-me con tokens persistentes. Esto no es "finalizar": es una hoja de ruta de producto multiusuario disfrazada de cierre. El registro público además **amplía la superficie de ataque** de un sitio que su autor no vigila a diario.

### Hallazgo n.º 3: seguridad declarada vs. observada

README y CLAUDE.md declaran "CSP centralizada". La cabecera CSP real servida por producción es únicamente `upgrade-insecure-requests` — una CSP vacía a efectos prácticos. `ops/scripts/backup.sh` existe pero con credenciales placeholder (`usuario`/`password`) y sin evidencia de cron en producción. Un backup no cableado ni restaurado alguna vez no es un backup. El README instruye `cp .env.example .env` pero `.env.example` no está en el repo.

---

## 2. Estimación por tramos (sesiones de ~2 h)

| Tramo | Contenido | Mín | Máx | Notas |
|---|---|---|---|---|
| (a) Auditoría del estado actual | 43 entry points + 4 APIs + SecurityManager (629 LOC), contraste código↔producción | 2 | 4 | Con Claude Code. La mitad ya está hecha: la tabla de deuda de CLAUDE.md es una auditoría razonable |
| (b) Optimización + endurecimiento | CSP real, revisión/retirada del registro público, rate limits verificados, backups cableados + **restore probado** | 3 | 6 | La mayor "optimización" de seguridad es eliminar superficie (registro), no añadir código |
| (c) Cierre + despliegue + formación | Flecos, smoke tests mínimos (no la suite completa), tutorial con capturas para la usuaria (2–3 sesiones, siempre se subestima), sesión de formación en vivo | 4 | 8 | El despliegue ya existe; el coste real es la documentación y el acompañamiento |
| **Total alcance declarado** | | **9** | **18** | **18–36 h de trabajo efectivo** |

Si se mantiene la suite PHPUnit completa de *Future Work*: **+4 a +8 sesiones** adicionales. Si se toca comentarios o analíticas: el proyecto deja de tener fecha de fin.

---

## 3. Sumideros ocultos (no presupuestados en la ficha)

| Sumidero | Coste estimado | Estado |
|---|---|---|
| Hosting/dominio/HTTPS | 0–1 sesiones | Ya resuelto (único punto donde la ficha es mejor que lo habitual) |
| Backups automatizados + restore probado | 1–2 sesiones | Script placeholder, sin cron. **Obligatorio antes de declarar cierre** |
| Soporte perpetuo ("mamá, no me funciona") | **1–3 h/mes indefinido** (0,5–1,5 sesiones/mes) | No termina nunca. Picos de 2–4 sesiones cuando Hostinger fuerce upgrade de PHP (hoy 8.3): TinyMCE self-hosted, HTMLPurifier y PHPMailer se mantienen a mano, sin ecosistema WordPress detrás |
| Tentación de rehacer/ampliar | Riesgo máximo, **ya materializado** | Registro público, roles, seguimiento de posts; comentarios y analíticas planificados |

El coste recurrente es el dato duro: cerrar el proyecto no lo saca de la cartera. Compra una suscripción vitalicia de ~1–3 h/mes contra las mismas horas que reclaman las 6 ideas en cola.

---

## 4. Confrontación con disponibilidad real

Ritmo declarado posible: horas sueltas + fines de semana, quizá 3–4 sesiones/semana en un buen mes (~12–15 sesiones/mes). Ritmo **observado**: 8 commits en los últimos 3,5 meses y 47 días a cero, con dos parones largos previos (feb→mar, abr→may). El histórico dice que este proyecto recibe ráfagas de fin de semana espaciadas por semanas de nada, porque compite —y pierde— contra el trabajo y las ideas healthtech alineadas con su pivote. Con el patrón real, 9–18 sesiones son **2–5 meses de calendario**, no uno.

### Recorte que lo hace terminable en ≤ 1 mes (~8–11 sesiones)

1. **Congelar *Future Work* entero por escrito**: sin comentarios, sin analíticas, sin remember-me, sin suite PHPUnit completa (solo smoke tests de login, CRUD de post y contacto: 1–2 sesiones).
2. **Retirar o desactivar el registro público** (1 sesión). Sin comentarios, el rol `usuario` no tiene caso de uso; solo es superficie de ataque y RGPD gratuito.
3. Auditoría ligera (2 sesiones) limitada a superficie pública + admin, no re-auditar lo ya tabulado.
4. CSP real + backups con cron y **un restore ejecutado** (2–3 sesiones).
5. Tutorial de ≤5 páginas con capturas + 1 sesión de formación con la usuaria (3 sesiones).
6. **Definición escrita de HECHO** y repo en modo mantenimiento: a partir de ahí, solo bugs, nunca features.

**Sacrificios:** todo *Future Work*, el sistema de usuarios multiusuario ya construido en mayo (se archiva), y la ambición de suite de tests "profesional". Lo que no se sacrifica: seguridad de superficie, backups, formación.

---

## 5. Alternativa de alcance: "traición constructiva" (solo dato, no decisión)

Migrar contenido a plataforma gestionada (WordPress hosted o equivalente) y retirar el custom:

| Concepto | Sesiones |
|---|---|
| Exportar posts/páginas (BD → importador) | 1–2 |
| Rehacer embeds Genially/Calameo/YouTube en la plataforma (lo doloroso) | 1–3 |
| Dominio, redirecciones 301, tema aproximado | 1–2 |
| Formación (plataforma estándar: tutoriales ya existen) | 1 |
| **Total** | **4–8** |

Coste añadido: ~5–10 €/mes de plataforma. Lo que compra: **elimina el sumidero perpetuo de mantener código propio** (queda soporte de uso, mucho menor) y las 21.900 LOC dejan de ser pasivo. Lo que pierde: los embeds a medida y la personalización, que son la razón de ser del custom, y da por hundido el sunk cost. Dato frío: migrar (4–8 sesiones) cuesta menos que cerrar el custom recortado (8–11) **y además cancela el coste recurrente**; la única defensa económica del custom es su valor de portfolio y que producción ya funciona hoy.

---

## Veredicto T4

**APTO CON CONDICIONES** (exclusivamente en el frente alcance/realismo):

1. **Alcance recortado obligatorio** (§4): congelación escrita de *Future Work* completo; tope duro de **12 sesiones** y fecha de cierre en calendario. Si al agotar el tope no está cerrado, se pasa automáticamente a la alternativa del §5.
2. **Retirar o desactivar el registro público** antes de declarar cierre, o justificar por escrito su caso de uso con una sola usuaria real.
3. **Backups automatizados con un restore probado** y CSP real en producción como criterio de "hecho" — no negociable en un CMS público.
4. **Corregir la ficha**: la "batería de tests reciente" no existe en el repositorio; o se commitea y se referencia, o se elimina la afirmación.
5. **Reconocer en cartera el coste recurrente**: ~1–3 h/mes de soporte perpetuo descontadas de la disponibilidad de las otras 6 ideas, con picos en upgrades de PHP del hosting.

Sin las cinco condiciones: NO APTO por alcance abierto, ritmo real incompatible (47 días a cero) y coste recurrente no presupuestado.
