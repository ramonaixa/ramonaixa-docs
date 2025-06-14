# 🧠 Laboratorios Técnicos · ramonaixa-docs

Documentación real y profesional de proyectos IT:  
Sistemas, redes, homelab, virtualización, DevOps y automatización 🛠️.

Este repositorio contiene mi documentación personal organizada con [MkDocs Material](https://squidfunk.github.io/mkdocs-material/), como si fuera un portal de conocimiento técnico.

> 📚 Todo estructurado como si fuera una wiki profesional para facilitar el acceso, mantenimiento y reutilización del conocimiento.

---

## 📦 Requisitos previos

Antes de empezar, asegúrate de tener instalado:

- **Python 3.8 o superior** – Lenguaje base para MkDocs
- **pip** – Gestor de paquetes de Python (suele venir con Python)
- **Git** – Para clonar este repositorio
- **Editor recomendado:** VS Code con extensiones YAML y Markdown

---

## 🚀 Instalación del proyecto

A continuación, se describen los pasos para instalar el entorno de desarrollo en tu ordenador, tanto en **Windows** como en **macOS/Linux**.

---

### ▶️ 1. Clonar el repositorio

Descarga una copia local del proyecto con:

```bash
git clone https://github.com/ramonaixa/ramonaixa-docs.git
cd ramonaixa-docs
```
### 🧰 2. Crear y activar un entorno virtual

Crear un entorno virtual te permite aislar las dependencias del proyecto, evitando conflictos con otros proyectos o instalaciones globales.

#### 🪟 En Windows:

```powershell
python -m venv venv
.\venv\Scripts\activate
```

#### 🍏 En macOS / 🐧 Linux:

```bash
python3 -m venv venv
source venv/bin/activate
```

Verás que el terminal cambia y aparece algo como `(venv)` al principio de la línea.

### 📦 3. Instalar las dependencias

Una vez activado el entorno, instala todas las librerías necesarias ejecutando:

```py
pip install -r requirements.txt
```

Esto instalará:

- MkDocs
- Material for MkDocs
- Extensiones de Markdown
- Plugins (como tags)
- Soporte para generación de social cards

### 🖼️ 4. Requisitos para generar Social Cards automáticas

#### 🪟 En Windows:
Para que MkDocs pueda generar imágenes sociales automáticamente (opengraph.png), necesitas instalar GTK en Windows:

1. Descarga e instala GTK desde este enlace:
    
    👉 [GTK Runtime for Windows (64-bit)](https://github.com/tschoonj/GTK-for-Windows-Runtime-Environment-Installer/releases/download/2022-01-04/gtk3-runtime-3.24.31-2022-01-04-ts-win64.exe) 

2. Durante la instalación, activa la opción:

    ✅ Add GTK to PATH

3. Reinicia la terminal y activa el entorno virtual otra vez:

    ```ps
    .\venv\Scripts\activate
    ```
4. Instala los paquetes necesarios:

    ```bash
    pip install mkdocs-material[imaging]
    ```

#### 🍏 En macOS (usando Homebrew):

Para que MkDocs Material pueda generar automáticamente las imágenes sociales (opengraph.png), es necesario tener instaladas algunas librerías del sistema que utiliza cairosvg.

1. Instala las dependencias del sistema con:

    ```bash
    brew install cairo pango gdk-pixbuf libffi
    ```

2. Asegúrate de tener actualizado Python y `pip`.

3. Instala los módulos de Python necesarios:

    ```bash
    pip install mkdocs-material[imaging]
    ```

#### 🐧 En Linux (Debian/Ubuntu):

Para que MkDocs Material pueda generar automáticamente las imágenes sociales (opengraph.png), es necesario tener instaladas algunas librerías del sistema que utiliza cairosvg.

1. Instala las dependencias del sistema:

    ```bash
    sudo apt update
    sudo apt install libcairo2 libpango-1.0-0 libgdk-pixbuf2.0-0 libffi-dev
    ```
2. Después, instala el soporte de imágenes para MkDocs:

    ```bash
    pip install mkdocs-material[imaging]
    ```

✅ Una vez hecho esto, puedes ejecutar `mkdocs build` o `mkdocs serve` y MkDocs generará automáticamente una imagen `opengraph.png` para cada página con metadatos tipo `title` y `description`.

### ▶️ 5. Ejecutar el sitio en modo local

Para ver la documentación en tu navegador mientras editas, ejecuta:

```bash
mkdocs serve
```
Esto inicia un servidor local en:

📍 http://127.0.0.1:8000

El sitio se actualiza automáticamente cada vez que guardas cambios.

---

## 📁 Estructura del proyecto

```bash
ramonaixa-docs/
├── docs/               # Archivos .md de la documentación
│   ├── index.md        # Página principal
│   ├── proxmox.md      # Ejemplo de tema técnico
│   ├── tags.md         # Página para mostrar etiquetas
│   └── ...
├── stylesheets/        # Estilos CSS personalizados
│   └── extra.css
├── mkdocs.yml          # Configuración del sitio MkDocs
├── requirements.txt    # Lista de dependencias Python
└── README.md           # Este archivo
```

---

## 🌐 Despliegue en GitHub Pages (opcional)

Cuando quieras publicar tu documentación en línea, puedes usar el siguiente comando:

```bash
mkdocs gh-deploy
```

Esto compilará la documentación y la subirá a la rama `gh-pages`.
Después estará accesible desde:

🔗 https://ramonaixa.github.io/ramonaixa-docs/

---

## 🧑‍💻 Autor

Ramón Aixa

Administrador IT & entusiasta de homelab y documentación técnica

🌐 Mi web [aqui](https://www.linkedin.com/in/ramon-aixa-juan) 
📬 Contacto profesional en [LinkedIn](https://www.linkedin.com/in/ramon-aixa-juan)  
🌍 Documentación online: [ramonaixa.github.io/ramonaixa-docs](https://ramonaixa.github.io/ramonaixa-docs)
---

⚖️ Licencia

Este proyecto se distribuye bajo la licencia MIT.
Consulta el archivo LICENSE para más detalles.