# 📊 Fórmulas Estadísticas

> [!NOTE]
> Para interpretar las fórmulas LaTeX puedes utilizar [este editor LaTeX](https://latexeditor.lagrida.com/) o verlas directamente renderizadas en GitHub.
>
> Para una versión simplificada de estas fórmulas (que es mejor para memorizarlas), consulta el archivo [formulas_cortas.md](formulas_cortas.md).

## 📑 Tabla de Contenidos
- [Estimación puntual](#estimación-puntual)
  - [Media](#media)
  - [Varianza](#varianza)
  - [Desviación estándar](#desviación-estandar)
  - [Proporción](#proporción)
- [Estimación por intervalo](#estimación-por-intervalo)
  - [Varianza conocida](#varianza-conocida-y-muestra-grande-o-pequeña)
  - [Varianza desconocida](#varianza-desconocida-y-muestra-grande)
  - [Proporción poblacional](#proporción-de-una-población)
  - [Varianza poblacional](#varianza-de-una-población)
  - [Razón de varianzas](#razón-de-varianzas-de-2-poblaciones)
  - [Diferencia de medias](#diferencia-de-medias-de-2-poblaciones-con-varianzas-conocidas)
  - [Diferencia de proporciones](#diferencia-de-proporciones-de-2-poblaciones)

# Estimación puntual

## Media

### Estimación puntual

```math
\color{#A98AE4}\Huge\bar{X} = \frac{\sum_{i=1}^{n} x_i}{n}
```

### Parámetro poblacional

```math
\color{#A98AE4}\Huge\mu = \frac{\sum x_i}{N}
```

## Varianza

### Estimación puntual

```math
\color{#A98AE4}\Huge{\delta^2} = \frac{\sum_{i=1}^{n} (x_i - \bar{x})^2}{n-1}
```

### Parámetro poblacional

```math
\color{#A98AE4}\Huge{\sigma^2} = \frac{\sum (x_i - {\mu})^2}{N}
```

## Desviación estandar

### Estimación puntual

```math
\color{#A98AE4}\Huge\delta = \sqrt{\frac{\sum_{i=1}^{n} (x_i - \bar{x})^2}{n-1}}
```

### Parámetro poblacional

```math
\color{#A98AE4}\Huge{\sigma} = \sqrt{\frac{\sum (x_i - {\mu})^2}{N}}
```

## Proporción

### Estimación puntual

```math
\color{#A98AE4}\Huge{P} = \frac{x}{n}
```

### Parámetro poblacional

```math
\color{#A98AE4}\Huge{\pi} = \frac{x}{N}
```

# Estimación por intervalo

## Varianza conocida y muestra grande o pequeña

```math
\color{#A98AE4}\Huge \bar{X} - Z_{\frac{\alpha}{2}}.{\frac{\sigma}{\sqrt{n}}} < \mu < \bar{X} + Z_{\frac{\alpha}{2}} .{\frac{\sigma}{\sqrt{n}}}
```

## Varianza desconocida y muestra grande

```math
\color{#A98AE4}\Huge \bar{X} - Z_{\frac{\alpha}{2}}.{\frac{\delta}{\sqrt{n}}} < \mu < \bar{X} + Z_{\frac{\alpha}{2}} .{\frac{\delta}{\sqrt{n}}}
```

## Varianza desconocida y muestra pequeña

```math
\color{#A98AE4}\Huge \bar{X} - t_{\frac{\alpha}{2}, n-1}.{\frac{\delta}{\sqrt{n}}} < \mu < \bar{X} + t_{\frac{\alpha}{2}, n-1} .{\frac{\delta}{\sqrt{n}}}
```

## Proporción de una población

### $` \hat{p} `$

```math
\color{#A98AE4}\Huge \hat p = \frac{x}{n}
```

### Fórmula completa

```math
\color{#A98AE4}\Huge \hat{p} - Z_{\frac{\alpha}{2}}.\sqrt{\frac{\hat{p} (1-\hat{p})}{n}} < p < \hat{p} + Z_{\frac{\alpha}{2}} .\sqrt{\frac{\hat{p} (1-\hat{p})}{n}}
```

## Varianza de una población

```math
\color{#A98AE4}\Huge \frac{(n-1)\delta^2}{\chi^2_{{\frac{\alpha}{2}}, n-1}} < \sigma^2 < \frac{(n-1)\delta^2}{\chi^2_{{1 - \frac{\alpha}{2}}, n-1}}
```

## Razón de varianzas de 2 poblaciones

```math
\color{#A98AE4}\Huge \frac{\delta^2_1}{\delta^2_2} . \frac{1}{F_{(\frac{\alpha}{2}, n_1-1, n_2-2)}} < \frac{\sigma^2_1}{\sigma^2_2} < \frac{\delta^2_1}{\delta^2_2} . F_{(\frac{\alpha}{2}, n_2-1, n_1-2)}
```

## Diferencia de medias de 2 poblaciones con varianzas conocidas

```math
\color{#A98AE4}\Huge (\bar x_1 - \bar x_2) - Z_{\frac{\alpha}{2}} . \sqrt{\frac{\sigma^2_1}{n_1} + \frac{\sigma^2_2}{n_2}} < \mu_1 - \mu_2 < (\bar x_1 - \bar x_2) + Z_{\frac{\alpha}{2}} . \sqrt{\frac{\sigma^2_1}{n_1} + \frac{\sigma^2_2}{n_2}}
```

## Diferencias de medias de 2 poblaciones con varianzas desconocidas

### $` \delta_x^2 `$

```math
\color{#A98AE4}\Huge \delta_x^2 = \frac{\sum_{i=1}^n {(x_i - \bar x)}^2} {n-1}
```

### Varianzas diferentes

#### v

```math
\color{#A98AE4}\Huge v = \frac{(\frac{\delta^2_1}{n_1} + \frac{\delta^2_2}{n_2})^2}{\frac{\frac{\delta^2_1}{n_1}}{n_1 - 1} + \frac{\frac{\delta^2_2}{n_2}}{n_2 - 1}}
```

#### Fórmula

```math
\color{#A98AE4}\Huge (\bar x_1 - \bar x_2) - t_{\frac{\alpha}{2}, v} . \sqrt{\frac{\delta^2_1}{n_1} + \frac{\delta^2_2}{n_2}} < \mu_1 - \mu_2 < (\bar x_1 - \bar x_2) + t_{\frac{\alpha}{2}, v} . \sqrt{\frac{\delta^2_1}{n_1} + \frac{\delta^2_2}{n_2}}
```

### Varianzas iguales

#### dp

```math
\color{#A98AE4}\Huge \delta_p = \sqrt{\frac{(n_1 - 1)\delta^2_1 + (n_2 - 1)\delta^2_2}{n_1 + n_2 - 1}}
```

#### v

```math
\color{#A98AE4}\Huge v = n_1 + n_2 - 1
```

#### Fórmula

```math
\color{#A98AE4}\Huge (\bar x_1 - \bar x_2) - t_{\frac{\alpha}{2}, v} . dp.\sqrt{\frac{1}{n_1} + \frac{1}{n_2}} < \mu_1 - \mu_2 < (\bar x_1 - \bar x_2) + t_{\frac{\alpha}{2}, v} . dp.\sqrt{\frac{1}{n_1} + \frac{1}{n_2}}
```

## Diferencia de proporciones de 2 poblaciones

### $` \hat{p_1} `$

```math
\color{#A98AE4}\Huge \hat p_1 = \frac{x_1}{n_1}
```

### $` \hat{p_2} `$

```math
\color{#A98AE4}\Huge \hat p_2 = \frac{x_2}{n_2}
```
