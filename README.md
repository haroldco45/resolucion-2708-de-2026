# 📱 Resolución 2708 de 2026 - App Web Instalable (PWA)

**Biblioteca Legal Colombiana - Derogación de 11 Circulares Laborales**

---

## 🎯 Descripción

App web progresiva (PWA) interactiva que contiene el análisis completo de la Resolución 2708 de 2026 del Ministerio de Trabajo colombiano. Derogación de 11 circulares laborales expedidas entre septiembre de 2025 y julio de 2026.

### Características

✅ **Instalable** — Agrégala a tu pantalla de inicio (Android, iOS, Windows, Mac)  
✅ **Offline** — Funciona sin conexión a internet tras primera carga  
✅ **Responsivo** — Optimizado para móvil, tablet y desktop  
✅ **Búsqueda** — Filtra circulares por número, tema o tags  
✅ **Tabs interactivos** — Navega entre circulares, normas, guía práctica y casos  
✅ **Compartible** — Open Graph + Twitter meta tags para redes sociales  
✅ **Dark mode** — Soporte automático para tema oscuro

---

## 📋 Contenido

### 1️⃣ Las 8 Circulares Analizadas (de 11 totales)

| Número | Tema | Fecha |
|--------|------|-------|
| **0101** | Jornada, horas extras, destajo | 22 sept 2025 |
| **0120** | Estabilidad reforzada (Parte I) | 2025 |
| **0049** | Estabilidad reforzada (Parte II) | 2026 |
| **0089** | Trabajo doméstico (⚠️ Inconstitucional) | 29 julio 2026 |
| **0086** | Plataformas digitales | 2026 |
| **0032** | Libertad sindical | 2026 |
| **0088** | Negociación colectiva | 2026 |
| **0040** | Vigilancia privada | 2026 |

### 2️⃣ Secciones de la App

**🔍 Circulares Derogadas**
- Grid interactivo de las 8 circulares principales
- Búsqueda por número, tema o categoría
- Click para ver detalles y normas sustitutivas

**📚 Normas Aplicables**
- Marco normativo sustitutivo para cada circular derogada
- Referencias a Código Sustantivo del Trabajo, Constitución, jurisprudencia

**📖 Guía Práctica**
- Qué deben hacer los empleadores
- Qué deben hacer los trabajadores
- Checklist de depuración normativa

**🔍 Casos de Aplicación**
- 3 casos prácticos resueltos bajo la nueva normativa
- Situación → Resultado

**⏱️ Medidas Transitorias**
- Tabla de plazos y responsables (30 y 90 días)

**📖 Referencias Normativas**
- Leyes, decretos, jurisprudencia aplicable

---

## 🚀 Despliegue a Netlify (Recomendado)

### Opción 1: Arrastra y Suelta

