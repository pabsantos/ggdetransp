# ggdetransp
Código de referência para fazer gráficos do ggplot2 no padrão do Detran.SP

```r
library(ggplot2)
library(showtext)

font_add_google("Open Sans", "opensans")
showtext_opts(dpi = 300) # Ajustar o DPI conforme a configuração da imagem exportada
showtext_auto()

detran_palette <- list(
    "blue" = "#005ca8",
    "lightblue" = "#3490ce",
    "darkblue" = "#004077"
)

theme_detran = function(...) {
    theme_minimal(
        base_family = "opensans",
        base_size = 11
    ) +
    theme(
        legend.position = "top",
        legend.justification = "left",
        legend.key.size = unit(0.5, "cm"),
        legend.direction = "horizontal",
        ...
    )
}
```
