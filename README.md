# 🎮 2D Video Game Intro

Intro / cinemática para videojuego 2D desarrollada en Unity 6 con Universal Render Pipeline (Renderer 2D).

---

### 👨‍💻 Colaboradores

<table>
  <tr>
    <td align="center"><a style="color: black" href="https://github.com/AxelLeo129"><img src="https://github.com/AxelLeo129.png" width="100" height="100" alt="Axel Leonardo"><br>Axel Leonardo</a></td>
  </tr>
</table>

---

### 🧰 Tecnologías utilizadas

- Unity **6000.4.1f1** (Unity 6)
- C# / .NET Standard 2.1
- Universal Render Pipeline (URP) **17.4.0** — Renderer 2D
- Input System **1.19.0**
- Timeline **1.8.11**
- Visual Scripting **1.9.11**
- uGUI **2.0.0**
- Suite 2D: Animation, Aseprite, PSD Importer, SpriteShape, Tilemap + Tilemap Extras
- Unity Test Framework **1.6.0**

---

### 🔧 Requisitos previos

Antes de comenzar, asegúrate de tener instalado:

- **Unity Hub**
- **Unity 6000.4.1f1** (debe ser esta versión exacta para evitar migraciones de assets)
- **Git**
- Un IDE con soporte para C#:
    - Visual Studio 2022 con el workload **Game development with Unity** (ya declarado en `.vsconfig`), o
    - JetBrains Rider

---

### 📦 Instalación

Sigue estos pasos para configurar el proyecto localmente:

1. 📥 Clonar repositorio
    ```bash
    git clone https://github.com/AxelLeo129/2d-video-game-intro
    cd 2d-video-game-intro
    ```

2. 📂 Abrir en Unity Hub

    `Add` → `Add project from disk` → seleccionar la carpeta del proyecto.

    Unity generará las carpetas `Library/`, `Temp/` y `Logs/` en la primera importación (puede tardar varios minutos). Estas carpetas están en `.gitignore` y **no deben versionarse**.

3. ⚙️ Configuración del proyecto

    Unity no usa `.env`. La configuración vive en assets versionados:

    | Archivo | Propósito |
    |---|---|
    | `ProjectSettings/` | Ajustes globales (resolución, física, calidad, tags) |
    | `Assets/Settings/UniversalRP.asset` | Pipeline asset de URP |
    | `Assets/Settings/Renderer2D.asset` | Renderer 2D e iluminación |
    | `Assets/InputSystem_Actions.inputactions` | Mapa de acciones del Input System |

    > ⚠️ Los archivos `.meta` **sí** se versionan: Unity los usa para mantener los GUIDs que enlazan los assets entre sí.

---

### ▶️ Iniciar en modo desarrollo

1. Abrir la escena principal:
    ```
    Assets/Scenes/SampleScene.unity
    ```
2. Pulsar **Play** (`Ctrl + P`) en el editor.

Resolución de referencia: **1920×1080** (960×600 en WebGL).

---

### 🚀 Compilar para producción

Desde el editor: `File` → `Build Profiles` → seleccionar plataforma → **Build**.

También desde línea de comandos (requiere un script de build en `Assets/Editor/`):

```bash
Unity.exe -quit -batchmode -projectPath "." -executeMethod BuildScript.PerformBuild -logFile build.log
```

Los archivos generados estarán en:
```bash
/Builds/
```

---

### 🚀 Despliegue en producción

Pendiente

---

MIT
Free Software, software to learn!
