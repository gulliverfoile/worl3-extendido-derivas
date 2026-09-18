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
NO es un modelo de control, quien lo use asi es su problema.
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
  Este modelo no está calibrado con datos reales. Combinarlo con World3
  y validarlo contra series históricas (1900–2025) es un trabajo pendiente
  que no he hecho. Si alguien quiere retomarlo, aquí está el punto de partida.
- **No es neutral.** Tiene sesgos. Los nombres de las capas, las
  funciones elegidas y los umbrales son decisiones humanas. Están
  documentadas en `docs/modelo.md` para que puedas discutirlas.

---

## Estructura del repositorio si escala.
derivas/
├── README.md ← este archivo
├── LICENSE ← agpl3
├── index.html ← el simulador (todo en uno)
├── docs/
│ ├── modelo.md ← explicación de las 4 capas
│ ├── bucles.md ← los bucles de retroalimentación
│ └── referencias.md ← World3, Meadows, Jevons, etc.
└── ejemplos/
├── colapso-gaia.md ← cómo reproducir el colapso ecológico
├── captura-agotada.md ← cómo reproducir el agotamiento de la captura
└── burnout-masivo.md ← cómo reproducir el colapso subjetivo

text

---

## Los bucles principales

El modelo no es una lista de variables. Es un **sistema de bucles
acoplados**. Estos son los principales:

**Gaia**
- Deshielo → menos albedo → más calor → más deshielo.
- Permafrost → metano → más calor → más permafrost.
- CO₂ → menos absorción oceánica → más CO₂.

**Economía**
- Capital → extracción → menos recursos → más coste → menos capital.
- Capital → producción → emisiones → Gaia → daño → menos población.

**Captura**
- Control → peaje → menos reinversión → menos capital → más narrativa
  → más control.
- Presión ecológica → más narrativa → más coste de perpetuación →
  captura agotada.

**Subjetividad**
- Carga laboral → burnout → menos productividad → menos producción →
  menos sentido → más burnout.
- Captura de información → menos atención → menos confianza → menos
  productividad.

**Acoplamientos entre capas**
- Captura filtra info → Economía decide con datos distorsionados.
- Economía extrae → emite → Gaia se calienta → EROI ecológico cae.
- Gaia dañada → más burnout → menos productividad → menos capacidad
  de mitigación.
- Captura sube peaje → menos producción libre → menos sentido →
  más burnout.

---

## Tests

El simulador incluye tests integrados que demuestran las lógicas
internas. Se ejecutan pulsando **Ejecutar tests** en la interfaz.

| Test | Qué verifica |
|------|--------------|
| 1 | Función de umbral (tipping points) |
| 2 | Bucle deshielo-albedo en Gaia |
| 3 | EROI ecológico vs económico |
| 4 | Burnout reduce productividad |
| 5 | Captura distorsiona la información |
| 6 | Simulación completa de 30 turnos |

Cada test imprime OK/FALLO en pantalla. No hay framework: son asserts
simples, legibles, modificables.

---

## Filosofía del modelo

- **No hay villanos.** Hay estructuras que seleccionan actores. El
  sistema no premia la libertad, premia la adaptación.
- **La captura no prohíbe.** Encarece, filtra, distorsiona. Convierte
  alternativas en lujos.
- **El EROI económico puede ser positivo mientras el ecológico es
  negativo.** El beneficio contable no mide el coste real.
- **Los bucles positivos en Gaia pueden cruzar umbrales irreversibles.**
  Una vez cruzados, ninguna optimización tecnológica los detiene.
- **La subjetividad no es un adorno.** Modifica la productividad real.
  El burnout no es una queja, es una variable de estado.
- **El sistema no tiene meta.** Tiene deriva. Y la deriva se puede
  estudiar.

---

## Cómo contribuir

Si quieres añadir una capa, un bucle o un test:
 haz un fork

Criterios:
- El dominio debe seguir siendo puro (sin DOM, sin WebGL).
- Cada capa nueva debe tener su `estadoInicial()` y su `step()`.
- Cada lógica nueva debe tener su test.
- Los cambios en el README deben reflejar cambios en el modelo.

---

## Licencia

MIT. Haz lo que quieras con esto. Si lo mejoras, compártelo.

---

## Referencias

- Meadows, D. et al. *The Limits to Growth*. 1972.
- Meadows, D. et al. *Beyond the Limits*. 1992.
- Meadows, D. et al. *Limits to Growth: The 30-Year Update*. 2004.
- Forrester, J. *World Dynamics*. 1971.
- Jevons, W.S. *The Coal Question*. 1865.
- Meadows, D. *Leverage Points: Places to Intervene in a System*. 1999.

---

*Este README es parte del modelo. Si el modelo cambia, el README cambia.
Si el README no cambia, el modelo no cambió de verdad.*

