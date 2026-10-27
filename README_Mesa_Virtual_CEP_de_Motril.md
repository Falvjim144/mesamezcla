# Mesa virtual interactiva RA EFX 8/2

**Radio escolar desde cero · CEP de Motril**  
**Docente de la formación:** Francisco J. Álvarez Jiménez  
**Tipo de recurso:** simulador educativo autocontenido, sin servidor ni base de datos.  
**Destinatarios:** profesorado y alumnado de Educación Primaria, con supervisión docente.

## 1. ¿Qué incluye esta versión?

- Recreación interactiva de la mesa RA EFX 8/2: ocho canales mono, dos entradas estéreo, secciones de efectos, master y USB.
- Controles manipulables para practicar GAIN, EQ, AUX, FX, PAN/BAL, faders, MUTE y PFL.
- Dos pistas musicales originales integradas, una en **STE1** y otra en **STE2**.
- Simulación de escucha PFL independiente de los faders de la mezcla principal.
- Puesta en marcha guiada y ayudas contextuales de cada mando.
- Nueve retos de aprendizaje con pistas opcionales, corrección automática y seguimiento del progreso **durante la sesión**.
- **Panel de retos a la izquierda en modo pantalla completa**: permite avanzar por los retos sin abandonar la mesa. Se puede plegar para ampliar la consola y volver a desplegar.
- Simulación de grabación con descarga del resultado en los navegadores compatibles (normalmente WebM).

## 2. Archivos y estructura de publicación

El paquete entregado contiene:

```text
radio-escolar/
├── index.html      ← aplicación completa
└── README.md       ← este documento
```

Los sonidos y estilos van incluidos en `index.html`, por lo que no hay que crear carpetas de imágenes, audio, CSS o JavaScript.

## 3. Publicación en el alojamiento web

1. Descomprime el ZIP descargado.
2. Accede a tu servidor por el panel de archivos del alojamiento o por FTP/SFTP.
3. Crea una carpeta para la actividad, por ejemplo `radio-escolar`, dentro de la carpeta pública del sitio (`public_html`, `www` o equivalente).
4. Sube **`index.html`** y, opcionalmente, **`README.md`** a esa carpeta.
5. Abre en el navegador la dirección de la carpeta, por ejemplo:
   `https://tu-dominio.es/radio-escolar/`
6. Comprueba que abre, que **Activar sonido** inicia la reproducción y que **Pantalla completa** muestra los retos a la izquierda.

> El servidor debe servir los archivos `.html` con el tipo habitual `text/html`. No son necesarias PHP, bases de datos ni instalaciones adicionales. Se recomienda HTTPS.

### Si se publica en WordPress

La opción más directa es alojar `index.html` como recurso estático en una carpeta accesible del mismo dominio y enlazar a él desde una página de WordPress.

Si el alojamiento permite incluirlo en un `iframe`, puedes utilizar, adaptando la dirección:

```html
<iframe src="https://tu-dominio.es/radio-escolar/"
        title="Mesa virtual de radio escolar — CEP de Motril"
        width="100%" height="850"
        style="border:0;border-radius:12px"
        allow="fullscreen; autoplay" allowfullscreen></iframe>
```

Para una experiencia de pantalla completa más estable, **abrir la actividad en una pestaña propia** mediante un enlace suele ser preferible. Algunas configuraciones de WordPress bloquean o filtran los `iframe`.

## 4. Cómo utilizar el simulador

1. Abre `index.html` o la URL publicada.
2. Pulsa **Mezcla de ejemplo** y después **Activar sonido**. Los navegadores requieren una interacción del usuario para iniciar audio.
3. Pulsa **Pantalla completa** para ver la consola grande.
4. Lee el reto de la **columna izquierda**. Si lo necesitas, pulsa **Pedir una pista**.
5. Manipula directamente los mandos o faders de la consola virtual.
6. Pulsa **Comprobar lo que he hecho**. Si completas el reto, avanza con **Siguiente**.
7. Pulsa **◀ Ocultar** para plegar la columna de retos cuando quieras ver la mesa más grande; vuelve a mostrarla pulsando **▶**.
8. Para salir de pantalla completa, usa el botón correspondiente o la tecla `Esc`.

También puedes consultar las secciones de conexiones, puesta en marcha, exploración, grabación y efectos desde las pestañas de la aplicación.

## 5. Requisitos y compatibilidad

- Navegadores recomendados: versiones actuales de **Chrome** o **Microsoft Edge**; otros navegadores modernos con Web Audio también pueden funcionar.
- Ordenador con teclado/ratón o pantalla táctil. Se recomienda un monitor de al menos 1280 píxeles de ancho para aprovechar toda la consola.
- Altavoces o auriculares y permiso del navegador para reproducir sonido.
- **No necesita Internet** después de cargar el archivo, ya que el HTML es autocontenido.
- Algunas funciones (grabación y pantalla completa) pueden depender de las capacidades y permisos del navegador, de su política de seguridad y de si la actividad se abre dentro de un `iframe`.

## 6. Privacidad y seguridad

- La aplicación **no pide registro**, no utiliza cuentas personales y no envía datos a un servidor propio.
- Los retos y sus resultados permanecen en la sesión abierta: recargar la página puede reiniciar el progreso.
- Las grabaciones simuladas se generan en el propio navegador; si el alumno las descarga, corresponde al centro gestionar su almacenamiento y difusión.
- Para proyectos con voces reales de menores, sigue las autorizaciones y las normas de protección de datos del centro.
- Es **un simulador didáctico**: no controla físicamente la mesa RA EFX 8/2, y las respuestas acústicas son aproximadas, no una emulación certificada de su electrónica.

## 7. Solución rápida de incidencias

| Incidencia | Qué comprobar |
|---|---|
| No suena la música | Pulsa **Activar sonido** y revisa el volumen del equipo y los faders STE1/STE2. |
| La mesa se ve pequeña | Pulsa **Pantalla completa**, **Encajar** o pliega los retos con **◀ Ocultar**. |
| No aparece el panel de retos | Maximiza la mesa y revisa si el panel está plegado (botón **▶**). |
| Un reto no se supera | Pulsa **Pedir una pista**, ajusta los controles y prueba **Comprobar lo que he hecho**. |
| No funciona la grabación | Prueba una versión reciente de Chrome/Edge y comprueba que se ha activado el sonido. |
| No funciona pantalla completa en un `iframe` | Abre el enlace de la actividad en una pestaña nueva. |

## 8. Actualizaciones

Para actualizar la actividad, sustituye únicamente `index.html` por la nueva versión, manteniendo el mismo nombre y la misma carpeta. Si el navegador muestra la versión anterior, recarga sin caché (`Ctrl` + `F5` en Windows).

## 9. Referencias y créditos

El simulador se ha preparado para la formación docente del **CEP de Motril**, tomando como referencia fotografías reales de la mesa del estudio y documentación técnica aportada para la actividad. Se han priorizado explicaciones claras, retos progresivos y la correspondencia visual de controles.

**Docente de la formación:** Francisco J. Álvarez Jiménez.

La presencia del nombre del docente identifica la formación; no debe interpretarse como una certificación técnica del fabricante de la mesa.
