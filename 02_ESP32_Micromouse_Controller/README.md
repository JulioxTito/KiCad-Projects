# ESP32-S3 Micromouse Robot Controller

<p align="center">
  <img src="images/board_iso_front.png" alt="ESP32 Micromouse 3D Isometric View" width="48%">
  <img src="images/board_layout.png" alt="ESP32 KiCad PCB Layout" width="48%">
</p>
<p align="center">
  <em>Figure 1: (Left) High-resolution raytraced 3D isometric perspective showing the ESP32-S3 module, USB-C port, and headers. (Right) KiCad PCB Editor layout with ground plane flood and thermal relief spokes.</em>
</p>

<p align="center">
  <img src="images/board_top_3d.png" alt="Top-Down 3D View" width="48%">
  <img src="images/board_bottom_3d.png" alt="Bottom Ground Plane View" width="48%">
</p>
<p align="center">
  <em>Figure 2: (Left) Top orthogonal assembly layout. (Right) Bottom ground plane flood with thermal relief spoke connections.</em>
</p>

<p align="center">
  <img src="images/board_iso_back.png" alt="Reverse Angle 3D View" width="75%">
  <br>
  <em>Figure 3: Rear isometric perspective illustrating chassis mounting clearances, motor driver header, and sensor breakouts.</em>
</p>

## 📌 Project Summary
A custom 2-layer autonomous robotics motherboard engineered for an IEEE Micromouse competition robot. Powered by the **ESP32-S3** dual-core microcontroller with onboard Wi-Fi and Bluetooth LE, this board integrates dual high-efficiency H-bridge motor drivers, optical quadrature encoder interfaces, multi-channel infrared distance sensor headers, and onboard DC-DC buck regulation.

---

## 📐 Key Specifications
* **Microcontroller**: Espressif ESP32-S3-WROOM-1 (240 MHz dual-core Xtensa LX7, 512 KB SRAM, 8 MB Flash).
* **Motor Drive Architecture**: Dual integrated H-bridge drivers capable of bidirectional PWM speed and direction control.
* **Sensor Interfaces**:
  * 4x IR distance sensor analog inputs with filtered reference rails.
  * Dual optical quadrature encoder inputs for closed-loop odometry and PID trajectory tracking.
* **Power Management**:
  * 2S LiPo battery input ($7.4\text{ V} - 8.4\text{ V}$).
  * High-efficiency DC-DC step-down buck converter delivering stable $+3.3\text{ V}$ and $+5.0\text{ V}$ logic rails.
* **Connectivity & Debug**: USB Type-C interface with dual 5.1 kΩ CC pull-down resistors for native USB serial/JTAG flashing.
* **Layer Count**: 2 Layers (Top Component/Signal + Bottom Ground Pour).

---

## 📁 Project Directory Contents
* [`hardware/`](hardware/): KiCad project files (`esp32_micromouse_controller.kicad_pro`), schematics, PCB layout, and production Gerbers.
* [`images/board_iso_front.png`](images/board_iso_front.png): High-resolution raytraced 3D isometric render.
* [`images/board_layout.png`](images/board_layout.png): KiCad PCB Editor layout artwork.
* [`images/board_top_3d.png`](images/board_top_3d.png): Top-down 3D orthogonal view.
* [`images/board_bottom_3d.png`](images/board_bottom_3d.png): Bottom ground plane 3D view.
* [`images/board_iso_back.png`](images/board_iso_back.png): Reverse angle 3D view.
* [`images/ESP32_Micromouse_Schematic.pdf`](images/ESP32_Micromouse_Schematic.pdf): Complete schematic diagram.
