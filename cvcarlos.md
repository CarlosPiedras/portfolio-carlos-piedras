# REPORTE EXHAUSTIVO DEL PROYECTO CV_CARLOS

## 1. INFORMACIÓN GENERAL DEL PROYECTO

**Ubicación:** `/home/cpiedrasj/proyectos/cv_carlos`

**Tipo de proyecto:** CV/Portfolio personal interactivo desarrollado con Next.js 15

**Tamaño del proyecto:** 745 MB (incluye node_modules y archivos de build)

**Repositorio Git:** https://github.com/CarlosPiedras/cv_carlos.git

**Estado del repositorio:** Limpio, sincronizado con origin/main

---

## 2. TECNOLOGÍAS Y DEPENDENCIAS

### Framework y Librerías Principales
- **Next.js:** v15.5.4 (con App Router)
- **React:** v19.1.1
- **React DOM:** v19.1.1
- **TypeScript:** v5
- **Tailwind CSS:** v4 con PostCSS
- **Lucide React:** v0.544.0 (iconos)
- **Nodemailer:** v7.0.6 (envío de emails)

### Dependencias de Desarrollo
- **ESLint:** v9 con configuración Next.js
- **@tailwindcss/postcss:** v4
- **@types/node, @types/react, @types/react-dom:** TypeScript types
- **@types/nodemailer:** v7.0.1

### Fuentes Tipográficas
- **Open Sans:** Fuente principal (Google Fonts)
- **Oswald:** Títulos y encabezados (Google Fonts)
- **Geist Mono:** Tipografía monoespaciada

---

## 3. ESTRUCTURA DEL PROYECTO

```
cv_carlos/
├── src/
│   └── app/
│       ├── api/
│       │   └── send-email/
│       │       └── route.ts          # API endpoint para formulario
│       ├── page.tsx                  # Página principal del CV
│       ├── layout.tsx                # Layout raíz con metadata
│       ├── globals.css               # Estilos globales
│       └── favicon.ico
├── public/
│   ├── VideoHero.mp4                 # Video hero (3.8MB)
│   ├── sobre-mi-2024.jpeg            # Foto perfil (2.9MB)
│   ├── Presupuesto.png               # Ilustración formulario (240KB)
│   ├── hero-bg.png, hero-portrait.png, yo.png, sobre.png
│   ├── projects/
│   │   ├── geomadrid-v2.png          # Screenshot proyecto (671KB)
│   │   ├── movana-v2.png             # Screenshot proyecto (466KB)
│   │   └── feedback-v2.png           # Screenshot proyecto (216KB)
│   └── *.svg                         # Íconos varios
├── imagenes/                         # Carpeta adicional con imágenes
│   ├── VideoHero.mp4
│   ├── Sobremi.jpeg (2.9MB)
│   ├── Yo.png (1.5MB)
│   └── 1.png
├── package.json
├── tsconfig.json
├── next.config.ts
├── postcss.config.mjs
├── eslint.config.mjs
├── README.md
├── AGENTS.md                         # Guías para desarrollo
└── .gitignore
```

---

## 4. INFORMACIÓN DEL CV - DATOS PERSONALES

**Nombre:** Carlos Piedras

**Título profesional:** "Desarrollador Web Full Stack"

**Eslogan principal:** "TRANSFORMO IDEAS EN EXPERIENCIAS DIGITALES EXTRAORDINARIAS"

**Subtítulo:** "Donde la visión estratégica se encuentra con la ejecución perfecta"

**Email de contacto:** carlospiedrasjimenez@gmail.com

**Perfil profesional:**
- Perfil técnico con alma creativa
- Fan de la naturaleza y el deporte
- Formación en administración de redes y diseño web
- Experiencia en empresas del sector tecnológico
- Freelance desarrollando soluciones digitales
- Enfoque práctico, seguro y de valor real

---

## 5. PROYECTOS DESTACADOS EN EL PORTFOLIO

### Proyecto 1: GeoMadrid
- **URL:** https://geomadrid.es/
- **Descripción:** Plataforma web informativa con enfoque en geolocalización y servicios digitales
- **Imagen:** `/projects/geomadrid-v2.png`
- **Colores:** Gradiente sky-500 → sky-600 → slate-900
- **Nota:** Página de oposiciones de bomberos

### Proyecto 2: Movana
- **URL:** https://movana.codemasterpartner.es/
- **Descripción:** Proyecto digital centrado en soluciones personalizadas para experiencias de usuario
- **Imagen:** `/projects/movana-v2.png`
- **Colores:** Gradiente indigo-500 → purple-500 → sky-600
- **Propuesta de valor:** "Sentir juntos es más fácil"

