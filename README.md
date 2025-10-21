# PWA Mixta — Calendario y Contacto

Aplicación Web Progresiva (PWA) creada por Jassiel Alejandro Peralta Santos.
Proyecto de la Universidad Tecnológica Emiliano Zapata (UTEZ) — 10mo Cuatrimestre.

## 🚀 Qué incluye

- ✅ PWA con Service Worker (soporte offline básico)
- 📱 Diseño responsive y moderno (fondo oscuro con acento teal)
- 📆 Página de calendario (integración prevista con FullCalendar)
- 📝 Formulario de contacto simple (Nombre, Email, Mensaje)
- 🎨 Iconos listos en la carpeta `icons/`

## Estructura del proyecto

```
PWApp-main/
├── index.html          # Página principal (hero con "Bienvenido")
├── about.html          # Acerca de (tu biografía)
├── calendar.html       # Calendario (integración con FullCalendar)
├── form.html           # Formulario de contacto (básico)
├── style.css           # Estilos principales
├── register.js         # Registro del Service Worker
├── sw.js               # Service Worker (caché)
├── manifest.json       # Manifest de la PWA
├── icons/              # Iconos de la PWA
└── README.md           # Este archivo
```

## 📦 Cómo generar y añadir iconos

1. Abre `generate-icons.html` en tu navegador.
2. Genera o descarga los iconos.
3. Guarda los archivos en la carpeta `icons/` con los tamaños requeridos:
   - 72x72, 96x96, 128x128, 144x144
   - 152x152, 192x192, 384x384, 512x512

> Nota: el proyecto ya incluye iconos de ejemplo. Si actualizas los iconos, revisa `manifest.json` para que apunten a los archivos correctos.

## 🌐 Despliegue en GitHub Pages (pasos)

1. Subir el repositorio a GitHub (ya subido a: `https://github.com/Jassiel-APS/PWA_Mixta-10A`)

```powershell
git add .
git commit -m "Add README and docs"
git push origin main
```

2. En GitHub: ve a `Settings` → `Pages`.
3. En `Source`, selecciona rama `main` y carpeta `/ (root)`, guarda.
4. Espera unos minutos; la URL típica será `https://Jassiel-APS.github.io/PWA_Mixta-10A/`.

### Ajustes en `manifest.json` y `sw.js` para GitHub Pages

Si la URL pública tiene un subpath (por ejemplo `https://usuario.github.io/miRepo/`), actualiza `manifest.json`:

```json
{
  "start_url": "/PWA_Mixta-10A/index.html",
  "scope": "/PWA_Mixta-10A/"
}
```

Y en `sw.js` ajusta `APP_SHELL_ASSETS` para incluir el prefijo `/PWA_Mixta-10A/` en las rutas si usas rutas absolutas.

## 📱 Instalar la PWA (usuario final)

- Android (Chrome): Abrir la URL en Chrome → menú ⋮ → "Instalar" o "Añadir a pantalla de inicio".
- iOS (Safari): Abrir la URL en Safari → botón Compartir → "Añadir a pantalla de inicio".
- Desktop (Chrome/Edge): Buscar el botón de instalación (+) en la barra de direcciones.

## 🔧 Notas técnicas

- El Service Worker (`sw.js`) precachea las páginas básicas y usa cache dinámico para recursos.
- Si trabajas localmente, registra `register.js` para probar offline.
- Advertencia (Windows/Git): Git puede mostrar avisos LF↔CRLF; puedes añadir `.gitattributes` si quieres normalizar.

## ✍️ Autor

Desarrollado por **Jassiel Alejandro Peralta Santos**

Universidad Tecnológica Emiliano Zapata (UTEZ)
10mo Cuatrimestre - Ingeniería en Desarrollo y Gestión de Software

---