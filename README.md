<p align="center"><img src="icon.png" width="96" alt="OxideCut"></p>

<p align="center"><b>English</b> · <a href="README.ar.md">العربية</a></p>

# OxideCut

Free laser design and control program for GRBL machines, for Windows. English and Arabic (right-to-left) interface.

**Download:** go to [Releases](../../releases/latest) and get `OxideCut-Setup-<version>.exe`. It installs for your user only and needs no administrator rights.

OxideCut is **free to use, but not open source**: the source code is not published and the program may not be modified or redistributed (see [LICENSE.txt](LICENSE.txt)).

## What it does

- Draw shapes, text (Arabic included), QR codes and barcodes, or import SVG, DXF and pictures.
- Boolean operations, offset, fillet, arrays, text on a path, auto-nesting, cut tabs, guides and rulers.
- Layers with speed, power, passes, kerf, lead-in, fill and image modes.
- Toolpath preview with time estimate, framing, and G-code export for GRBL.
- Connect to a real machine over USB or try everything on the built-in virtual machine.
- Export the layout as SVG or DXF.
- Updates from inside the program (Help > Check for updates). Only files signed by the author are installed.

## Help me test it

OxideCut is new, and the best way to make it better is real use. Please try it and tell me **everything** that goes wrong or feels awkward: crashes, wrong results, confusing screens, missing features, bad Arabic text or layout, anything.

1. Open an [issue](../../issues/new/choose) (a GitHub account is free).
2. In the program, open **Help > About** and press **Copy diagnostic info**, then paste it into the issue. It holds the version, Windows version and the machine state, and hides your user name. It never contains your projects.
3. Say what you did, what you expected and what happened. A screenshot helps. A small project file that shows the problem helps even more (remove anything private first).

Good to know:
- Try new jobs on scrap material first, and stay next to the machine.
- Tests so far were in simulation and on a virtual machine, so reports from **real GRBL machines** (model, firmware version, what worked, what did not) are especially valuable.
- Ideas are welcome too: use the issue type "Idea".

## Safety

A laser can burn, blind and start fires. Wear eye protection, ventilate, never leave a running job unattended, and check the toolpath, speed and power before every job. OxideCut was tested in simulation and with a virtual machine; behaviour on your hardware may differ. See the license for the full terms.

## Install from PowerShell (optional)

Downloads the latest installer and installs it silently for your user (no administrator rights):

```powershell
$r = Invoke-RestMethod "https://api.github.com/repos/abduhalmawla-tech/OxideCut/releases/latest"
$a = $r.assets | Where-Object name -like "OxideCut-Setup-*.exe" | Select-Object -First 1
$f = Join-Path $env:TEMP $a.name
Invoke-WebRequest $a.browser_download_url -OutFile $f
& $f /VERYSILENT /SUPPRESSMSGBOXES /NORESTART
```

Useful options: `/DIR="D:\OxideCut"` (install folder), `/LANG=arabic` (installer language).
To remove it silently: `& "$env:LOCALAPPDATA\Programs\OxideCut\unins000.exe" /VERYSILENT`
(use your install folder if you chose another one). Your settings in `%APPDATA%\OxideCut` are kept.

## Windows warning

The installer is not signed with a paid code-signing certificate, so Windows SmartScreen may say "unknown publisher". Choose **More info > Run anyway** if you downloaded it from this page.

## Bugs and ideas

Use [Issues](../../issues). Please do not post private project files.
