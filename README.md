# Bar Piscina — Comandas

App de comandas del Bar Piscina (Mota del Cuervo). Una sola página
(`index.html`), sin build. Se sincroniza entre todos los dispositivos en
tiempo real con Supabase.

## Archivos del repositorio
- `index.html` — la app completa.
- `manifest.json` — datos de la web app (nombre, colores, icono).
- `icon-192.png`, `icon-512.png`, `apple-touch-icon.png` — icono de la app.
- `vercel.json` — despliegue sin caché.
- `README.md` — este archivo.

Todos van en la **raíz** del repositorio, al mismo nivel.

## Desplegar / actualizar (GitHub → Vercel)
- El repositorio está conectado a Vercel: al subir cambios se publica solo.
- En los móviles, cerrar y volver a abrir la app para ver la versión nueva.

## Instalar en el móvil
Abrir la URL → menú del navegador → «Añadir a pantalla de inicio».
Queda con el icono del molino y se abre a pantalla completa.

## Editar la carta y los precios
- Menú en el objeto `MENU`, al principio del `<script>`. Formato: `['Nombre', precio]`.
- Extras y qué categoría los ofrece: `EXTRAS` y `EXTRAS_BY_CAT`.
- Si se renombra un producto, añadir el nombre antiguo a `ALIAS` para que el
  histórico y el ranking lo sigan contando como el mismo.

## Datos (Supabase)
- Mesas, pedidos, tickets y reservas viven en Supabase.
- Claves en las dos primeras líneas del `<script>` (`SUPABASE_URL`, `SUPABASE_KEY`).
  La key es la *publishable* (pública a propósito); la seguridad la dan las
  políticas RLS.
- No subir aquí la contraseña de la base de datos ni la *secret key*.
