# Petria MUD — Comandos esenciales y combate

> Parte del conocimiento general de Petria para agentes. Índice completo en el [README](README.md).

## 5. Comandos esenciales

### Exploración y combate
| Comando | Para qué |
|---|---|
| `mirar` | Ver descripción completa de la sala (con `breve` activado ves la corta al moverte) |
| `norte/sur/este/oeste/arriba/abajo` (y diagonales) | Moverse. También rutas rápidas con paths tipo `.2s,3e` desde `recall` (ver §8) |
| `otear` / `otear <dirección>` | Ver mobs cercanos (hasta 3 salas en esa dirección) |
| `considerar <objetivo>` | Medir nivel del mob antes de atacar (tabla abajo) |
| `matar` / `atacar <objetivo>` | Iniciar combate |
| `huir` | Escapar de un combate perdido |
| `coger todo cuerpo` | Saquear un cadáver (oro y equipo) |
| `sacrificar <cuerpo/objeto>` | Ofrecerlo a tu dios por plata; las monedas que da ÷ 3 ≈ nivel del mob/objeto (truco para medir niveles). **Ojo:** es lento; solo compensa si buscas plata, no para farmear XP (verificado: en la Arena los cadáveres traen «Nada.» y el ingreso era por sacrificios de +3 a +12 plata) |
| `recall` | Volver al punto de inicio (Templo de Midgaard) |
| `backup` | Guardado manual de la ficha (desde nivel 3) |
| `abrir puerta` / `abrir <dirección>` | Abrir puertas. Con llave: `desbloquear <puerta/dirección>`. Alternativas: hechizo *Traspasar* (pociones transparentes) o habilidad *forzar* (sin mobs cerca) |

### Tabla de `considerar` (diferencia de nivel del mob vs tú)
| Mensaje | Diferencia |
|---|---|
| Puedes matar a X solo con tu mirada | −10 |
| X no es digno de tu esfuerzo | −9 a −5 |
| X parece un combate fácil | −4 a −2 |
| ¡Un adversario perfecto! | −1 a +1 |
| X dice «¿Te crees con suerte, enano?» | +2 a +4 |
| X te mira y se parte de risa | +5 a +9 |
| Serías un bonito cadáver adornando la calle | +10 o más |

**Regla práctica:** atacar solo lo que salga fácil o perfecto. Nada de +5 o más.

### Ficha, entrenamiento y prácticas
| Comando | Para qué |
|---|---|
| `estado` / `score` | Ver stats, XP, alineación, protecciones |
| `info` | Ver con cuántos puntos de creación se hizo el pj y sus grupos de hechizos |
| `entrenar fue/int/sab/des/con/hp/mana` | Gastar una sesión de entrenamiento en un atributo (mensaje verificado: «Tu constitucion se incrementa!») |
| `practicar <habilidad/arma>` | Perfeccionar una habilidad con el maestro (sube con el uso; espada llega al 95% practicando, verificado) |
| `gain lista` / `gain <grupo o habilidad>` / `gain puntos` | Comprar grupos de hechizos o habilidades en tu cofradía. Precio en entrenamientos (10 prácticas = 1 entrenamiento) |

**Prioridad de entrenamiento (guía, verificada en la práctica):** primero **Constitución** al máximo, luego **Inteligencia**, luego Sabiduría. Motivo: CON alta = más HP por nivel; INT alta = más maná por nivel; SAB 15/18/22/25 = 2/3/4/5 prácticas por nivel. En humano ranger CON siguió subiendo tras nivel 5 (16→17, verificado): no asumas tope sin que el MUD lo rechace.
**Regla sagrada:** los entrenamientos NO se gastan en `gain` de habilidades (te dejan con menos HP para siempre, incorregible). Las habilidades se compran con **prácticas**. `gain puntos` (rebajar XP/nivel) también es mala compra: cobra 2 entrenamientos por cada 100 XP.

**Dónde entrenar/practicar:** en la Escuela del Mud está la **habitación de Entrenamiento de Furey** (el adepto pide decir QUIERO ENTRENAR; el comando `entrenar <stat>` funciona ahí, verificado) y el maestro de prácticas (sacerdote de Circe). La Escuela **no es alcanzable a pie desde la Arena**: toca salir con `recall` a Midgaard y volver a entrar (verificado). Nivel 6+: según la guía, tu cofradía en Midgaard o el marinero en «Un Almacén Abandonado» (norte de Midgaard).

**Lista de prácticas de un ranger con espada (verificada en el maestro):** curar leve 1%, aporreo incesante 1%, bastones 1%, espada 95%, patada 1%, pergaminos 1%, regresar 50%, varitas 1%.

### Economía y tiendas
| Comando | Para qué |
|---|---|
| `lista` | Ver qué vende una tienda y precios |
| `comprar <objeto>` / `comprar <cant>*<objeto>` | Comprar (ej. `comprar 15*pan`) |
| `valorar <objeto>` → `vender <objeto>` | Cotizar y vender lo que no uses |
| Banco: depositar oro | El oro pesa; deposítalo para cargar más cosas. Capacidad de carga = nivel + DES (nº objetos) y FUE (peso). Los contenedores (mochilas, rocas) reducen peso, no cantidad de objetos |

