# Petria MUD — Creación de personaje y conceptos base

> Parte del conocimiento general de Petria para agentes. Índice completo en el [README](README.md).

## 3. Creación de personaje (flujo verificado)

Orden exacto de preguntas al crear (2026-10-02):

1. Nombre → 2. Idioma `[1] Español` → 3. Confirmar nombre (Sí) → 4. Password + repetir → 5. Modo accesible lector de pantalla (No) → 6. Raza (lista numerada) → 7. Sexo (M/F) → 8. Clase (lista numerada) → 9. Alineación (B/N/M) → 10. ¿Personalizar? (S/N) → 11. Arma inicial.

### Razas (8) y clases (9 en la lista actual)
- **Razas:** Humano, Elfo, Enano, Gigante, Hobbit, Gnomo, Drow, Orco.
- **Clases ofrecidas al crear:** Mago, Clérigo, Ladrón, Guerrero, Paladín, Ranger, Asesino, Brujo, Druida.
- La guía advierte: mago/clérigo/brujo son difíciles para empezar. **Recomendadas para principiante: Paladín o Ranger** (autosuficientes, equilibrio ataque/defensa). Humano es la raza más polivalente y sin debilidades específicas.
- **Personalización:** si eres nuevo, responder **No**. Personalizar mal sube el costo de XP por nivel. Regla de la guía: nunca pasar de 50–60 puntos de creación (cada punto ≈ +100 XP/nivel; pasado 60 cobra el doble).
- **Arma inicial recomendada por clase:** guerrero/ranger → espada · clérigo → maza · mago/ladrón → daga. En un humano ranger solo se ofreció espada (verificado).

## 4. Conceptos base

- **Mob:** todo ser controlado por el servidor (fidos, guardias, el dios Probador, etc.). Se sube de nivel matándolos.
- **HP / Maná / Mov:** vida, energía mágica para conjuros (ver costo con `hechizos`) y puntos de movimiento. Con Mov en 0 no puedes caminar ni esquivar bien. Montaña cansa más que ciudad; `volar` ahorra movimiento.
- **Recuperarse:** `descansar` (más lento) o `dormir` (más rápido), curandero, o habilidades *rápida curación* (HP) y *meditación* (maná). No estar afectado por `acelerar` al curarse.
- **Prompt:** línea siempre visible con tus valores, ej. `<20/20hp 100/100m 100/100mv 2100xp>`. Personalizable con `prompt` (ver `ayuda prompt`).
- **Tu ficha:** `estado` o `score`. **Tus conjuros/habilidades:** `hechizos` / habilidades según la guía; lo que te afecta y su duración se consulta en la misma ficha.
- **Hitroll:** probabilidad de acertar golpes físicos (se compara contra la armadura/AC del rival). **Damroll:** daño extra por golpe acertado. Mantener ambos lo más alto posible.
- **Alineación:** de angelical (+1000) a satánico (−1000) según a quién mates. Afecta qué equipo puedes usar (flags anti-good/anti-evil → «zap» si no cumples) y hechizos como *rayo de sinceridad/corrupción*. Se detecta con *detectar bondad/maldad* (aura dorada = bueno, roja = malo, sin aura = neutral).
- **Experiencia máxima por mob:** 250 XP. Influye la diferencia de nivel y la alineación (misma moral = menos XP).
- **Guardar el personaje:** un pj nuevo **no se guarda hasta nivel 3** (verificado). Desde ahí se guarda solo; aun así `backup` manual da el mensaje «Perfecto, has hecho un BACKUP de tu ficha» (verificado).
- **Subida de nivel (verificado):** mensaje «¡¡¡ HAS SUBIDO UN NIVEL !!!» + ganancias de HP/maná/mov y **+1 práctica** por nivel. Al subir, el título visible pasa automáticamente al **título de clase** (ej. ranger → «El Acechador»): hay que reaplicar el título personal con `titulo` tras cada subida.
- **Morir:** no pierdes nivel ni equipo; pierdes 2/3 de la XP ganada desde el último nivel. Tu cadáver va a la Cámara de Cadáveres (laberinto bajando desde el curandero); recógelo pronto o se pudre y cualquiera podrá saquearlo. Hasta nivel 5, si abandonaste sin recoger: `equipmin` te da luz, escudo y arma básicos.
