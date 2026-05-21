# [ ARKIV ] × PunaTech 2026 — Preguntas frecuentes

---

### General

**¿Qué es el Hackathon de [ ARKIV ] en PunaTech 2026?**
Una invitación a crear aplicaciones usando [ ARKIV ] como capa de datos, en el marco del Ideathon + Hackathon de PunaTech 2026 en Salta, del 28 al 30 de mayo. Los 4 mejores proyectos reciben premios por un total de $1.500 USD.

**¿Quién puede participar?**
Cualquier persona mayor de 18 años. Solo o en equipo (máximo 5 integrantes).

**¿Necesito conocer [ ARKIV ] de antemano?**
No. Los materiales y la documentación están pensados para que arranques desde cero. El canal de soporte en Discord está activo durante toda la ventana de construcción.

**¿Dónde están las reglas?**
En este repositorio — ver [RULES.md](RULES.md).

**¿Puedo usar herramientas de IA (Copilot, Claude, ChatGPT)?**
Sí. Nos importa el resultado, no cómo llegaste ahí.

**¿Puedo usar código existente, librerías o boilerplate?**
Sí para librerías, frameworks y boilerplate. La integración con [ ARKIV ] y la lógica central de la aplicación tienen que ser trabajo original creado durante el hackathon.

---

### Temática

**¿Cuál es la temática?**

**Aplicaciones de IA sobre [ ARKIV ]** — Construí aplicaciones de IA que usen [ ARKIV ] como capa de datos. Algunos ejemplos orientativos:

- **Memoria de IA que es tuya** — datos de contexto de agentes almacenados en [ ARKIV ], con expiración, que sólo vos controlás.
- **Procedencia y auditoría de IA** — rastros de decisiones y outputs de modelos, a prueba de manipulación.
- **Capas de datos personales para IA** — perfiles y preferencias del usuario almacenados en [ ARKIV ] en lugar de en servidores centralizados.

Estas son referencias, no categorías cerradas. Descripciones completas en la [Guía para participantes](docs/builders-guide.md).

**¿Tengo que elegir uno de los ejemplos?**
No es obligatorio encuadrarte en un ejemplo específico. Tu proyecto tiene que estar dentro de la temática general "Aplicaciones de IA sobre [ ARKIV ]". Indicá tu enfoque en el formulario de envío.

**¿La temática que elija afecta mi puntuación?**
No. Todos los proyectos se evalúan con el mismo criterio.

**¿Varios equipos pueden trabajar sobre el mismo enfoque?**
Sí. No hay límite por enfoque.

---

### Equipos y envíos

**¿Puedo participar en equipo?**
Sí. El límite es 5 integrantes. Hay un solo premio por equipo ganador; cómo lo repartís entre ustedes es decisión de ustedes.

**¿Puedo enviar más de un proyecto?**
No. Un envío por persona o equipo. Si enviás varias veces, sólo cuenta el último.

**¿Puedo actualizar mi envío después de haberlo enviado?**
Sí — hasta el cierre. Después del **sábado 30 de mayo a las 4:00 PM (hora Argentina)**, los envíos son definitivos.

**¿Qué tengo que incluir en mi envío?**
- Repositorio público en GitHub (todos los integrantes del equipo como colaboradores)
- Video público de demostración
- Formulario completado en `https://forms.arkiv.network/punatech26`
- Pitch en español

Detalles completos en [RULES.md](RULES.md).

---

### Construcción

**¿Dónde encuentro los requisitos de la temática?**
La [Guía para participantes](docs/builders-guide.md) tiene ideas concretas, sugerencias de diseño de entidades y orientación sobre fechas de expiración de datos.

**¿Puedo usar cualquier stack tecnológico?**
Sí. [ ARKIV ] es la capa de datos — elegí lo que quieras para el frontend, el estilo, la conexión de wallets y el hosting.

**¿Necesito un smart contract?**
No es obligatorio. Podés hacer un proyecto completamente funcional usando sólo el SDK de [ ARKIV ].

**¿En qué red corre esto?**
Testnet de [ ARKIV ] — **Arkiv Testnet**:

| | |
|---|---|
| **Network ID** | `60138453102` |
| **HTTP RPC** | `https://braga.hoodi.arkiv.network/rpc` |
| **WebSocket RPC** | `wss://braga.hoodi.arkiv.network/rpc/ws` |
| **Faucet** | Próximamente — chequeá Discord para novedades |

Usá `@arkiv-network/sdk@0.6.8`.

**¿Hay algún skill de agente que conozca [ ARKIV ]?**
Sí — `arkiv-best-practices`. Instalalo en tu asistente de código con IA y tu agente deja de inventarse llamadas al SDK. Instrucciones de configuración en [docs/agent-skill.md](docs/agent-skill.md).

**¿Dónde pido ayuda si me trabo?**
En el **canal de soporte dedicado (próximamente)** del [Discord de Arkiv](https://discord.gg/arkiv). El equipo de [ ARKIV ] está disponible todos los días durante la ventana de construcción.

---

### Premios

**¿Qué premio recibo si gano?**
Los 4 mejores proyectos reciben: **$600 USD (1°), $450 USD (2°), $300 USD (3°), $150 USD (4°)**.

**¿Necesito completar KYC para participar?**
No para inscribirte ni competir. Sin embargo, **el KYC es obligatorio para cobrar el premio**. Si ganás y no completás el KYC en el plazo indicado, el premio puede pasar al siguiente clasificado. Tené esto en cuenta antes de participar — no hay excepciones.

**¿Qué pasa si gano pero no puedo completar el KYC?**
El premio puede transferirse al siguiente clasificado. Tenés 3 días para completar el KYC desde que te notificamos.

**¿Qué KYC se requiere?**
Todos los integrantes del equipo tienen que completar el KYC individualmente. Necesitás: un documento de identidad emitido por el gobierno, un formulario de declaración firmado (se entrega a los ganadores tras la notificación — imprimilo y firmalo a mano), y una selfie con tu documento. Detalles completos en [RULES Sección 7](RULES.md#7-kyc--prize-disbursement).

---

### Evaluación

**¿Cómo se puntúan los proyectos?**
Cuatro criterios con pesos publicados — mismo criterio para todos:

| Criterio | Peso |
|----------|------|
| Profundidad de integración con [ ARKIV ] | 40% |
| Funcionalidad | 30% |
| Diseño y UX | 20% |
| Calidad del código y documentación | 10% |

Ver la [Rúbrica de evaluación](docs/scoring-rubric.md) para los sub-criterios detallados.

---

### Reglas

**¿Dónde están las reglas completas?**
[Reglas y términos oficiales](RULES.md)

**¿De quién es el código que escribo?**
Tuyo. Al participar, le otorgás a [ ARKIV ] una licencia no exclusiva para mostrar tu proyecto. Podés hacer lo que quieras con tu propio código.

**¿Qué licencia necesito usar?**
Open source — MIT, Apache 2.0 o equivalente.

---

*¿No encontrás tu pregunta? Unite a nuestro [Discord](https://discord.gg/arkiv) y preguntá en el **canal de soporte dedicado (próximamente)**.*
