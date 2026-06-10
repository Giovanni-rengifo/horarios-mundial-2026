# Design

## Theme

Claro, papel cálido. Estrategia de color **Committed**: el amarillo Colombia es dueño de la cabecera; la tinta azul profunda lleva texto y estados activos; el rojo es acento puntual (badge HOY). La tricolor aparece solo con significado de bandera: cinta superior de la página, banda superior de tarjetas de Colombia, micro-indicador en fechas donde juega Colombia.

## Colors

Todo en OKLCH, definido en `:root` de index.html. Sin blancos ni negros puros.

- `--paper` oklch(96.5% 0.012 95): fondo de página (cálido)
- `--card` oklch(99.2% 0.005 95): superficies de tarjeta
- `--ink` oklch(24% 0.05 270): texto principal, fondos activos
- `--ink-soft` oklch(38% 0.04 270): texto secundario (sedes)
- `--muted` oklch(46% 0.028 270): meta-texto (cumple AA sobre card)
- `--border` oklch(90% 0.014 95)
- `--yellow` oklch(86% 0.165 95): cabecera, mitad de la tricolor, texto sobre tinta
- `--yellow-soft` oklch(96% 0.055 98): fondo de tarjetas de Colombia
- `--blue` oklch(42% 0.13 265): nombre de Colombia, foco
- `--red` oklch(51% 0.2 27): badge HOY, tercio de la tricolor

Tricolor: `linear-gradient(90deg, yellow 0 50%, blue 50% 75%, red 75%)` (proporciones de la bandera).

## Typography

- **Archivo** (Google Fonts, variable 400–900): UI, números tabulares para horas y fechas.
- **Archivo Black**: solo display (título, encabezados de día en mayúsculas, títulos de estado vacío). Nunca en labels, botones ni datos.
- La hora es el elemento jerárquico principal de cada tarjeta: 1.02rem / 800, con am-pm en `small`.

## Components

- **Toggle Solo Colombia**: pill con borde tinta sobre amarillo; activo = relleno tinta + texto amarillo; estado vía `aria-pressed`, el texto no cambia.
- **Pills de fecha**: `<button>` con `aria-pressed`; activo = fondo tinta; con filtro activo, los días sin Colombia se atenúan (opacity .35); micro-tricolor siempre reserva su espacio (visibility) para evitar saltos.
- **Tarjeta de partido**: lista agrupada por día con divisores. Todo centrado: hora arriba, debajo cada equipo en columna (bandera encima del nombre, centrados) con "VS" en medio. Tarjeta de Colombia con banda tricolor superior (::before) y fondo `--yellow-soft`. Prohibido el side-stripe (border-left).
- **Estado vacío**: enseña el próximo (o último) partido de Colombia y ofrece botón "Ver ese día".

## Motion

- Entrada de bloques de día: `rise` 220ms cubic-bezier(.22,1,.36,1), fade + 6px.
- Transiciones de controles 150ms, misma curva. Sin bounce.
- `prefers-reduced-motion: reduce` desactiva todo.

## Layout & A11y

- Contenido max-width 560px; cabecera + nav de fechas en un único wrapper sticky (sin offsets mágicos).
- Objetivos táctiles ≥44px (toggle, botones de nav, pills ≥56px de alto).
- `:focus-visible` azul (tinta dentro de la cabecera amarilla); controles interactivos son `<button>` con aria-labels en español.
- Fechas "HOY" e inicial calculadas en zona `America/Bogota` (nunca `toISOString`).
