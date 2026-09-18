![Banniere Github_Autom](https://github.com/user-attachments/assets/0f058a29-b6db-4e5d-a5cb-125b06e851d9)
*A complete preservation and turnkey execution package for **Silver** (1999) by Infogrames, running on a pre-configured 86Box Windows 98 SE virtual machine.*

---

## 📌 Project Intent & Preservation Notice

The primary goal of **Verdante** is **digital preservation**. This project is built to ensure that a classic piece of PC gaming history remains playable, stable, and accessible on modern hardware through a meticulously tuned virtualization environment.

### The Problem with Original Code & Modern Hardware

Running the original PC release of *Silver* natively on modern hardware has long been practically impossible to maintain or execute realistically. Beyond the deep-seated engine bugs that plagued various historical versions (requiring a patchwork of community fixes just to run on shifting OS architectures of the past), the fundamental shift from 32-bit to 64-bit computing completely broke the game's internal clock structures and time management. Trying to keep the native game functional on modern hardware requires constant, costly intervention that quickly becomes unsustainable.

### The Compromises of the THQ Nordic Port (Steam & GOG)

To address modern compatibility, a modern port was published by THQ Nordic on Steam and GOG, intended to bring the game to contemporary systems with built-in fixes. However, this port comes with major compromises:

* **Clock Speeds & Input Lag:** Because modern CPUs break the original timing, the port attempts to work around it by slowing down the global game speed, resulting in sluggish performance and persistent input lag on all character actions.
* **Forced Visual Filters:** It introduces harsh graphical filters designed to mask underlying rendering incompatibilities, distorting the original art style.
* **Framerate Caps:** The experience is locked down, failing to deliver the smooth fluidity the game deserves.

### The Purpose of Verdante

Because of these issues, **Verdante** was engineered through extensive trial and error to bypass modern port limitations entirely. Countless hours were spent testing combinations of retro hardware components, BIOS ROMs, CD-ROM read speeds, and precise driver pairings to discover the exact "sweet spot" that preserves the genuine original experience.

* **Not for Distribution of Copyrighted Media:** This repository and its releases do not aim to distribute commercial software illegally.
* **Support the Developers & Publishers:** We strongly encourage everyone to legally obtain and own copies of the games they love. Please ensure you own an official retail copy or a digital version (such as from Steam or GOG) to support the rights holders before utilizing this archival package.

---

## 💻 Under the Hood: The Custom Emulated Hardware Spec

Unlike a standard virtual machine (like VirtualBox), **Verdante** uses **86Box** to emulate a physical retro computer down to the individual component and controller level. The exact hardware cocktail engineered for this setup consists of:

* **Processor:** Intel Pentium II (450 MHz)
* **Memory:** 1024 MB RAM
* **Graphics:** 3dfx Voodoo3 3500 (with optimized driver pairings to eliminate visual bugs)
* **Storage:** 5 GB Hard Disk Drive (5400 RPM)
* **Optical Drives:** Dual 8x CD-ROM drives (facilitating multi-disc image mounting via ISO files using tools like ImgBurn)
* **Floppy Drives:** Dual 360 KB floppy drives
* **Audio:** Sound Blaster PCI 4.1 (CT5880)

### Software & Driver Stack

* **Operating System:** Windows 98 SE
* **Graphics & Multimedia Drivers:** 
    * Voodoo3 10700 drivers
    * Specific sound/system drivers (`win9x-me-nt-2000-driver`)
    * **DirectX 8.1** (coupled together to guarantee maximum stability and pristine visual rendering without glitches)
---

## 🗂️ Archive & Folder Structure

For those inspecting the complete release layout, the archive is structured as follows:

* `Silver/` — Contains the game source media separated into language-specific folders:
    * `Silver French/` — CD 1 & CD 2 ISOs for the French version.
    * `Silver English/` — CD 1 & CD 2 ISOs for the English version.
* `Game Solutions/` — Archived HTML walkthroughs and guides preserved from historical fan websites.
* `machine/` — Houses the core virtual machine compressed archive (`PC-Silver-Win98-Stable.zip`).
* `drivers/` — *(Complete Edition only)* Contains raw driver ISOs and the Windows 98 installation media used to build the environment.
* `roms/` — Contains the comprehensive 86Box component ROM set (~112 MB) used for hardware validation and testing.

---

## 📥 Downloads & Releases

Due to file size limits on GitHub, **the source code repository itself does not contain the runtime binaries or game assets**. 

👉 **Head over to the [GitHub Releases tab](../../releases) to download the package archives.**

In the Releases section, you will find the complete, ready-to-run package:

1. **The Core Archive (~1.4 GB):** A turnkey, 100% built execution environment containing pre-configured 86Box, necessary component ROMs, the virtual machine disk image with preinstalled drivers, and the English version of the game.
2. **French Language Pack:** A separate downloadable ISO containing the French version of the game if you prefer to play in French (place it alongside the English version as show above).

*(Note: Separate Windows and Linux targeted archives are provided in the releases to match your host operating system environment.)*

---

## 🚀 Quick Start (Windows Setup)

1. Download your preferred archive edition from the **Releases** tab and extract it to a directory of your choice.
2. Run the **`Silver First Setup.bat`** script located at the root of the project. This will automatically unpack and set up the virtual machine structure from its compressed template.
3. Once the setup script has completed, use **`Launch Silver.bat`** whenever you want to boot up the game environment.

---

## 🎮 Essential Controls & Shortcuts

* **Reclaiming Your Mouse Cursor:** Press the **Middle Mouse Button** to release the mouse cursor from the 86Box window back to your host operating system.
* **Fullscreen / Windowed Toggle:** Press **Ctrl + Alt + Page Up** to switch between fullscreen and windowed mode.
* **Changing Discs (CD Swapping):** Open the top menu bar of the 86Box window, navigate to the media settings, and swap the ISO file when prompted by the game during multi-disc sequences.
