# 🐟 Hay Pesca

App web instalable (PWA) para pescadores: clima en una sola gráfica, tabla solunar por horas y bitácora de piques con mapa. Funciona sin conexión.

## Funciones
- **Clima**: temperatura, presión atmosférica, viento y lluvia en una sola gráfica (3 días) con tendencia de presión.
- **Solunar**: puntaje de pesca hora por hora según el paso de la Luna, su salida/puesta y el amanecer/atardecer. Se calcula en el dispositivo, sin conexión.
- **Mapa**: tu posición GPS, búsqueda de localidades y elección de puntos tocando el mapa.
- **Piques**: fecha y hora, calidad, profundidad, carnada y notas, guardados en el teléfono (`localStorage`).

## Publicar en GitHub Pages
1. Crea un repositorio nuevo en GitHub y sube estos archivos a la rama `main`.
2. En **Settings → Pages → Source**, elige **GitHub Actions**.
3. Cada `push` a `main` publica en `https://TU-USUARIO.github.io/NOMBRE-DEL-REPO/`.

## Instalar en Android
Abre la URL en Chrome → menú ⋮ → **Instalar app** (o **Añadir a pantalla de inicio**). La primera vez necesita internet; después abre sin conexión.

## Uso sin conexión
- Piques y último pronóstico consultado quedan guardados en el teléfono.
- Los mosaicos del mapa solo están disponibles sin conexión en las zonas que ya viste con internet.

## Datos y créditos
- Clima y búsqueda: [Open-Meteo](https://open-meteo.com/)
- Mapa: © [OpenStreetMap](https://www.openstreetmap.org/copyright) · [Leaflet](https://leafletjs.com/)
- Cálculo lunar y solar: fórmulas astronómicas de baja precisión (error de unos minutos).

Licencia MIT.
