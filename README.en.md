# pcb-expose

> **Under development** — early release for hardware testing. Bugs and breaking changes are expected.

A utility for **exposing photoresist on PCBs** using an **Anycubic Photon Mono 4** resin (UV) printer.  
It takes **Altium** Gerbers (OutJob folder) and exports a `.pm4n` file for UV exposure on the printer.

Mono 4 only.

Русский: [README.md](README.md)

## Download

[Releases](https://github.com/Ainstraf/pcb-expose-dist/releases) → `pcb-expose-windows-x64.zip`

## How to use

1. Unzip the archive.
2. Run `pcb-expose\pcb-expose.exe` (**entire folder required**, not the exe alone).
3. Open a Gerber folder (Altium OutJob) or drag it into the window.
4. Select layers; optionally invert / mirror / offset.
5. Enable **“Как на LCD”** (native LCD) → **Export .pm4n**.
6. Copy the file to the **root** of a FAT32 USB stick, **Latin** filename, plug into the printer.

Optional: 3×2 exposure test (six times in one file).

## Limitations

- Photon Mono 4 only  
- Windows build  
- Under development  
