# 🚀 GUÍA: Cómo Subir a GitHub y Desplegar en Vercel

## PASO 1: Crear una Cuenta en GitHub (si no tienes)

1. Ve a https://github.com
2. Haz clic en "Sign up"
3. Completa el formulario con:
   - Email
   - Contraseña
   - Username (ej: tu-nombre-usuario)
4. Verifica tu email
5. ¡Listo! Ya tienes cuenta en GitHub

---

## PASO 2: Crear un Nuevo Repositorio en GitHub

### Opción A: Desde la web (más fácil)

1. Inicia sesión en GitHub
2. Ve a https://github.com/new
3. Completa los campos:
   - **Repository name**: `inventoryai-mvp`
   - **Description**: "SaaS de Automatización de Inventarios con Visión Artificial - MVP"
   - **Public** (selecciona este)
   - ✅ "Initialize this repository with a README" (opcional)
4. Haz clic en "Create repository"
5. ¡Repositorio creado!

---

## PASO 3: Subir Archivos a GitHub

Tienes 2 opciones:

### Opción A: Subir por Web (Súper fácil, sin terminal)

1. En tu repositorio, haz clic en "Upload files"
2. Arrastra los archivos aquí:
   ```
   - landing_page.html → renombra a index.html
   - dashboard-mvp.html → renombra a dashboard.html
   - vercel.json
   - package.json
   - README.md
   - .gitignore
   ```
3. Escribe un mensaje de commit:
   ```
   Initial commit: MVP InventoryAI
   ```
4. Haz clic en "Commit changes"
5. ¡Archivos subidos!

### Opción B: Usar Terminal (Para usuarios avanzados)

```bash
# 1. Ir a la carpeta del proyecto
cd /ruta/a/tu/carpeta/inventoryai-mvp

# 2. Inicializar repositorio git
git init

# 3. Añadir archivos
git add .

# 4. Crear primer commit
git commit -m "Initial commit: MVP InventoryAI"

# 5. Crear rama main (si es necesario)
git branch -M main

# 6. Conectar con GitHub (reemplaza TU_USUARIO y REPO_NAME)
git remote add origin https://github.com/TU_USUARIO/inventoryai-mvp.git

# 7. Subir archivos a GitHub
git push -u origin main
```

**Nota**: GitHub pedirá autenticación. Usa tu username y contraseña.

---

## PASO 4: Desplegar en Vercel

### Opción A: Deploy desde Vercel.com (Recomendado)

1. Ve a https://vercel.com
2. Haz clic en "Sign Up"
3. Selecciona "Continue with GitHub"
4. Autoriza a Vercel a acceder a tu GitHub
5. Vercel mostrará tus repositorios
6. Haz clic en "Import" en el repositorio `inventoryai-mvp`
7. Vercel detectará automáticamente que es un proyecto estático
8. Haz clic en "Deploy"
9. ¡En 30-60 segundos tu app estará en línea!

Vercel te dará una URL como:
```
https://inventoryai-mvp.vercel.app
```

### Opción B: Deploy desde GitHub (Alternativa)

1. En tu repositorio GitHub, ve a "Settings"
2. En el lado izquierdo, busca "Pages"
3. En "Source", selecciona "Deploy from a branch"
4. En "Branch", selecciona "main" y carpeta "/root" (o donde estén los HTML)
5. Haz clic en "Save"
6. GitHub creará un sitio en: `https://TU_USUARIO.github.io/inventoryai-mvp`

---

## PASO 5: Verificar que Funciona

1. Abre la URL que te dio Vercel:
   ```
   https://inventoryai-mvp.vercel.app
   ```

2. Deberías ver la Landing Page con:
   - Logo de InventoryAI
   - Hero section
   - Características
   - Precios
   - Formulario de contacto

3. Haz clic en "Ver Demo" para ver el Dashboard:
   ```
   https://inventoryai-mvp.vercel.app/dashboard.html
   ```

4. ¡Listo! Tu MVP está en línea y es accesible desde cualquier lugar

