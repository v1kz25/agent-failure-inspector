# agent-failure-inspector

> Estado: planificación inicial. **Aún no hay MVP implementado**.

Analizador local y privado de fallos en ejecuciones de agentes de programación.

## Objetivo

Comparar ejecuciones de agentes, agrupar errores y localizar el punto de divergencia con trazas procesadas localmente.

## Stack provisional

Go + SQLite + TypeScript (interfaz web local sólo si el spike lo valida). La versión concreta y la idoneidad se validarán en el primer spike técnico.

## MVP previsto

- importar traces locales de Codex y Claude Code con formatos verificados
- normalizar eventos esenciales y errores sin perder fuente raw
- comparar dos ejecuciones y localizar divergencias
- exportar diagnósticos locales con redacción de secretos

### Fuera del MVP

- visor universal de todos los agentes
- interceptar TLS
- cloud y telemetría
- LLM/API comerciales
- replay que ejecute acciones

## Desarrollo

- Ver [roadmap](docs/ROADMAP.md), [guía de desarrollo](docs/DEVELOPMENT.md) y [AGENTS.md](AGENTS.md).
- El punto de entrada son los GitHub Issues, no implementar el MVP de golpe.
- Desarrollo principalmente desde Windows 11; sin infraestructura de pago.

## Riesgos

Formatos internos inestables, alta sensibilidad de logs, falsos diagnósticos y mantenimiento de adaptadores.

## Referencias

- https://github.com/camtrik/agent-trail
- https://github.com/Atituiset/agent-viewer
- https://github.com/openai/codex/blob/main/codex-rs/rollout-trace/README.md

## Licencia

**Pendiente de decisión.** Este repositorio se publica sin archivo LICENSE por ahora. Ser público en GitHub no otorga automáticamente permiso para copiar, modificar o redistribuir su contenido.
