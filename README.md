# Rumbo — descargas y respaldo web

Este repo es **público y de solo lectura por diseño**: es un espejo generado
a mano desde `mercadateapp/rumbo` (privado), que es la única fuente de
verdad del código. Acá NUNCA se edita directo — todo cambio se hace en el
repo privado y se vuelve a copiar acá cuando se quiere publicar una
actualización.

Qué hay acá:
- `www/index.html` — web del pasajero (respaldo si la app falla).
- `www/admin.html` — web del conductor, con login (respaldo si la app falla).
- `www/img/` — íconos y logo.
- `index.html` (raíz) — landing **pública, para pasajeros**: web + APK.
  Deliberadamente NO enlaza a la página del conductor.
- `conductor.html` (raíz) — landing **separada, solo para conductores**:
  web + APK. No está enlazada desde `index.html` ni indexada por buscadores
  (`robots.txt`, `<meta name="robots" content="noindex">`) — se comparte a
  mano con cada conductor de la red, nunca con un pasajero.
- Releases (tag `latest`) — los `.apk` de "Rumbo" (pasajero) y "Rumbo
  Conductor". El link no cambia entre versiones, solo el archivo detrás
  (se actualiza con `gh release upload latest <archivo> --clobber`).

Qué NO hay acá (y nunca debe copiarse): `backend/Codigo.gs`,
`backend/Porticos.gs`, ni ninguna API key. El backend vive solo en Google
Apps Script, dentro del proyecto privado.
