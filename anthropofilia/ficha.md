# Ficha — Anthropofilia

**Fase:** 1 completada — pendiente decisión de Julius (2b)
**Actualizada:** 2026-07-17 (tras tribunal; ficha original de Fase 0 corregida con lo aprendido)

## Problema
La madre de Julius necesita gestionar contenido web sin depender de un desarrollador ni de un CMS pesado.

## Usuario objetivo
Un único usuario real (su madre). Producción viva en `anthropofilia.es`.

## Propuesta de valor (una frase)
Finalizar el miniCMS a medida (PHP + JS + HTML + CSS) como cierre auditado: seguridad verificada a mano, tests reales, backups probados y plan de salida documentado para la usuaria.

## Motivo real (corregido por el tribunal)
Utilidad afectiva + finalización + aprendizaje de seguridad web. NO es una necesidad funcional insatisfecha (WordPress.com/Publii/Google Sites la cubren gratis, verificado 2026-07-17) ni un proyecto de mercado. Prohibido justificar horas con argumentos de mercado.

## Relación con el pivote healthtech
No temáticamente. Alineamiento ~40% como techo condicional: solo la auditoría de seguridad web hecha A MANO transfiere (~70% de esa bolsa) a healthtech; si se delega en IA, cae a 10-15%.

## Estado real (verificado 2026-07-17, clon de `JDiaz-healthTech/Anthropofilia`)
- ~21.9k LOC, 98 commits, 47 días sin actividad. Base de seguridad del código sólida (PDO preparado, HTMLPurifier, subida blindada, bcrypt + CSRF + CSP).
- **Corrección de ficha:** la "batería de tests reciente hecha con Claude Code" NO existe en el repo (0 tests; rama `feature/testing-suite` idéntica a main).
- **Brecha RGPD activa:** volcados de BD de producción con PII real (email, hash, IPs, mensajes) en el repo público y su historial — remediar hoy.
- PHP 8.0 en Dockerfile (EOL nov-2023); migrar a 8.3+. Scope creep: registro público añadido, incoherente con un solo usuario — amputar.

## Veredicto del orquestador (propuesto, pendiente 2b)
**GO** — cierre auditado con tope duro de 12 sesiones y cláusula de migración automática a plataforma gestionada si se agota. Remediación RGPD inmediata incondicional. Auditoría de seguridad y tests a mano (núcleo de aprendizaje). Detalle en `orquestador.md`; dictámenes íntegros en `tribunal.md`.

## Acción inmediata (independiente de la decisión)
Purgar historial del repo (o hacerlo privado), rotar contraseña de la usuaria y credenciales de BD, valorar notificación art. 33/34 RGPD.
