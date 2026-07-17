# Orquestador — Anthropofilia

**Fecha:** 2026-07-17
**Entrada:** 4 dictámenes independientes (tribunal.md). Única voz que los lee juntos.
**Criterio dominante de ponderación:** aprendizaje + pivote healthtech.

---

## 0. Incidencia de emergencia (fuera de todo veredicto)

T2 encontró **volcados de la BD de producción en el repo público** (`database/blogdb.sql` + 3 más en el historial) con datos personales reales: email y hash bcrypt de la usuaria, 19 IPs y mensajes de contacto. Es una brecha RGPD activa en `anthropofilia.es` (producción viva, según T4). **Esto se remedia hoy, decida lo que decida Julius sobre la idea:** purgar historial (`git filter-repo`/BFG) o hacer privado el repo, rotar contraseña de la usuaria y credenciales de BD, y valorar el deber de notificación (art. 33/34).

## 1. Resumen de veredictos

| Frente | Veredicto | Núcleo |
|---|---|---|
| T1 Mercado | APTO CON CONDICIONES | Como producto: no apto (alternativas gratis, TCO 10×, Julius = vendor lock-in de su madre). No bloquea solo porque la ficha renuncia al mercado honestamente. |
| T2 Técnica | APTO CON CONDICIONES (bloqueantes) | Brecha RGPD en repo; PHP 8.0 EOL; la "batería de tests" NO existe en el repo. Base de seguridad del código sorprendentemente sólida (PDO, HTMLPurifier, subida blindada, bcrypt+CSRF+CSP). |
| T3 Aprendizaje | APTO CON CONDICIONES | Única bolsa de aprendizaje transferible: auditoría de seguridad web A MANO (~70% transferible a healthtech). Alineamiento total ~40% techo; cae a 10-15% si delega en IA. |
| T4 Alcance | APTO CON CONDICIONES | 9-18 sesiones el alcance declarado; terminable en ≤1 mes con recorte a 8-11. Tope duro 12 sesiones. Soporte perpetuo ~1-3 h/mes. Migrar a plataforma gestionada costaría MENOS (4-8 sesiones) que cerrar el custom. |

## 2. Contradicciones y resolución

**T4 §5 vs. la ficha — ¿cerrar el custom o migrar y retirar?** T4 demuestra que migrar a una plataforma gestionada es más barato (4-8 sesiones) y cancela el recurrente perpetuo. T1 exige plan de salida documentado. Pero el criterio dominante es aprendizaje: la migración enseña ~nada, mientras que el cierre del custom contiene la única bolsa de aprendizaje valiosa del proyecto (auditoría de seguridad a mano sobre código real en producción — transferible a healthtech, donde seguridad y protección de datos son centrales). **Resolución:** se cierra el custom (idea original), y el plan de salida de T1 se incorpora como entregable del cierre — la migración queda como plan B automático si se agota el tope de sesiones (cláusula de T4).

**Mentira involuntaria en la ficha:** T2 y T4 coinciden, desde frentes distintos, en que la "batería de tests reciente hecha con Claude Code" **no está en el repositorio** (0 ficheros de test; rama `feature/testing-suite` idéntica a main). La ficha se corrige y los tests pasan a ser trabajo pendiente real — con la condición de reapropiación de T3 (escribirlos/entenderlos él).

**Scope creep detectado:** subsistema de registro público añadido a un CMS "de un único usuario" (T2 y T4 coinciden). Se amputa.

## 3. Estrategia óptima reformulada

**"Cierre auditado con seguridad a mano"** — tope duro **12 sesiones** + emergencia previa:

1. **Hoy (no cuenta como sesión):** remediación de la brecha (purga de historial, rotación, valorar notificación).
2. **Sesiones 1-2 — Auditoría propia:** Julius lista a mano qué falta y qué optimizar ANTES de que la IA opine (condición 4 de T3). Congelación escrita del *Future Work*.
3. **Sesiones 3-6 — Seguridad a mano:** ataque real a los 5 vectores (CSRF, subida, SQLi, XSS, CSP), correcciones, credenciales fuera de `docker-compose.yml`/`backup.sh`, CSRF obligatorio en upload. IA solo explica, no ejecuta.
4. **Sesiones 7-9 — Tests reales:** batería phpunit versionada cubriendo login/CSRF, autorización, sanitización, subida. Escrita o reapropiada línea a línea por Julius.
5. **Sesiones 10-12 — Cierre:** PHP 8.3+ en hosting, amputar registro público, backups cron off-site con restore probado, plan de salida documentado para la usuaria (exportación a WordPress.com/Publii), mini-tutorial para la madre. Entregable de comprensión en Obsidian (condición 2 de T3).

Presupuesto reconocido en cartera: ~1-3 h/mes de soporte perpetuo mientras el custom viva (T4).

## 4. Veredicto propuesto

**GO** — con el alcance ya redefinido en la ficha ("finalizar, no construir") y estas condiciones vinculantes consolidadas:

1. Remediación RGPD inmediata e incondicional (T2-1).
2. Tope duro de 12 sesiones con cláusula de migración automática si se agota (T4-1): el contenido se migra a plataforma gestionada y el custom se retira con dignidad.
3. Núcleo a mano: auditoría de seguridad y tests son de Julius; la IA no los ejecuta (T3-1/3/4). Es la única razón por la que este proyecto puntúa algo hacia el pivote.
4. Cero horas justificadas por mercado o "futuros usuarios" (T1-1); amputar registro público (T2-5/T4-2).
5. Corrección de ficha: los tests no existían; el motivo del proyecto es afecto + finalización + aprendizaje de seguridad (T1-2, T4-4).
6. Criterio de "hecho": backups probados + CSP en producción + plan de salida entregado (T4-3, T1-4).

**Decisión de Fase 2b: pendiente de Julius.**
