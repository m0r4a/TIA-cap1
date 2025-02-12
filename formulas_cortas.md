# 📊 Fórmulas Estadísticas Simplificadas

> [!TIP]
> Esta es una versión simplificada de las fórmulas estadísticas para facilitar su memorización.
> Para las fórmulas completas en LaTeX, consulta el archivo [formulas.md](formulas.md).

## 📑 Tabla de Contenidos
- [Estimación puntual](#estimación-puntual)
  - [Media](#media)
  - [Varianza](#varianza)
  - [Desviación estándar](#desviación-estandar)
  - [Proporción](#proporción)
- [Estimación por intervalo](#estimación-por-intervalo)
  - [Intervalos de confianza](#intervalos-de-confianza)
  - [Diferencias entre poblaciones](#diferencias-entre-poblaciones)

# Estimación puntual

## Media
### Muestral
```math
\Huge \bar{X} = \frac{\sum_{i=1}^{n} x_i}{n}
```

### Poblacional
```math
\Huge \mu = \frac{\sum x_i}{N}
```

## Varianza
### Muestral
```math
\Huge \delta^2 = \frac{\sum_{i=1}^{n} (x_i - \bar{x})^2}{n-1}
```

### Poblacional
```math
\Huge \sigma^2 = \frac{\sum (x_i - \mu)^2}{N}
```

## Desviación estándar
### Muestral
```math
\Huge \delta = \sqrt{\frac{\sum_{i=1}^{n} (x_i - \bar{x})^2}{n-1}}
```

### Poblacional
```math
\Huge \sigma = \sqrt{\frac{\sum (x_i - \mu)^2}{N}}
```

## Proporción
### Muestral
```math
\Huge P = \frac{x}{n}
```

### Poblacional
```math
\Huge \pi = \frac{x}{N}
```

# Estimación por intervalo

## Intervalos de confianza

- [Para la media](#para-la-media)
  - [Varianza conocida](#varianza-conocida)
  - [Varanza desconocida y (n>=30)](#varianza-desconocida-n30)
  - [Varanza desconocida y (n<30)](#varianza-desconocida-n30-1)
- [Para la proporción](#para-la-proporción)
- [Para la varianza](#para-la-varianza)

### Para la media
#### Varianza conocida
```math
\Huge \bar{X} \pm Z_{\frac{\alpha}{2}}\frac{\sigma}{\sqrt{n}}
```

#### Varianza desconocida (n>30)
```math
\Huge \bar{X} \pm Z_{\frac{\alpha}{2}}\frac{\delta}{\sqrt{n}}
```

#### Varianza desconocida (n<30)
```math
\Huge \bar{X} \pm t_{\frac{\alpha}{2}, n-1}\frac{\delta}{\sqrt{n}}
```

### Para la proporción
```math
\Huge \hat{p} \pm Z_{\frac{\alpha}{2}}\sqrt{\frac{\hat{p}(1-\hat{p})}{n}}
```

### Para la varianza
```math
\Huge \frac{(n-1)\delta^2}{\chi^2_{\frac{\alpha}{2}}} < \sigma^2 < \frac{(n-1)\delta^2}{\chi^2_{1-\frac{\alpha}{2}}}
```

## Diferencias entre poblaciones

- [Diferencia de medias](#diferencia-de-medias)
  - [Varianzas conocidas](#varianzas-conocidas)
  - [Varianzas desconocidas diferentes](#varianzas-desconocidas-diferentes)
  - [Varianzas desconocidas iguales](#varianzas-desconocidas-iguales-con-δp)
- [Razón de varianzas](#razón-de-varianzas)
- [Diferencia de proporciones](#diferencia-de-proporciones)

### Diferencia de medias

#### Varianzas conocidas
```math
\Huge (\bar{x}_1 - \bar{x}_2) \pm Z_{\frac{\alpha}{2}}\sqrt{\frac{\sigma^2_1}{n_1} + \frac{\sigma^2_2}{n_2}}
```

#### Varianzas desconocidas diferentes

```math
\Huge (\bar{x}_1 - \bar{x}_2) \pm t_{\frac{\alpha}{2}, v}\sqrt{\frac{\delta^2_1}{n_1} + \frac{\delta^2_2}{n_2}}
```
donde:
```math
\Huge v = \frac{(\frac{\delta^2_1}{n_1} + \frac{\delta^2_2}{n_2})^2}{\frac{\frac{\delta^2_1}{n_1}}{n_1 - 1} + \frac{\frac{\delta^2_2}{n_2}}{n_2 - 1}}
```
y:
```math
\Huge \delta_x^2 = \frac{\sum_{i=1}^n {(x_i - \bar x)}^2} {n-1}
```

#### Varianzas desconocidas iguales con δp
```math
\Huge (\bar{x}_1 - \bar{x}_2) \pm t_{\frac{\alpha}{2}, v}\delta_p\sqrt{\frac{1}{n_1} + \frac{1}{n_2}}
```
donde:
```math
\Huge \delta_p = \sqrt{\frac{(n_1-1)\delta^2_1 + (n_2-1)\delta^2_2}{n_1 + n_2 - 1}}
```
```math
\Huge v = n_1 + n_2 - 1
```

### Razón de varianzas
```math
\Huge \frac{\delta^2_1}{\delta^2_2}\frac{1}{F} < \frac{\sigma^2_1}{\sigma^2_2} < \frac{\delta^2_1}{\delta^2_2}F
```

### Diferencia de proporciones
```math
\Huge (\hat{p}_1 - \hat{p}_2) \pm Z_{\frac{\alpha}{2}}\sqrt{\frac{\hat{p}_1(1-\hat{p}_1)}{n_1} + \frac{\hat{p}_2(1-\hat{p}_2)}{n_2}}
```
