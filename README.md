# 🎺 Mariachi Estrella Brillante

App de gestión de horarios para grupos de mariachi.

## Subir a Railway (paso a paso)

### Opción A — Desde GitHub (recomendado)

1. Crea una cuenta en https://github.com si no tienes
2. Crea un repositorio nuevo llamado `mariachi-app` (público o privado)
3. Sube esta carpeta a ese repositorio
4. Ve a https://railway.app → New Project → Deploy from GitHub repo
5. Selecciona `mariachi-app` → Deploy
6. Railway detecta automáticamente que es Node.js y lo despliega
7. En Settings → Domains → Generate Domain → copias tu URL pública

### Opción B — Desde Railway CLI (sin GitHub)

```bash
npm install -g @railway/cli
railway login
railway init
railway up
```

## Estructura del proyecto

```
mariachi-railway/
├── index.html      ← App principal
├── manifest.json   ← PWA config
├── sw.js           ← Service Worker (offline)
├── server.js       ← Servidor Express (para Railway)
├── package.json    ← Dependencias Node
└── .gitignore
```

## URL de producción para Google Calendar API

Una vez desplegado en Railway, tu URL será algo como:
`https://mariachi-app-production.up.railway.app`

Agrégala en Google Cloud Console → OAuth Client ID → Authorized JavaScript origins.
