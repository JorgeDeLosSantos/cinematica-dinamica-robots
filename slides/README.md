# Diapositivas con Slidev

Las presentaciones se agrupan por área temática en `cinematica/` y `dinamica/`. Cada archivo Markdown representa una presentación independiente.

## Desarrollo local

Requiere Node.js 22 y pnpm 10.

```bash
cd slides
pnpm install
pnpm dev:cinematica-intro
```

## Compilación

```bash
pnpm build
```

La salida se genera en `slides/dist/`. La publicación en GitHub Pages **no** está activada todavía.

Al agregar una presentación, incluye scripts `dev:` y `build:` en `package.json` y actualiza el script general `build`.

La presentación de introducción es únicamente una prueba de infraestructura.