1. Ve a [https://app.netlify.com/drop](https://app.netlify.com/drop)
2. Arrastra la carpeta con los archivos (`index.html`, `manifest.json`, `sw.js`)
3. ¡Listo! Se genera un enlace automáticamente

### Opción 2: Git + Netlify Connect

```bash
# 1. Crea un repo en GitHub (public)
git init
git add .
git commit -m "Resolución 2708 PWA"
git branch -M main
git remote add origin https://github.com/tu-usuario/resolucion-2708.git
git push -u origin main

# 2. En Netlify:
# - New site from Git
# - Selecciona el repo
# - Build command: (dejar vacío)
# - Publish directory: (dejar como raíz)
# - Deploy
```

### Opción 3: Netlify CLI

```bash
# 1. Instala Netlify CLI
npm install -g netlify-cli

# 2. Desde la carpeta del proyecto
netlify deploy --prod

# 3. Sigue los pasos interactivos
```

---

## 📱 Instalación en Dispositivos

### Android (Chrome/Firefox)
1. Abre la app en el navegador
2. Tap en ⋮ (menú) → "Instalar aplicación"
3. Confirma

### iOS (Safari)
1. Abre la app en Safari
2. Tap en Compartir → "Añadir a la pantalla de inicio"
3. Nombra la app (sugerencia: "Res. 2708")

### Windows/Mac
1. Abre la app en Chrome/Edge
2. Haz clic en el icono de instalación (arriba a la derecha de la barra de URL)
3. Confirma

---

## 🔗 URLs de Compartición Social

Una vez deployada en Netlify, estos meta tags hacen que al compartir en redes salga:

- **Título:** Resolución 2708 de 2026 - Biblioteca Legal Colombiana
- **Descripción:** Análisis completo. Derogación de 11 circulares laborales.
- **Imagen:** Imagen representativa (og-image.png)
- **URL:** Tu enlace de Netlify

### Probar Open Graph
- [Facebook Debugger](https://developers.facebook.com/tools/debug/)
- [Twitter Card Validator](https://cards-dev.twitter.com/validator)
- [LinkedIn Inspector](https://www.linkedin.com/post-inspector/)

---

## 📂 Estructura de Archivos

```
/
├── index.html           # Aplicación principal (HTML + CSS + JS)
├── manifest.json        # Configuración PWA (instalación, iconos)
├── sw.js                # Service Worker (offline, cache)
├── README.md            # Este archivo
└── og-image.png         # Imagen para Open Graph (opcional, crear en Netlify)
```

### Generar og-image.png

Opción 1: Online (Recomendado)
- Usa [OG Image Generator](https://www.brandmark.io/tools/og-image-generator/)
- Dimensiones: 1200x630px
- Descarga como PNG

Opción 2: Localmente
```bash
# Con ImageMagick
convert -size 1200x630 xc:#1d4a8e \
  -gravity center -fill white -pointsize 72 \
  -annotate 0 "Resolución 2708" \
  og-image.png
```

Opción 3: En Netlify
- Crea la imagen localmente o en canva
- Úpela a Netlify en la carpeta raíz
- Actualiza la ruta en `index.html` (línea ~30)

---

## ⚙️ Configuración

### Cambiar Color Temático
En `index.html` busca:
```html
<meta name="theme-color" content="#1d4a8e">
```

En `manifest.json` busca:
```json
"theme_color": "#1d4a8e",
"background_color": "#ffffff"
```

### Cambiar URL Base
En `index.html` línea ~30:
```html
<meta property="og:url" content="https://biblioteca-legal-2708.netlify.app">
```

En `manifest.json`:
```json
"start_url": "/",
"scope": "/"
```

### Actualizar Dominio
Después de deployar en Netlify, cambia `biblioteca-legal-2708.netlify.app` por tu dominio personalizado en los meta tags.

---

## 🔍 Validación

### PWA Audit (Chrome DevTools)
1. Abre DevTools (F12)
2. Lighthouse → Generate Report
3. Verifica que PWA score sea 90+

### Checklist
- [ ] Manifest válido (DevTools → Application → Manifest)
- [ ] Service Worker registrado (DevTools → Application → Service Workers)
- [ ] Icono 192x192 presente
- [ ] Meta tags OG completos
- [ ] Responsive en móvil
- [ ] HTTPS en producción (Netlify lo hace automático)

---

## 🌐 Netlify Específico

### Build Settings (si los necesitas)
```
Build command: (vacío)
Publish directory: (raíz)
```

### Redirects (_redirects file, opcional)
```
/*  /index.html  200
```

### Headers (_headers file, opcional)
```
/*
  X-Frame-Options: SAMEORIGIN
  X-Content-Type-Options: nosniff
  Referrer-Policy: strict-origin-when-cross-origin
```

---

## 📊 Analytics

### Agregar Google Analytics (Opcional)
En `index.html`, antes de `</head>`:
```html
<script async src="https://www.googletagmanager.com/gtag/js?id=GA_MEASUREMENT_ID"></script>
<script>
  window.dataLayer = window.dataLayer || [];
  function gtag(){dataLayer.push(arguments);}
  gtag('js', new Date());
  gtag('config', 'GA_MEASUREMENT_ID');
</script>
```

Reemplaza `GA_MEASUREMENT_ID` con tu ID de Google Analytics.

---

## 🛡️ Seguridad

- ✅ HTTPS automático en Netlify
- ✅ CSP headers (recomendado en _headers)
- ✅ No hay conexiones externas (offline-first)
- ✅ Datos guardados localmente (IndexedDB/LocalStorage)

---

## 🐛 Solución de Problemas

### "No se instala en iOS"
- Asegúrate de tener HTTPS
- En Safari, añade primero a pantalla de inicio manualmente
- Actualiza iOS a versión reciente

### "Service Worker no funciona"
- Abre DevTools → Application → Service Workers
- Verifica que esté "activated"
- Limpia caché (DevTools → Storage → Clear site data)

### "Open Graph no muestra imagen"
- Verifica que og-image.png esté en la raíz
- Usa [Facebook Debugger](https://developers.facebook.com/tools/debug/) para cachear
- Espera 24h para que redes sociales actualicen

### "Búsqueda no funciona"
- Abre DevTools → Console
- Verifica que no haya errores de JavaScript
- Intenta limpiar caché del navegador

---

## 📝 Notas Importantes

1. **Vigencia:** Resolución 2708 rige desde el 20 de agosto de 2026
2. **Actualización:** Los nuevos protocolos del Ministerio se esperan en 30 días
3. **Fuente:** Análisis basado en comunicados oficiales del Ministerio de Trabajo
4. **Footer obligatorio:** Toda app debe incluir "Desarrollada por Vibras Positivas HM"
5. **Responsabilidad legal:** Esta es una herramienta informativa, no reemplaza asesoría legal

---

## 📞 Soporte

- **Reporte de errores:** Abre issue en GitHub
- **Solicitudes de features:** Discussions en GitHub
- **Contacto:** vibraspositivashm.com

---

## 📄 Créditos

**Desarrollada por Vibras Positivas HM — Derechos de Autor Reservados**

Biblioteca Legal Colombiana | Resolución 2708 de 2026  
Última actualización: 21 de agosto de 2026

---

## 📚 Referencias

- [Resolución 2708/2026](https://www.mincit.gov.co) - Ministerio de Trabajo
- [MDN: Progressive Web Apps](https://developer.mozilla.org/en-US/docs/Web/Progressive_web_apps)
- [Netlify Docs](https://docs.netlify.com/)
- [Código Sustantivo del Trabajo](https://www.funcionpublica.gov.co/)
