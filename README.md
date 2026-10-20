# Bancarrota empresarial · Bookdown

Autoras: Laura Rivera · Natalý Cárdenas.

La fuente principal es `EDA_completo.Rmd`; `_bookdown.yml` la compila como un único libro en `docs/index.html`. Los archivos numerados y la copia del documento no forman parte de esta compilación.

Desde R, con los paquetes del documento y Pandoc instalados:

```r
bookdown::render_book("EDA_completo.Rmd", "bookdown::gitbook")
```

En Windows, R debe usar una configuración regional UTF-8 para interpretar los identificadores con tildes; si fuera necesario, ejecutar antes `Sys.setlocale("LC_CTYPE", "English_United States.utf8")`.

El libro permite desplegar tablas ETL y consultar por variable las tablas y gráficas univariadas. Los boxplots muestran el rango completo de observaciones. Los cambios de presentación no modifican la partición, los cálculos estadísticos ni los modelos.
