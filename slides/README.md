# Diapositivas con Slidev

Las presentaciones se organizan primero por tipo de material (`slides/`) y luego por tema. Cada archivo Markdown es una presentación independiente.

## Áreas temáticas

- `preliminares-matematicos/`: álgebra lineal y métodos numéricos.
- `cinematica/`: cinemática directa, inversa y diferencial.
- `dinamica/`: formulaciones Euler-Lagrange y Newton-Euler.

Los archivos nuevos son plantillas mínimas; su contenido se desarrollará posteriormente.

## Desarrollo local

Requiere Node.js 22 y pnpm 10.

```bash
cd slides
pnpm install --frozen-lockfile
pnpm dev:cinematica-directa
```

También están disponibles, por ejemplo, `pnpm dev:dinamica-euler-lagrange`, `pnpm dev:preliminares-algebra-lineal` y `pnpm dev:cinematica-intro`.

## Compilación

```bash
pnpm build
```

Este comando compila todas las presentaciones registradas en `package.json`. Para compilar una sola, utiliza su comando `build:`, como `pnpm build:cinematica-directa`.

La salida se genera en `slides/dist/`. La publicación en GitHub Pages **no** está activada.

Para nuevas presentaciones, añade los scripts `dev:` y `build:` correspondientes en `package.json`, y actualiza el script general `build`.

## Recursos reutilizables

Cada presentación habilita el addon local `./addons/shared` desde su encabezado YAML. Incluye `Callout`, `EquationBox`, `Footnote` y el layout `two-cols-example`.

La presentación `cinematica/00-introduccion.md` contiene pruebas de infraestructura.
