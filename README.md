<img width="1600" height="900" alt="image" src="https://github.com/user-attachments/assets/ab537617-4b3e-45ab-8f29-0bf2d55d18cb" />


> [!IMPORTANT]
> **Este Hackathon ha concluido.** Se recibieron 18 proyectos. Gracias a todos los que buildearon con nosotros. Conocé a los [ganadores](#ganadores) y [todos los proyectos](#lista-completa-de-proyectos) más abajo.

# [ ARKIV ] × PunaTech — Hackathon

Nos sumamos a [PunaTech](https://www.punatech.ar/) con nuestra propia track. Cuatro premios — $600, $450, $300 y $150 USDC — para los mejores proyectos.

---

## Ganadores

Cuatro proyectos premiados, evaluados por el equipo de [ ARKIV ] contra el [rubric publicado](docs/scoring-rubric.md).

### 🥇 Susurro — $600 USDC

Un coach de bienestar con voz cuya memoria vive cifrada en Arkiv y es del usuario, no de la plataforma. El cifrado AES-256-GCM ocurre en el navegador con la firma de la wallet, y el acceso al coach se vence solo vía `expiresIn` nativo de Arkiv — la expiración *es* el control de acceso, sin cron ni background jobs.

[GitHub](https://github.com/artugrande/susurro) · [Demo](https://susurro-nine.vercel.app/) · [Video](https://youtu.be/7JWos7N7RuA)

### 🥈 Licita Verify — $450 USDC

Una bitácora inalterable y consultable de cada licitación pública, anclada en Arkiv. Registra cada hito desde la convocatoria hasta la adjudicación, con consultas en lenguaje natural vía IA y un bot de Telegram autónomo conectado por MCP.

[GitHub](https://github.com/hallzyx/licita-verify) · [Demo](https://licita-verify.arroz.dev) · [Video](https://youtu.be/HaGdi7J3W64)

### 🥉 NotarIA — $300 USDC

Un escribano digital para decisiones médicas con IA. Asegura la inalterabilidad de prompts e historiales con hashes criptográficos en Arkiv —sin subir PII— y transfiere la propiedad soberana del registro a la wallet del médico vía `changeOwnership`.

[GitHub](https://github.com/ignaw05/notaria-arkiv) · [Demo](https://notaria-arkiv.vercel.app) · [Video](https://youtu.be/fHvbg9qbpq8)

### 4° Mediation Rooms — $150 USDC

Una capa plug-and-play que agrega una ventana temporal de reclamo antes de ejecutar acciones críticas. Las partes suben evidencia y abren disputas; Arkiv guarda los datos con expiración programada (48h para reclamos, 90 días para evidencia) mientras el sistema externo solo consulta si puede ejecutar o debe bloquear la acción.

[GitHub](https://github.com/TheMrMatt/mediation-rooms) · [Demo](https://mediation-rooms.vercel.app/) · [Video](https://www.loom.com/share/51f8bdde84ae421bb47ff75d4f42e024)

---

## Track: Aplicaciones de IA sobre [ ARKIV ]

Construí aplicaciones de IA que usen [ ARKIV ] como capa de datos. Tres verticales para orientarte (aunque no son las únicas):

- **Memoria de IA que es tuya** — memoria de agentes, historial de chat portable, contexto a prueba de manipulación que sobrevive entre apps.
- **Procedencia y auditoría de IA** — registros consultables y a prueba de manipulación de lo que un modelo dijo o hizo (útil para periodismo, compliance, debate).
- **Capas de datos personales para IA** — perfiles y preferencias propiedad del usuario que cualquier app de IA puede leer con permiso explícito.

¿Tu idea no encaja exacto en estas tres? Si combina IA con [ ARKIV ] como capa de datos, queremos verla.

Para más info, revisá la **[Guía para builders](docs/builders-guide.md)**.

---

## Qué ganás

**Lo obvio:**

- **4 premios** — $600 USDC (1°), $450 USDC (2°), $300 USDC (3°), $150 USDC (4°).

**Lo menos obvio:**

- Vas a shipear un producto sobre una tecnología que la mayoría de los desarrolladores todavía no tocó.
- El código es open source. Las mejores entregas se convierten en referencia para otros builders que construyan sobre [ ARKIV ].
- Soporte del equipo de [ ARKIV ] durante todo el build. Unite al [Discord](https://discord.gg/arkiv)

---

## Para quién es esto

- Desarrolladores que puedan construir una aplicación web full-stack
- Solo o en equipo (máx. 5 integrantes) — el premio es por equipo
- Cualquier stack en el frontend. [ ARKIV ] es la capa de datos — vos elegís el resto
- No necesitás conocer [ ARKIV ] de antemano. Las guías y documentación te llevan hasta donde necesitás llegar

---

## Cronograma

| Fecha                                            | Qué pasa                                         |
| :----------------------------------------------- | :----------------------------------------------- |
| **28 de mayo de 2026**                           | Abre el Hackathon / Kickoff de la track          |
| **30 de mayo de 2026, 2:00 PM (hora Argentina)** | **Cierre de entregas** ← esta es la fecha límite |
| **30 de mayo de 2026, 4:00 PM (hora Argentina)** | Anuncio de ganadores                             |

*Arkiv se reserva el derecho de ajustar estas fechas. Cualquier cambio se comunicará por Discord y canales oficiales. Ver [RULES.md](RULES.md) para los TyCs.*

---

## Cómo entregar

Antes del **sábado 30 de mayo a las 2:00 PM (hora Argentina)**, completá los cuatro entregables:

1. **Repo público en GitHub** con todos los integrantes del equipo como colaboradores
2. **Video público** (YouTube o Google Drive) mostrando el proyecto funcionando
3. **Llená el form** en [https://forms.arkiv.network/punatech26](https://forms.arkiv.network/punatech26)
4. **Pitch en español** (puede ser el video o una presentación por separado)
5. **Demo funcional** desplegada y accesible por URL, conectada a la testnet de [ ARKIV ]

> ⚠️ **Importante:** los ganadores deberán completar un proceso de KYC (verificación de identidad) antes de recibir el premio. Esto implica enviar documentación de identidad.

---

## Links rápidos

| Qué | Dónde |
| :---- | :---- |
| **Guía para builders** | [docs/builders-guide.md](docs/builders-guide.md) — track, requisitos, cómo arrancar |
| **Reglas oficiales** | [RULES.md](RULES.md) — términos, premios, elegibilidad |
| **Rubric de evaluación** | [docs/scoring-rubric.md](docs/scoring-rubric.md) — cómo puntuamos, qué buscamos |
| **FAQ** | [FAQ.md](FAQ.md) — preguntas frecuentes |
| **Agent Skill** | [docs/agent-skill.md](docs/agent-skill.md) — instalá `arkiv-best-practices` para que tu asistente de IA conozca el SDK |

### Empezá a construir

| Qué | Dónde |
| :---- | :---- |
| **Docs de Arkiv** | [docs.arkiv.network](https://docs.arkiv.network) |
| **TypeScript SDK** | [Getting started](https://docs.arkiv.network/start-here/fundamentals/) |
| **Data Explorer** | [data.arkiv.network](https://data.arkiv.network/) — inspeccioná tus entidades y probá queries en el navegador ([docs](https://docs.arkiv.network/start-here/data-explorer/)). En Beta. |

### Entregá y conseguí ayuda

| Qué                       | Dónde                                                                            |
| :------------------------ | :------------------------------------------------------------------------------- |
| **Formulario de entrega** | [https://forms.arkiv.network/punatech26](https://forms.arkiv.network/punatech26) |
| **Discord**               | [Uníte al servidor](https://discord.gg/arkiv)                                    |

---

## Lista Completa de Proyectos

18 proyectos shipearon sobre [ ARKIV ]. Ganadores marcados con ★.

| Proyecto | Código | Demo |
| :------- | :----- | :--- |
| ★ **Susurro** | [GitHub](https://github.com/artugrande/susurro) | [Demo](https://susurro-nine.vercel.app/) |
| ★ **Licita Verify** | [GitHub](https://github.com/hallzyx/licita-verify) | [Demo](https://licita-verify.arroz.dev) |
| ★ **NotarIA** | [GitHub](https://github.com/ignaw05/notaria-arkiv) | [Demo](https://notaria-arkiv.vercel.app) |
| ★ **Mediation Rooms** | [GitHub](https://github.com/TheMrMatt/mediation-rooms) | [Demo](https://mediation-rooms.vercel.app/) |
| AeroTrack Sentinel | [GitHub](https://github.com/gabriel-alejandropereagarcia/aerotrack-sentinel) | [Demo](https://aerotrack-sentinel.vercel.app/) |
| Arkiv Notes | [GitHub](https://github.com/melyteo/arkiv-notes-mvp) | [Demo](https://arkiv-notes-mvp.vercel.app/) |
| ArkivLog | [GitHub](https://github.com/ivantaddei/arkivlog) | [Demo](https://demo-iota-mocha-51.vercel.app/) |
| Climate Crisis Dashboard | [GitHub](https://github.com/Marceloalvarez12/climate-crisis-dashboard) | [Demo](https://climate-crisis-dashboard.vercel.app/) |
| FerIA Salta | [GitHub](https://github.com/Apunados-punatechteam/ferIA-Salta) | [Demo](https://test.saltia.com.ar/) |
| InforMed | [GitHub](https://github.com/Jehp23/InforMed) | [Demo](https://infor-med.vercel.app/) |
| ManoLocal | [GitHub](https://github.com/santiemanuel/manolocal) | [Demo](https://manolocal.code-hello.com/) |
| MemoryForge AI | [GitHub](https://github.com/blastonyz/arkiv-punatech) | [Demo](https://arkiv-punatech.vercel.app/) |
| Norte Vivo | [GitHub](https://github.com/facutech3-design/nortevivo) | — |
| PAWSI AI | [GitHub](https://github.com/MaritoSAS/pawsi-ai) | — |
| TruthStamp | [GitHub](https://github.com/laupro10-ctrl/TruthStamp-Hookia) | [Demo](https://truthstamp.netlify.app/) |
| VendorPass | [GitHub](https://github.com/pgallar/vendor-pass) | — |
| ViArkiv | [GitHub](https://github.com/Antony27c/Arikiv) | [Demo](https://arikiv-production.up.railway.app/) |
| vialibre | [GitHub](https://github.com/veneciaedith/vialibre1) | [Demo](https://vialibre.vercel.app/) |