### Proyecto 3: BP Feedback
- **URL:** https://www.bpfeedback.com/
- **Descripción:** Herramienta web de gestión y análisis de feedback en entornos profesionales
- **Imagen:** `/projects/feedback-v2.png`
- **Colores:** Gradiente amber-500 → orange-500 → rose-500
- **Especialidad:** Consultora de clima laboral

---

## 6. METODOLOGÍA DE TRABAJO (4 PASOS)

### Paso 01: Contacto cercano
- **Icono:** Handshake (manos estrechadas)
- **Descripción:** Abrimos conversación para comprender objetivos, alcance y equipo involucrado
- **Gradiente:** sky-400/70 → sky-400/30 → sky-400/10

### Paso 02: Planificación clara
- **Icono:** Compass (brújula)
- **Descripción:** Defino diagnóstico, roadmap y entregables clave para asegurar claridad compartida
- **Gradiente:** sky-500/70 → sky-500/35 → sky-500/15

### Paso 03: Creación iterativa
- **Icono:** Wrench (herramienta)
- **Descripción:** Construyo soluciones iterativas con prototipos y avances visibles en cada sprint
- **Gradiente:** sky-600/70 → sky-600/40 → sky-600/20

### Paso 04: Entrega con métricas
- **Icono:** Rocket (cohete)
- **Descripción:** Realizamos handoff completo, medimos impacto y trazamos mejoras continuas
- **Gradiente:** sky-700/70 → sky-600/45 → sky-500/25

---

## 7. FUNCIONALIDADES TÉCNICAS IMPLEMENTADAS

### 7.1 Sistema de Navegación Dual
El sitio implementa DOS sistemas de navegación sincronizados:

1. **Navegación estática en hero:** Visible cuando el usuario está en la parte superior
2. **Navegación fija flotante:** Aparece/desaparece según dirección del scroll
   - Aparece al hacer scroll hacia arriba
   - Se oculta al hacer scroll hacia abajo (excepto si el menú móvil está abierto)
   - Solo funciona después de salir del hero (>100vh)

