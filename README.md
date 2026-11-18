# Miseño · App del alumno

Prototipo de la app que usa el alumno en el escenario **Enseñanza Scan 360** (Diseño Interactivo, UTDT, 2026).
Es un tutor de voz para primaria: saluda, pregunta cómo estás, te lleva por las lecciones del día y, antes del recreo,
te muestra qué cambió en tu camino, tu perfil y tu agenda. Nunca explica por qué el sistema decide lo que decide.

## Cómo se usa

Abrir la página en Chrome y tocar **Tocá para empezar**.

- **Teclado:** 1–4 ánimo · Enter listo/seguir · N no entiendo · R repetir · F panel de notas y modo de voz · Shift+R reiniciar.
- **Recorrido:** Lección → Mi camino → Mi perfil → Agenda → Recreo. Cada etapa se desbloquea al terminar la anterior.

## Modos de voz

- **Testing** (por defecto): voz robótica del navegador. No gasta créditos.
- **Voz de ElevenLabs (recomendado):** ElevenLabs lee exactamente el guion de la app con la voz de Miseño. No hay agente que improvise, así que no se pisa ni habla dos veces. En el panel (tecla F) pegar la API key y el Voice ID; quedan guardados solo en ese navegador, nunca en el repo. El chico habla con el micrófono del navegador.
- **Agente conversacional (experimental):** agente de voz de ElevenLabs que conversa siguiendo el guion de cada pantalla.
  Se activa en el panel (tecla F): elegir *Agente conversacional* y tocar *Conectar ahora* (el Agent ID de Miseño ya viene cargado).
  Si no conecta, la app sigue en modo testing.

La configuración del agente y el guion completo están en el doc "Tutor Miseño con IA de voz: configuración y guion".

## Publicar con GitHub Pages

Settings → Pages → *Deploy from a branch* → `main` / `(root)`. La página queda en `https://<usuario>.github.io/<repo>/`.

## Carpetas

- `index.html`: la app completa (un solo archivo, sin servidor).
- `versiones/`: copias de las versiones anteriores (también se pueden abrir online, por ejemplo `/versiones/v0.3/`).
- `feedback/`: para guardar los JSON de notas de los tests (botón "Copiar JSON" del panel).

## Versiones

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
