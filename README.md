# Presentador de Diapositivas — Documentación en Markdown

## Descripción

Este proyecto corresponde a un **presentador de diapositivas dinámico en HTML, CSS y JavaScript** diseñado para mostrar imágenes y videos con múltiples efectos de transición.

Incluye:

* Navegación con botones.
* Indicadores de diapositivas.
* Transiciones animadas aleatorias.
* Compatibilidad con imágenes y videos.
* Diseño responsive.
* Footer personalizado.

---

# Estructura General del Proyecto

```html
<!DOCTYPE html>
<html lang="es">
<head>
    <!-- Metadatos -->
    <!-- Estilos CSS -->
</head>
<body>
    <div class="presentation">
        <div id="slideContainer"></div>

        <button id="prevBtn"></button>
        <button id="nextBtn"></button>

        <div class="indicators"></div>

        <footer>
            Diseñado por el profesor Édgar Herrera Morales con tecnología NotebookLM
        </footer>
    </div>

    <script type="module">
        // Código JavaScript
    </script>
</body>
</html>
```

---

# Configuración del Documento HTML

## Metadatos

```html
<meta charset="UTF-8">
<meta name="viewport" content="width=device-width, initial-scale=1">
```

### Función

Permiten:

* Compatibilidad móvil.
* Diseño responsive.
* Correcta codificación UTF-8.

---

# Estilos CSS

## Estilos Base

```css
body, html {
    margin: 0;
    padding: 0;
    font-family: Arial, sans-serif;
    height: 100%;
    overflow: hidden;
}
```

### Características

* Elimina márgenes.
* Usa fuente Arial.
* Ocupa toda la pantalla.
* Evita scroll.

---

# Contenedor Principal

```css
.presentation {
    position: relative;
    width: 100%;
    height: 100%;
    background-color: #1a1a1a;
    color: white;
}
```

## Función

Actúa como el escenario principal de la presentación.

---

# Diapositivas

```css
.slide {
    position: absolute;
    width: 100%;
    height: 100%;
    display: flex;
    justify-content: center;
    align-items: center;
    opacity: 0;
}

.slide.active {
    opacity: 1;
}
```

## Características

* Las diapositivas se superponen.
* Solo una está visible.
* Se usa `opacity` para transición suave.

---

# Multimedia

## Imágenes y Videos

```css
.slide img,
.slide video {
    max-width: 100%;
    max-height: 85%;
    object-fit: contain;
    border-radius: 10px;
}
```

## Función

* Mantiene proporciones.
* Evita deformaciones.
* Aplica bordes redondeados.

---

# Navegación

## Botones

```css
.nav-button {
    position: absolute;
    top: 50%;
    transform: translateY(-50%);
}
```

### IDs

```html
<button id="prevBtn">&#10094;</button>
<button id="nextBtn">&#10095;</button>
```

## Función

Permiten:

* Avanzar diapositivas.
* Retroceder diapositivas.

---

# Indicadores

```css
.indicator {
    width: 12px;
    height: 12px;
    border-radius: 50%;
}
```

## Función

Representan visualmente:

* Número de diapositivas.
* Diapositiva activa.

---

# Footer

```html
<footer>
Diseñado por el profesor Édgar Herrera Morales con tecnología NotebookLM
</footer>
```

## Características

* Visible en todas las diapositivas.
* Posición fija inferior.
* Texto semitransparente.

---

# JavaScript

## Variables Iniciales

```javascript
const slideContainer = document.getElementById('slideContainer');
const prevBtn = document.getElementById('prevBtn');
const nextBtn = document.getElementById('nextBtn');
```

## Función

Obtienen referencias del DOM.

---

# Inicialización de Diapositivas

```javascript
function initSlides() {
    mediaItems.forEach((item, index) => {
        const slide = document.createElement('div');
    });
}
```

## Función

* Genera diapositivas dinámicamente.
* Inserta imágenes o videos.
* Configura errores de carga.

---

# Mostrar Diapositiva

```javascript
function showSlide(index) {
    slides[currentSlide].classList.remove('active');
    slides[index].classList.add('active');
}
```

## Función

Controla:

* Cambio de diapositiva.
* Activación visual.
* Transiciones.

---

# Navegación de Diapositivas

## Siguiente

```javascript
function nextSlide() {
    if (currentSlide < slides.length - 1) {
        showSlide(currentSlide + 1);
    }
}
```

## Anterior

```javascript
function prevSlide() {
    if (currentSlide > 0) {
        showSlide(currentSlide - 1);
    }
}
```

---

# Eventos de Teclado

```javascript
document.addEventListener('keydown', (e) => {
    if (e.key === 'ArrowRight') nextSlide();
    if (e.key === 'ArrowLeft') prevSlide();
});
```

## Función

Permite navegar usando:

* Flecha derecha.
* Flecha izquierda.

---

# Transiciones Animadas

## Lista de Transiciones

```javascript
const transitions = [
    'fade',
    'slideLeft',
    'slideRight',
    'rotate',
    'scale',
    'flipX',
    'flipY',
    'zoomBlur'
];
```

## Función

Cada diapositiva aplica una animación aleatoria.

---

# Ejemplo de Keyframes

```css
@keyframes fade {
    from { opacity: 0; }
    to { opacity: 1; }
}
```

## Otras Animaciones

* slideLeft
* slideRight
* slideUp
* slideDown
* rotate
* scale
* flipX
* flipY
* zoomBlur
* swingIn
* bounceIn
* glitch
* spiralIn
* dropIn
* unfold

---

# Inserción de Medios

```javascript
const mediaItems = [
    { url: 'imagen.webp', type: 'image' },
    { url: 'video.mp4', type: 'video' }
];
```

## Función

Define:

* Recursos multimedia.
* Tipo de contenido.
* Orden de diapositivas.

---

# Características Técnicas

| Característica | Descripción            |
| -------------- | ---------------------- |
| Responsive     | Compatible con móviles |
| Multimedia     | Imágenes y videos      |
| Animaciones    | 15+ transiciones       |
| Navegación     | Botones y teclado      |
| Diseño moderno | Fondo oscuro y sombras |
| Dinámico       | Generación automática  |

---

# Tecnologías Utilizadas

* HTML5
* CSS3
* JavaScript ES6
* Animaciones CSS
* Flexbox

---

# Posibles Mejoras

* Pantalla completa.
* Auto reproducción.
* Temporizador.
* Música de fondo.
* Soporte táctil.
* Transiciones configurables.
* Precarga de imágenes.

---

# Autor

**Profesor Édgar Herrera Morales**

Desarrollado con apoyo de NotebookLM.
