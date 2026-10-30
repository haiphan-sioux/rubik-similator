# 🧊 3D Rubik's Cube Simulator

An interactive, browser-based 3D Rubik's Cube simulator built with **Three.js**. It features smooth layer animations, speedcubing notations, a solve timer, and fully customizable key bindings supporting single keys and 2-key combinations.

---

## ✨ Features

- **Realistic 3D Simulation**:
  - Built with Three.js with perspective camera and smooth lighting.
  - Orbit controls: mouse drag to rotate the viewing angle, scroll to zoom in/out.
  - 3D face labels (**U**, **D**, **F**, **B**, **R**, **L**) floating in front of each face, rotating along with cube transformations.
  - Standard speedcube color scheme: White (Up), Yellow (Down), Green (Front), Blue (Back), Red (Right), Orange (Left).

- **Standard Speedcubing Notation & Moves**:
  - **Face Moves**: `R`, `R'`, `R2`, `L`, `L'`, `L2`, `U`, `U'`, `U2`, `D`, `D'`, `D2`, `F`, `F'`, `F2`, `B`, `B'`, `B2`.
  - **Wide Moves**: `r`, `r'`, `r2`, `l`, `l'`, `l2`, `u`, `u'`, `u2`, `d`, `d'`, `d2`, `f`, `f'`, `f2`, `b`, `b'`, `b2`.
  - **Slice Moves**: `M`, `M'`, `M2`, `E`, `E'`, `E2`, `S`, `S'`, `S2`.
  - **Cube Rotations**: `x`, `x'`, `x2`, `y`, `y'`, `y2`, `z`, `z'`, `z2`.

- **Flexible Key Bindings & 2-Key Combinations**:
  - Follows standard speedcubing defaults (based on [jperm.net/3x3/moves](https://jperm.net/3x3/moves)).
  - **Customizable**: click any move in Settings (⚙) to reassign.
  - **Supports 2-key combinations**:
    - **Letter + Letter**: e.g., `R+U`, `J+K`, `A+B`
    - **Letter + Number**: e.g., `R+1`, `R+2`, `U+2`
    - **Letter + Modifier**: `R+Ctrl`, `R+Cmd`, `R+Option`, `R+Shift` (in either order)
    - **Modifier + Key/Number**: `Ctrl+R`, `Cmd+R`, `Option+1`, `Shift+R`
    - **Number + Letter / Number + Number**: `1+R`, `1+2`
    - **Single Keys**: letters, numbers (`0`–`9`), and symbols
  - Settings are automatically saved to `localStorage`.

- **Solve Timer & Move Counter**:
  - Spacebar to start and stop the inspection/solve timer.
  - Live move counter and recent move history ticker.
  - Quick **Scramble** (random 20-move state) and **Reset** buttons.

---

## 🚀 Getting Started

No build process or dependencies required. Everything runs directly in the browser via standard ES modules and CDN imports.

### Run with any static server:

```bash
# Python 3
python3 -m http.server 8080

# Or Node http-server / npx serve
npx serve .
```

Open [http://localhost:8080](http://localhost:8080) in your browser.

---

## ⌨️ Default Keyboard Controls

| Key | Action / Move | Key | Action / Move |
|:---:|:---:|:---:|:---:|
| `I` | R | `K` | R' |
| `D` | L | `E` | L' |
| `J` | U | `F` | U' |
| `L` | D | `S` | D' |
| `H` | F | `G` | F' |
| `O` | B | `W` | B' |
| `U` | r (wide) | `M` | r' (wide) |
| `V` | l (wide) | `R` | l' (wide) |
| `N` | M' (slice) | `C` | M (slice) |
| `T` | x (cube rotation) | `Y` | x' (cube rotation) |
| `;` | y (cube rotation) | `A` | y' (cube rotation) |
| `P` | z (cube rotation) | `Q` | z' (cube rotation) |
| `5` | Scramble (20 random moves) | `6` | Reset cube |
| `Space` | Start / Stop Timer | `?` | Toggle Help Overlay |

> **Tip**: Hold **Shift** + any face key for a 180° double turn (e.g. `Shift+I` = `R2`, `Shift+J` = `U2`).
