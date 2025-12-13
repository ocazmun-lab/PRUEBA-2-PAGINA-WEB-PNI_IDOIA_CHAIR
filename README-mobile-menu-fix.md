Verificación y depuración del menú móvil

Qué se cambió
- Uso de Pointer Events (pointerdown) cuando están disponibles; fallback touchstart+click.
- Prevención de duplicados (debounce 400ms) para evitar que el menú se abra y se cierre de inmediato.
- stopPropagation en handlers y mejoras CSS (touch-action, pointer-events en overlay/menú)
- DEBUG_MENU (false por defecto) para habilitar console.debug cuando se necesite investigar.

Cómo probar en Android (Chrome)
1. Abrir la página en un dispositivo Android o emulador.
2. Conectar el móvil al ordenador, abrir Chrome en el ordenador, ir a chrome://inspect y seleccionar el dispositivo.
3. Activar la consola y tocar el botón hamburguesa para observar el orden de eventos.
4. Si el problema persiste, activar DEBUG_MENU = true en el script para ver mensajes de toggle/close.

Cómo probar en iPhone (Safari)
1. Abrir la página en Safari móvil.
2. Conectar el iPhone al Mac y abrir Safari -> Develop -> [device] -> [page].
3. Abrir la consola de Web Inspector y tocar el botón para ver eventos.

Pasos a compartir si el bug persiste
- ¿Sucede en ambos Android y iPhone o solo uno de los dos?
- ¿Sucede en Chrome/Firefox/Safari o solo en un navegador específico?
- ¿Qué versión del SO y del navegador están usando?
- Desactivar las extensiones / probar en modo incógnito (si aplica).

Notas
- No se previene el comportamiento por defecto de los enlaces para que la navegación de anclas funcione correctamente.
- Si aún falla, puedo añadir una versión mínima y reproducible para ayudarte a probar en varios dispositivos.
