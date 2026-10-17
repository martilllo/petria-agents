# Petria MUD — Juego y conexión

> Parte del conocimiento general de Petria para agentes. Índice completo en el [README](README.md).

## 1. Qué es Petria

- MUD (Multi-User Dungeon) español clásico, RPG 100% texto estilo D&D.
- Creas un personaje, subes de nivel matando mobs (NPCs controlados por el servidor), exploras áreas, haces quests, te equipas, comercias y, a nivel alto, puedes entrar a clanes PK (player-killing).
- A nivel 111 existe la opción de **renacer** en raza/profesión más potente (pensado para PK).
- Comunidad activa en Discord y WhatsApp de ayuda a nuevos.
- Sitio oficial: https://www.petriamud.com
- Guía de principiantes (fuente principal de teoría): https://www.petriamud.com/wp-content/uploads/2024/08/guia_principiantes_v2.html
- Mapas y rutas: https://www.petriamud.com/mapas/
- **Inventarios oficiales del sitio web (orden de Andrés, 2026-10-09):** la web oficial de Petria también publica inventarios (listados de objetos/equipo) y hay que usarlos como fuente para decidir equipo por nivel antes de comprar o farmear equipo en el juego.
- Reglas: https://www.petriamud.com/reglas/

## 2. Cómo conectarse

| Vía | Datos |
|---|---|
| Servidor MUD | `game.petriamud.com` puerto `6600` |
| Cliente web | https://game.petriamud.com/ — Lociterm, se conecta por WebSocket `wss://game.petriamud.com/` y de ahí al MUD |
| Cliente recomendado por la comunidad | Mudlet (gratis) apuntando al mismo host/puerto |

### Flujo de entrada en el cliente web (verificado 2026-10-02)
1. Splash «Petria – Vive tu Leyenda / ✦ Comienza tu Aventura ✦» → clic o tecla para empezar; el cliente conecta solo.
2. Banner con castillo ASCII + `PETRIA` en letras grandes, web/Discord/host-puerto.
3. Pregunta: «Por que nombre quieres ser conocido? / What name would you like to use?»
4. Si el nombre es nuevo: «Nuevo personaje.» → pide password y confirmación.
5. Si el nombre ya existe: pide el password de ese personaje. Nunca probar variantes si falla: reportar el mensaje exacto.

### Cliente alternativo probado: MudForge (verificado 2026-10-17)
- MudForge (mudforge.org, cliente en play.mudvault.org) SÍ conecta a Petria escribiendo «game.petriamud.com 6600», vía su puente WebSocket a Telnet, y acepta el servidor arbitrario sin registro.
- Su transcripción en juego es más fiel que la de Lociterm: cada comando devuelve su salida completa, en orden, cerrada por prompt y sin mezclar salidas ni tragarse líneas, y el tráfico ambiental llega entre prompts, nunca dentro de un bloque. Hay que esperar al prompt y no fiarse de la primera captura tras Enter, porque equipo, mirar y backup aparecieron completos solo al reobservar.
- Ventajas para un agente: el widget de mapa GMCP expone en el DOM el nombre y número de sala (El Altar del Templo, #3054, Midgaard) y el widget de estado expone nombre, nivel y valores exactos de PV, maná y movimiento; además trae disparadores, alias, temporizadores, macros y plugins Lua.
- Riesgos verificados: el arranque es frágil, porque dos conexiones se cortaron exactamente a los 10 segundos en la pantalla de nombre y solo funcionó enviando el nombre sin demora (no hay campos de entrada automática); la terminal es un lienzo xterm.js y su texto no está en el DOM, así que un agente lee por capturas (el modo lector de pantalla anunciado quedó sin verificar); varios diálogos interrumpen el flujo al inicio y la exportación de la transcripción no quedó verificada.
