# Cómo desplegar esto en Railway

## 1. Personalizá el mensaje
Abrí `index.html` y editá el texto dentro de los `<p>` para que sea tu mensaje.

## 2. Agregá tu canción de Spotify
1. Abrí Spotify (app o web) y buscá la canción.
2. Clic en los tres puntos "..." → Compartir → Insertar canción (Embed).
3. Copiá la URL que aparece dentro del `src="..."` (algo como
   `https://open.spotify.com/embed/track/4uLU6hMCjMI75M1A2tKUQC`).
4. Pegala en `index.html`, reemplazando el `src` del `<iframe>` que dice
   `REEMPLAZA_ESTE_ID`.

## 3. Subilo a GitHub (recomendado)
```
git init
git add .
git commit -m "primera version"
```
Subilo a un repo nuevo en GitHub (podés crearlo desde github.com/new).

## 4. Desplegar en Railway
1. Entrá a https://railway.app y logueate (podés usar GitHub).
2. Click en "New Project" → "Deploy from GitHub repo".
3. Elegí el repositorio que acabás de subir.
4. Railway detecta automáticamente que es un proyecto Node.js (gracias al
   `package.json`) y va a correr `npm install` y luego `npm start`.
5. Esperá a que termine el build. Te va a dar una URL pública (algo como
   `tuapp.up.railway.app`) — ¡esa es la que le mandás a la persona!

### Alternativa sin GitHub
Si tenés el CLI de Railway instalado:
```
npm install -g @railway/cli
railway login
railway init
railway up
```
Esto sube la carpeta directamente sin necesidad de un repo.

## 5. (Opcional) Dominio personalizado
En el panel de Railway, dentro de tu proyecto → Settings → Networking,
podés generar un dominio público o conectar uno propio.
