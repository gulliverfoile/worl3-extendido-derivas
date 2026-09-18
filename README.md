# derivas

**Un simulador de 4 capas acopladas: Gaia, Economía, Captura y Subjetividad.**

Inspirado en World3 (*Los límites del crecimiento*), extendido con capas que
el modelo original no tiene: la captura de plataformas, la subjetividad como
stock que modifica la productividad, y un EROI ecológico que puede ser
negativo aunque el económico sea positivo.

No es un modelo predictivo. No es un paper. No es una herramienta de decisión.
Es una **herramienta de pensamiento** para explorar cómo interactúan cuatro
niveles de un sistema complejo y cómo emergen derivas como el colapso
ecológico, el agotamiento de recursos, la captura de plataformas o el burnout.

---

## ¿Qué es esto?

Un archivo HTML autocontenido. Sin dependencias, sin build, sin servidor.
Lo abres en un navegador y funciona.

Modela cuatro capas acopladas:

| Capa | Qué modela | Stocks principales |
|------|-----------|-------------------|
| **Gaia** | Biogeoquímica, clima, umbrales planetarios | temperatura, albedo, permafrost, CO₂, metano |
| **Economía** | Extracción, capital, producción, recursos | capital, recursos, producción, población |
| **Captura** | Plataformas, peajes, filtro de información | control, filtroInfo, narrativa, peaje |
| **Subjetividad** | Burnout, confianza, sentido, atención | burnout, confianza, sentido, atención |

Las cuatro capas se acoplan en cada turno. Una modifica a las otras. Y el
resultado es una deriva que no está programada: emerge del acoplamiento.

---

## ¿Para qué sirve?

Para explorar bucles de retroalimentación sin necesidad de escribir código.

- Mueve el slider de emisiones y mira cómo Gaia cruza umbrales.
- Sube el control de captura y observa cómo el peaje se dispara, la
  reinversión cae, el capital se estanca, pero la narrativa sube.
- Aumenta la carga laboral y mira cómo el burnout reduce la productividad
  real aunque el capital siga alto.
- Baja el umbral de permafrost y verás el efecto runaway mucho antes.

No te da respuestas. Te da un espacio para hacer mejores preguntas.

---

## ¿En qué se basa?

- **World3** (Meadows et al., 1972; actualizado 1992, 2004) para la
  estructura de economía, población y recursos.
- **Teoría de plataformas** (captura de flujos, peajes, filtro de
  información) para la capa de Captura.
- **EROI ecológico** (energía devuelta vs daño ecológico total) para
  distinguir beneficio económico de beneficio real.
- **Paradoja de Jevons** (la eficiencia no reduce el consumo, lo
  reconfigura) para los bucles de tecnología.
- **Dinámica de sistemas** (Forrester, Meadows) para el formalismo:
  stocks, flujos, bucles, retardos, no linealidades, umbrales.

---

## ¿Cómo lo uso?

1. Guarda el archivo `index.html` en tu ordenador.
2. Ábrelo en cualquier navegador moderno (Chrome, Firefox, Safari).
3. Mueve los sliders de la derecha.
4. Pulsa los botones para avanzar +1, +10 o +50 turnos.
5. Observa el cubo y el registro de turnos.
6. Pulsa **Ejecutar tests** para verificar las lógicas internas.

No requiere instalación. No requiere internet. No requiere nada.

---

## ¿Qué NO es?

- **No es predictivo.** No dice qué va a pasar. Dice qué puede pasar
  si las relaciones entre capas se mantienen.
- **No es un paper.** No ha sido revisado por pares. Es un modelo
  conceptual, con decisiones de diseño explícitas y discutibles.
- **No es una herramienta de decisión.** No lo uses para justificar
  políticas públicas. Úsalo para entender por qué las políticas fallan.
- **No es el sucesor de World3.** Es una extensión conceptual, escrita
  desde cero, con capas que World3 no tiene.
- **No es neutral.** Tiene sesgos. Los nombres de las capas, las
  funciones elegidas y los umbrales son decisiones humanas. Están
  documentadas en `docs/modelo.md` para que puedas discutirlas.

---

## Estructura del repositorio
