# Preparación del entorno de Baula

## Estado verificado el 6 de octubre de 2026

- GitHub: DennisRojass/baulaapp.github.io, público. Conector disponible.
- Carpeta original: contiene documentos internos y archivos temporales; no es una web.
- Git y Node disponibles dentro de Codex. npm y gh no están en PATH.
- Cloudflare, dominio exacto, formularios y despliegue: pendientes.

## Instalar en orden

1. Node.js LTS para Windows, con npm: https://nodejs.org/en/download . Mantener npm y la opción de PATH del instalador.
2. Git for Windows si `git --version` no funciona en PowerShell externo: https://git-scm.com/downloads/win . El Git incluido en Codex no confirma instalación global.
3. GitHub CLI, recomendado para clonar y autenticar Git: https://cli.github.com/ . El conector de Codex y la autenticación local de Git son independientes.
4. Reiniciar Codex y abrir una terminal nueva. Verificar `node --version`, `npm.cmd --version`, `git --version`, `gh --version`.
5. Ejecutar `gh auth login`, elegir GitHub.com, HTTPS y acceso por navegador. Después `gh auth setup-git` y `gh auth status`. No pegar tokens en el chat.
6. Clonar el repositorio en una carpeta nueva y abrir esa carpeta como proyecto de Codex. No ejecutar `git init` dentro de un clon.
7. Cuando se cree el sitio, instalar sus dependencias y Wrangler como dependencia de desarrollo del proyecto. No hace falta instalar Astro ni Wrangler globalmente.

En Windows, usar npm.cmd si PowerShell bloquea npm.ps1. No cambiar políticas de ejecución globales para resolverlo.

## Espacio de trabajo

Mantener la carpeta actual como documentación interna. Usar un clon separado para la web, por ejemplo `Baula-web`, junto a `Baulaapp`. Los archivos públicos y las reglas vivirán en el clon. Si el clon está en otra carpeta, abrirlo como proyecto para que Codex trabaje allí.

## Configuración de GitHub pendiente de aplicar

En Settings > General: usar squash merge como método preferido y activar eliminación automática de ramas tras fusionar.

En Settings > Rules > Rulesets (o Branches): proteger main, exigir pull request, bloquear force push y eliminación. Si trabaja una sola persona, no exigir una aprobación de otro revisor inexistente. La aprobación del dueño se registra en el proceso antes de fusionar. Añadir comprobaciones obligatorias cuando exista CI y sus nombres estén verificados; no exigir checks inexistentes.

La protección no queda activada por escribir estas reglas en AGENTS.md. Este documento no confirma cambios de administración.

En la cuenta: habilitar autenticación de dos factores y guardar códigos de recuperación de forma privada. Conceder a las integraciones solo acceso necesario. No agregar licencia abierta sin decisión del propietario.

## Conceptos

- Commit: versión guardada de un cambio.
- Rama: línea de trabajo separada.
- Pull request: propuesta de cambio para revisión.
- main: versión aprobada.
- CI: comprobaciones automáticas.
- Vista previa: sitio para revisar cambios.
- Producción: sitio que visitan los usuarios.

## Cloudflare

Conectar el repositorio después de preparar la primera versión y definir vistas previas y producción. Obtener dominio exacto y verificar registros existentes antes de editar DNS, especialmente correo. No configurar publicación automática desde main hasta acordar el procedimiento de aprobación.

## Herramientas

GitHub conectado; navegador para revisión; skills de Figma y herramientas de imagen solo si hacen falta. Un MCP de Cloudflare no es requisito para construir. No hace falta API de OpenAI para una landing sin funciones de IA.

## Pendiente para construir

Dominio, descripción de Baula, público objetivo, acción principal del visitante, logo, colores, contenido público, destino del formulario y presupuesto.

## Referencias

- https://nodejs.org/en/download
- https://cli.github.com/
- https://docs.github.com/en/repositories/configuring-branches-and-merges-in-your-repository/managing-protected-branches/about-protected-branches
- https://developers.cloudflare.com/workers/static-assets/
