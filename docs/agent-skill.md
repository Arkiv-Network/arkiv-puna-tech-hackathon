# Skill de agente — [ ARKIV ] × Puna Tech Hackathon

Acelerá el desarrollo instalando el skill oficial de [ ARKIV ] en tu asistente de código con IA. Le da a tu agente conocimiento instantáneo del SDK, las mejores prácticas y los patrones de integración más comunes — especialmente útil en una ventana de construcción corta.

## ¿Qué es un skill?

Un **skill** es un conjunto de instrucciones y conocimiento de dominio que instalás en tu agente de código con IA (Claude Code, Cursor, GitHub Copilot, Cline, Windsurf, etc.). Una vez instalado, el agente puede consultarlo automáticamente cada vez que le preguntás sobre el tema relevante — sin necesidad de copiar y pegar documentación en el chat.

## El skill de [ ARKIV ]

[ ARKIV ] publica un skill oficial llamado **arkiv-best-practices**. Le enseña a tu agente:

- Cómo funciona el SDK de [ ARKIV ] (clientes, queries, mutations, eventos)
- Mejores prácticas (atributos de proyecto, seguridad, modelado de datos, manejo de errores)
- Patrones de integración (backend, React, wagmi)
- Errores frecuentes y cómo evitarlos

Instalalo en tu proyecto:

```bash
npx skills add https://github.com/arkiv-network/skills --skill arkiv-best-practices
```

**Tip:** El skill está publicado en [skills.sh/arkiv-network/skills/arkiv-best-practices](https://skills.sh/arkiv-network/skills/arkiv-best-practices).

## Qué podés probar

Una vez instalado, abrí tu agente de IA y probá prompts como:

- *"Build a feature that lets users create and list posts stored on Arkiv"*
- *"Audit my project — am I following Arkiv best practices?"*
- *"Set up a React hook that reads Arkiv entities with TanStack Query"*

---

## Reportar bugs y sugerir funcionalidades

[ ARKIV ] también publica un skill llamado **arkiv-feedback**. Te guía a través de un formulario interactivo de reporte de bugs o solicitud de funcionalidades, y envía el resultado directamente al repositorio público [`Arkiv-Network/reported-issues`](https://github.com/Arkiv-Network/reported-issues) en GitHub.

Instalalo junto con `arkiv-best-practices`:

```bash
npx skills add https://github.com/arkiv-network/skills --skill arkiv-feedback
```

Una vez instalado, invocalo en tu agente de IA:

```
/arkiv-feedback
```

El skill te pide los detalles relevantes (qué esperabas, qué pasó, pasos para reproducirlo, versión del SDK), y luego abre o crea el issue en tu nombre. El equipo de [ ARKIV ] monitorea el repositorio durante toda la ventana de construcción.
