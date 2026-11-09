---
title: "Lección 12 - Publicar el sitio con GitHub Pages"
description: "Usa la aplicación GitHub Copilot para configurar un flujo de trabajo de Pages, revisar su solicitud de incorporación de cambios y comprobar el Space Quiz publicado."
authors:
  - jamesmontemagno
lastUpdated: 2026-10-12
---

Publica Space Quiz en GitHub Pages para que cualquiera pueda acceder a él. Copilot puede preparar el flujo de trabajo y guiarte durante la publicación, pero eres responsable de revisar los cambios y confirmar que el sitio está disponible.

En esta lección:

- pedirás a Copilot que configure una implementación con GitHub Pages.
- revisarás el flujo de trabajo y la solicitud de incorporación de cambios antes de combinarla.
- seguirás la implementación y comprobarás el sitio publicado.

## Escenario

Space Quiz ya está en un repositorio de GitHub, pero todavía hace falta una forma sencilla de probarlo. Publicar el sitio de un solo archivo con GitHub Pages permite acceder a él desde una URL pública sin añadir un servidor ni dependencias de ejecución.

## Pide a Copilot que publique el sitio

En la sesión de la aplicación Copilot para `space-quiz`, envía este prompt:

```plaintext
Habilita GitHub Pages para este repositorio. Crea un flujo de trabajo de GitHub Actions que compile el sitio web si es necesario y lo publique en GitHub Pages. Añade un README que describa la aplicación y cómo ejecutarla en local si aún no existe. Crea una solicitud de incorporación de cambios con estos cambios y combínala cuando se superen las comprobaciones obligatorias. Supervisa la implementación hasta que se complete correctamente y, después, indica la URL final del sitio web publicado. Si no tienes permiso para habilitar Pages o combinar la solicitud, dime exactamente qué debo aprobar o hacer; no indiques que se ha completado correctamente hasta que el sitio esté publicado.
```

![Diagrama de tres fases: una solicitud de incorporación de cambios de space-quiz combinada; una ejecución correcta de Deploy website en GitHub Actions con los pasos Build website, Upload artifact y Deploy to Pages; y Space Quiz publicado en yourname.github.io/space-quiz/.](../../../_images/first-steps-app-pages-deploy.svg)

> [!WARNING]
> Este prompt pide al agente que cree y combine una solicitud de incorporación de cambios y cambie la configuración de Pages del repositorio. Antes de continuar, revisa las diferencias, los permisos de implementación y cualquier solicitud de aprobación de GitHub.

## Revisa el flujo de trabajo y comprueba la implementación

1. Confirma que el README solo se ha añadido si el repositorio aún no tenía uno.
2. Revisa los cambios de la solicitud de incorporación de cambios, incluidos los pasos de compilación e implementación del flujo de trabajo.
3. Combina los cambios únicamente cuando se superen las comprobaciones obligatorias de la solicitud.
4. Sigue la ejecución de implementación de GitHub Actions hasta que se complete correctamente.
5. Abre la URL indicada y confirma que se carga Space Quiz.

Si el agente no puede habilitar Pages o combinar la solicitud de incorporación de cambios, sigue las instrucciones concretas que te proporcione. No des la tarea por terminada hasta que la implementación se complete correctamente y el sitio publicado se cargue.

## Resumen y próximos pasos

Space Quiz ya está publicado como sitio web y has comprobado la implementación en lugar de depender del informe del agente. Continúa con la [lección 13: Repaso y próximos pasos][next-lesson].

[next-lesson]: ../13-review/
