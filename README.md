# Bar Piscina — Comandas

App de comandas del Bar Piscina (Mota del Cuervo). Es una sola página
(`index.html`), sin proceso de build. Se sincroniza entre todos los
dispositivos en tiempo real usando Supabase.

## Desplegar / actualizar (GitHub → Vercel)
- Este repositorio está conectado a Vercel.
- Cada vez que cambies `index.html` y lo subas a GitHub, Vercel publica solo.
- En los móviles/tablets basta con cerrar y volver a abrir la app para ver la
  versión nueva (el `vercel.json` evita que se quede en caché una versión vieja).

## Editar la carta y los precios
- Todo el menú está en el objeto `MENU`, cerca del principio del `<script>`
  dentro de `index.html`. Formato de cada producto: `['Nombre', precio]`.
- Los extras (bacon, queso, tomate, patatas, hielo) y qué categoría los ofrece
  están en `EXTRAS` y `EXTRAS_BY_CAT`.

## Datos (Supabase)
- Mesas, pedidos y tickets viven en el proyecto de Supabase ya configurado.
- Las claves están en las dos primeras líneas del `<script>`
  (`SUPABASE_URL` y `SUPABASE_KEY`). La key es la *publishable* (pública, va en
  el cliente a propósito); la seguridad la dan las políticas RLS de Supabase.
- No subir aquí la contraseña de la base de datos ni la *secret key*.

## Archivos
- `index.html` — la app completa.
- `vercel.json` — configuración de despliegue (sin caché).
- `README.md` — este archivo.
