# Aitana Studio — deploy en Cloudflare Pages

Contenido de este ZIP:
- `index.html` — la página completa (es `aitana.html` renombrado para que Cloudflare lo sirva por defecto).
- `img/aitana/` — las 37 fotos de productos.

## Paso a paso

### 1. Comprar el dominio en Cloudflare
1. Entrá a dash.cloudflare.com → **Domain Registration** → **Register Domains**.
2. Buscá `aitanastudio.com` (o el que elijas) y comprá. Cloudflare lo cobra al costo, sin markup.

### 2. Subir los archivos a GitHub
1. Creá cuenta en github.com (si no tenés) y hacé un repositorio nuevo privado llamado `aitana-studio`.
2. En la página del repo, **"Add file" → "Upload files"**.
3. Arrastrá `index.html` + la carpeta entera `img/` adentro.
4. Commit changes.

### 3. Conectar GitHub con Cloudflare Pages
1. En dash.cloudflare.com → **Workers & Pages** → **Create** → **Pages** → **Connect to Git**.
2. Autorizás GitHub y elegís el repo `aitana-studio`.
3. Build settings: dejá todo en blanco (no hay build). "Save and Deploy".
4. En 1 minuto tenés la página en `aitana-studio.pages.dev`.

### 4. Conectar el dominio
1. En la misma Page → **Custom domains** → **Set up a custom domain** → escribís `aitanastudio.com`.
2. Como el dominio ya está en Cloudflare, el DNS se configura solo. HTTPS activo en 5 minutos.

## Para editar productos / precios después

Opción simple:
1. En GitHub, abrí `index.html` → botón **"Edit this file"** (ícono del lápiz).
2. Buscá (Ctrl+F) el código del producto (ej. `ACR26013`).
3. Cambiá el precio dentro del campo `"price": 36960` por el nuevo valor.
4. Al final de la página, **"Commit changes"**. Cloudflare redeploy automático en 30 segundos.

Opción visual (segunda etapa):
Agregamos **Decap CMS** (panel web con formularios) encima. Avisame cuando quieras y te paso los archivos para sumarlo.

## Para agregar o cambiar fotos

1. Nombrá la foto con el código del producto (ej. `BCN26036.jpeg`).
2. En GitHub, entrá a `img/aitana/` → **"Add file" → "Upload files"** → arrastrá la foto.
3. Si el nombre coincide con una existente, la reemplaza.
