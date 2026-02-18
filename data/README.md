Archivos de datos para Zero Fight Club

Formato y uso:

- `events.json`: lista de eventos. Cada evento tiene: `id`, `date` (YYYY-MM-DD), `title`, `info`, `location`.
- `modes.json`: objeto con lista `modes`, cada modo tiene: `id`, `name`, `description`, `rules` (array de strings).
- `estatutos.json`: estatutos en formato JSON con `title` y `content`.

Ejemplo de carga desde `index.html` o JS:

```js
fetch('/data/events.json')
  .then(res => res.json())
  .then(events => console.log(events));

fetch('/data/modes.json')
  .then(res => res.json())
  .then(data => console.log(data.modes));
```

Notas:
- En GitHub Pages los archivos estarán disponibles en la ruta `/data/`.
- Si deseas que `index.html` cargue dinámicamente estos archivos puedo integrar `fetch()` y reemplazar los datos hardcodeados.
