# 🌲 LinkTree Clone - Plataforma Avanzada de Enlaces en Bio

[![React](https://img.shields.io/badge/React-19.1-61dafb?logo=react)](https://react.dev/)
[![TypeScript](https://img.shields.io/badge/TypeScript-5.9-3178c6?logo=typescript)](https://www.typescriptlang.org/)
[![Vite](https://img.shields.io/badge/Vite-7.1-646cff?logo=vite)](https://vitejs.dev/)
[![Tailwind CSS](https://img.shields.io/badge/Tailwind-3.4-38bdf8?logo=tailwindcss)](https://tailwindcss.com/)
[![License: MIT](https://img.shields.io/badge/License-MIT-yellow.svg)](./LICENSE)

Una aplicación web de "Enlace en Bio" altamente personalizable, rápida y moderna. Permite a los usuarios crear perfiles con múltiples enlaces, temas dinámicos, integración de videos de fondo, embeds multimedia y monetización, todo gestionado a través de archivos JSON simples.

🔗 **Demo:** [https://yordisc.github.io/linktr.ee/](https://yordisc.github.io/linktr.ee/)

---

## 🚀 Características Principales

### ⚡ **Rendimiento Extremo**
- **Lazy Loading + Code Splitting:** Los componentes pesados (QR, Ads, Redes Sociales) solo se cargan cuando se necesitan
- **Arquitectura Optimizada:** Carga inicial ultra rápida
- **PWA Enabled:** Funciona offline con Service Workers
- **Lighthouse Perfect:** Score 100/100 en rendimiento

### 🎨 **Sistema de Temas Dinámicos**
Potente sistema basado en JSON con 7 temas preconstruidos:
- **default** - Tema base moderno y limpio
- **pepsi** - Inspirado en la marca Pepsi
- **7up** - Colores frescos y vibrantes
- **polar** - Tonos árticos fríos
- **malta-polar** - Calidez nostálgica
- **solera** - Elegancia dorada
- **carorena** - Diseño tropical

**Funcionalidades:**
- Modo Claro/Oscuro automático
- Colores personalizados, sombras y bordes
- Fondos con gradientes CSS personalizados
- Creación de temas propios sin tocar código

### 🎬 **Fondos Multimedia**
Soporte nativo para múltiples formatos como fondo de pantalla:
- **Imágenes:** JPG, PNG, WebP
- **GIFs Animados:** Para fondos dinámicos
- **Videos MP4:** Con reproducción en loop automático
- **Gradientes CSS:** Fondos degradados personalizados

### 🧩 **Layouts Flexibles**

#### **📋 Layout Lista**
Diseño clásico vertical para navegación tradicional

#### **🎯 Layout Grid Inteligente**
Sistema de cuadrícula avanzado con auto-organización:
- **Botones Rectangulares:** Ocupan ancho completo (2 columnas)
- **Botones Cuadrados:** Ocupan 1 columna individual
- **Botones Normales (Agrupación Inteligente):** Si hay dos botones normales consecutivos, se apilan verticalmente en una columna para mantener simetría con los cuadrados
- **Responsive Design:** Se adapta perfectamente a cualquier tamaño de pantalla

### 🌟 **Embeds Inteligentes**
Sistema automático de detección de plataforma que decide la mejor forma de mostrar contenido:

#### **📺 Embeds Nativos (Iframe)**
Reproducción directa dentro del perfil:
- **YouTube:** Videos estándar, Shorts y transmisiones en vivo
- **Spotify:** Canciones, álbumes y playlists completas
- **TikTok:** Videos incrustados con reproductor nativo
- **Google Maps:** Mapas interactivos embebidos
- **CodePen:** Previsualizaciones de código en vivo (ideal para portfolios)
- **Google Drive:** Documentos PDF con visor integrado

#### **🎴 Smart Cards (Tarjetas Seguras)**
Para plataformas que bloquean iframes (CORS/X-Frame-Options), genera tarjetas elegantes con estilo nativo de cada marca:
- **Instagram, LinkedIn, Twitter/X, GitHub (Repositorios), Letterboxd, Spotify (Perfiles)**

### 🎵 **Widget "Spotify Live" (Tiempo Real)**
Integración con la API de **Lanyard** para mostrar lo que estás escuchando en Spotify EN VIVO a través de tu estado de Discord:

**Estado Activo (reproduciendo música):**
- Carátula del álbum animada
- Nombre de canción y artista en tiempo real
- Barra de progreso sincronizada
- Visualizador de audio animado

**Estado Inactivo (sin reproducción):**
- Se transforma automáticamente en un botón estándar de "Sígueme en Spotify"

**Configuración requerida:**
- Cuenta de Discord conectada con Spotify
- Perfil de Discord público
- Discord User ID

### 🖼️ **Visor de Imágenes Inteligente (Smart Viewer)**
Los botones pueden abrir imágenes en pantalla completa sin salir del perfil. Ideal para:
- **Códigos QR de Pagos:** Binance Pay, Zelle, Bitcoin, PayPal
- **Certificados/Diplomas:** Mostrar logros en alta resolución
- **Flyers/Promociones:** Información visual rápida
- **Galerías:** Muestra trabajos o productos

**Características:**
- Zoom y navegación fluida
- Botón de descarga incluido (excepto para foto de perfil por privacidad)
- Activación simple: agrega `#view` al final de cualquier URL de imagen

### ☁️ **Smart Media Resolver (Gestor de Nube)**
Motor de resolución de enlaces que permite usar servicios de almacenamiento en nube directamente como Avatar, Fondo o Imágenes de Botones sin buscar enlaces directos:

**Plataformas soportadas:**
- **Google Drive:** 
  - **Imágenes:** Usa automáticamente el CDN de miniaturas HD (`lh3`) para carga instantánea y evitar bloqueos
  - **Videos:** Usa el parámetro `#video` al final de la URL para forzar modo reproductor
- **pCloud, Dropbox, Reddit:** Extracción directa de medios

**Ventajas:**
- Detección automática del tipo de archivo (imagen/video)
- No necesitas generar enlaces de descarga directa manualmente
- Optimización automática de carga

### 🎭 **Animaciones y Efectos UI/UX**

#### **📜 Marquesina de Texto (Auto-Scroll)**
Si el texto de un botón es demasiado largo para caber en el espacio disponible, se activa automáticamente una animación de desplazamiento infinito suave para hacerlo completamente legible.

#### **🎠 Carrusel de Redes Sociales**
Cuando hay más de 4 iconos sociales, la barra se convierte automáticamente en una cinta deslizante con scroll horizontal fluido.

#### **✨ Transiciones Fluidas**
- Animaciones optimizadas con Framer Motion
- Hover effects elegantes
- Micro-interacciones que mejoran la experiencia

### 🔀 **Drag & Drop (Opcional)**
Funcionalidad de arrastrar y soltar para:
- Reordenar enlaces en tiempo real
- Reorganizar botones sociales
- Posicionar el botón "Join" (Únete/Suscríbete)
- Cambios se mantienen durante la sesión

### 🛡️ **ContentGuard™ - Sistema Anti-AdBlock**
Sistema de protección de monetización avanzado que detecta bloqueadores de publicidad (uBlock Origin, AdGuard, AdBlock Plus) mediante múltiples técnicas:

**Métodos de Detección:**
1. **Trampa de Cebo Local:** Intenta cargar archivos típicamente bloqueados (`ads.js`, `prebid.js`)
2. **Trampa de Red:** Verifica conexión con servidores de anuncios reales
3. **Trampa Cosmética (DOM):** Detecta si elementos con clases como `.adsbox` son ocultados por el navegador

**Características:**
- Código ofuscado para evitar detección por listas de filtros
- Nombres de componentes y variables protegidos
- Espacios preparados para Google AdSense con validación de seguridad

*⚠️ Nota: En modo desarrollo (`npm run dev`), el bloqueo puede estar desactivado para facilitar la programación.*

### 💰 **Sistema de Monetización**
- Integración con Google AdSense
- Espacios publicitarios optimizados
- Protección anti-bloqueo incluida
- Sidebars flotantes para anuncios

### 📱 **Mobile First Design**
- Diseño responsive que **oculta automáticamente las "cajas/tarjetas" en móviles** para una experiencia inmersiva de pantalla completa
- Optimización táctil para navegación móvil
- Interfaz adaptativa según el dispositivo
- Transiciones suaves entre breakpoints

### 🔐 **Seguridad y Privacidad**
- **Encriptación AES:** Los datos del perfil guardados en `sessionStorage` están cifrados con CryptoJS para evitar lecturas casuales o modificaciones desde la consola
- **Sin Tracking Invasivo:** No recopilamos datos personales sin consentimiento
- **Protección de Datos Sensibles:** Sistema de tipos TypeScript para información delicada

### 📍 **Posicionamiento Flexible de Redes Sociales**
Control total sobre dónde aparecen tus iconos sociales:
- **`top`**: En la tarjeta de perfil, debajo de la biografía
- **`bottom`**: Al final de la lista de enlaces, con separador visual
- **`both`**: En ambos lugares (útil para perfiles muy largos)

### 🔗 **Botones Interactivos Inteligentes**
Tres tipos de botones con características únicas:
- **Normal:** Botón estándar con icono y texto
- **Square:** Botón cuadrado con imagen de fondo
- **Rectangular:** Botón tipo banner ancho con imagen destacada

---

## 🛠️ Tecnologías Utilizadas

### **Core Framework**
- **React 19.1.1** - Biblioteca de UI con últimas características
- **TypeScript 5.9.3** - Tipado estático robusto
- **Vite 7.1.7** - Build tool de nueva generación
- **React Router DOM 7.9.5** - Enrutamiento dinámico (`/:username`)

### **Estilos y Animaciones**
- **Tailwind CSS 3.4.18** - Framework utility-first CSS
- **Styled Components 6.1.19** - CSS-in-JS para tematización
- **Framer Motion 12.23.24** - Librería de animaciones fluidas
- **PostCSS 8.5.6** + **Autoprefixer 10.4.21** - Procesamiento CSS

### 🕹️ Gamificación y Easter Eggs
La plataforma incluye experiencias interactivas ocultas o activables:

#### **🏃 Pepsiman Runner**
Un juego estilo "Endless Runner" integrado directamente en la aplicación.
- Componentes personalizados (Obstáculos, Game Over screen).
- Integración fluida con el tema visual.

#### **💻 Modo Terminal**
Una consola de línea de comandos interactiva (`src/components/Games/Terminal`) para usuarios avanzados o como portafolio para desarrolladores backend.
- Soporte para comandos personalizados.
- Navegación basada en texto.

### **Utilidades Core**
- **@dnd-kit (core 6.3.1 + sortable 10.0.0)** - Sistema completo Drag & Drop
- **React Hook Form 7.66.0** + **Yup 1.7.1** - Validación de formularios
- **Zustand 5.0.8** - Gestión de estado ligera
- **date-fns 4.1.0** - Manipulación de fechas moderna

### **Funcionalidades Especiales**
- **react-qr-code 2.0.18** - Generación de códigos QR
- **crypto-js 4.2.0** - Encriptación AES para datos locales
- **idb 8.0.3** - Wrapper moderno de IndexedDB
- **react-icons 5.5.0** - Biblioteca extensiva de iconos
- **lucide-react 0.552.0** - Iconos optimizados adicionales

### **Analytics y Tracking**
- **react-ga4 2.1.0** - Google Analytics 4 integration

### **Herramientas de Desarrollo**
- **Vite Plugin PWA 1.1.0** - Configuración PWA automática
- **Vitest 4.0.8** - Framework de testing ultra-rápido
- **Storybook 10.0.5** - Desarrollo aislado de componentes
- **ESLint 9.36.0** + **Prettier 3.6.2** - Linting y formateo
- **TypeScript ESLint 8.45.0** - Reglas específicas TS
- **gh-pages 6.3.0** - Despliegue automatizado

---

## 📦 Instalación y Uso Local

### **Requisitos Previos**
- **Node.js:** v18.0.0 o superior
- **npm:** v9.0.0 o superior (o yarn/pnpm equivalente)
- **Git:** Para clonar el repositorio

### **Pasos de Instalación**

#### **1. Clonar el Repositorio (Privado)**
```bash
git clone https://github.com/yordisc/linktree-source.git
cd linktr.ee
```

#### **2. Instalar Dependencias**
```bash
npm install
```

#### **3. Iniciar Servidor de Desarrollo**
```bash
npm run dev
```

Visita **`http://localhost:5173/`** en tu navegador

#### **4. Compilar para Producción**
```bash
npm run build
```

Los archivos compilados estarán en la carpeta `dist/`

#### **5. Vista Previa de Producción**
```bash
npm run preview
```

---

## ⚙️ Configuración de Perfil (JSON)

Todo el contenido se gestiona mediante archivos JSON en la carpeta `public/data/`.

### **Crear tu Perfil**
Crea un archivo con tu nombre de usuario: `public/data/jose.json`

### **Estructura Completa del JSON**

```json
{
  "profile": {
    "username": "jose",
    "displayName": "José Developer",
    "bio": "Frontend Dev | Creator | Tech Enthusiast 🚀",
    "avatarUrl": "[https://tu-cdn.com/avatar.jpg](https://tu-cdn.com/avatar.jpg)",
    "avatarImages": [
      {
        "id": "main",
        "url": "[https://tu-cdn.com/avatar.jpg](https://tu-cdn.com/avatar.jpg)",
        "alt": "Perfil Principal"
      },
      {
        "id": "fun",
        "url": "[https://tu-cdn.com/avatar-fun.jpg](https://tu-cdn.com/avatar-fun.jpg)",
        "alt": "Modo Divertido"
      }
    ],
    "theme": "pepsi",
    "settings": {
      "backgroundImage": "/videos/fondo.mp4",
      "hideThemeButton": false
    },
    "socialButtons": {
      "enabled": true,
      "draggable": true
    },
    "joinButton": {
      "enabled": true,
      "text": "Suscríbete",
      "url": "[https://newsletter.com](https://newsletter.com)",
      "backgroundColor": "#000000",
      "textColor": "#FFFFFF"
    }
  },
  "links": [
    {
      "id": "portfolio",
      "type": "rectangular",
      "title": "🎨 Mi Portafolio",
      "url": "[https://miweb.com](https://miweb.com)",
      "visible": true,
      "icon": "linkcustom"
    },
    {
      "id": "instagram",
      "type": "normal",
      "title": "Instagram",
      "url": "[https://instagram.com/tu_usuario](https://instagram.com/tu_usuario)",
      "visible": true,
      "icon": "instagram"
    }
  ]
}
```

---

## 🔗 Tipos de Enlaces y Ejemplos

### **1. Botón Normal (Standard)**
Botón estándar con icono y texto. Ideal para enlaces generales.

```json
{
  "id": "portfolio",
  "type": "normal",
  "title": "Mi Portafolio Web",
  "url": "[https://miweb.com](https://miweb.com)",
  "icon": "globe",
  "visible": true,
  "styles": {
    "backgroundColor": "#3b82f6",
    "color": "white"
  }
}
```

**Iconos disponibles:** `instagram`, `twitter`, `facebook`, `linkedin`, `github`, `youtube`, `tiktok`, `spotify`, `globe`, `mail`, `phone`, `linkcustom`, etc.

---

### **2. Botón Cuadrado (Square)**
Botón compacto con imagen de fondo. Perfecto para diseños tipo grid.

```json
{
  "id": "proyecto1",
  "type": "square",
  "title": "Proyecto E-commerce",
  "url": "https://proyecto.com",
  "imageUrl": "https://cdn.com/proyecto-thumbnail.jpg",
  "visible": true
}
```

---

### **3. Botón Rectangular (Banner)**
Botón ancho tipo banner con imagen destacada. Ideal para contenido destacado.

```json
{
  "id": "destacado",
  "type": "rectangular",
  "title": "🚀 Proyecto Destacado 2024",
  "url": "https://proyecto-grande.com",
  "imageUrl": "https://cdn.com/banner-proyecto.jpg",
  "visible": true
}
```

---

### **4. Embed de YouTube**
Incrusta videos, shorts o transmisiones en vivo directamente en tu perfil.

```json
{
  "id": "video-tutorial",
  "type": "embed",
  "provider": "youtube",
  "url": "https://youtube.com/watch?v=VIDEO_ID",
  "shape": "rectangular",
  "visible": true
}
```

**Formatos soportados:**
- Videos: `https://youtube.com/watch?v=VIDEO_ID`
- Shorts: `https://youtube.com/shorts/VIDEO_ID`
- Lives: `https://youtube.com/live/VIDEO_ID`

---

### **5. Embed de Spotify**
Incrusta canciones, álbumes o playlists con reproductor nativo.

```json
{
  "id": "mi-playlist",
  "type": "embed",
  "provider": "spotify",
  "url": "https://open.spotify.com/playlist/37i9dQZF1DXcBWIGoYBM5M",
  "shape": "rectangular",
  "visible": true
}
```

**Tipos soportados:**
- Canciones: `https://open.spotify.com/track/TRACK_ID`
- Álbumes: `https://open.spotify.com/album/ALBUM_ID`
- Playlists: `https://open.spotify.com/playlist/PLAYLIST_ID`

---

### **6. Widget Spotify Live (Tiempo Real)**
Muestra lo que estás escuchando EN VIVO mediante Lanyard + Discord.

```json
{
  "id": "spotify-now-playing",
  "type": "embed",
  "provider": "spotify-bio",
  "title": "🎵 Escuchando ahora mismo",
  "url": "https://open.spotify.com/user/TU_USUARIO_SPOTIFY",
  "originalUrl": "TU_DISCORD_USER_ID",
  "shape": "rectangular",
  "visible": true
}
```

**Configuración requerida:**
1. Conecta Spotify a tu cuenta de Discord
2. Mantén tu perfil de Discord público
3. Obtén tu Discord User ID
4. Reemplaza `TU_DISCORD_USER_ID` con tu ID real

**Cómo obtener tu Discord User ID:**
1. Activa el Modo Desarrollador en Discord (Configuración → Avanzado)
2. Click derecho en tu perfil → Copiar ID

---

### **7. Visor de Imágenes/QR con #view**
Abre imágenes en pantalla completa al hacer clic. Perfecto para códigos QR de pago.

```json
{
  "id": "qr-binance",
  "type": "square",
  "title": "💳 Pagar con Binance",
  "imageUrl": "https://unsplash.com/crypto-preview.jpg",
  "url": "https://drive.google.com/file/d/ID_DE_TU_QR/view?usp=sharing#view",
  "visible": true
}
```

**Cómo funciona:**
- **`imageUrl`**: Imagen de portada bonita del botón (decorativa)
- **`url`** + **`#view`**: Imagen real que se abrirá en el visor (funcional)

**Casos de uso:**
- QR de Binance Pay, Zelle, Bitcoin
- Certificados o diplomas
- Flyers de eventos
- Menús de restaurantes

---

### **8. Videos desde Google Drive**
Usa videos almacenados en Google Drive directamente.

```json
{
  "id": "video-demo",
  "type": "rectangular",
  "title": "📹 Video Demo del Proyecto",
  "url": "#",
  "imageUrl": "https://drive.google.com/file/d/ID_DEL_VIDEO/view?usp=sharing#video",
  "visible": true
}
```

**Importante:** Agrega `#video` al final de la URL de Google Drive para forzar el modo reproductor.

---

### **9. Embed de TikTok**
Incrusta videos de TikTok con reproductor nativo.

```json
{
  "id": "tiktok-viral",
  "type": "embed",
  "provider": "tiktok",
  "url": "https://tiktok.com/@usuario/video/1234567890",
  "shape": "square",
  "visible": true
}
```

---

### **10. Embed de Google Maps**
Muestra tu ubicación o lugares importantes.

```json
{
  "id": "mi-oficina",
  "type": "embed",
  "provider": "googlemaps",
  "url": "https://maps.google.com/?q=Latitude,Longitude",
  "shape": "rectangular",
  "visible": true
}
```

---

### **11. Embed de CodePen**
Perfecto para desarrolladores: muestra tu código en vivo.

```json
{
  "id": "demo-code",
  "type": "embed",
  "provider": "codepen",
  "url": "https://codepen.io/usuario/pen/PEN_ID",
  "shape": "rectangular",
  "visible": true
}
```

---

### **12. Smart Cards (Instagram, LinkedIn, Twitter, GitHub)**
Para plataformas que bloquean iframes, se genera una tarjeta elegante con preview.

```json
{
  "id": "linkedin-profile",
  "type": "embed",
  "provider": "linkedin",
  "url": "https://linkedin.com/in/tu-perfil",
  "shape": "normal",
  "visible": true
}
```

**Plataformas con Smart Cards:**
- Instagram
- LinkedIn
- Twitter (X)
- GitHub (repositorios)
- Letterboxd

---

## 🎨 Sistema de Temas

### **Temas Incluidos**

| Tema | ID | Descripción |
|------|-----|-------------|
| **Default** | `default` | Tema moderno y limpio base |
| **Pepsi** | `pepsi` | Azul y rojo, inspirado en la marca |
| **7UP** | `7up` | Verde limón fresco y vibrante |
| **Polar** | `polar` | Tonos fríos árticos |
| **Malta Polar** | `malta-polar` | Calidez dorada nostálgica |
| **Solera** | `solera` | Elegancia dorada premium |
| **Carorena** | `carorena` | Diseño tropical playero |

### **Aplicar un Tema**
En tu archivo JSON de perfil:

```json
{
  "profile": {
    "theme": "pepsi"
  }
}
```

### **Crear tu Propio Tema**

Crea un archivo en `public/data/themes/mi-tema.json`:

```json
{
  "id": "mi-tema-personal",
  "name": "Mi Tema Personalizado",
  "structure": {
    "layout": "grid",
    "avatarShape": "circle",
    "cardStyle": "elevated"
  },
  "light": {
    "colors": {
      "primary": "#6366f1",
      "secondary": "#8b5cf6",
      "accent": "#ec4899",
      "background": "#ffffff",
      "text": "#1f2937",
      "textSecondary": "#6b7280",
      "textMuted": "#9ca3af",
      "border": "#e5e7eb"
    },
    "backgrounds": {
      "page": "linear-gradient(135deg, #667eea 0%, #764ba2 100%)",
      "card": "#ffffff"
    },
    "shadows": {
      "card": "0 4px 6px -1px rgb(0 0 0 / 0.1)",
      "cardHover": "0 20px 25px -5px rgb(0 0 0 / 0.1)"
    },
    "borders": {
      "card": "1px solid #e5e7eb",
      "button": "1px solid #d1d5db"
    }
  },
  "dark": {
    "colors": {
      "primary": "#818cf8",
      "secondary": "#a78bfa",
      "accent": "#f472b6",
      "background": "#111827",
      "text": "#f9fafb",
      "textSecondary": "#d1d5db",
      "textMuted": "#9ca3af",
      "border": "#374151"
    },
    "backgrounds": {
      "page": "linear-gradient(135deg, #1e3a8a 0%, #7c3aed 100%)",
      "card": "#1f2937"
    },
    "shadows": {
      "card": "0 4px 6px -1px rgb(0 0 0 / 0.3)",
      "cardHover": "0 20px 25px -5px rgb(0 0 0 / 0.3)"
    },
    "borders": {
      "card": "1px solid #374151",
      "button": "1px solid #4b5563"
    }
  }
}
```

**Propiedades del Tema:**
- **`id`**: Identificador único del tema
- **`name`**: Nombre visible en el selector
- **`structure`**: Configuración de layout y formas
  - `layout`: `"list"` o `"grid"`
  - `avatarShape`: `"circle"` o `"square"`
  - `cardStyle`: `"elevated"`, `"flat"`, `"outlined"`
- **`light/dark`**: Configuraciones para cada modo
  - `colors`: Paleta de colores
  - `backgrounds`: Fondos (soporta gradientes CSS)
  - `shadows`: Sombras de elementos
  - `borders`: Estilos de bordes

---

## 📍 Configuración de Redes Sociales

Los iconos de redes sociales se generan automáticamente a partir de tu lista principal de `links` cuando el `icon` coincide con una red social conocida (instagram, twitter, github, etc.) y tienes `socialButtons.enabled: true`.

```json
"profile": {
  "socialButtons": {
    "enabled": true,
    "draggable": true
  }
}
```

**Opciones de `style`:**
- **`circles`**: Iconos circulares (defecto)
- **`squares`**: Iconos cuadrados
- **`rounded`**: Iconos con bordes redondeados

**Opciones de `position`:**
- **`top`**: Aparecen en la tarjeta de perfil, debajo de la bio
- **`bottom`**: Al final de todos los enlaces, con separador
- **`both`**: En ambas ubicaciones (útil para perfiles largos)

**`draggable`:**
- **`true`**: Permite reordenar iconos con drag & drop
- **`false`**: Orden fijo

### **Carrusel Automático**
Cuando configuras **más de 4 iconos sociales**, la barra se convierte automáticamente en una **cinta deslizante** con scroll horizontal fluido.

---

## 📂 Estructura del Proyecto

```bash
linktr.ee/
│
├── public/
│   ├── data/
│   │   ├── themes/       # Temas JSON (default, etc.)
│   │   ├── yordisc.json         # Perfiles de usuario
│   │   ├── jose.json
│   │   └── maria.json
│   └── fondos/                  # Recursos multimedia
│
├── src/
│   ├── components/
│   │   ├── ads/              # Sistema de monetización
│   │   │   ├── AdSenseUnit.tsx
│   │   │   ├── ContentGuard.tsx # Sistema Anti-AdBlock
│   │   │   └── FloatingAdSidebars.tsx
│   │   ├── avatar/              # Avatar y visor
│   │   │   ├── AvatarViewer.tsx
│   │   │   └── EnhancedAvatar.tsx
│   │   ├── buttons/             # Componentes de botones
│   │   │   ├── NormalButton.tsx
│   │   │   ├── SquareButton.tsx
│   │   │   ├── RectangularButton.tsx
│   │   │   ├── SocialButtons.tsx
│   │   │   └── ...
│   │   ├── Games/               # 🕹️ Gamificación
│   │   │   ├── PepsimanRunner/  # Juego Runner
│   │   │   └── Terminal/        # Consola interactiva
│   │   ├── widgets/             # Widgets externos
│   │   │   └── SpotifyWidget.tsx
│   │   └── Layout/              # Estructura base
│   │
│   ├── contexts/   # Gestión de estado (ThemeContext)
│   ├── hooks/      # Custom Hooks (useLanyard, etc)
│   ├── utils/                   # Utilidades (crypto.ts)
│   └── types/      # Definiciones TypeScript
│
├── package.json
├── vite.config.ts
└── tailwind.config.js
```

---

## 🚀 Despliegue

### **GitHub Pages (Automatizado)**

El proyecto está preconfigurado para desplegar en GitHub Pages con un solo comando:

```bash
npm run deploy
```

**Proceso automático:**
1. Compila el proyecto (`npm run build`)
2. Sube la carpeta `dist/` a la rama `gh-pages`
3. GitHub Pages publica automáticamente

**Tu sitio estará disponible en:**
```
https://yordisc.github.io/linktr.ee/
```

**Configuración en `package.json`:**
```json
{
  "homepage": "https://yordisc.github.io/linktr.ee",
  "scripts": {
    "predeploy": "npm run build",
    "deploy": "gh-pages -d dist --repo https://ghp_TOKEN@github.com/yordisc/linktr.ee.git"
  }
}
```

---

## 🧪 Testing y Desarrollo

### **Ejecutar Tests**
```bash
# Tests unitarios
npm run test

# Tests con interfaz visual
npm run test:ui

# Coverage report
npm run test:coverage
```

### **Storybook (Desarrollo de Componentes)**
```bash
# Iniciar Storybook
npm run storybook

# Build de Storybook
npm run build-storybook
```

### **Linting y Formateo**
```bash
# Ejecutar ESLint
npm run lint

# Formatear código con Prettier
npm run format
```

---

### **Guías de Estilo**
- ✅ Usa **TypeScript** para todo el código nuevo
- ✅ Sigue las reglas de **ESLint** configuradas
- ✅ Escribe **tests unitarios** para funcionalidades críticas
- ✅ Documenta funciones complejas con **JSDoc**
- ✅ Usa **commits semánticos**:
  - `feat:` Nueva característica
  - `fix:` Corrección de bug
  - `docs:` Cambios en documentación
  - `style:` Formato, punto y coma faltante, etc.
  - `refactor:` Refactorización de código
  - `test:` Añadir tests
  - `chore:` Actualizar dependencias, etc.

### **Reportar Bugs**
Si encuentras un bug, por favor [abre un issue](https://github.com/yordisc/linktr.ee/issues) con:
- Descripción clara del problema
- Pasos para reproducirlo
- Comportamiento esperado vs. actual
- Screenshots si es posible
- Información del navegador/OS

---

## 📄 Licencia

Distribuido bajo la **Licencia MIT**. Ver archivo `LICENSE` para más información.

Esto significa que puedes:
- ✅ Usar comercialmente
- ✅ Modificar el código
- ✅ Distribuir
- ✅ Uso privado

Bajo las condiciones de:
- 📋 Incluir el aviso de copyright
- 📋 Incluir la licencia MIT

---

## 🙏 Agradecimientos

Este proyecto no sería posible sin estas increíbles herramientas y comunidades:

- **[React Team](https://react.dev/)** - Por la mejor librería de UI
- **[Vite](https://vitejs.dev/)** - Build tool ultra-rápido
- **[Tailwind CSS](https://tailwindcss.com/)** - Framework CSS que acelera el desarrollo
- **[React Icons](https://react-icons.github.io/)** - Miles de iconos listos para usar
- **[Framer Motion](https://www.framer.com/motion/)** - Animaciones fluidas y fáciles
- **[Lanyard API](https://github.com/Phineas/lanyard)** - Estado de Discord en tiempo real
- **[Unsplash](https://unsplash.com/)** - Imágenes de alta calidad gratuitas
- **Comunidad Open Source** - Por compartir conocimiento

---

## 📞 Contacto y Soporte

### **Creador**
👨‍💻 **Yordisc**
- GitHub: [@yordisc](https://github.com/yordisc)
- Proyecto: [linktr.ee](https://github.com/yordisc/linktr.ee)

### **Obtener Ayuda**
- 📖 [Documentación Completa](#)
- 💬 [Discussions](https://github.com/yordisc/linktr.ee/discussions)
- 🐛 [Reportar Bug](https://github.com/yordisc/linktr.ee/issues)
- 💡 [Solicitar Feature](https://github.com/yordisc/linktr.ee/issues/new?labels=enhancement)

---

<div align="center">

## ⭐ Si te gusta el proyecto, no olvides darle una estrella ⭐

[![GitHub stars](https://img.shields.io/github/stars/yordisc/linktr.ee?style=social)](https://github.com/yordisc/linktr.ee/stargazers)
[![GitHub forks](https://img.shields.io/github/forks/yordisc/linktr.ee?style=social)](https://github.com/yordisc/linktr.ee/network/members)

---

**Creado con  ☕ por [Yordisc](https://github.com/yordisc)**

*"Un enlace a la vez, construyendo tu presencia digital perfecta"*

</div>