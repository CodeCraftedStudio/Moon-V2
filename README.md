# 🌕 Lunar Vision - 3D Moon Visualizer Version 2

**Lunar Vision** is a highly realistic, interactive 3D web-based visualization of the Moon, built entirely within a single HTML file using **Three.js**. It features high-fidelity textures, procedural crater generation, real-time lighting, interactive Apollo landing site markers, and a dynamic 3D starfield.

## ✨ Features

- **Realistic 3D Rendering**: Utilizes `THREE.WebGLRenderer` with high-performance settings, antialiasing, and soft shadows.
- **Procedural & Authentic Textures**:
  - Uses an official Three.js high-resolution color map of the Moon.
  - Dynamically generates **Procedural Normal Maps** and **Displacement Maps** directly via the HTML `<canvas>` to create deep, realistic craters and surface roughness.
  - Features an automatic fallback to complete procedural texturing if the external texture fails to load.
- **Historical Landing Sites (Markers)**: Plots major lunar missions directly onto the 3D surface using `CSS2DRenderer`. Includes:
  - 🇺🇸 Apollo 11, 12, 14, 15, 16, & 17
  - 🇷🇺 Luna 9
  - 🇨🇳 Chang'e 4 (Far Side)
- **Advanced Lighting & Glow**: Contains an elaborate atmospheric lighting setup including Directional Sunlight, Ambient Light, Rim Light, and a subtle glowing aura (`AdditiveBlending`) around the moon.
- **Parallax Starfield**: Features a multi-layered, slow-moving 3D star environment with thousands of particles to simulate the depth of space. 
- **Interactive UI Controls**:
  - **🔲 Wireframe Mode**: Toggles the Moon's geometry into a wireframe view to observe the underlying displacement geometry and sphere structure.
  - **🔄 Auto-Rotate (Idle)**: Automatically begins rotating the camera around the Moon after 3.5 seconds of inactivity.
- **Responsive & Mobile-Ready**: Adapts automatically to window resizing and includes touch-friendly `OrbitControls` for zooming, panning, and orbiting on mobile devices.

## 🚀 How to Run

Because this project relies on ES modules (`<script type="module">`) and fetches external textures, you must run it through a local web server to prevent browser CORS (Cross-Origin Resource Sharing) restrictions.

### Option 1: Using VS Code (Recommended)
1. Open the folder containing `moon.html` in **Visual Studio Code**.
2. Install the **Live Server** extension by Ritwick Dey.
3. Right-click on `moon.html` and select **"Open with Live Server"**.

### Option 2: Using Python
If you have Python installed on your system, you can easily start a local server:
1. Open your terminal or command prompt.
2. Navigate to the directory containing `moon.html`.
3. Run the following command:
   ```bash
   # For Python 3.x
   python -m http.server 8000
   ```
4. Open your web browser and go to `http://localhost:8000/moon.html`.

### Option 3: Using Node.js (npx)
If you have Node.js installed, use the `serve` package:
1. Run this command in the folder:
   ```bash
   npx serve .
   ```
2. Visit the local address provided (usually `http://localhost:3000`).

## 🛠️ Built With

- **HTML5 & CSS3** - For layout, responsive design, and glassmorphic UI elements.
- **Three.js (v0.128.0)** - Core 3D WebGL library.
- **OrbitControls.js** - For smooth camera interaction and damping.
- **CSS2DRenderer.js** - To map DOM elements (landing site labels) to 3D spatial coordinates.

## 🎮 Controls

- **Left Click + Drag**: Rotate the camera around the Moon.
- **Scroll Wheel**: Zoom in and out.
- **Right Click + Drag**: Pan the camera.
- **Touch Devices**: One-finger drag to rotate, two-finger pinch to zoom.

## 📂 File Structure

The entire application—including styles, DOM layout, texture generation, and 3D logic—is self-contained within the single `moon.html` file. 

Enjoy exploring the lunar surface! 🚀