---

## PASO 6: Actualizar Cambios (si necesitas modificar algo)

Si necesitas hacer cambios a los archivos HTML:

### Con terminal:
```bash
# 1. Edita los archivos localmente
# 2. Añade cambios
git add .

# 3. Confirma cambios
git commit -m "Actualización: [describe qué cambió]"

# 4. Sube a GitHub
git push

# 5. Vercel se actualiza automáticamente (en 30 segundos)
```

### Sin terminal (por web):
1. En GitHub, abre el archivo que quieres editar
2. Haz clic en el ícono de lápiz (Edit)
3. Haz cambios
4. Haz clic en "Commit changes"
5. Vercel se actualiza automáticamente

---

## ✅ Verificación Final

Después del deploy, verifica que todo funcione:

- [ ] Landing page carga correctamente
- [ ] Todos los estilos CSS se ven bien
- [ ] El formulario funciona (aunque no envíe datos)
- [ ] El botón "Ver Demo" lleva al dashboard
- [ ] El dashboard muestra todas las secciones
- [ ] Los gráficos y tablas se ven correctamente

---

## 🔗 Links Importantes

Una vez deployado, compartirás estos links:

```
Landing Page: https://inventoryai-mvp.vercel.app
Dashboard: https://inventoryai-mvp.vercel.app/dashboard.html
GitHub: https://github.com/TU_USUARIO/inventoryai-mvp
```

---

## 🆘 Problemas Comunes

### "No encuentro el botón de Upload"
- En GitHub, en la página del repo, hay un botón verde que dice "Code"
- A la derecha hay un botón "Upload files"

### "Mi URL de Vercel dice 'Not Found'"
- Verifica que los archivos HTML estén en la carpeta `public/`
- Verifica que el archivo principal se llame `index.html`
- Espera 1 minuto después del push a GitHub

### "Los estilos CSS no se ven"
- Es un problema de rutas relativas
- Verifica que los `<link>` en el HTML usen rutas correctas
- Los archivos HTML tienen CSS integrado (inline), así que no debería pasar

### "El formulario no envía datos"
- Es normal en MVP. El formulario solo simula capturas
- Para que funcione realmente, necesitarías un backend (Node.js, Python, etc.)

---

## 🎓 Concepto Técnico

**¿Cómo funciona todo esto?**

1. **GitHub**: Repositorio donde almacenas el código
2. **Vercel**: Servicio que detecta cambios en GitHub y despliega automáticamente
3. **Flujo**:
   ```
   Editas archivos localmente
       ↓
   Haces commit y push a GitHub
       ↓
   Vercel detecta cambios
       ↓
   Vercel compila y despliega
       ↓
   Tu sitio se actualiza en línea
   ```

---

## 💡 Próximos Pasos (Opcionales)

Si quieres mejorar aún más:

1. **Agregar un dominio personalizado**:
   - En Vercel → Settings → Domains
   - Añade tu dominio (inventoryai.com)

2. **Agregar analytics**:
   - Vercel tiene analytics gratis
   - Ve a Vercel → Analytics

3. **Agregar variables de entorno**:
   - Vercel → Settings → Environment Variables
   - Útil si luego añades un backend

4. **Crear un backend real**:
   - Para que el formulario envíe datos realmente
   - Vercel soporta serverless functions con Node.js

---

## 📚 Resumen Rápido

| Paso | Qué hacer | Tiempo |
|------|-----------|--------|
| 1 | Crear cuenta GitHub | 2 min |
| 2 | Crear repositorio | 1 min |
| 3 | Subir archivos | 5 min |
| 4 | Conectar con Vercel | 3 min |
| 5 | Deploy | 1 min |
| **TOTAL** | | **12 minutos** |

---

**¡Listo! Tu MVP estará en línea en menos de 15 minutos.** 🎉

Para cualquier duda, revisa la documentación oficial:
- GitHub: https://docs.github.com
- Vercel: https://vercel.com/docs
