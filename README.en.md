# pcb-expose

**PCB photoresist exposure** using an **Anycubic Photon Mono 4** LCD resin printer — without pouring resin. You feed an **Altium** Gerber folder (OutJob), build a mask for the panel, and export a `.pm4n` job. Copy it to a USB stick and run it on the printer like a normal print: UV hits the resist.

**Русский:** [README.md](README.md)

> Early public release. The Windows build has been run on a real Mono 4, but the tool is still evolving — expect bugs and changes. **Source code is not in this repository**; this repo is the distributable build plus user-facing docs.

## Who it’s for

- You make boards at home / in a small shop and already have (or plan to get) a Photon Mono 4  
- You design in Altium and want Gerber → exposure file instead of film / guesswork  
- You want a short path: Gerbers → mask → printer file  

Other Photon models and slicers are **not** supported. This is tuned for Mono 4 (LCD 9024×5120, ~17 µm pitch).

## Download

Latest build: **[Releases](https://github.com/Ainstraf/pcb-expose-dist/releases)** → `pcb-expose-windows-x64.zip`

1. Unzip  
2. Run `pcb-expose\pcb-expose.exe`  
3. Keep the **whole folder** (`_internal` next to the exe). The exe alone will not run  

Windows x64. No installer.

## How to use

1. Open a Gerber folder (Altium OutJob) or drag it into the window.  
2. Enable layers; optionally invert, mirror, offset.  
3. Turn on **native LCD** mode (“Как на LCD”) — that’s what actually goes to the panel.  
4. Optionally tune raster quality and/or run an **exposure test** (several zones, different times — handy for dialing in resist and gap).  
5. **Export .pm4n**.  
6. Copy the file to the **root** of a **FAT32** stick, **Latin** filename, plug into the printer, start the job.

It shows up like a normal file in the printer list, with its own preview thumbnail.

### Practical notes

- For export, trust **native LCD** mode, not the quick overview preview.  
- The board must fit the fixture safe area; otherwise you’ll get a warning — nudge offset or shrink the blank.  
- Exposure test is for finding a dose, not for “ship this board tomorrow.”  
- Etching is a separate rabbit hole. To judge exposure, developing the resist and inspecting the pattern is often enough.

## Feedback

Bug, weird Gerber, or “worked solidly on my setup”?  
Open an **[Issue](https://github.com/Ainstraf/pcb-expose-dist/issues)**: release version, what you did, a screenshot or short description. That helps decide what a next patch should fix.

The project direction comes from the author; builds are published as the hardware workflow gets more predictable. One-off requests in a vacuum aren’t the priority — clear feedback from real exposure runs is.

## Limitations (straight)

| | |
|---|---|
| Printer | **Anycubic Photon Mono 4** only |
| OS | Windows (prebuilt) |
| Input | Gerber folder in the Altium OutJob style |
| Source | Not in this repository |
| Status | Under development |

## Keywords

PCB photoresist exposure, Anycubic Photon Mono 4, Altium Gerber, UV dry film / solder mask, `.pm4n`, DIY PCB fabrication.

---

Hardware and process questions → Issues. Good luck with the exposure.
