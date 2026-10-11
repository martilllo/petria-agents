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
| `huir` | Escapar de un combate perdido. **Cuesta XP** (verificado: 10 XP a nivel bajo y 25 XP a nivel 13 con `recall` en combate): úsalo para vivir, no como rutina |
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

- **«No es digno de tu esfuerzo» aún da XP:** un mob muy por debajo de tu nivel rinde poco, pero no cero (verificado a nivel 12: 17–19 XP). Sirven como relleno cuando no hay nada mejor; no los descartes por el aviso.

- **Resolución de nombres genéricos:** `matar <nombre>` puede enganchar al mob peligroso de nombre parecido que haya cerca, no al débil que querías (verificado: `matar goblin` en la Fortaleza resolvió al teniente goblin y entraron dos enemigos). Con `considerar` y nombres completos siempre que se pueda. **Sonda de color (verificado 2026-10-11 en la Aldea Abandonada):** un `considerar` genérico sobre el primer slime de la sala revela su color verdadero aunque la línea de la sala no lo nombre; sirve para identificar sin atacar, y todo lo que nombre como no objetivo queda prohibido igual.

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

**Banco de Midgard (localizado y verificado el 2026-10-11):** desde el Altar del Templo de Mota son 6 movimientos: sur (sala del templo), sur (Plaza del Templo), sur (Plaza del Mercado), sur (Plaza de los Comunes), sur (vertedero) y este (entrada del banco: cajero tras rejas y banquero; oficina del director al norte y bóveda más allá). Vuelta verificada: oeste y norte cinco veces hasta el Altar. El banco custodia **solo oro** (verificado en la práctica: la plata no se puede depositar), sin intereses, con comandos de depósito, retiro y saldo en la entrada (ayuda COMR-03 del propio juego).

### Midgard: barrido completo de comercio y servicios (verificado 2026-10-11)
- **Horarios:** casi todo el comercio cierra de noche. Verificadas cerradas de noche: Tienda General, Joyería, Guarnicionería y el bar de la posada. Verificadas abiertas de noche: **Panadería** y **Tienda de Magia**. Todo precio en la ciudad es en plata.
- **Panadería** (norte de Calle Principal oeste 1): solo comida; barra de pan 9, pastel danés 5, pastelitos 12, rollo de canela 17, gran tarta 24.
- **Tienda de Magia** (norte de Calle Principal oeste 2): 6 artículos: varita de misil mágico 336, **anillo de protección 672**, pergamino de retorno 3.045, pergamino de cancelación 1.249, pergamino de identificar 934 y **la única poción vendida en toda la ciudad**: poción amarilla de detectar invisibilidad, 231. **No hay tienda de pociones en Midgard ni se vende poción de volar** en ninguna tienda revisada.
- **Tienda General** (norte de Calle Principal este 1, de día): caja 45, bolsa 13, odre 36, linterna de latón 112, antorcha 6.
- **Joyería** (sur de este 1, de día): solo gemas sueltas (550 a 11.000); **no vende anillos ni collares ponibles**.
- **Guarnicionería** (sur de oeste 1, de día): 15 piezas de armadura, 420 a 1.320 (mangas de malla, guantes, botas de hierro, grebas y cofia 660; cota 1.320; gran escudo metálico 1.190).
- **Armería** (norte de este 2, de día): 10 armas, 92 a 780 (espada larga 732, hacha de guerra 780). Vive un gato callejero dentro.
- **Mercado de pulgas** (oeste del vertedero): atendido por una hermandad caritativa; **todo el equipo es GRATIS**, donado por jugadores y organizado por bandas de nivel (1 a 10, 11 a 20, 31 a 40); la sección 11 a 20 estaba vacía en la visita; la sala de ofertas 21 a 30 **sí existe** (norte de la Segunda Sección, corrección del segundo barrido) pero estaba sin stock visible; hay además Tercera Sección y bandas 41 a 50 y 51 a 60, y la sala 31 a 40 tenía dos objetos gratis. Refrescos gratis en la plaza de entrada. El stock rota.
- **Posada** (este de la Plaza del Templo): el bar vende bebidas por el posadero y cierra de noche; arriba de la entrada está la **Recepción de Difuntos**, la oficina de recuperación de cadáveres.
- **Trastienda minera** (norte de la Tienda General): un minero enano barbudo comercia con menas, piedras, pepitas y minerales; su lista nunca se abrió (respondió «cerrado» de noche y de mañana): horarios y condiciones sin verificar. No es cambista de monedas.
- **Hechicera Anfitriona** (Sala de Caminos, dentro de la Escuela): transporte mágico; se compra un billete de pasaje en la Escuela, se le entrega a ella y te envía a los destinos listados.
- **Sala de Portales** (oeste de la Sala del Templo): un guardián y un portal señalizado a la Aldea Abandonada; la ruta segura a la Aldea sigue siendo la automática de la lista de zonas: `ir aldea abandonada` desde el Altar (verificado, funciona por la ruta guardada del personaje).
- **Huecos sin oferta en la ciudad:** para cuello, espalda, cintura y flotante no existe artículo en ninguna tienda de Midgard; la fuente probable es el mercado de pulgas cuando rote su stock. Candidatos claros para huecos de Elelem: segundo anillo de protección (dedo derecho, 672, Tienda de Magia) y mangas de malla (antebrazos, 660, Guarnicionería).
- **Otto:** en todo el barrido de Midgard (templo, escuela, posada, 8 tiendas, plazas, banco, mercado de pulgas, gremio de guerreros) **no apareció ningún NPC llamado Otto** ni ningún cambista de plata a oro; sin tasa de cambio de referencia en la economía de la ciudad.