**Secciones de navegación:**
- Sobre mí (#sobre-mi)
- Proyectos (#proyectos)
- Metodología (#metodologia)
- Presupuesto (#presupuesto)

### 7.2 Menú Hamburguesa Móvil
- Animación suave de transformación de barras
- Menú desplegable con efectos de transición
- Puntos de color distintos por sección
- Cierre automático al hacer clic en enlace

### 7.3 Formulario de Contacto/Presupuesto
**Campos del formulario:**
- Nombre (requerido)
- Email (requerido)
- Teléfono (opcional)
- Descripción del proyecto (textarea)
- Checkbox de política de privacidad (requerido)

**Estados del formulario:**
- Loading state con spinner
- Mensajes de éxito/error
- Reset automático tras envío exitoso
- Validación HTML5

**API de envío:**
- Endpoint: `/api/send-email` (POST)
- Backend: Nodemailer con Gmail SMTP
- Destinatario: carlospiedrasjimenez@gmail.com
- Asunto: "PRESUPUESTO WEB"
- Variables de entorno requeridas:
  - `EMAIL_USER`: Cuenta Gmail
  - `EMAIL_PASS`: App password de Gmail

### 7.4 Optimizaciones de Rendimiento
- **useRef para lastScrollY:** Previene re-renders infinitos en scroll listener
- **Passive event listener:** `{ passive: true }` para mejor performance
- **Imágenes optimizadas:** Uso de `next/image` con:
  - Prop `priority` en imagen hero (LCP)
  - Prop `sizes` responsive
  - Lazy loading automático
- **Video autoplay:** Video hero con autoPlay, loop, muted, playsInline

### 7.5 Animaciones CSS Personalizadas
```css
@keyframes wave          # Efecto ondulante en texto del hero
@keyframes gentle-fade-in
@keyframes gentle-rise
@keyframes float
@keyframes sparkle
```

### 7.6 Sistema de Diseño
**Colores principales:**
- Sky (azul cielo): sky-400 a sky-700
- Indigo: indigo-500 a indigo-700
- Purple: purple-500 a purple-700
- Slate (grises): slate-100 a slate-900

**Gradientes característicos:**
- Primario: `from-sky-600 via-indigo-600 to-purple-600`
- Backgrounds: Degradados sutiles con opacidad

**Modo oscuro:** Soporte completo con `prefers-color-scheme: dark`

---

## 8. CONFIGURACIONES DEL PROYECTO

### 8.1 TypeScript (tsconfig.json)
- Target: ES2017
- Modo estricto habilitado
- Module resolution: bundler
- Path alias: `@/*` → `./src/*`
- Plugin de Next.js integrado

### 8.2 ESLint
- Configuración: `next/core-web-vitals` y `next/typescript`
- Ignora: node_modules, .next, out, build, next-env.d.ts

### 8.3 PostCSS
- Plugin: `@tailwindcss/postcss`

### 8.4 Next.js Config
- Configuración mínima (sin opciones personalizadas adicionales)

### 8.5 Git Ignore
- Ignora: node_modules, .next, build, archivos .env, archivos de debug

---

## 9. SCRIPTS NPM DISPONIBLES

```json
"dev": "next dev"           # Servidor desarrollo con Turbopack
"build": "next build"       # Build producción
"start": "next start"       # Servidor producción
"lint": "eslint"           # Linter
```

---

## 10. METADATA Y SEO

**Título:** "Carlos Piedras - Desarrollador Web Full Stack"

**Descripción:** "Transformo ideas en experiencias digitales extraordinarias. Desarrollador web con experiencia en diseño UX/UI, React, Next.js y soluciones digitales a medida."

**Keywords:** desarrollador web, diseño web, freelance, React, Next.js, desarrollo frontend, Carlos Piedras

**OpenGraph:**
- Type: website
- Locale: es_ES
- Optimizado para compartir en redes sociales

**Idioma:** Español (es)

---

## 11. HISTORIAL DE COMMITS RECIENTES

```
8f62756 - feat: refine scroll behavior and layout adjustments
b85d408 - feat: adjust hero section layout and video styling
6ac4e70 - feat: improve hero section layout and typography
f3c31dc - aaa
501c5ab - VERSION ORDENADOR 2
9620382 - feat: enhance video section with improved styling
8457f80 - Refactor code structure for improved readability
8c929f3 - feat: enhance navigation and SEO with performance optimizations
4b4a988 - VERSION ORDENADOR
3903026 - fix: adjust scroll behavior and margin for sections
```

---

## 12. DOCUMENTACIÓN DISPONIBLE

### README.md
- Documentación estándar de Next.js
- Instrucciones para ejecutar el proyecto
- Enlaces a recursos de Next.js

### AGENTS.md
Guías completas para desarrollo que incluyen:
- Estructura de módulos y organización
- Comandos de build, test y desarrollo
- Convenciones de código y estilo
- Guidelines de testing (no implementado aún)
- Pautas para commits y PRs
- Tips de seguridad y configuración

### CLAUDE.md (en caché del sistema)
Documentación detallada sobre:
- Comandos de desarrollo
- Arquitectura del proyecto
- Estructura de componentes
- Configuraciones de fuentes y estilos
- Testing guidelines
- Rutas API
- Optimizaciones de performance
- Actualizaciones de contenido
- Detalles de implementación del sistema de navegación

---

## 13. CONFIGURACIÓN DE PERMISOS (.claude/settings.local.json)

Permisos configurados para Claude Code:
- Lectura completa de `/home/cpiedrasj/**`
- Comandos npm: build, install, dev, lint
- Comandos del sistema: rm, pkill, curl, cp, ffprobe
- Acceso a screenshots de Windows

---

## 14. DISEÑO Y UX

### Características de Diseño
- **Responsive design:** Mobile-first con breakpoints sm, md, lg, xl, 2xl
- **Glassmorphism:** Elementos con backdrop-blur y transparencias
- **Bordes redondeados:** rounded-xl, rounded-2xl, rounded-3xl
- **Sombras dinámicas:** shadow-sm a shadow-xl con hover effects
- **Micro-interacciones:** Hover states con translate, scale, opacity
- **Elementos decorativos:** Puntos, líneas de gradiente, efectos visuales

### Secciones de la Página
1. **Hero Section (100vh):**
   - Video en loop como elemento visual
   - Título grande con gradientes
   - Subtítulo animado con efecto wave
   - Grid layout responsive

2. **Sobre Mí:**
   - Texto descriptivo en tarjeta
   - Foto profesional grande
   - Líneas decorativas de gradiente
   - Layout de 2 columnas en desktop

3. **Proyectos:**
   - Grid de 3 tarjetas en desktop
   - Scroll horizontal en móvil
   - Screenshots de cada proyecto
   - Enlaces externos con efecto hover

4. **Metodología:**
   - Grid de 4 pasos (2x2 en desktop)
   - Iconos de Lucide React
   - Gradientes progresivos por paso
   - Líneas decorativas conectoras

5. **Presupuesto:**
   - Formulario funcional de contacto
   - Ilustración decorativa
   - Badge "Gratis y sin compromiso"
   - Emojis animados

6. **Footer:**
   - Simple con copyright
   - Diseño minimalista

---

## 15. VARIABLES DE ENTORNO NECESARIAS

Para que el formulario de contacto funcione, se requieren:

```env
EMAIL_USER=tu-email@gmail.com
EMAIL_PASS=tu-app-password-gmail
```

**Nota:** El password debe ser un "App Password" de Gmail, no la contraseña regular.

---

## 16. RECURSOS VISUALES

### Videos
- `VideoHero.mp4` (3.8MB) - Video principal en loop para hero section

### Imágenes de Perfil
- `sobre-mi-2024.jpeg` (2.9MB) - Foto profesional actual
- `yo.png` (269KB) - Retrato alternativo
- `hero-portrait.png` (536KB) - Retrato para hero

### Imágenes de Proyectos
- `geomadrid-v2.png` (671KB)
- `movana-v2.png` (466KB)
- `feedback-v2.png` (216KB)

### Ilustraciones
- `Presupuesto.png` (240KB) - Ilustración formulario

### SVGs
- next.svg, vercel.svg, globe.svg, file.svg, window.svg

---

## 17. CARACTERÍSTICAS TÉCNICAS AVANZADAS

### Client-Side Rendering
- Página principal marcada con `'use client'`
- Hooks de React: useState, useEffect, useRef
- Event listeners optimizados

### Scroll Behavior
- `scroll-behavior: smooth` en CSS global
- `scrollMarginTop: '-2rem'` en secciones para offset de navegación

### Accesibilidad
- Atributos ARIA: aria-label, aria-hidden, aria-expanded
- Elementos semánticos: header, nav, main, section, article, footer
- Focus states visibles con outline
- Alt text descriptivo en imágenes
- Screen reader only content con `.sr-only`

### Performance
- Turbopack en modo desarrollo
- Optimización automática de Next.js
- Code splitting automático
- Cache de imágenes de Next.js

---

## 18. OPORTUNIDADES DE MEJORA IDENTIFICADAS

Según AGENTS.md, hay áreas sin implementar:
- **Testing:** No hay framework de testing configurado
  - Recomendación: Vitest + Testing Library
  - Target: 80% coverage en nuevos módulos
  - Script `npm run test` pendiente

---

## 19. RESUMEN EJECUTIVO

**CV_Carlos** es un portfolio web personal profesional y moderno desarrollado con las últimas tecnologías del ecosistema React/Next.js. El proyecto presenta:

- **Diseño visual impactante** con gradientes vibrantes y animaciones sutiles
- **Experiencia de usuario fluida** con navegación intuitiva y responsive
- **Funcionalidad completa** incluyendo formulario de contacto con backend
- **Código limpio y bien estructurado** siguiendo mejores prácticas de Next.js 15
- **Performance optimizada** con lazy loading y caching inteligente
- **SEO optimizado** con metadata completa y estructura semántica

El CV digital presenta a **Carlos Piedras** como un desarrollador full-stack con experiencia en diseño web, administración de redes, y desarrollo de soluciones digitales. El portfolio destaca tres proyectos principales (GeoMadrid, Movana, BP Feedback) y presenta una metodología de trabajo estructurada en 4 pasos claros.

---

## 20. ARCHIVOS PRINCIPALES DEL CÓDIGO

### /src/app/page.tsx (840 líneas)
Archivo principal que contiene:
- Componente Home con toda la lógica
- Arrays de datos: PROJECTS, METHODOLOGY_STEPS
- Sistema de navegación dual
- Todas las secciones del CV
- Formulario de contacto
- Lógica de scroll y menú móvil

### /src/app/layout.tsx (52 líneas)
- Configuración de fuentes Google
- Metadata SEO completa
- RootLayout con providers

### /src/app/globals.css (96 líneas)
- Import de Tailwind
- Variables CSS custom
- Theme tokens
- Animaciones personalizadas
- Configuración de fuentes

### /src/app/api/send-email/route.ts (60 líneas)
- Endpoint POST para formulario
- Integración con Nodemailer
- Validaciones de campos
- Manejo de errores

---

**FIN DEL REPORTE EXHAUSTIVO**

Esta documentación contiene toda la información disponible del proyecto CV_Carlos, incluyendo estructura de archivos, código fuente, configuraciones, dependencias, contenido del CV, proyectos, metodología, funcionalidades técnicas, y documentación.
