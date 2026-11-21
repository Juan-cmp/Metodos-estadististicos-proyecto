# Proyecto final de Metodos Estadisticos

Analisis estadistico del efecto de la ceniza volante y del tiempo de curado sobre la resistencia a la compresion del concreto.

El proyecto utiliza el conjunto de datos **Concrete Compressive Strength** y presenta analisis exploratorio, intervalos de confianza, pruebas de hipotesis, comparacion de grupos, correlacion y un modelo de regresion lineal multiple.

## Contenido

- `index.Rmd`: portada, presentacion, configuracion general y funciones compartidas (tablas, tema y colores de los graficos).
- `01-introduccion.Rmd`: contexto, problematica, objetivos y justificacion.
- `02-eda-concrete.Rmd`: analisis exploratorio del conjunto de datos y pruebas de normalidad.
- `03-intervalos-confianza.Rmd`: intervalos de confianza (objetivo 1).
- `04-comparacion-ceniza.Rmd`: comparacion de mezclas con y sin ceniza (objetivo 2).
- `05-anova-curado.Rmd`: resistencia segun las etapas de curado (objetivo 3).
- `06-correlacion-ceniza.Rmd`: correlacion entre ceniza y resistencia (objetivo 4).
- `07-regresion-multiple.Rmd`: modelo de regresion lineal multiple (objetivo 5).
- `08-conclusiones.Rmd`: conclusiones.
- `concrete+compressive+strength/`: datos y documentacion de la fuente.
- `_bookdown.yml`: orden de los capitulos y nombre del libro.
- `_output.yml`: configuracion de la salida HTML.
- `docs/`: sitio HTML generado.

## Requisitos

- R 4.6 o posterior.
- RStudio recomendado (incluye Pandoc).
- Paquetes de R: `bookdown`, `rmarkdown`, `knitr`, `kableExtra`, `tidyverse`, `readxl`, `moments`, `patchwork`, `GGally`, `effsize`, `rstatix`, `lmtest`, `car`, `janitor` y `nortest`.

## Instalacion

En RStudio, instala los paquetes:

```r
install.packages(c(
  "bookdown", "rmarkdown", "knitr", "kableExtra", "tidyverse", "readxl",
  "moments", "patchwork", "GGally", "effsize", "rstatix", "lmtest",
  "car", "janitor", "nortest"
))
```

## Construccion del libro

El libro se genera solo en formato HTML. Desde la raiz del proyecto, ejecuta en RStudio:

```r
bookdown::render_book("index.Rmd")
```

El sitio HTML se genera en `docs/`. Los capitulos comparten los mismos objetos, por lo que hay que construir el libro completo y no cada capitulo por separado.

## Publicacion

El contenido HTML listo para publicar queda en `docs/`. La configuracion del repositorio apunta a esa carpeta como directorio de salida.

## Autores

Camilo Padilla y Juan Campo.