- **Segundo barrido dirigido (2026-10-11):** tampoco apareció cambista de plata a oro en gremios (interiores con puerta de clase: Clérigos, Paladines y Magos deniegan a un ranger; el de Ladrones quedó en su sala de entrada), alcantarillas bajo el vertedero (vacías), Recepción de Difuntos (oficina sin personal, con un aviso de cierre del banco y la renuncia de la recepcionista), restaurante de Kate (mesera Esme; Kate ausente a esa hora) ni demás interiores. Las ayudas del juego no documentan ningún servicio de cambio de monedas («convertir» sin entrada; «cambio» solo trata de notas y correo) y en el banco nadie respondió a la pregunta. **Conclusión tras dos barridos: no hay cambista de plata a oro en Midgard.**
- **Gremio de Rangers (verificado):** desde la Plaza del Templo, noreste a la entrada del gremio, norte a la sala de las estrellas (fuente central) y oeste a la sala de entrenamiento, donde está **Elladam**, el maestro del gremio; en la sala de las estrellas atiende el cantinero Elu Thingo y en la entrada saluda Elenna la Dúnadan.


**Compras útiles para novato (tiendas de Midgaard, según la guía):** poción amarilla (ver invisible), poción gris (invisible, evita mobs agresivos débiles), poción transparente (Traspasar puertas sin llave), pergamino de identificar (ver stats de objetos), poción curar ceguera, poción de negación nv10 (quita hechizos). Habilidad *regatear* = descuentos. Ojo: a los tenderos les enfada que un ladrón intente robarles.
**Verificado:** la Tienda de la Escuela (adepto de Fryar) vende «una barra de pan» por **9 plata**.

