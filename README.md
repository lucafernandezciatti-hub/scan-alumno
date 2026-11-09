# Scan · App del alumno

Prototipo de la app que usa el alumno en el escenario **Enseñanza Scan 360** (Diseño Interactivo, UTDT, 2026).
Es un tutor de voz para primaria: saluda, pregunta cómo estás, te lleva por las lecciones del día y, antes del recreo,
te muestra qué cambió en tu camino, tu perfil y tu agenda. Nunca explica por qué el sistema decide lo que decide.

## Cómo se usa

Abrir la página en Chrome y tocar **Tocá para empezar**.

- **Teclado:** 1–4 ánimo · 1–3 responder · N no entiendo · R repetir · F panel de notas y modo de voz · Shift+R reiniciar.
- **Recorrido:** Lección → Mi camino → Mi perfil → Agenda → Recreo. Cada etapa se desbloquea al terminar la anterior.

## Modos de voz

- **Testing** (por defecto): voz robótica del navegador. No gasta créditos.
- **Real:** agente de voz de ElevenLabs que conversa siguiendo el guion de cada pantalla.
  Se activa en el panel (tecla F): elegir *Real* y tocar *Conectar ahora* (el Agent ID de Miseño ya viene cargado).
  Si no conecta, la app sigue en modo testing.

La configuración del agente y el guion completo están en el doc "Tutor Scan con IA de voz: configuración y guion".

## Publicar con GitHub Pages

Settings → Pages → *Deploy from a branch* → `main` / `(root)`. La página queda en `https://<usuario>.github.io/<repo>/`.

## Carpetas

- `index.html`: la app completa (un solo archivo, sin servidor).
- `versiones/`: copias de las versiones anteriores (también se pueden abrir online, por ejemplo `/versiones/v0.3/`).
- `feedback/`: para guardar los JSON de notas de los tests (botón "Copiar JSON" del panel).

## Versiones

- **v0.4.4:** también prueba por WebSocket; botón "Diagnosticar conexión" en el panel F.
- **v0.4.3:** si ElevenLabs rechaza el guion de la app, usa el del panel del agente.
- **v0.4.1:** el tutor de IA se llama Miseño.
- **v0.4:** modo real con IA de voz (ElevenLabs) y modo testing.
- **v0.3:** recorrido guiado y secuencial; Agenda y chat del recreo.
- **v0.2:** bloques de Lengua y Ciencias; Mi camino, Mi perfil y Avisos.
- **v0.1:** check-in, plan del día y bloque de Matemática con "No entiendo".