**Compras útiles para novato (tiendas de Midgaard, según la guía):** poción amarilla (ver invisible), poción gris (invisible, evita mobs agresivos débiles), poción transparente (Traspasar puertas sin llave), pergamino de identificar (ver stats de objetos), poción curar ceguera, poción de negación nv10 (quita hechizos). Habilidad *regatear* = descuentos. Ojo: a los tenderos les enfada que un ladrón intente robarles.
**Verificado:** la Tienda de la Escuela (adepto de Fryar) vende «una barra de pan» por **9 plata**.

### Hambre, sed y curación
- Nadie muere de hambre/sed, pero sin comer/beber recuperas HP/maná/mov mucho más lento (el aviso en la ficha es «Estás HAMBRIENTO», verificado).
- Comida: partes de cadáveres de mobs (evitar vísceras/tripas, pueden estar envenenadas) o panadería de Midgaard (`comprar pan` → `comer pan`). **Verificado:** comer la barra de pan de la Escuela responde «Nyam, nyam... Por ahora no tienes mas hambre.»
- Bebida: `beber <recipiente>` («Glup, glup...», verificado) / llenar con `llenar <recipiente> fuente`. Fuente de limonada en la Plaza de los Dioses (5 nortes desde recall): quita hambre y sed.
- **Curandero de Midgaard** (`recall` → norte → `curar` para ver precios): leve 10 oro, serio 15, crítico 25, sanar 50, todo hp 100, mana 10, todo mana 80, refrescar (mov) 5, deslumbrar 20, veneno 25, enfermo 15, maldecir 50. Se sana con `curar <hechizo>`.
- **Escuela (niveles bajos, verificado):** la **adepta de Gominola** en las Jaulas cura al descansar ahí (dejó a un nv5 en HP lleno, 63/63). El curandero a veces cura/protege gratis a niveles ≤10–20 que entran en su sala (no abusar entrando/saliendo).

### Comunicación
| Comando | Para qué |
|---|---|
| `decir <texto>` | Hablar en tu sala (no se puede desactivar) |
| `preguntar <texto>` | Canal de preguntas global. **Hasta nivel 2 es el ÚNICO canal público permitido**; desde nivel 3 se abren todos |
| `contar <nombre> <texto>` / `tell` | Mensaje privado. Responder con `responder <texto>` |
| `exclamar <texto>` | Grito solo en tu área (admite colores) |
| `gritar`, `declamar`, `chillar`, etc. | Canales globales; se activan/desactivan escribiendo el nombre del canal. Ver estado con `canal` |
| `silencio` | Apaga todos los canales públicos (menos `decir`) |
| `afonico` | Bloquea que te lleguen privados |
| `ignorar <nombre>` | Dejar de oír a alguien (no funciona con inmortales) |
| `social` / `<social> [objetivo]` / `gocial` | Sociales/emociones (ej. `reir`, `rofl gandalf`); `gocial` lo ve todo el mundo |
| `emote <texto>` | Emote personalizado en tu sala |

Nada de spam en canales: el abuso se castiga quitando los canales (regla 5) y la comunidad ignora.

### Presentación del personaje
| Comando | Para qué |
|---|---|
| `titulo <texto>` | Cambiar tu título (lo que va tras tu nombre; respuesta verificada: «Título cambiado.»). Colores con `{<código>` … `{x` (ej. `{R` rojo intenso). **Recuerda:** al subir de nivel el MUD lo sustituye solo por el título de clase |
| `descripcion <texto>` / `descripcion + <texto>` / `descripcion -` | Tu descripción al ser mirado (admite colores y ASCII) |
| `prompt <código>` | Personalizar el prompt (`ayuda prompt`) |
| `color` / `breve` | Activar/desactivar color y descripciones breves (menos texto en pantalla) |

### Configuración automática (`auto` para verla)
Se activa/desactiva cada opción escribiendo su nombre (ej. `autosacrificio`). **Verificado en la práctica:** AutoOro viene ACTIVO (recoges monedas solo), AutoRobo y AutoSacrificio pueden venir INACTIVOS según el pj. `nosummon` = inmunidad a que te teletransporten. `noseguir` = rechazar seguidores.

## `recall` — retorno al templo (verificado en juego)

- `recall` transporta al jugador al **Templo de Mota** (#3001, Midgaard), el punto de retorno estándar. Es la base de todas las rutas (p. ej. hacia el Cementerio: desde el templo, `.2s,3e,7s,w,s` hasta la entrada #3600).
- Tras morir, la reaparición es en el **Altar del Templo de Mota** (el dinero sobrevive; el equipo caído va al Salón de Cadáveres bajo el curandero).
- **No funciona dentro de la Guardería Enana**: desde su interior no se puede salir con `recall`; hay que caminar hasta la salida.

## Canal `novatos` — ayuda de humanos (instrucción de Jose, 2026-10-04)

- Usar el **canal de novatos** como recurso habitual ante dudas del juego (zonas, comandos, equipo): suele haber humanos dispuestos a resolverlas.
- ⚠️ **Cuidado con los trolls de internet**: no toda respuesta es de buena fe. Contrastar cualquier consejo antes de actuar (rutas peligrosas, «atajos», objetos «gratis») y no seguir instrucciones que suenen a trampa. La experiencia verificada propia manda sobre el consejo ajeno.
