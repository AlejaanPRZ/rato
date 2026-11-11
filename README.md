# RATO

Web de la marca de ropa **RATO** y su colección de lanzamiento *Bajamos un momento*.

Una sola página estática, sin dependencias, sin framework y sin proceso de compilación:
un `index.html` con todo el CSS y los SVG en línea, más las imágenes de las prendas.

**Concepto visual:** póster de calle. Escritura a mano a gran tamaño detrás, camisetas
recortadas encima, menú apilado a la derecha y bordes rasgados entre secciones.

---

## Cómo está hecho

Sin librerías. Todo es HTML y CSS escritos a mano:

- **Maquetación** con CSS Grid y Flexbox, en un único documento.
- **Tipografía y espaciado fluidos** con `clamp()`: la página escala entre móvil y
  escritorio sin saltos bruscos entre puntos de ruptura.
- **Paleta y tipos** como variables CSS, para cambiar el mundo visual desde un solo sitio.
- **Logotipos e ilustraciones en SVG en línea**, que heredan el color del contenedor con
  `currentColor` y no suman peticiones al servidor.
- **Imágenes en WebP**, con `max-width` y `height:auto` para que no desborden.
- **Accesibilidad:** foco visible con `:focus-visible` y contraste adaptado a cada fondo,
  y texto solo para lectores de pantalla donde hace falta.
- **Pantallas con muesca** contempladas con `env(safe-area-inset-*)`.
- **Desplazamiento suave** entre secciones con anclas.

```
index.html   la página completa (CSS y SVG en línea)
img/         vistas de diseño de las camisetas, en .webp
```

---

## Ver en local

No hace falta instalar nada. Basta con servir la carpeta:

```bash
python3 -m http.server 8000
# abrir http://localhost:8000
```

## Publicar

Al ser estática, se publica con GitHub Pages sin más pasos:

`Settings` → `Pages` → `Source`: *Deploy from a branch* → rama `main`, carpeta `/ (root)`.

---

Las imágenes son vistas de diseño de las prendas, no fotografías de producto.

© 2026 RATO · Alejandro Pérez Marco — [github.com/AlejaanPRZ](https://github.com/AlejaanPRZ)
