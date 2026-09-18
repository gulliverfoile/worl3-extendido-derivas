# Modelo

Cuatro capas acopladas. Cada una es un módulo puro con estado inicial
y función de paso. El orquestador las conecta en orden.

## Capa 1 · Gaia

Biogeoquímica del planeta. Stocks: temperatura, albedo, permafrost,
CO₂, metano. La temperatura sube con las emisiones y con la pérdida
de albedo. El permafrost se libera por encima de un umbral y emite
metano, que a su vez sube la temperatura.

**Bucles positivos**: deshielo → menos albedo → más calor → más
deshielo. Permafrost → metano → más calor → más permafrost.

**Umbrales**: aviso (1.5 °C), permafrost (2.0 °C, ajustable),
runaway (3.0 °C).

**EROI ecológico**: energía devuelta menos daño ecológico, dividido
por energía invertida. Puede ser negativo aunque el económico sea
positivo.

## Capa 2 · Economía

Extracción, capital, producción, población. La productividad real
depende del capital y de la subjetividad (burnout, confianza). Pero
la economía solo ve la productividad percibida, que está filtrada
por la captura.

**Bucles**: capital → extracción → menos recursos → más coste → menos
capital. Capital → producción → emisiones → Gaia → daño → menos
población.

**Coste de extracción**: sube no linealmente cuando los recursos
escasean.

## Capa 3 · Captura

Plataformas, peajes, filtro de información. El control se refuerza a
sí mismo (+2% por turno). El peaje crece con el control medio. El
filtro de información crece con el control de información. La
narrativa sube cuando hay presión ecológica, para mantener
legitimidad.

**Coste de perpetuación**: sube con la presión ecológica y la
narrativa. Si supera la producción, la captura se agota.

## Capa 4 · Subjetividad

Burnout, confianza, sentido, atención. El burnout sube con la carga
laboral y baja con el sentido. La confianza baja con el filtro de
información. El sentido sube con producción libre (no capturada).
La atención baja con el control de información.

**Bienestar**: media de (100 - burnout), confianza, sentido y
atención.

## Coherencia

Métrica sintética que combina las cuatro capas.

- M = (capital / 100) · (recursos / 1000)
- S = (confianza / 100) · (1 - filtroInfo)
- I = (temperatura / 3) + (burnout / 200)
- f(I) = I si I ≤ 1; exp(-0.5 · (I-1)²) si I > 1
- Coherencia = M · S · f(I)
