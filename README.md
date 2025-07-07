# From Now On - Sitio Web

## Problemas Identificados y Soluciones

### ✅ Problemas Corregidos:

1. **Error en app.js (línea 85)**: Variable `mediaSrc` no definida
   - **Solución**: Cambiado a `mediaElement.src`

2. **Error de sintaxis en home.html**: Barra invertida extra
   - **Solución**: Eliminada la barra invertida

3. **Problema con particles.js**: Archivo JSON cargado como script
   - **Solución**: Implementado fetch para cargar la configuración correctamente

4. **Error en Bstyles.css**: Valor CSS extremadamente grande (1200vw)
   - **Solución**: Cambiado a 8vw

### ⚠️ Problemas Pendientes:

#### 1. Archivos de Video (Git LFS)
Los archivos de video en la carpeta `VID/` están usando Git LFS y no están descargados:
- `vid1.mp4` (debería ser ~8.6MB)
- `vid2.mp4` (debería ser ~8.6MB) 
- `vid3.mp4` (debería ser ~8.6MB)

**Para solucionar:**
```bash
# Instalar Git LFS si no está instalado
git lfs install

# Descargar los archivos LFS
git lfs pull

# O clonar el repositorio con LFS
git clone --recurse-submodules [URL_DEL_REPOSITORIO]
```

#### 2. Verificación de Archivos de Audio
Los archivos de audio parecen estar correctos:
- `In_My_Arms_By_Kid_Jones.mp3` (6.2MB)
- `Late_Night_Thoughts_By_Daniel_Pupp.mp3` (8.1MB)
- `Up_And_Down_By_Emi_Massmer.mp3` (12MB)

### 🚀 Cómo Ejecutar el Proyecto:

1. **Servidor Local:**
   ```bash
   # Python 3
   python -m http.server 8000
   
   # O Python 2
   python -m SimpleHTTPServer 8000
   
   # O con Node.js
   npx http-server
   ```

2. **Abrir en navegador:**
   ```
   http://localhost:8000
   ```

### 📁 Estructura del Proyecto:

```
FromNowOn-main/
├── index.html              # Página de bienvenida
├── HTML/
│   ├── home.html          # Página principal
│   ├── about.html         # Página sobre nosotros
│   ├── contact.html       # Página de contacto
│   └── behindthescenes.html # Behind the scenes
├── CSS/
│   ├── stylesWelcome.css  # Estilos de bienvenida
│   ├── style.css          # Estilos principales
│   ├── styleAbout.css     # Estilos de about
│   ├── Bstyles.css        # Estilos de contacto
│   └── stylesbehindscenes.css # Estilos BTS
├── JS/
│   ├── welcomeApp.js      # Lógica de bienvenida
│   ├── app.js             # Lógica principal
│   ├── about.js           # Lógica de about
│   ├── audioManager.js    # Gestor de audio
│   ├── scriptbehindscenes.js # Lógica BTS
│   ├── particles.min.js   # Librería particles
│   └── particlesjs-config.json # Config particles
├── AUDIO/                 # Archivos de audio
├── VID/                   # Archivos de video (LFS)
└── IMG/                   # Imágenes
```

### 🔧 Funcionalidades Principales:

1. **Página de Bienvenida**: Selección de música y animación de texto
2. **Slider de Videos**: Navegación con rueda del mouse
3. **Reproductor de Audio Global**: Continúa entre páginas
4. **Galería Behind the Scenes**: Efecto 3D con mouse
5. **Carousel de Clientes**: Navegación automática
6. **Efectos Particles**: Fondo animado en About

### 🐛 Posibles Problemas Adicionales:

1. **CORS**: Si usas un servidor local, algunos navegadores pueden bloquear recursos
2. **Autoplay**: Los navegadores modernos bloquean autoplay de audio/video
3. **Responsive**: Verificar en diferentes tamaños de pantalla

### 📞 Contacto:
Para soporte técnico: info@fromnowon.it 