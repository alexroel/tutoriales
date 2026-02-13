# 🚀 Personalizar Visual Studio Code como un Pro

**Visual Studio Code (VS Code)** es uno de los editores más potentes y personalizables del mundo. Gracias a su flexibilidad, puedes transformarlo completamente para que se adapte a tu estilo de trabajo 💻✨

En esta guía aprenderás cómo:

* Configurar VS Code a tu gusto ⚙️
* Instalar extensiones clave 🔌
* Mejorar tu productividad 🚀
* Guardar tu configuración como backup en GitHub 🔐

---

# ⚙️ Configuraciones esenciales de VS Code

Abre tu archivo `settings.json` con:

```
Ctrl + Shift + P → Preferences: Open Settings (JSON)
```

---

## 1️⃣ Quitar el minimap

```json
"editor.minimap.enabled": false
```

---

## 2️⃣ Quitar la ruta del archivo (breadcrumbs)

```json
"breadcrumbs.enabled": false
```

---

## 3️⃣ Habilitar el ajuste automático de línea

```json
"editor.wordWrap": "on"
```

---

## 4️⃣ Ajustar fuente y tamaño (editor + terminal)

```json
"editor.fontFamily": "RobotoMono Nerd Font",
"editor.fontSize": 16,
"terminal.integrated.fontFamily": "RobotoMono Nerd Font Mono",
"terminal.integrated.fontWeight": "600",
"terminal.integrated.fontSize": 16
```

💡 Recomendación: Usa una Nerd Font para que los íconos se vean increíbles.

---

## 5️⃣ Quitar sugerencias de punto de interrupción

```json
"debug.showInlineBreakpointCandidates": false
```

---

## 6️⃣ Quitar margen de glifos

```json
"editor.glyphMargin": false
```

---

# 🎨 Extensiones para personalizar la apariencia

Estas extensiones hacen que tu VS Code se vea moderno y profesional:

* **Flow Icons** → Íconos personalizados para archivos y carpetas.
* **Fluent Icons** → Íconos inspirados en el diseño Fluent de Microsoft.
* **Symbols** → Mejora los íconos de la barra lateral y estado.
* **Themes (Temas de VS Code)** → Instala temas como Dark, Light o personalizados para cambiar completamente la estética.

🔥 Consejo: Combina un buen tema + iconos + Nerd Font para un setup visual top.

---

# 🚀 Extensiones para mejorar la productividad

Estas extensiones te ahorran tiempo y errores:

* **Auto Close Tag** → Cierra etiquetas HTML automáticamente.
* **Auto Rename Tag** → Renombra etiquetas de apertura y cierre al mismo tiempo.
* **Error Lens** → Muestra errores directamente en línea con colores visibles.
* **ESLint** → Mantiene tu código limpio y estandarizado.
* **Image Preview** → Muestra vista previa de imágenes dentro del editor.
* **Live Preview** → Visualiza cambios en tiempo real en proyectos web.
* **Path Intellisense** → Autocompletado de rutas de archivos.
* **Prettier - Code formatter** → Formatea automáticamente tu código.

💡 Si trabajas con JavaScript o TypeScript, **ESLint + Prettier** es combinación obligatoria.

---

# 🔐 Cómo guardar tu configuración como backup en GitHub

Aquí viene la parte PRO 😎

## Opción 1: Usando Settings Sync (Más fácil)

1. Ve a:

   ```
   Settings → Turn On Settings Sync
   ```
2. Inicia sesión con tu cuenta de GitHub.
3. Activa:

   * Settings
   * Extensions
   * Keybindings
   * Snippets

✅ VS Code sincronizará todo automáticamente en tu cuenta.

---

## Opción 2: Manual (Más control)

### Paso 1️⃣ Ubica tu carpeta de configuración

En Windows:

```
C:\Users\TU_USUARIO\AppData\Roaming\Code\User
```

Archivos importantes:

* `settings.json`
* `keybindings.json`
* `snippets/`

---

### Paso 2️⃣ Crea un repositorio en GitHub

1. Ve a GitHub.
2. Crea un nuevo repositorio (por ejemplo: `vscode-config`).
3. Sube esos archivos.

---

### Paso 3️⃣ Subir desde terminal

```bash
git init
git add .
git commit -m "Mi configuración personalizada de VS Code"
git branch -M main
git remote add origin https://github.com/tuusuario/vscode-config.git
git push -u origin main
```

🔥 Así tendrás tu configuración respaldada y lista para usar en cualquier PC.

---

# 🎯 Conclusión

Personalizar **Visual Studio Code** no es solo cuestión estética — es optimizar tu entorno de trabajo para ser más rápido, más cómodo y más profesional.

Un buen setup:

✔ Reduce distracciones
✔ Mejora la productividad
✔ Hace que programar sea más disfrutable


