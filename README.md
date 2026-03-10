# Agents Mega Music App

Interfaz de streaming de música y tienda digital construida en modo oscuro con HTML5 semántico y CSS3 modular. Sin frameworks, sin JavaScript.

---

## Descripción del Proyecto

Agents Mega Music App es el rediseño digital de Acme Records: una plataforma híbrida que unifica la experiencia de escuchar música en streaming con la compra de álbumes digitales en una sola sesión. El usuario puede descubrir música, reproducirla en el reproductor inmersivo y adquirir el álbum completo sin salir del flujo.

---

## Estructura de Archivos
```
music-stream-app/
├── css/
│   ├── main.css            # Reset, variables de diseño, tipografía e importación de fuentes
│   ├── layout.css          # Shell de la app, Header, Sidebar, Main
│   ├── components.css      # Botones, Cards, Inputs, Tablas, encabezados de sección
│   └── views/
│       ├── store.css       # Hero banner, grilla de álbumes, grilla de tracks
│       ├── album.css       # Detalle de álbum, tracklist, tabs de información, mini-player
│       ├── player.css      # Reproductor inmersivo, cola Up Next, barra de controles
│       └── checkout.css    # Carrito, formulario de pago, dirección, confirmación
├── assets/
│   ├── img/                # Portadas de álbumes y avatares de usuario
│   └── icons/              # Iconos SVG (Play, Pause, Carrito, Búsqueda)
├── index.html              # Storefront principal (Home)
├── album-detail.html       # Detalle de álbum y decisión de compra
├── player.html             # Reproductor inmersivo de pantalla completa
├── cart.html               # Carrito de compras
├── checkout.html           # Pasarela de pago seguro
├── success.html            # Confirmación de compra y biblioteca personal
└── README.md               # Documentación del proyecto
```

---

## Vistas del Proyecto

### Storefront — index.html
Puerta de entrada a la plataforma. Incluye sidebar de categorías, hero banner del Editor's Pick, grilla de nuevos álbumes de la semana y grilla de tracks más vendidos. Cada tarjeta enlaza a su vista correspondiente.

### Detalle de Álbum — album-detail.html
Vista de decisión de compra o reproducción. Muestra la portada del álbum, metadata (artista, año, género), botón de compra, lista de canciones con efecto hover que revela el control de reproducción, y pestañas informativas del artista. Incluye mini-player fijo en el footer.

### Reproductor Inmersivo — player.html
Vista dedicada a la escucha activa. La portada del álbum es protagonista en una tarjeta con sombra profunda. Panel lateral con la cola de reproducción (Up Next) y barra de controles fija en la parte inferior con progreso, volumen y controles completos.

### Carrito — cart.html
Lista de álbumes seleccionados con controles de cantidad, precio unitario y opción de eliminar. Resumen de orden lateral con subtotal, impuesto estimado y total. Enlace directo a checkout.

### Checkout — checkout.html
Formulario de pago seguro dividido en dos secciones: método de pago (tarjeta de crédito con campos de número, expiración, CVC y nombre) y dirección de facturación. Resumen de orden en sidebar con los productos a pagar y botón de confirmación.

### Confirmación — success.html
Mensaje de compra exitosa con resumen de la transacción y número de orden. Sidebar de biblioteca personal con accesos a Compras Recientes, Mis Álbumes y Canciones Favoritas.

---

## Sistema de Diseño

### Paleta de Colores

| Token              | Valor                    | Uso                                        |
|--------------------|--------------------------|--------------------------------------------|
| `--bg-base`        | `#0d1117`                | Fondo principal de la aplicación           |
| `--bg-surface`     | `#111827`                | Cards, headers, mini-player                |
| `--bg-elevated`    | `#1a2233`                | Hover de filas, fondos de inputs           |
| `--bg-overlay`     | `#1e2a3f`                | Barras de progreso, fondos secundarios     |
| `--bg-card`        | `#141f2e`                | Fondo de tarjetas de productos             |
| `--accent-primary` | `#3b82f6`                | Botones primarios, links activos, progreso |
| `--accent-hover`   | `#60a5fa`                | Estado hover del acento principal          |
| `--accent-muted`   | `rgba(59,130,246,0.15)`  | Fondos sutiles sobre acento                |
| `--text-primary`   | `#ffffff`                | Títulos y contenido principal              |
| `--text-secondary` | `#94a3b8`                | Subtítulos, artistas, labels               |
| `--text-muted`     | `#4b5563`                | Placeholders, metadatos secundarios        |
| `--border-subtle`  | `rgba(255,255,255,0.06)` | Separadores y bordes de sección            |
| `--border-card`    | `rgba(255,255,255,0.08)` | Bordes de cards y inputs                   |

