# ⚡ QUICKSTART (30 segundos)

## Para la gente que no quiere leer mucho:

### 1️⃣ Crea cuenta GitHub
https://github.com/signup

### 2️⃣ Crea nuevo repositorio
https://github.com/new
- Nombre: `inventoryai-mvp`
- Público
- Crear

### 3️⃣ Sube archivos (sin terminal)
En tu repo → "Upload files" → Arrastra estos archivos:
```
📄 landing_page.html (renombra a index.html)
📄 dashboard-mvp.html (renombra a dashboard.html)
📄 vercel.json
📄 package.json
📄 README.md
📄 .gitignore
```

### 4️⃣ Deploy a Vercel
https://vercel.com → "Sign Up with GitHub" → "Import" tu repo → "Deploy"

### 5️⃣ ¡LISTO! 
Tu URL: `https://inventoryai-mvp.vercel.app`

---

## Si usas Terminal (15 segundos)

```bash
cd tu/carpeta/inventoryai-mvp

git init
git add .
git commit -m "Initial commit"
git branch -M main
git remote add origin https://github.com/TU_USUARIO/inventoryai-mvp.git
git push -u origin main
```

Luego en Vercel:
https://vercel.com → Connect GitHub → "Import" → "Deploy" ✅

---

## Problemas?

- **"Git command not found"**: Instala Git desde https://git-scm.com
- **"401 Unauthorized"**: GitHub pide autenticación. Usa tu username/password o token
- **"Vercel dice Not Found"**: Verifica que index.html esté en la raíz o en `/public`

---

**¡LISTO EN 5 MINUTOS! 🚀**
