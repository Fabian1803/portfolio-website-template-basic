# 🚀 Guía de Deployment - Cómo Subir tu Página a la Nube

Esta guía te ayudará a subir tu página web a internet de forma gratuita usando diferentes plataformas.

## 📋 Antes de Empezar

1. **Verifica que todo funcione localmente**:
   - Abre `index.html` en tu navegador
   - Prueba todas las funciones (botones, formulario, navegación)
   - Revisa que se vea bien en móvil y desktop

2. **Prepara tu código**:
   - Todo está listo en tu carpeta actual
   - Los archivos están optimizados para deployment

## 🌟 Opción 1: Netlify (Más Fácil - Recomendado)

### Método A: Drag & Drop (Sin Git)
1. Ve a [netlify.com](https://netlify.com)
2. Regístrate con email o GitHub
3. En el dashboard, busca "Sites" 
4. Arrastra toda tu carpeta `Plantilla web` al área que dice "Drag and drop your site folder here"
5. ¡Listo! Tu sitio estará online en segundos

### Método B: Con GitHub (Más Profesional)
1. Crea una cuenta en [GitHub](https://github.com) si no tienes
2. Crea un nuevo repositorio llamado `mi-primera-web`
3. Sube todos tus archivos:
   ```bash
   git init
   git add .
   git commit -m "Mi primera página web"
   git branch -M main
   git remote add origin https://github.com/TU-USUARIO/mi-primera-web.git
   git push -u origin main
   ```
4. En Netlify: "New site from Git" > Conecta GitHub > Selecciona tu repo
5. Deploy automático cada vez que hagas cambios

## ⚡ Opción 2: Vercel

1. Ve a [vercel.com](https://vercel.com)
2. Regístrate con GitHub
3. "New Project" > Importa tu repositorio
4. Deploy automático

## 📄 Opción 3: GitHub Pages (Gratis con GitHub)

1. Sube tu código a un repositorio de GitHub
2. Ve a Settings > Pages
3. Source: "Deploy from a branch"
4. Branch: "main" / Folder: "/ (root)"
5. Tu sitio estará en: `https://TU-USUARIO.github.io/NOMBRE-REPO`

## 🔧 Opción 4: Firebase Hosting (Google)

1. Instala Firebase CLI:
   ```bash
   npm install -g firebase-tools
   ```
2. En tu carpeta:
   ```bash
   firebase login
   firebase init hosting
   firebase deploy
   ```

## 🌐 Opción 5: Surge.sh (Súper Rápido)

1. Instala Surge:
   ```bash
   npm install -g surge
   ```
2. En tu carpeta:
   ```bash
   surge
   ```
3. Sigue las instrucciones

## 📱 Después del Deploy

### ✅ Verificaciones Post-Deploy
1. **Funcionalidad**: Prueba todos los botones y enlaces
2. **Responsive**: Verifica en móvil y tablet
3. **Performance**: Usa PageSpeed Insights de Google
4. **SEO**: Verifica que los meta tags funcionen

### 🔗 Conectar Dominio Personalizado (Opcional)
- En Netlify/Vercel: Settings > Domain Management
- Compra un dominio en Namecheap, GoDaddy, etc.
- Configura los DNS según las instrucciones de la plataforma

### 📊 Analytics (Opcional)
```html
<!-- Añade antes de </head> en index.html -->
<!-- Google Analytics -->
<script async src="https://www.googletagmanager.com/gtag/js?id=GA_TRACKING_ID"></script>
<script>
  window.dataLayer = window.dataLayer || [];
  function gtag(){dataLayer.push(arguments);}
  gtag('js', new Date());
  gtag('config', 'GA_TRACKING_ID');
</script>
```

## 🛠️ Comandos Útiles de Git

```bash
# Inicializar repositorio
git init

# Añadir todos los archivos
git add .

# Hacer commit
git commit -m "Descripción de cambios"

# Conectar con repositorio remoto
git remote add origin https://github.com/usuario/repo.git

# Subir cambios
git push origin main

# Ver estado
git status

# Ver historial
git log --oneline
```

## 🆘 Solución de Problemas Comunes

### Error: "Page not found"
- Verifica que `index.html` esté en la raíz
- Revisa la configuración de build en la plataforma

### Error: "CSS/JS no carga"
- Verifica las rutas relativas en tu HTML
- Asegúrate de que los archivos estén en el mismo directorio

### Error: "Formulario no funciona"
- El formulario actual es solo frontend
- Para funcionalidad real, necesitas un backend o servicio como Formspree

### Error de HTTPS
- Todas las plataformas modernas incluyen SSL automático
- Si hay problemas, verifica la configuración de dominio

## 🎯 Próximos Pasos

1. **Personaliza tu contenido**:
   - Cambia los textos por información real tuya
   - Añade tus proyectos reales
   - Actualiza información de contacto

2. **Mejora continua**:
   - Añade más proyectos
   - Mejora el diseño
   - Añade nuevas funcionalidades

3. **Aprende más**:
   - React/Vue para interfaces más complejas
   - Node.js para backend
   - Bases de datos

## 📞 ¿Necesitas Ayuda?

- **Documentation**: Cada plataforma tiene docs excelentes
- **Community**: Stack Overflow, Reddit r/webdev
- **Tutoriales**: YouTube, freeCodeCamp, Platzi

---

¡Felicidades! 🎉 Tu primera página web estará online muy pronto. ¡Es un gran logro!
