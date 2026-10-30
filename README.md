# Aula Lista · Edukole

Demo estática sin cuentas, servicios de IA ni claves API. Los recursos de marca y el CSS de Tailwind están en `assets/` y se sirven localmente.

## Abrir

Abre `D:\Startup\MVP` en VS Code y elige **Open with Live Server** sobre `index.html`. Abre la dirección y el puerto que muestre VS Code. Mantén un solo servidor en ese puerto.

Para publicar, conserva `index.html`, `app.js`, `styles.css` y la carpeta `assets/` juntos en cualquier alojamiento estático. No se necesita compilar para presentar.

## Recorrido de un minuto

1. Activa **Modo presentación** (pantalla completa es opcional).
2. Pulsa **Cargar ejemplo**, luego **Crear mi sesión**.
3. Tras tres segundos, edita una frase del documento.
4. Abre el koala **Habla con tu asistente** y pulsa **Probar ejemplo**. Se añade la actividad en parejas, se resalta el cambio y el koala responde si hay una voz española disponible. En móvil, usa **Ver cambio en mi sesión** para cerrar el panel y ver el documento.
5. Di o escribe **Cambia la duración a 60 minutos**. Los tiempos pasan a 10 + 40 + 10. Prueba **Deshacer cambio** y **Copiar sesión**.
6. **Imprimir / Guardar PDF** abre el diálogo del navegador con solo el documento.
7. **Reiniciar demo** permite repetir el pitch.

El progreso se guarda en el navegador. Las opciones preparadas cubren quinto grado, Matemática y fracciones, con sesiones de 45, 60 o 90 minutos. El contexto del aula se incorpora a los datos generales para revisión docente. Las adaptaciones son locales y predeterminadas.

## Probar el micrófono

1. Sirve la demo desde `http://localhost` / `http://127.0.0.1` con Live Server o publícala mediante HTTPS.
2. Genera una sesión y abre el koala. Pulsa **Hablar por micrófono** y permite el acceso cuando el navegador lo solicite.
3. Habla en español, por ejemplo: **Usa materiales reciclados**. Verás la transcripción; solo su resultado final aplica el cambio. La escucha termina antes de la respuesta hablada.
4. Prueba también **Haz las instrucciones más sencillas**, **Agrega una lista de cotejo** y **Añade una actividad en parejas**. Usa una solicitud a la vez. Las órdenes repetidas no duplican cambios.
5. **Voz activada / Voz silenciada** controla las respuestas; **Detener voz** interrumpe la reproducción. No hay reproducción automática al cargar. La selección de voz prefiere español de Perú y admite otras voces en español instaladas.

El reconocimiento depende del navegador, el permiso y el servicio que este utilice; puede requerir conexión a Internet. Si no está disponible, o no deseas permitir el micrófono, escribe una instrucción o usa cualquiera de los cinco botones. **Probar ejemplo** ejecuta la adaptación de parejas de forma local y es la ruta más predecible para el pitch.

Las últimas tres acciones y su estado para deshacer se guardan junto con la sesión. **Deshacer cambio** restaura los bloques implicados en la última acción y conserva las ediciones de los demás bloques. Si editas un bloque después de adaptarlo, deshacer esa adaptación recupera la versión de ese bloque anterior a ella.

## Verificación

Flujo probado en Chrome a 360, 768 y 1440 px: cinco adaptaciones, variaciones de frases, ausencia de duplicados, ediciones conservadas, tiempos de 60 minutos, historial y deshacer tras recargar, alternativa sin reconocimiento, estilos de impresión y reinicio. Los eventos de reconocimiento (parcial/final, permiso rechazado) y síntesis (voces asíncronas, silencio y detención) se comprobaron con servicios simulados; la captura real del micrófono y la salida de audio deben probarse en el dispositivo del pitch.

Referencias de la plataforma: [resultados finales de reconocimiento](https://developer.mozilla.org/en-US/docs/Web/API/SpeechRecognitionResult/isFinal), [voces disponibles y carga asíncrona](https://developer.mozilla.org/en-US/docs/Web/API/SpeechSynthesis/voiceschanged_event).

## Estilos

Tailwind CSS está compilado en `assets/tailwind.css`. Para regenerarlo (opcional; requiere Node y acceso a npm):

`npx --yes --package tailwindcss@3.4.17 tailwindcss -i tailwind.input.css -o assets/tailwind.css --minify`
