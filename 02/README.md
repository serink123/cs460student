# CS460 Assignment 2 - XTK Cube Art Visualization

An interactive, animated 3D WebGL art visualization built with the **XTK (The X Toolkit)** framework and **dat.GUI**, created based on the hand-drawn concept sketch.

---

## 🎨 Visualization Design & Features

### 1. The Core Cube (Black Background)
- Centered 3D base cube ($28 \times 28 \times 28$) set against a pure `#000000` pitch-black background.
- Charcoal/basalt core structure that responds dynamically to internal and external lighting.

### 2. Green Spikes (2 Sides: Top & Bottom Faces)
- Protruding 3D pyramid/cone spikes pointing outwards from the top ($+Y$) and bottom ($-Y$) faces.
- **Interactive Sizing & Controls**:
  - `Spike Sizing (Height)`: Dynamically adjusts spike length from subtle needles to massive horns ($4$ to $45$).
  - `Spike Base Width`: Controls thorn caliber and sharpness.
  - `Spike Density`: Changes the grid resolution ($3\times3$ to $6\times6$).
  - `Organic Sway`: Realistic breathing/swaying idle animation.
  - **Color**: Vibrant emerald-to-chartreuse gradient with glistening specular tips.

### 3. Rough Stone-Like Texture (2 Sides: Left & Right Faces)
- Rugged, craggy 3D rock relief on the left ($-X$) and right ($+X$) faces.
- **Interactive Sizing & Controls**:
  - `Stone Sizing (Scale)`: Modulates the crater frequency and bump scale from fine gravel to giant boulders.
  - `Relief Depth`: Extrudes or flattens the 3D rocky chiseled facets.
  - `Stone Palette`: Switch between *Basalt Charcoal*, *Granite Grey*, *Lunar Slate*, and *Obsidian*.
  - **Lighting Reaction**: Sharp facet normals cast dramatic grazing shadows and highlights as the light source moves across.

### 4. Blood Vessels with Pumping Mechanism (2 Sides: Front & Back Faces)
- Intricate dendritic vascular arborization spanning the front ($+Z$) and back ($-Z$) faces.
- **Pumping Mechanism**:
  - Cardiac cycle simulation with dual-peak systolic pulse profile ($P_1$ ventricular ejection, $P_2$ dicrotic notch rebound).
  - Physical dilation: vessels physically expand and throb in thickness on each beat.
  - Color pulsation: pulses between deep deoxygenated venous maroon and glowing oxygenated arterial scarlet.
- **Interactive Controls**:
  - `Vessel Sizing`: Adjusts resting vascular caliber ($0.5$ to $4.0$).
  - `Pump Rate (BPM)`: Speeds up or slows down the pulse rate ($35$ to $175$ BPM).
  - `Pump Amplitude`: Controls systolic dilation intensity.
  - `Heartbeat Sound`: Procedural Web Audio API synthesizer generating realistic $S_1$ ("LUB") and $S_2$ ("DUB") heart sounds.

### 5. Movable 3D Light Source ("Move Through the Cube")
- A luminous glowing 3D sun orb with radiating coronal light rays.
- **Move Through Cube Feature**:
  - User can fly the light source in full 3D space ($X, Y, Z \in [-55, 55]$).
  - When the light enters the interior of the cube ($|X|, |Y|, |Z| < 14$):
    - The cube shell becomes semi-translucent.
    - Light radiates outward from the core, illuminating the fissures in the stone, roots of the spikes, and blood vessels from within!
  - **Path Animations**:
    - `Pass Core (Z)`: Flies smoothly through back face, center core $(0,0,0)$, and out the front.
    - `Pass Core (Y)`: Flies from bottom to top through the spikes.
    - `Pass Core (X)`: Flies from left to right through the stone.
    - `Orbit Light`: Continuous spherical orbit illuminating each face in sequence.
  - **Sketch Presets**: One-click jump to the 3 specific angles shown in the sketch:
    - *Top (Spikes)*
    - *Right (Stone)*
    - *Front (Vessels)*

---

## 🕹️ Controls & Navigation

### Mouse / Touch
- **Left Click + Drag**: Rotate the camera/cube freely in 3D.
- **Right Click / Scroll Wheel**: Zoom in and out.
- **Middle Click + Drag**: Pan the camera.

### Keyboard Shortcuts
- `Arrow Keys`: Move light source along $X$ and $Y$ axes.
- `W / S`: Move light source along $Z$ axis (forward / backward / through cube).
- `Spacebar`: Trigger smooth core pass.
- `H`: Toggle realistic heartbeat audio synthesizer on/off.
- `Esc`: Close sketch comparison modal.

---

## 📁 Files
- [index.html](file:///Users/serinkitery/cs460student/02/index.html): Complete WebGL visualization application.
- [sketch.jpeg](file:///Users/serinkitery/cs460student/02/sketch.jpeg): Reference hand-drawn concept sketch.
