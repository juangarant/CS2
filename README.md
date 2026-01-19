# CS2 Competitive Config & Optimization Guide (AMD Ryzen + Radeon)

Este repositorio contiene mi configuración personal y pasos de optimización para **Counter-Strike 2**.
El objetivo de esta config es obtener la **máxima visibilidad en 1080p**, latencia de entrada mínima y eliminar el *stuttering* (tirones) causados por el "downclocking" en procesadores Ryzen modernos.

## 🖥️ Ajustes de Vídeo (In-Game)

Configuración optimizada para **1920x1080 (Nativa)**. Prioriza la claridad de imagen y la ventaja competitiva (sombras) sin sacrificar estabilidad.

| Opción | Valor Configurado | Notas |
| :--- | :--- | :--- |
| **Relación de Aspecto** | `Panorámica 16:9` | |
| **Resolución** | `1920 x 1080` | Nitidez máxima. |
| **Modo de Visualización** | `Pantalla Completa` | **Obligatorio** para reducir input lag. |
| **Frecuencia de Actualización** | `Máxima (Hz)` | La nativa de tu monitor. |
| **Aumentar Contraste de Jugadores** | `Habilitado` | Mejora visibilidad en zonas oscuras. |
| **V-Sync** | `Desactivado` | **CRÍTICO**. Nunca activar. |
| **AMD Anti-Lag 2.0** | `Activado` |  |
| **Multisampling (MSAA)** | `4x MSAA` | Balance perfecto calidad/rendimiento en 1080p. |
| **Calidad de Sombras Global** | `ALTA` | **Ventaja Táctica:** Permite ver sombras enemigas antes que el modelo. |
| **Sombras dinámicas** | `TODAS` |  |
| **Detalle de Modelos y Texturas** | `ALTA` | |
| **Filtrado de Texturas** | `Bilineal` | El más rápido y estable. |
| **Detalle del sombreador** | `ALTA` |  |
| **Detalle de Partículas** | `BAJO` | **Estabilidad:** Evita caídas de FPS en humos/explosiones. |
| **Oclusión Ambiental** | `Desactivado` | |
| **Alto rango dinámico (HDR)** | `Rendimiento` | |
| **FidelityFX (FSR)** | `Desactivado` | **Importante:** FSR añade latencia y emborrona en CS2. |
| **NVIDIA Reflex** | `N/A` | No aplica (GPU AMD). |

---

## 🔴 Configuración AMD Adrenalin (Drivers)

Ajustes críticos para evitar conflictos de ahorro de energía con CS2.

* **Radeon Anti-Lag 2:** `Activado` (Reduce latencia click-to-response).
* **Radeon Chill:** `DESACTIVADO` ⛔ (Causa principal de bajones de Hz en CPU).
* **Radeon Image Sharpening:** `Desactivado`.
* **Radeon Boost:** `Desactivado`.

---

## ⚡ Optimizaciones de Sistema (Anti-Stutter)

Estos pasos son necesarios para evitar que el procesador Ryzen baje frecuencias (downclocking) durante la partida.

### 1. BIOS (UEFI)
* **Global C-State Control:** `Disabled`
* **PSS Support (o Cool'n'Quiet):** `Disabled`
* **Power Supply Idle Control:** `Typical Current Idle`

### 2. Windows Power Plan
* **Plan:** `Alto Rendimiento` (High Performance).
* **Estado mínimo del procesador:** `100%`.

### 3. Process Lasso (Opcional pero recomendado)
Reglas aplicadas a `cs2.exe`:
* **CPU Priority:** `High` (Always).
* **Induce Performance Mode:** `Enabled` (Fuerza el plan "Bitsum Highest Performance" al abrir el juego).

---

## 🚀 Opciones de Lanzamiento (Launch Options)

Copiar en las propiedades del juego en Steam:

-novid -fullscreen +exec autoexec.cfg

---

### 📝 Notas adicionales
* Si se juega con ratones de **4000Hz/8000Hz**, bajar el Polling Rate a **1000Hz** si se notan tirones al mover la cámara.
* Esta configuración ha sido testeada en hardware **AMD Ryzen 7000 Series + Radeon RX Series (7800x3d + 9060XT)**.