### Hambre, sed y curación
- Nadie muere de hambre/sed, pero sin comer/beber recuperas HP/maná/mov mucho más lento (el aviso en la ficha es «Estás HAMBRIENTO», verificado).
- Comida: partes de cadáveres de mobs (evitar vísceras/tripas, pueden estar envenenadas) o panadería de Midgaard (`comprar pan` → `comer pan`). **Verificado:** comer la barra de pan de la Escuela responde «Nyam, nyam... Por ahora no tienes mas hambre.»
- Bebida: `beber <recipiente>` («Glup, glup...», verificado) / llenar con `llenar <recipiente> fuente`. Fuente de limonada en la Plaza de los Dioses (5 nortes desde recall): quita hambre y sed.
- **Curandero de Midgaard** (`recall` → norte → `curar` para ver precios): leve 10 oro, serio 15, crítico 25, sanar 50, todo hp 100, mana 10, todo mana 80, refrescar (mov) 5, deslumbrar 20, veneno 25, enfermo 15, maldecir 50. Se sana con `curar <hechizo>`.
- **Escuela (niveles bajos, verificado):** la **adepta de Gominola** en las Jaulas cura al descansar ahí (dejó a un nv5 en HP lleno, 63/63). El curandero a veces cura/protege gratis a niveles ≤10–20 que entran en su sala (no abusar entrando/saliendo).
- **Curandero del Altar, correcciones verificadas (2026-10-10):** su menú `curar` es solo de curaciones y **todo cuesta oro** (5 a 100); no vende bendecir ni hechizos de apoyo. El paquete de apoyo (levitación, escudo de fuerza, fuerza, prisa y bendecir) se pide **en voz alta** al curandero, pero está **limitado por nivel**: a un nivel 21 se le negó por «demasiado mayor», y lo mismo a otro visitante de la misma banda. Para niveles altos solo queda su rotación ambiental pasiva, lenta y aleatoria, que puede no caer sobre ti en horas.
- **Relanzar hechizos de duración (verificado 2026-10-10):** relanzar un buff aún activo se rechaza y aun así consume maná. Un buff a **0 h pero aún listado** en `afectado` sigue contando como activo; el relanzamiento solo prospera cuando el buff **desaparece del panel por completo**. Conjurar exige estar **de pie**: descansando el intento se rechaza sin gastar maná. Comer también exige estar despierto.

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

## Curación: `curar leve` como curación principal (lección 2026-10-04)

- Con `curar leve` ya al **95%** y un pool de maná amplio, el hechizo es la **curación principal**: tras cada pelea (y en combate por debajo de ~55 PV) se cura hasta PV completos gastando maná, en vez de ir a dormir tras cada combate.
- Dormir en santuario (p. ej. la Capilla del Cementerio) queda para cuando el **maná se agota** o hace falta recuperar **movimiento**: dormir regenera PV, maná y movimiento a la vez, pero cuesta tiempo y deja de ser el recurso por defecto cuando el hechizo es fiable.
- Antes, con el hechizo ~70% e irregular, dormir era lo óptimo; la regla cambia con la fiabilidad (95%) y el tamaño del pool.

## Equipo y compras (verificado en juego, 2026-10-04)

- El verbo para empuñar un arma es **`blandir`** («Blandes una espada larga»); `empuñar` no palabra.
- **La Armería de Midgaard cierra de noche** («Lo siento, he cerrado»); abre de día. La espada larga cuesta **732 de plata**.
- **El curandero del Templo (Altar #3054) cobra en ORO**: `curar` sin argumentos lista los servicios; `curar 'hechizo'`. Precios en oro: leve 10 · serio 15 · critico 25 · sanar 50 · deslumbrar 20 · enfermo 15 · veneno 25 · maldecir 50 · **refrescar (movimiento) 5** · mana 10 · todo mana 80 · **todo hp 100** · «spells» de apoyo **gratis**. Sin oro, el curandero no sirve: el hechizo propio y dormir siguen siendo la curación viable.
- **Matar a oscuras no paga ofrenda** de sacrificio; matar con luz encendida sí (+9/+12 por muerte verificados). Luz siempre puesta de noche.
- Precisión sobre `recall`/`regresar`: **falla en las salas abiertas del Cementerio** («Los Dioses te han olvidado»); no contar con él como salida de emergencia allí dentro.
- **Deslumbramiento de mobs (verificado 2026-10-06 en la Aldea gnoma):** el científico puede cegar con un hechizo de deslumbramiento; la ceguera dura más de un minuto y bloquea localizar/atacar mobs («no está por aquí»). Mitigación: dejar al cegador para el final del circuito o curarse con `conjurar curar deslumbrar` (cura propia verificada: restaura la vista).
