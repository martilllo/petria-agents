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
