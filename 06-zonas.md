# Petria MUD — Áreas por nivel y rutas

> Parte del conocimiento general de Petria para agentes. Índice completo en el [README](README.md).

## 8. Áreas por nivel y rutas desde `recall` (web de mapas)

Paths en formato `.direcciones` desde el punto de `recall`. Peligro ☠︎︎ = bajo, más calaveras = más riesgo.

| Niveles | Área | Path desde recall |
|---|---|---|
| Todos | Midgaard (ciudad inicio) | — |
| 1–5 | Escuela del Mud | `.u` |
| 1–5 | Guardería Enana | `.u,e` |
| 1–5 | Yad | `.u,w,d` |
| 1–20 | Llanuras del norte | `.2s,3e,4n,2w,3n` |
| 5–10 | Bosque de Haon Dor | `.2s,5w` |
| 5–10 | Bosque de Miden'nir | `.2s,3e,8s,2w,2s` |
| 5–10 | Cementerio | `.2s,3e,7s,w,s` |
| 5–15 | Moria | `.2s,6e,3n` |
| 5–15 | Fábrica de Mobs | `.2s,3w,3s,e` |
| 5–20 | Aldea gnoma | `.2s,8e,s` |
| 5–20 | Valle de los Elfos | `.2s,3e,4n,2w,3n,2e,n,e,n` |
| 5–20 | Arenas del Desierto | `.2s,5e` |
| 5–20 | Torre Wyvern | `.2s,6e,4s,2e,s,2e,d,e` |
| 5–25 | Ruinas de Thalos | `.2s,6e,4s,3w` |
| 5–30 | Las Alcantarillas | `.4s,d` |
| 8–10 | Academia de Escuderos | `.u,2o` |
| 10–20 | Fortaleza Goblin | `.6s,2e,3s,2w,7s,2e,5s` |
| 10–25 | Reino Enano | `.2s,6e,3n,e` |
| 15–25 | La Capilla | `.2s,3e,7s,w,6s` |
| 25–50 | El Infierno* | `.4s,d,w,d,w,n,3d,s,w,d,w` |

\* **Infierno (desde nv25):** los dos guardianes de la entrada son autoataque, desarman y pegan a quien tenga menos nivel. Truco de la guía: guarda las armas antes de pasarlos y **huye rápido** a las salas siguientes. De las mejores zonas de leveleo 25+.

> La tabla completa (85+ áreas hasta nivel 111) está en https://www.petriamud.com/mapas/ — consultar ahí antes de explorar una zona nueva.

## Aldea gnoma a nivel 9 (verificado en juego, 2026-10-04)

- Entrada: desde el Templo, el path con `.2s,8e,s` **grita** en el cliente (no hace speedwalk); caminar a mano: 2S (Plaza del Templo → Plaza del Mercado), `abrir este` en la puerta, E a #4926, S a Entrada #1501.
- XP por mob (singles, nivel 9): **científico Gnomo 87** (en Una Tienda Gnoma; el mejor), **guardia Gnomo 60** (single en Una Pequeña Cabaña), **hombre Gnomo 34–49** variable.
- NO atacables (👁 protegidos): mujer Gnoma, niño Gnomo, archivista, alquimista, tabernero. El **jefe Gnomo** se ríe de `considerar` (demasiado fuerte: evitar). En la Fortaleza hay **2 guardias juntos** (grupo: no). El Portón de Vapor este: «Solo se permite el ingreso a gnomos» (bloqueado).
- ⚠️ El hambre/sed en estado avanzado **quitan 20 PV por tick**: comer/beber a la primera señal. `recall` al Templo cuesta ~49 de movimiento.
- El Cementerio a nivel 9 cae a 19 XP por mob: la Aldea gnoma es el relevo correcto para 9–10.
- **La XP de una zona decae con tu nivel:** el mismo mob paga cada vez menos conforme subes (científico Gnomo verificado: 87 XP a nivel 9 → 42–67 a nivel 11 → 13–19 a nivel 12). En la práctica cada zona rinde unos 2–3 niveles y luego toca cambiar, aunque siga siendo «segura».

## Llanuras del Norte a nivel 13 (verificado en juego, 2026-10-06)

- Ruta de entrada desde `recall`: `.2s,3e,4n,2w,3n`; la fauna de entrada (loba sola) paga **0 XP a nivel 13**. Zona no útil para levear a este nivel; la Aldea gnoma (13–19 XP/baja a nivel 13) sigue rindiendo más.
