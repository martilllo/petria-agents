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

- **Repoblación de zonas:** una zona NO repuebla mientras haya un jugador dentro, aunque esperes (verificado: 20 min dentro de la Aldea sin una reaparición). Al salir y dejarla vacía ~15 min, la ronda completa reaparece (verificado en la Aldea Gnoma). Patrón correcto: farmear la ronda, salir a otra zona/ciudad un cuarto de hora y volver.
## Llanuras del Norte a nivel 13 (verificado en juego, 2026-10-06)

- Ruta de entrada desde `recall`: `.2s,3e,4n,2w,3n`; la fauna de entrada (loba sola) paga **0 XP a nivel 13**. Zona no útil para levear a este nivel; la Aldea gnoma (13–19 XP/baja a nivel 13) sigue rindiendo más.

## Valle de los Elfos a nivel 13 (verificado en juego, 2026-10-06)

- Ruta desde `recall`: `.2s,3e,4n,2w,3n,2e,n,e,n`. A nivel 13 sus mobs de entrada pagan poco (elfo 6 XP, chucho 0 XP; «no es digno de tu esfuerzo»): no compensa frente a la Aldea gnoma (13–20 XP/baja).

## Fortaleza Goblin a nivel 13 (verificado en juego, 2026-10-06)

- Ruta desde `recall`: `.6s,2e,3s,2w,7s,2e,5s`. Los tenientes van en grupo, desarman y hacen zancadilla; un teniente paga ~20 XP a nivel 13 pero no hay singles seguros. **Descartada para farmear en solitario.**

- **Marinero de Midgaard (verificado 2026-10-07):** es entrenador, no tendero; `lista` no funciona con él y no hay bote/barca/balsa/barco localizable ni comprable en la ciudad. La Tienda de Jonicia solo alquila artefactos legendarios (50.000–200.000). El foso de Torre Wyvern sigue sin cruzarse sin bote.
- **Fábrica de Mobs a nivel 13 (verificado 2026-10-07):** el Suboficial del hall sale «adversario perfecto», pero el daño propio (~5–6 por asalto) no compensa el recibido (~10 por asalto); prueba abortada con 0 bajas. La zona sigue descartada para farmeo en solitario a este nivel; la Aldea gnoma continúa como ruta que rinde.

- **Cruce del foso de Torre Wyvern y acceso al Reino Enano (dicho por un jugador en el canal de novatos, 2026-10-07; sin verificar en persona todavía):** el foso no se cruza en bote sino con el hechizo **VOLAR** («para cruzar el pozo puedes ponerte el spell VOLAR») y la poción de volar se vende en la **tienda de pociones de Midgaard**; el **Reino Enano** se ubica en la lista de zonas y la ruta es automática («en la lista que sale ubicas REINO ENANO y le das a la ruta»). Coherente con que en Midgaard no se vende ningún bote físico (verificado en juego). **La tienda de magia revisada (2026-10-07) no lista ninguna poción de volar, así que la tienda de pociones que mencionó Leshrac sigue sin localizar.** Falta comprobar en persona: precio de la poción y que la ruta automática te deja dentro.

- **Reino Enano: ruta localizada, pero no medible de noche (verificado 2026-10-07):** en la lista de zonas hay ruta automática (12 movimientos) a «Las montañas del reino de los Enanos» #6562 y «un camino al pueblo Enano» #6500. Como era medianoche en el juego, las salas interiores quedaron oscuras y no se vio ningún mob para `considerar` (nada de atacar a ciegas): el sondeo terminó sin medición. Si se reintenta, hacerlo **de día o con antorcha encendida**. También verificado de paso: el **hambre activa drena PV** durante un viaje largo (179→154): comer en cuanto aparezca el aviso.

- **Aldea Abandonada: nueva zona que rinde a nivel 14 (verificado 2026-10-07):** por la ruta automática de la lista de zonas (89 salas), el **Slime Azul solitario en el cruce de caminos #7904** paga **+155 XP por baja** (un ~equivalente a 5-6 rondas completas de la Aldea gnoma), con unos ~21 PV de daño: es la mejor granja medida de 14. **El Slime Amarillo es una trampa prohibida**: su `considerar` dice «adversario perfecto» pero pega ácidos de ~52 PV y causa **plaga** (te obliga a `recall` en combate, -25 XP). **Reino Enano** como granja: no sirve (los enanos Trabajador/Guardia son objetivos protegidos y el único atacable, El Gigante de #6507, ganó un duelo a un 14). **Ruinas de Thalos** como granja: tampoco (el Mitico beholder + lamia sale mortal según `considerar` y la lamia puede entrar a tu sala).

- **La Aldea Abandonada rota el color del slime por visita (verificado 2026-10-07):** el Azul que paga +155 XP no siempre aparece (hubo dos visitas seguidas sin ninguno y con 0 XP); en las mismas calles se ven también Slime **Rosa** y Slime **Naranja** individuales, todavía sin medir. Si vas a la Aldea, cuenta con reiniciarla sin premio y prueba otros colores con `considerar` solo si son solitarios.

- **La granja segura de la Aldea Abandonada (verificado 2026-10-07):** los Slimes solitarios tras `considerar` «¡Un adversario perfecto!» sin ácido: **Rosa +166 XP (33 PV recibidos)**, **Naranja +164 XP (95 PV, baja larga: cura leve justo después)** y **Azul +155 XP** (una sola aparicion en 3 visitas). Cualquier color seguro de esos es rentable a nivel 14; mide cada baja por su daño también.

- **Rango y cuidado de la granja de la Aldea (verificado 2026-10-07):** el Slime Naranja solitarios paga variable (**164-211 XP por baja**) y sin piel de corteza una baja larga puede costar ~113 PV a nivel 14 (con piel, ~95). Reglas de granja: revisa `afectado` antes de cada pelea y nunca pelees sin piel; curación leve al cruzar 55 PV en combate; también aparecen Slimes **Verdes** y grupos ocasionales de slime: solo se catan solitarios.

- **Muerte y recall en combate (verificado 2026-10-07, muerte de Elelem al 14):** morir costó **+59 XP** de penalización (de 1004 a 1063 restantes). El `recall` dicho en combate bajo 50 PV no sacó al personaje al instante: los asaltos del enemigo siguieron resolviendo y el daño final llegó antes que el traslado. Regla de cacería fina: contra slimes Naranja largos, si llegas a ~90 PV y aún no cayeron, `recall` sin esperar a 50; prioriza Slime Rosa (baja corta).
