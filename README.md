Benjamin Iucht 5to B TIC Catalogo de VIdeojuegos
# 🕹️ GAME VAULT — Catálogo de Videojuegos

Catálogo de videojuegos con estética arcade/retro construido con **Astro**. Consume datos reales de la [RAWG API](https://rawg.io/apidocs) — la base de datos de videojuegos más grande del mundo.

## Funcionalidades

- **Datos reales** — 24 juegos con rating Metacritic 70+ cargados desde RAWG API al momento de hacer el build
- **Búsqueda en tiempo real** — filtra por nombre y género mientras escribís
- **Modal de detalle** — hacé click en cualquier juego para ver descripción, plataformas, desarrolladora, tags y más datos traídos en vivo desde la API
- **Estética arcade/retro** — tipografía pixel art, colores neón, scanlines de fondo, animaciones de flicker

## Herramientas usadas

| Herramienta | Uso |
|---|---|
| [Astro](https://astro.build/) | Framework principal |
| [RAWG API](https://rawg.io/apidocs) | Fuente de datos de videojuegos |
| CSS custom con variables | Diseño retro, animaciones, responsive |
| JavaScript vanilla | Búsqueda en tiempo real, fetch al modal, manipulación DOM |
| Google Fonts (Press Start 2P + Rajdhani) | Tipografías |

## Estructura

```
src/
├── components/
│   └── GameCard.astro    # Tarjeta reutilizable con estilo arcade
├── layouts/
│   └── Layout.astro      # Layout base con fuentes, variables CSS y animaciones
└── pages/
    └── index.astro       # Página principal: fetch a RAWG, grilla, buscador, modal
```

## Cómo ejecutarlo

### Requisitos
- Node.js 18 o superior

### Pasos

```bash
# 1. Clonar el repo
git clone https://github.com/tu-usuario/game-catalog.git
cd game-catalog

# 2. Instalar dependencias
npm install

# 3. Correr en desarrollo
npm run dev
# → http://localhost:4321

# 4. Build para producción (opcional)
npm run build
npm run preview
```

## API Key

El proyecto usa una clave pública de demostración de RAWG. Para uso en producción, registrá tu propia clave gratuita en [rawg.io/apidocs](https://rawg.io/apidocs) y reemplazala en `src/pages/index.astro`.
