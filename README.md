# Torres & Guerrero — Sitio web

Landing page del estudio jurídico **Torres & Guerrero**, dirigido por el abogado penalista Rodrigo Torres Jurado. Sitio estático de una sola página (HTML + CSS + JS, sin frameworks ni dependencias de build).

## Estructura

```
site/
├── index.html        # Toda la página: markup, estilos y JS inline
└── assets/
    ├── crest-mark.png       # Escudo del estudio (header, sobre fondo oscuro)
    ├── favicon.png          # Ícono de pestaña del navegador
    ├── logo-light.webp      # Logo completo (isotipo + wordmark), para el pie de página
    ├── og-image.jpg         # Imagen de vista previa al compartir en redes
    ├── rodrigo-torres.jpg / .webp    # Foto de portada
    └── rodrigo-oficina.jpg / .webp   # Foto de la sección "Quién lo defenderá"
```

No hay build ni dependencias: es HTML plano listo para servir tal cual.

## Ver el sitio en local

Cualquier servidor estático sirve. Por ejemplo, desde esta carpeta:

```bash
python3 -m http.server 4173
```

Luego abrir `http://localhost:4173` en el navegador.

## Publicar

El sitio no requiere backend: el formulario de contacto arma un mensaje de WhatsApp (o un `mailto:`) en el navegador del visitante, sin servidor propio. Puede desplegarse en cualquier hosting estático (Cloudflare Pages, Netlify, Vercel, GitHub Pages, etc.) apuntando la raíz a esta carpeta.

### Datos de contacto a mantener actualizados

Los siguientes datos están repetidos en varios lugares de `index.html` (barra superior, sección de contacto, pie de página, botones de WhatsApp y los metadatos `schema.org`/Open Graph):

- Teléfono: `+56 9 7478 3978`
- Correo: `contacto@torresguerrero.cl`
- Dirección física: **pendiente de agregar** (se retiró la dirección de Morandé; falta incorporar la definitiva en la barra de contacto, el pie de página y los datos estructurados).

## Pendientes conocidos

- Agregar la dirección física del estudio una vez definida.
- Confirmar que el correo `contacto@torresguerrero.cl` sea el definitivo.
- Confirmar con Rodrigo Torres si los casos "Publicam" y "Fermex" pueden mencionarse públicamente.
