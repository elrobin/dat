# Documentación aplicada a la traducción — Materiales del curso

Sitio web de materiales docentes construido con [Quarto](https://quarto.org).

## Estructura

```
documentacion_traduccion/
├── _quarto.yml          # Configuración del libro
├── index.qmd            # Página de bienvenida
├── styles.css           # Estilos personalizados
├── references.bib       # Referencias bibliográficas
└── tema9/
    ├── sesion1.qmd      # ¿Qué es y cómo funciona?
    ├── sesion2.qmd      # Riesgos, limitaciones y uso crítico
    └── sesion3.qmd      # Prompts, flujos de trabajo y aplicaciones
```

## Para añadir un nuevo tema

1. Crea una carpeta `temaX/`
2. Añade los archivos `sesionX.qmd` dentro
3. Registra las sesiones en `_quarto.yml` bajo un nuevo `part`

Ejemplo en `_quarto.yml`:

```yaml
- part: "Tema 1. Fuentes de información especializadas"
  chapters:
    - tema1/sesion1.qmd
    - tema1/sesion2.qmd
```

## Para renderizar en local

Necesitas tener instalado [Quarto](https://quarto.org/docs/get-started/).

```bash
quarto preview   # Vista previa en el navegador con recarga automática
quarto render    # Genera el sitio en la carpeta _book/
```

## Para publicar en GitHub Pages

```bash
quarto publish gh-pages
```

La primera vez te pedirá autorización. Las siguientes, actualiza con el mismo comando.

## Para publicar en Netlify

```bash
quarto publish netlify
```

O conecta el repositorio de GitHub a Netlify y configura el comando de build como `quarto render` y el directorio de publicación como `_book`.
