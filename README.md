# MusicStream Store - Plataforma de Comercio Electronico y Reproduccion de Musica Digital

Interfaz web moderna y adaptativa para la exploracion de catalogo musical, adquisicion de vinilos de coleccion y reproduccion en linea basada en estandares puros de HTML5 y CSS3.

[![Dominio](https://img.shields.io/badge/Dominio-Comercio%20Electronico%20%26%20Streaming-0052CC.svg)]()
[![HTML5](https://img.shields.io/badge/HTML5-Semantico-orange.svg)]()
[![CSS3](https://img.shields.io/badge/CSS3-Grid%20%26%20Flexbox-blue.svg)]()
[![Diseno](https://img.shields.io/badge/Diseno-Mobile%20First-success.svg)]()

## Resumen Ejecutivo

El diseno de plataformas digitales para la industria musical requiere un balance riguroso entre estetica vanguardista, rendimiento optimo y jerarquia visual intuitiva. MusicStream Store ofrece una arquitectura de interfaz limpia que simula la experiencia completa de una tienda de musica: desde el descubrimiento de lanzamientos discograficos, visualizacion de pistas y fichas tecnicas de masterizacion, hasta el flujo de carrito de compras, pasarela de pago y reproductor embebido.

## Alcance y Objetivos de Negocio

- Arquitectura de interfaz orientada a componentes modulares utilizando CSS nativo sin dependencias de frameworks externos.
- Diseno adaptativo (Mobile-First y Desktop) con soporte para altas densidades de pixeles.
- Flujo transaccional completo: Catalogo -> Detalle de Album -> Carrito de Compras -> Checkout -> Confirmacion de Compra.
- Reproductor multimedia estilizado con controles de reproduccion, barra de progreso y lista de canciones.
- Optimizacion estricta de tiempos de carga y compatibilidad semantica accesible.

## Arquitectura del Sistema

El proyecto implementa una arquitectura basada en la metodologia de organizacion modular de estilos y paginas estaticas:
1. Capa de Base y Variables Globales (`css/main.css`).
2. Capa de Estructura y Distribucion de Grid (`css/layout.css`).
3. Capa de Componentes Reutilizables (`css/components.css`).
4. Capa de Vistas Especificas (`css/views/*.css`).
5. Paginas HTML interconectadas mediante hiperenlaces semanticos.

### Diagrama de Flujo Arquitectonico y Navegacion

```mermaid
flowchart TD
    A[Pagina Principal / Tienda index.html] -->|Seleccionar Album| B[Detalle de Album album-detail.html]
    A -->|Reproducir Track| C[Reproductor de Musica player.html]
    B -->|Agregar al Carrito| D[Carrito de Compras cart.html]
    D -->|Proceder al Pago| E[Pasarela de Pago checkout.html]
    E -->|Confirmar Transaccion| F[Confirmacion Exitosa success.html]
    C -->|Volver a la Tienda| A
    F -->|Continuar Explorando| A
```

### Estructura de Directorios

```text
Proyecto-HTML-CSS-C/
├── index.html           # Vista principal de la tienda y catalogo discografico
├── album-detail.html    # Ficha tecnica del album, tracklist y opciones de compra
├── player.html          # Interfaz dedicada del reproductor de audio digital
├── cart.html            # Resumen del carrito de compras y calculo de subtotal
├── checkout.html        # Formulario de direccion de envio y datos de pago
├── success.html         # Pantalla de confirmacion de orden con resumen de compra
├── README.md            # Documentacion tecnica de ingenieria del proyecto
├── assets/              # Recursos multimedia
│   ├── icons/           # Iconografia vectorial y logos de alta resolucion
│   └── img/             # Portadas de albumes y recursos graficos en WebP/AVIF
└── css/                 # Hojas de estilo estructuradas en capas
    ├── main.css         # Reset CSS, variables CSS y tipografias globales
    ├── layout.css       # Sistema de grillas (Header, Sidebar, Main, Footer)
    ├── components.css   # Botones, badges, tarjetas de producto y reproductores
    └── views/           # Reglas especificas por cada vista individual
```

## Stack Tecnologico

Construido exclusivamente con estandares web oficiales del W3C para garantizar rendimiento maximo, mantenibilidad y accesibilidad universal.

### Estandares de Marcado y Estructuracion

- ![HTML5](https://img.shields.io/badge/HTML5-E34F26?style=for-the-badge&logo=html5&logoColor=white) Estandar semantico oficial (W3C Semantic Elements: header, main, nav, section, article, aside, footer).
- ![Web Accessibility](https://img.shields.io/badge/Accessibility-WAI--ARIA-blue.svg?style=for-the-badge) Atributos accesibles y roles semanticos para tecnologias asistivas.

### Diseno Visual, Tipografia y Maquetacion

- ![CSS3](https://img.shields.io/badge/CSS3-1572B6?style=for-the-badge&logo=css3&logoColor=white) Sistema de estilos nativo con Custom Properties y selectores avanzados.
- ![CSS Grid](https://img.shields.io/badge/CSS_Grid_Layout-264DE4?style=for-the-badge&logo=css3&logoColor=white) Distribucion bidimensional para el dashboard de tienda y paneles laterales.
- ![CSS Flexbox](https://img.shields.io/badge/CSS_Flexbox-1572B6?style=for-the-badge&logo=css3&logoColor=white) Alineacion unidimensional para barras de navegacion, listas de reproduccion y tarjetas.
- ![Google Fonts](https://img.shields.io/badge/Google_Fonts-4285F4?style=for-the-badge&logo=googlefonts&logoColor=white) Fuentes tipograficas Inter (lectura fluida) y Space Grotesk (titulares).

### Formatos Multimedia y Optimizacion de Recursos

- **Imagenes AVIF / WebP**: Compresion de ultima generacion reduciendo el peso de transferencia en mas de un 60% frente a JPEG/PNG tradicionales.
- **Google Fonts CDN**: Enlace optimizado con preconeccion anticipada (`rel='preconnect'`).

## Requisitos Previos del Sistema

- Cualquier navegador web con soporte de CSS Grid y CSS Variables:
  - Chrome 60+
  - Firefox 55+
  - Safari 11+
  - Edge 79+
- No se requiere instalacion de Node.js, Python ni compiladores adicionales para su visualizacion basica.
