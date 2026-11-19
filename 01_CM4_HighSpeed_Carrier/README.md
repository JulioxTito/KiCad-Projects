# Raspberry Pi CM4 High-Speed Carrier Board

<p align="center">
  <img src="images/cm4_3d_render.png" alt="CM4 Carrier 3D Raytrace" width="48%">
  <img src="images/cm4_pcb_layout.jpg" alt="CM4 KiCad PCB Layout" width="48%">
</p>
<p align="center">
  <em>Figure 1: (Left) High-resolution raytraced 3D render showing M.2 NVMe SSD, RJ45, HDMI, and dual Hirose DF40 connectors. (Right) KiCad PCB Editor layout showing component clusters and high-speed routing.</em>
</p>

<p align="center">
  <img src="images/cm4_3d_top.png" alt="CM4 Top View" width="48%">
  <img src="images/cm4_3d_bottom.png" alt="CM4 Bottom View" width="48%">
</p>
<p align="center">
  <em>Figure 2: Orthogonal Top and Bottom views showing symmetrical port layout and bottom copper ground planes.</em>
</p>

## 📌 Project Summary
A custom 4-layer carrier board designed for the **Raspberry Pi Compute Module 4 (CM4)**. Engineered for high-speed edge computing, this board integrates a high-performance M.2 NVMe SSD over PCIe Gen 2, Gigabit Ethernet, 4K HDMI display output, dual USB 2.0 ports, a real-time clock (RTC), and a 40-pin GPIO expansion interface.

---

## 📐 Key Specifications
* **Host Processor**: Raspberry Pi Compute Module 4 (Broadcom BCM2711 quad-core Cortex-A72) via dual 100-pin Hirose DF40 high-density connectors.
* **Storage Interface**: M.2 Key-M socket supporting PCIe Gen 2 x1 ($5\text{ Gbps}$) NVMe Solid-State Drives.
* **Networking**: 1000BASE-T Gigabit Ethernet via integrated magnetic RJ45 jack.
* **Display Output**: Full-size HDMI 2.0 connector with integrated ESD protection.
* **Peripherals**: 2x USB 2.0 Type-A ports via onboard USB 2.0 hub; Micro-SD slot for CM4 Lite; RTC battery backup.
* **Board Dimensions**: $85\text{ mm} \times 56\text{ mm}$ (compact credit-card form factor).
* **Layer Count**: 4 Layers (Signal – Ground Reference – Power Split – Signal).

---

## ⚡ High-Speed Controlled Impedance & Stackup
Designed against the **JLCPCB JLC04161H-7628** stackup ($1.6\text{ mm}$ total thickness, FR-4 $\epsilon_r \approx 4.6$):

| Layer | Type | Copper Thickness | Dielectric / Prepreg | Nominal Dielectric Thickness |
| :--- | :--- | :---: | :--- | :---: |
| **Layer 1 (Top)** | High-Speed Signals & Local Power | $35\,\mu\text{m}$ ($1\text{ oz}$) | Prepreg 7628 | $0.21\text{ mm}$ ($8.27\text{ mils}$) |
| **Layer 2 (In1)** | **Unbroken Solid Ground Plane (GND)** | $17.5\,\mu\text{m}$ ($0.5\text{ oz}$) | FR-4 Core | $1.065\text{ mm}$ |
| **Layer 3 (In2)** | **Power Distribution Planes (+3.3V, +5V, +12V)** | $17.5\,\mu\text{m}$ ($0.5\text{ oz}$) | Prepreg 7628 | $0.21\text{ mm}$ ($8.27\text{ mils}$) |
| **Layer 4 (Bottom)**| High-Speed Signals & Low-Speed I/O | $35\,\mu\text{m}$ ($1\text{ oz}$) | — | — |

### Differential Pair Constraints
* **PCIe Gen 2 Differential Pairs** (`PCIE_TX_P/N`, `PCIE_RX_P/N`, `PCIE_CLK_P/N`):
  * Target Differential Impedance: $100\,\Omega \pm 10\%$
  * Trace Width ($W$): $0.20\text{ mm}$ | Gap ($S$): $0.18\text{ mm}$ | Intra-pair Length Mismatch: $<0.15\text{ mm}$ ($6\text{ mils}$)
* **USB 2.0 High-Speed Pairs** (`USB_D_P/N`):
  * Target Differential Impedance: $90\,\Omega \pm 10\%$
  * Trace Width ($W$): $0.30\text{ mm}$ | Gap ($S$): $0.18\text{ mm}$ | Intra-pair Length Mismatch: $<0.50\text{ mm}$

---

## 📁 Project Directory Contents
* [`hardware/`](hardware/): Complete KiCad project database (`CM4_Mini_PC.kicad_pro`), hierarchical schematics, and PCB layout (`CM4_Mini_PC.kicad_pcb`).
* [`images/cm4_3d_render.png`](images/cm4_3d_render.png): High-resolution raytraced 3D rendering.
* [`images/cm4_pcb_layout.jpg`](images/cm4_pcb_layout.jpg): KiCad PCB Editor layout and floorplan screenshot.
* [`images/CM4_PCB_Layout.pdf`](images/CM4_PCB_Layout.pdf): Vector 2D layout artwork showing copper layers and silk.
* [`images/CM4_Schematics.pdf`](images/CM4_Schematics.pdf): 7-sheet hierarchical schematic packet.