### Sombras

| Token            | Valor                         | Uso               |
|------------------|-------------------------------|-------------------|
| `--shadow-card`  | `0 4px 24px rgba(0,0,0,0.5)` | Tarjeta en reposo |
| `--shadow-hover` | `0 8px 32px rgba(0,0,0,0.7)` | Tarjeta en hover  |

### Tipografía

| Fuente        | Uso                                                        | Pesos           |
|---------------|------------------------------------------------------------|-----------------|
| Space Grotesk | Títulos de página, logo, hero title, nombres de álbumes   | 500 600 700 800 |
| Inter         | Navegación, cuerpo de texto, labels, precios, formularios | 300 400 500 600 700 |

### Espaciado

| Token         | Valor |
|---------------|-------|
| `--space-xs`  | 4px   |
| `--space-sm`  | 8px   |
| `--space-md`  | 16px  |
| `--space-lg`  | 24px  |
| `--space-xl`  | 32px  |
| `--space-2xl` | 48px  |
| `--space-3xl` | 64px  |

### Radios de Borde

| Token           | Valor  |
|-----------------|--------|
| `--radius-sm`   | 6px    |
| `--radius-md`   | 10px   |
| `--radius-lg`   | 14px   |
| `--radius-xl`   | 20px   |
| `--radius-full` | 9999px |

---

## Reparto de Responsabilidades

| Desarrollador   | Archivos                                                                                    |
|-----------------|---------------------------------------------------------------------------------------------|
| Dev1 — Santiago | `index.html`, `css/main.css`, `css/layout.css`, `css/components.css`, `css/views/store.css` |
| Dev2 — Jonatan  | `album-detail.html`, `player.html`, `css/views/album.css`, `css/views/player.css`           |
| Dev3 — Fabio    | `cart.html`, `checkout.html`, `success.html`, `css/views/checkout.css`                      |

---

## Navegación entre Vistas
```
index.html
  └── album-detail.html     (clic en portada o "Buy Now")
        ├── player.html     (clic en track o botón play)
        └── cart.html       (clic en "Add Album to Cart")
              └── checkout.html   (clic en "Proceed to Checkout")
                    └── success.html    (clic en "Place Order")
                          └── index.html   (clic en "Return to Store")
```

---

## Especificaciones Técnicas

- **HTML5 semántico** — uso de `<header>`, `<nav>`, `<main>`, `<section>`, `<article>`, `<aside>`, `<footer>` en todas las vistas
- **CSS3 puro** — sin frameworks, sin librerías externas
- **Sin JavaScript** — toda la interacción es visual y estática
- **Variables CSS** — sistema de design tokens centralizado en `main.css`
- **Responsive Mobile First** — funcional desde 375px; layouts de múltiples columnas en desktop
- **Accesibilidad** — atributos ARIA (`aria-label`, `aria-current`, `role`, `aria-valuenow`) en componentes interactivos

---

## Cómo Visualizar el Proyecto

1. Clonar o descargar el repositorio
2. Abrir `index.html` directamente en el navegador
3. No requiere servidor ni dependencias adicionales
```bash
git clone https://github.com/SantiSarmiento11/Agents-Mega-Music-App.git
cd Agents-Mega-Music-App
# Abrir index.html en el navegador
```

---

## Convenciones de Commits

Todos los mensajes de commit siguen el estándar Conventional Commits:

| Tipo          | Uso                                               |
|---------------|---------------------------------------------------|
| `feat:`       | Nueva vista o componente                          |
| `style:`      | Cambios visuales de CSS sin afectar funcionalidad |
| `docs:`       | Cambios en README u otra documentación            |

Ejemplo: `feat: agregar vista de detalle de álbum con tracklist`

---

## Metodología de Ramas y créditos

El desarrollo está GitHub con las siguientes ramas:

- `main` — versión estable y entregable
- `DevSantiago` — Dev1 Santiago - @SantiSarmiento11 (GitHub)
- `DevJonatan` — Dev2 Jonatan - @Jonatan-17 (GitHub)
- `DevFabio` — Dev3 Fabio - @Fcnfabio (GitHub)
