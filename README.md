# Miseño · App del alumno

Prototipo de la app que usa el alumno en el escenario **Enseñanza Scan 360** (Diseño Interactivo, UTDT, 2026).
Joaquín (11) pasa una mañana con Miseño, su tutor principal, que lo deriva con un profe por materia: 22 momentos,
solo hacia adelante, con una línea de tiempo del día a la izquierda y la interfaz cambiando de tono en cada clase.
La voz es solo guionada: dice exactamente el texto de cada momento.

Definición completa (recorrido, componentes, identidad, guion): https://claude.ai/artifact/6tipJiz2sJz1bDrqohDWve

## Cómo se usa

Abrir la página en Chrome y tocar **Empezar**.

- **Teclado:** Enter acción principal · N no entiendo · R repetir · F panel de prueba · Shift+R reiniciar.
- **Panel de prueba (F):** notas del observador, saltar a un momento, voz (ElevenLabs, navegador o sin voz),
  lectura de los sensores y copiar el registro.
- La voz de ElevenLabs no suena dentro del link de claude.ai: usar GitHub Pages o el archivo local.

## Versiones

- **v1.0:** rediseño completo desde el doc de definición. Línea de tiempo del día, tonos pastel por momento, Miseño y profes (figuras provisorias), lecciones en 4 momentos (explorar, explicar, descubrir, mostrame), voz solo guionada.
- **v0.5.3:** guardada en `versiones/v0.5.3/`.
- **v0.5.2:** la app se llama Miseño (antes Scan). Nuevo modo de voz recomendado: ElevenLabs lee exactamente el guion de la app (sin agente conversacional), con API key y Voice ID en el panel F. Cada frase se paga una sola vez.
- **v0.5.1:** voz real más confiable: se ocultan las etiquetas de entonación, los toques llegan a Miseño como [UI], cola y reintento de mensajes.
- **v0.5:** lecciones interactivas, sin multiple choice: Explorar → Descubrir → Practicar → Mostrame, con widgets (cortar y pintar fracciones, buscar pistas en el cuento, armar frases con "porque", simulador del pasto). Selector de interés en el panel F. "Miseño anotó cómo resolviste esto" al cerrar cada bloque.
- **v0.4.5:** compatible con el plan gratis de ElevenLabs (sin sobrescribir el primer mensaje).
- **v0.4.4:** también prueba por WebSocket; botón "Diagnosticar conexión" en el panel F.
- **v0.4.3:** si ElevenLabs rechaza el guion de la app, usa el del panel del agente.
- **v0.4.1:** el tutor de IA se llama Miseño.
- **v0.4:** modo real con IA de voz (ElevenLabs) y modo testing.
- **v0.3:** recorrido guiado y secuencial; Agenda y chat del recreo.
- **v0.2:** bloques de Lengua y Ciencias; Mi camino, Mi perfil y Avisos.
- **v0.1:** check-in, plan del día y bloque de Matemática con "No entiendo".

## v1.1 (18/11/2026)
- Personajes con 5 estados (reposo, habla, piensa, festeja, anima): Guio (tutor), Numi (Matemática), Otto (Lengua), Fini (Ciencias). Imágenes optimizadas en `img/` (originales en `Personajes/`).
- Apertura con logo y nombre; el pájaro vuela al lugar de Guio.
- Todo entra y sale con animación; transición entre pantallas; relevo cuando arranca cada materia.
- Al final de cada clase, pregunta metacognitiva en vez de resultados (dificultad, gusto, seguridad para explicarlo). Las respuestas se usan en "Lo que cambió hoy".
- Para GitHub Pages hay que subir también la carpeta `img/`.
