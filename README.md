# Octavos Oracle · Mundial 2026

Estimador de cruces del Mundial 2026. Elegís dos países y la app calcula marcador, 1·X·2 y quién avanza — sin cargar nada más.

## Uso

**https://andromb23.github.io/octavos-oracle/**

Elegís equipo local, equipo visita, y opcionalmente la sede (neutral / de local para uno u otro). Listo.

## Cómo funciona

Cada país tiene un **rating combinado**, calculado una sola vez y guardado en los datos de la app:

- **82% Elo** (eloratings.net)
- **18% señal de mercado**, que mezcla el % de ser campeón según el modelo de **Goldman Sachs** ("World Cup 2026: Predictions, Probabilities, and Paths to Victory", 29-may-2026) y el % de campeón del consenso de **Polymarket/Betano**.

Ese rating combinado alimenta un motor **Elo-Poisson**: convierte la diferencia de rating en goles esperados por equipo y corre dos distribuciones de Poisson para sacar el marcador más probable, el 1·X·2, y quién avanza (incluye una estimación de prórroga/penales con leve ventaja al favorito).

No hace falta cargar cuotas de partidos individuales — todo el consenso de mercado ya está incorporado en el rating de cada país.

## Actualizar datos

Los ratings están en el array `TEAMS` dentro del `<script>` de `index.html`. Cada equipo tiene:
- `elo`: rating Elo actual
- `gs`: % de campeón según Goldman Sachs
- `pm`: % de campeón según el mercado (Polymarket)

Para reflejar resultados nuevos según avance el torneo, editá esos tres valores por equipo.

## Nota

Es una herramienta de estimación, no consejo de apuestas. El fútbol es ruido — tomalo como punto de partida, no como certeza.
