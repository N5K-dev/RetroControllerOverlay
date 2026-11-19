# Retro Controller Overlay (Universal + 8-Bit Audio)

Overlay de inputs estilo **retro / pixel art** diseñado para **Tekken** y juegos de lucha en directo (OBS Studio), contenido íntegramente en un único archivo `index.html` sin dependencias externas.

## Características principales

- **Compatibilidad universal de mandos:**
  - Detección automática (**Auto**) y perfiles dedicados para **PS5 / Haute42 (modo PS5/PS4 DirectInput HID)**, **PS5 DualSense / PS4 DualShock (Estándar)**, **PS3 / DirectInput**, **XInput / Xbox**, **Nintendo Switch** (HID, Pro y botones invertidos) y clones **SNES USB**.
  - Soporte completo para botones digitales, **POV Hat Switch de 8 direcciones** (diagonales incluidas), sticks analógicos con deadzone ajustable, gatillos analógicos y teclado.
  - **Asistente de mapeo rápido**, remapeo individual (permite múltiples entradas por botón) y **Monitor de Mando en Vivo**.
- **Layouts y editor de botones pixel art:**
  - Diseños intercambiables: **Cruceta Retro (D-Pad)** o **Leverless / Haute42 (Hitbox)**, y **Rombo Tekken** o **Arcade (2 filas curvas)**.
  - Presets rápidos (`Retro 4`, `Pad + Gatillos`, `Haute42 8`) y botones extra personalizables (`L1`, `R1`, `L2`, `R2`, `1+2`, `3+4`, `HEAT`, `RA`, etc.) con fuente pixel-art SVG propia (admite letras, números, `+` y símbolos `□ △ ○ ✕`).
- **Macros / combinaciones simultáneas (con D-Pad incluido):**
  - Vincula cualquier entrada física (como `R1`, `R2`, `L1`, `L2`) para iluminar múltiples botones y direcciones del D-Pad a la vez (`↑ U`, `↓ D`, `← B`, `→ F`, `1`, `2`, `3`, `4`) — ideal para `1+2`, `3+4`, `Heat Burst (2+3)`, `Rage Art (df+1+2)` o `Ki Charge`.
- **Historial de Inputs estilo Tekken:**
  - 8 direcciones pixel art + neutral (`★`), **contador de frames real a 60 FPS** (independiente de la tasa de refresco del monitor), modo **Mini Botones** o **Mini Rombo Tekken**, orientación horizontal o vertical y auto-desvanecimiento tras inactividad.
- **Audio Retro 8-Bits (Web Audio API):**
  - Sintetizador de baja latencia con volumen, forma de onda (`square`, `triangle`, `sawtooth`, `sine`), duración y frecuencias editables por dirección y botón (acordes normalizados sin saturación).

## Cómo usarlo en OBS Studio

1. **Archivo local (directo en OBS):**
   - Añade una **Fuente de navegador**, marca *Archivo local* y selecciona `index.html`.
   - Fondo 100% transparente y sin interfaz visible en directo.
   - Haz clic derecho en la fuente → **Interactuar** y pulsa **`F2`** (o mueve el ratón) para abrir el panel de configuración. Los cambios se guardan automáticamente.
2. **Configurar en navegador y llevarlo a OBS:**
   - Abre `index.html` en Chrome/Edge, configura tu mando y layout, y entra en la pestaña **OBS** → **Copiar URL para OBS** (`#cfg=...`) o **Copiar URL bloqueada** (`?lock=1#cfg=...` para ocultar el botón flotante en stream).
   - También puedes **exportar e importar tu configuración en JSON**.
3. **GitHub Pages (opcional):**
   - Si activas **GitHub Pages** en este repositorio (`Settings → Pages → Branch: main`), podrás cargar el overlay directamente por URL en OBS sin depender de archivos locales.

## Atajos de teclado

| Atajo / Parámetro | Acción |
| --- | --- |
| `F2` | Abrir / cerrar el panel de configuración |
| `Esc` | Cerrar el panel o cancelar remapeo |
| `?config=1` | Abrir directamente con el panel de configuración desplegado |
| `?lock=1` | Modo stream bloqueado (oculta por completo la barra flotante) |
| `WASD` / Flechas + `U I J K` (`1 2 3 4`) | Controles de prueba por teclado |
