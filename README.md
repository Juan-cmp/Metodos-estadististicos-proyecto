# Proyecto final de Metodos Estadisticos

Analisis estadistico del efecto de la ceniza volante y del tiempo de curado sobre la resistencia a la compresion del concreto.

El proyecto utiliza el conjunto de datos **Concrete Compressive Strength** y presenta analisis exploratorio, pruebas de hipotesis, comparacion de grupos, correlacion y modelacion estadistica.

## Contenido

- `index.Rmd`: portada, presentacion y configuracion general.
- `01-introduccion.Rmd`: contexto, problematica, objetivos y justificacion.
- `02-eda-concrete.Rmd`: analisis exploratorio del conjunto de datos.
- `concrete+compressive+strength/`: datos y documentacion de la fuente.
- `_bookdown.yml`: orden de los capitulos y nombre del libro.
- `_output.yml`: formatos de salida y configuracion de LaTeX.
- `docs/`: sitio HTML generado.

## Requisitos

- R 4.6 o posterior.
- RStudio recomendado.
- Paquetes de R: `bookdown`, `rmarkdown`, `knitr` y los paquetes utilizados en los chunks del libro.
- TinyTeX para generar PDF. El proyecto usa `xelatex` como motor LaTeX.

## Instalacion

En RStudio, instala los paquetes principales:

```r
install.packages(c("bookdown", "rmarkdown", "knitr", "tinytex"))
```

Para habilitar la salida PDF, instala TinyTeX una sola vez:

```r
tinytex::install_tinytex()
```

Si RStudio no encuentra `xelatex` despues de la instalacion, reinicia la sesion con `Ctrl + Shift + F10` y verifica:

```r
tinytex::tlmgr_path("add")
Sys.which("xelatex")
```

El segundo comando debe devolver la ruta a `xelatex.exe`.

## Construccion del libro

Desde la raiz del proyecto, ejecuta en RStudio:

```r
bookdown::render_book("index.Rmd")
```

El sitio HTML se genera en `docs/`. Tambien puedes construir un formato especifico:

```r
bookdown::render_book("index.Rmd", "bookdown::gitbook")
bookdown::render_book("index.Rmd", "bookdown::pdf_book")
```

El formato PDF requiere que `Sys.which("xelatex")` devuelva una ruta valida.

## Publicacion

El contenido HTML listo para publicar queda en `docs/`. La configuracion del repositorio apunta a esa carpeta como directorio de salida.

## Autores

Camilo Padilla y Juan Campo.
