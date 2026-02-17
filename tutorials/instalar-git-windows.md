# Guía Completa: Instalar Git en Windows con Winget y Configuración Inicial

## 📌 ¿Qué vamos a hacer?

* Instalar **Git** usando Winget
* Verificar que quedó bien instalado
* Configurar nombre y correo
* Ajustar rama principal
* Activar colores y editor

---

## 🚀 Paso 1: Instalar Git con Winget

Primero, abre **PowerShell o CMD como administrador**.

Ejecuta este comando:

```bash
winget install --id Git.Git -e --source winget
```

💡 ¿Qué significa?

* `--id Git.Git` → Instalamos el paquete oficial de Git
* `-e` → Coincidencia exacta
* `--source winget` → Desde el repositorio oficial

Winget descargará e instalará Git automáticamente.

---

## ✅ Paso 2: Verificar que Git se instaló correctamente

Después de la instalación, cierra y vuelve a abrir la terminal.

Ejecuta:

```bash
git --version
```

Si todo salió bien, verás algo como:

```
git version 2.xx.x.windows.x
```

Eso significa que ya está listo 🎉

---

## 🔧 Paso 3: Configuración Inicial de Git

Ahora vamos a dejar Git configurado como un profesional.

---

### 👤 1. Configurar tu nombre

```bash
git config --global user.name "Tu Nombre"
```

Ejemplo:

```bash
git config --global user.name "Alex Roel"
```

---

### 📧 2. Configurar tu correo

Usa el mismo correo que usas en GitHub:

```bash
git config --global user.email "tuemail@gmail.com"
```

---

### 🌿 3. Cambiar la rama principal a main (Recomendado)

```bash
git config --global init.defaultBranch main
```

Así todos tus proyectos nuevos usarán `main` en vez de `master`.

---

### 🎨 4. Activar colores en la terminal

```bash
git config --global color.ui auto
```

Hace que Git se vea más claro y legible.

---

### 📝 5. Configurar editor por defecto (VS Code recomendado)

Si usas VS Code:

```bash
git config --global core.editor "code --wait"
```

👉 Asegúrate de tener habilitado el comando `code` en la terminal.

---

## 🔍 Paso 4: Verificar tu configuración

Puedes revisar todo lo que configuraste con:

```bash
git config --list
```

O más limpio:

```bash
git config --global --list
```

---

# 🎯 Resultado Final

Ahora tienes:

✅ Git instalado con Winget
✅ Nombre y correo configurados
✅ Rama principal en main
✅ Editor configurado
✅ Colores activados

Ya estás oficialmente listo para trabajar con Git como desarrollador 💻🔥

