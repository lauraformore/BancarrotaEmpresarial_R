# Bancarrota empresarial · Bookdown

Autoras: Laura Rivera · Natalý Cárdenas.

`portada.Rmd` contiene la presentación, los objetivos y el marco teórico. `EDA_completo.Rmd` contiene el análisis en R. `_bookdown.yml` los compila en `docs/index.html` y `docs/EDA.html`, con la misma organización de contenidos que [Jupyter Book](https://lauraformore.github.io/BancarrotaEmpresarial_VIZ/).

Desde R, con los paquetes del documento y Pandoc instalados:

```r
bookdown::render_book("portada.Rmd", "bookdown::gitbook")
```

En Windows, R debe usar una configuración regional UTF-8 para interpretar los identificadores con tildes; si fuera necesario, ejecutar antes `Sys.setlocale("LC_CTYPE", "English_United States.utf8")`.

Las salidas individuales se muestran directamente como tablas formateadas o figuras. Los desplegables se reservan para las colecciones de muchas variables. Todas las gráficas se exportan a SVG mediante el dispositivo vectorial de R, para mantener la nitidez al ampliar la página. Las galerías se guardan en `docs/figures/` y se cargan bajo demanda para evitar incrustar decenas de megabytes en el HTML. `book-ui.html` añade el índice de la página a la derecha, separado de la navegación del libro. Los boxplots conservan el rango completo y muestran los atípicos en rojo.

Se conserva la partición y la lógica estadística propias de R; no se sustituyen sus resultados por los de Python. Los archivos numerados y la copia del documento no forman parte de esta compilación. GitHub Pages sirve el contenido de `docs/` en la rama `master`.
