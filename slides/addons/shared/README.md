# Recursos compartidos para Slidev

Addon local (no publicado en npm) que centraliza componentes y layouts reutilizables.

## Componentes

- `<Callout type="note|tip|warning|important" title="...">...</Callout>`
- `<EquationBox title="...">...</EquationBox>`
- `<Footnote align="left|center|right">...</Footnote>`

## Layouts

- `two-cols-example`: dos columnas separadas por una línea; el segundo bloque utiliza el slot `::right::`.

Las presentaciones ubicadas en `slides/cinematica/` o `slides/dinamica/` habilitan este addon en su headmatter:

```yaml
---
theme: default
addons:
  - ./addons/shared
---
```

La ruta se resuelve respecto al directorio de trabajo de Slidev (`slides/`), desde el que se ejecutan los scripts de `package.json`.

Se adapta la implementación de los componentes originales del repositorio `analisis-de-mecanismos`.
