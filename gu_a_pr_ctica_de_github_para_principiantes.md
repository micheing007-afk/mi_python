# 🚀 Guía Práctica de GitHub para Principiantes

¡Bienvenido/a a la guía esencial de Git y GitHub! Si estás empezando en el mundo del desarrollo de software, esta guía te explicará los conceptos fundamentales y te llevará paso a paso en tu primer proyecto.

---

## 📌 1. ¿Qué es Git y qué es GitHub?

Para no confundirte, lo primero es entender la diferencia entre ambos:

* **Git** es un **sistema de control de versiones**. Es como una "máquina del tiempo" para tu código que guarda el historial de cambios, permitiéndote volver a versiones anteriores si algo sale mal.
* **GitHub** es una **plataforma en la nube** que aloja tus proyectos guardados con Git. Es donde puedes colaborar con otras personas, mostrar tu trabajo y respaldar tus archivos.

---

## 🛠️ 2. Conceptos Clave que Debes Conocer

| Término | Definición Sencilla |
| :--- | :--- |
| **Repositorio (Repo)** | Es la carpeta de tu proyecto donde se guardan todos los archivos y su historial. |
| **Commit** | Es una "fotografía" o guardado de los cambios que realizaste en tu código. |
| **Branch (Rama)** | Una línea de tiempo independiente dentro de tu proyecto para probar funciones sin alterar el código principal. |
| **Main/Master** | La rama principal de tu proyecto con la versión estable o final. |
| **Pull Request (PR)** | Una petición para fusionar o unir los cambios de una rama secundaria a la rama principal. |
| **Clone** | Descargar una copia de un repositorio remoto de GitHub a tu computadora. |
| **Push** | Subir los cambios locales de tu computadora a GitHub. |
| **Pull** | Traer los cambios de GitHub a tu computadora. |

---

## 🏁 3. Preparación Inicial (Configuración)

Antes de empezar, necesitas realizar estos tres pasos:

1. **Crea una cuenta gratuita:** Ve a [GitHub.com](https://github.com) y regístrate.
2. **Instala Git:** Descárgalo e instálalo desde [git-scm.com](https://git-scm.com/).
3. **Configura tu identidad en tu computadora:** Abre tu terminal (o Git Bash) y ejecuta:

```bash
git config --global user.name "Tu Nombre"
git config --global user.email "tu_email@ejemplo.com"
```

---

## 💻 4. Tu Primer Proyecto Paso a Paso

### Paso 1: Crear un Repositorio en GitHub
1. Inicia sesión en GitHub.
2. Haz clic en el botón **"+"** arriba a la derecha y selecciona **New repository**.
3. Dale un nombre a tu repositorio (ej. `mi-primer-proyecto`).
4. Selecciona si será **Público** o **Privado**.
5. Marca la casilla **Add a README file** (el archivo donde explicas de qué trata tu proyecto).
6. Haz clic en **Create repository**.

---

### Paso 2: Clonar el Repositorio en tu Computadora
1. En la página de tu repositorio, haz clic en el botón verde **Code** y copia la URL (ej. `https://github.com/usuario/mi-primer-proyecto.git`).
2. Abre tu terminal en tu computadora y navega hasta la carpeta donde quieras guardar el proyecto.
3. Ejecuta el comando:

```bash
git clone https://github.com/usuario/mi-primer-proyecto.git
```
4. Entra a la carpeta del proyecto:

```bash
cd mi-primer-proyecto
```

---

### Paso 3: Hacer Cambios y Guardar tu Primer Commit

1. Abre la carpeta en tu editor de código favorito (como VS Code) o crea un nuevo archivo:
   ```bash
   echo "# Hola Mundo" > index.html
   ```
2. Revisa el estado de tus archivos:
   ```bash
   git status
   ```
   *(Verás el nuevo archivo en color rojo)*.

3. Prepara los archivos para guardar (Staging):
   ```bash
   git add .
   ```

4. Guarda la "fotografía" de tus cambios con un mensaje explicativo:
   ```bash
   git commit -m "Añade archivo index.html inicial"
   ```

---

### Paso 4: Subir tus Cambios a GitHub

Para enviar los cambios guardados localmente a la nube (GitHub), ejecuta:

```bash
git push origin main
```

¡Listo! Ve a tu navegador, refresca la página de tu repositorio en GitHub y verás tus nuevos archivos reflejados.

---

## 🌿 5. Flujo de Trabajo Recomendado (Uso de Ramas)

Cuando trabajas en proyectos reales, nunca debes hacer cambios directamente en la rama principal (`main`). Sigue estos pasos:

1. **Crear y cambiar a una nueva rama:**
   ```bash
   git checkout -b nueva-funcionalidad
   ```
2. **Trabajar y hacer commits:**
   ```bash
   git add .
   git commit -m "Añade formulario de contacto"
   ```
3. **Subir la rama a GitHub:**
   ```bash
   git push origin nueva-funcionalidad
   ```
4. **Crear un Pull Request:**
   * Entra a GitHub y verás un botón que dice **Compare & pull request**.
   * Revisa tus cambios, escribe un título/descripción y haz clic en **Create pull request**.
   * Si todo está correcto, presiona **Merge pull request** para integrar los cambios a la rama `main`.

---

## 📝 Comandos Rápidos de Referencia (Cheatsheet)

```bash
git status              # Ver el estado de los archivos
git log                 # Ver el historial de commits
git pull origin main    # Actualizar tu código local con el de GitHub
git branch              # Ver en qué rama te encuentras
```

---

## 💡 Consejos Finales
* **Escribe mensajes de commit claros:** Prefiere `"Corrige error en la barra de navegación"` sobre `"cambios finalisimos"`.
* **Haz commits frecuentes:** Es mejor hacer varios commits pequeños que uno gigante.
* **Usa `.gitignore`:** Crea un archivo llamado `.gitignore` para listar carpetas o claves secretas que no quieras subir a GitHub (como `node_modules` o archivos `.env`).