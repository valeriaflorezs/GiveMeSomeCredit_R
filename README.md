# Give Me Some Credit — EDA en R (bookdown)

Traducción a R (tidyverse + plotly + reactable) del EDA interactivo de [Give Me Some Credit](https://www.kaggle.com/c/GiveMeSomeCredit), organizado como libro **bookdown**.

## Estructura

- `index.Rmd` — introducción, librerías, paleta de colores y descripción de variables.
- `01-carga-datos.Rmd` — carga, estructura, valores faltantes e imputación.
- `02-target.Rmd` — análisis de la variable objetivo (`SeriousDlqin2yrs`).
- `03-univariado.Rmd` — estadísticos descriptivos y visualización interactiva por variable.
- `04-bivariado.Rmd` — pruebas de hipótesis y dashboards segmentados por morosidad.
- `05-multicolinealidad.Rmd` — matriz de correlación, VIF y coordenadas paralelas.
- `06-shap.Rmd` — Random Forest + interpretabilidad con SHAP (importancia, beeswarm, dependencia).
- `RDataSets/` — `cs-training.csv` y `cs-test.csv` (fuente original en Kaggle).

## Cómo renderizar

En RStudio, abre el proyecto en esta carpeta y ejecuta:

```r
install.packages(c("tidyverse", "plotly", "reactable", "scales",
                    "randomForest", "fastshap", "bookdown"))
bookdown::render_book("index.Rmd")
```

El libro se genera en `docs/`, listo para publicarse con GitHub Pages (Settings → Pages → Deploy from branch → `main` / `docs`).
