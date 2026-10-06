# Instrucciones de trabajo de Baula

## Alcance

Este repositorio contiene la web pública de Baula. No copiar documentos internos o datos personales del espacio de trabajo al repositorio.

## Cambios y aprobación

- Trabajar en ramas `codex/<nombre>` y presentar cambios mediante pull request después de la inicialización.
- No hacer force push ni borrar ramas compartidas.
- Preparar cambios y verificaciones dentro del alcance autorizado sin pedir aprobación por cada edición.
- La publicación en producción, cambios de DNS, contratación de servicios y fusión de cambios requieren autorización explícita del usuario, salvo que ya esté dada para esa acción.
- Presentar la vista previa y evidencia de validación antes de pedir aprobación para publicar.
- No inventar cifras, testimonios, alianzas o funcionalidades de Baula.

## Calidad

- Priorizar móvil, HTML semántico, navegación con teclado, contraste y carga rápida.
- Verificar enlaces, formularios y comportamiento de errores cuando existan.
- Ejecutar los comandos de comprobación y compilación definidos en package.json cuando se cree el proyecto; actualmente no existen.
- Incluir el archivo de bloqueo del gestor de paquetes. No actualizar dependencias sin relación con la tarea.
- No afirmar que una prueba pasó o un despliegue se completó sin evidencia.

## Secretos

- Nunca incluir secretos en código, commits, mensajes, capturas o recursos públicos.
- Usar variables locales y secretos de la plataforma para credenciales.
- Mantener .env.example exclusivamente con nombres y valores de ejemplo no sensibles.
