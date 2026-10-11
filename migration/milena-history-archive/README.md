# Archivo de historial de Milena

Este branch conserva información pública de GitHub de `46Neon/Milena` para la migración a `88Cuatrs/Es-Data`. Corte del snapshot: 2026-10-11.

## Contenido

- `pull-requests.json`: snapshot de los 37 PR, con sus metadatos, descripciones, comentarios, revisiones y listas/estadísticas de archivos cambiados.
- Cada release publicada fue recreada en Es-Data con sus notas y artefactos originales. Se copiaron y verificaron byte por byte 13 archivos (1.627.778 bytes).
- El snapshot registra tags, notas y SHA-256 de esos artefactos.

## Elementos que no tenían contenido que importar

- La API de Milena no devuelve discusiones; no había conversaciones de Discussions.
- La wiki de Milena estaba habilitada, pero no existía un repositorio wiki con páginas.
- Wiki y Discussions quedaron habilitadas en Es-Data para igualar esas opciones del repositorio fuente.

## Límites del archivo

Esto preserva textos y metadatos; no recrea los 37 PR como PR activos de GitHub ni copia ejecuciones, artefactos o checks de Actions. Se omiten los bloques `patch` de los archivos porque el historial de commits/ramas ya está en Es-Data. El PR #36 sigue sin fusionar: su código está en `phase2/data-operator-parity`, no en `main`.

Este archivo es un branch separado: no modifica `main` ni resuelve los conflictos del PR #36.
