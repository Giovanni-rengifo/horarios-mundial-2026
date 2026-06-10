# Product

## Register

product

## Users

Un hincha colombiano (y su círculo cercano) consultando desde el celular, muchas veces de día y al aire libre o en el trabajo, con una sola pregunta: "¿quién juega hoy y a qué hora?". Uso de vistazo rápido, no de sesión larga. La pregunta estrella es cuándo juega Colombia.

## Product Purpose

Calendario completo del Mundial FIFA 2026 (104 partidos, 11 de junio – 19 de julio) con horarios en hora colombiana (COT). Incluye navegación por fechas, modo "Solo Colombia" (Grupo K: Uzbekistán 17/jun, RD Congo 23/jun, Portugal 27/jun) y registro manual de goles en cada partido: la app calcula las tablas de posiciones (victoria 3 pts, empate 1), clasifica a dieciseisavos a los 1º, 2º y 8 mejores terceros (puntos → DG → GF → resultado entre sí), y propaga ganadores por el cuadro eliminatorio (empate → penales) hasta el tercer puesto y la final. Cruces 73–104 ratificados con FIFA/Wikipedia. Éxito = responder en menos de 5 segundos quién juega y a qué hora, sin errores de fecha ni de zona horaria.

## Brand Personality

Mundialista, colombiano, confiable. La identidad visual celebra la tricolor (amarillo dominante, azul tinta, rojo como acento) sin disfrazar la función: es una herramienta de consulta con alma de hincha.

## Anti-references

- El look genérico de app deportiva oscura con verde césped y gradientes neón.
- Dashboards SaaS de tarjetas idénticas con métricas gigantes.
- Decoración que retrase la lectura del horario (animaciones de carga, glassmorphism, confeti permanente).

## Design Principles

1. **La hora es la heroína**: el horario y los equipos se leen de un vistazo, todo lo demás es secundario.
2. **Colombia se siente, no se grita**: la tricolor marca los partidos de Colombia con significado (la bandera), no con adornos arbitrarios.
3. **Cero mentiras de fecha**: "HOY" y la fecha inicial se calculan en hora de Bogotá, nunca en UTC.
4. **Pulgar primero**: objetivos táctiles ≥44px, navegación de fechas cómoda con una mano.
5. **Los estados vacíos guían**: si Colombia no juega ese día, la app dice cuándo sí y te lleva ahí.

## Accessibility & Inclusion

WCAG AA: contraste 4.5:1 en texto, foco visible en todo control, elementos interactivos semánticos (button), `prefers-reduced-motion` respetado, alt en banderas.
