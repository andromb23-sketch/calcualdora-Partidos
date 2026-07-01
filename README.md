# Octavos Oracle · Mundial 2026

Estimador de cruces del Mundial 2026 con motor Elo-Poisson, blend de modelo Goldman Sachs, Betano y Polymarket.

## Uso

Abrí `index.html` en el navegador, o entrá a:

**https://andromb23.github.io/octavos-oracle/**

Elegí dos selecciones, opcionalmente metés la cuota real de Betano/Polymarket del partido, y la app te da marcador estimado, probabilidad 1·X·2 y quién avanza.

## Cómo funciona

- **Motor Elo-Poisson**: convierte la diferencia de rating Elo en goles esperados y corre distribuciones de Poisson para sacar el resultado más probable.
- **Modelo Goldman Sachs**: derivado del research "World Cup 2026: Predictions, Probabilities, and Paths to Victory" (29 mayo 2026).
- **Betano / Polymarket**: cuotas del partido que cargás vos, se mezclan con pesos ajustables.

Es una herramienta de estimación, no consejo de apuestas.

## Actualizar datos

Los ratings Elo y probabilidades están hardcodeados en el `<script>` de `index.html`, en el array `TEAMS`. Para actualizar según avance el torneo, editá ese array directamente.
