# Cabaña Santa Cecilia — sitio web

Sitio estático (un `index.html` + carpeta `img/`). No necesita build ni dependencias.

## Primer deploy (Vercel CLI)

```bash
npm i -g vercel
cd cabana-santa-cecilia
vercel            # primera vez: login, "Set up and deploy" → Y
                  # nombre del proyecto: cabana-santa-cecilia
                  # "In which directory is your code located?" → ./
                  # Framework: Other  (no hay build command ni output dir)
vercel --prod     # publica en https://cabana-santa-cecilia.vercel.app
```

Si Vercel te da otra URL (porque el nombre estaba tomado), cambiá `https://cabana-santa-cecilia.vercel.app`
en las dos líneas `og:url` y `og:image` de `index.html` y volvé a correr `vercel --prod`.

## Cambios posteriores

Reemplazá los archivos que cambien y corré `vercel --prod` de nuevo. La URL no cambia, el QR sigue sirviendo.

Alternativa más cómoda a futuro: subir esta carpeta a un repo de GitHub e importarlo en Vercel
(Add New → Project). Cada `git push` publica solo.

## Probar la vista previa de WhatsApp

Después del deploy, pegá la URL en https://www.opengraph.xyz para ver cómo se ve el link compartido.
WhatsApp guarda la vista previa en caché: si la cambiás, puede tardar en actualizarse.
