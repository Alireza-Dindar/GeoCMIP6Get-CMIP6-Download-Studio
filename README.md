# GeoCMIP6Get

Desktop application for **CMIP6 climate data subsetting and download orchestration** using:

- **Pangeo CMIP6 Zarr catalog** (cloud-first workflow)
- **Copernicus CDS API** (official archive workflow)

The app provides an interactive GUI to define spatial domain, models, scenarios, variables, levels, and time ranges, then stage and run batch downloads.

---

## Features

- Interactive map-based bounding box selection
- Multi-model CMIP6 selection
- Scenario selection (Historical + SSPs)
- Pressure-level and variable selection
- Download cart (queue staging before execution)
- Batch execution controls (start/pause/resume/cancel/skip)
- Console telemetry/log view inside the app
- Export staged cart to Excel
- Built-in generated Python script for reproducible runs

---

## Tech Stack

- Python 3.11+
- `pywebview` (desktop shell)
- `pandas`, `numpy`, `xarray`, `fsspec`
- `cdsapi`
- `openpyxl`

---

## Run from source (development)

From project root:

```powershell
python -m venv .venv
.\.venv\Scripts\Activate.ps1
python -m pip install -r requirements.txt
python desktop_app.py
```

---

## Build standalone `.exe`

```powershell
.\build_exe.ps1 -Clean
```

Output:

- `dist\CMIP6Studio.exe`

Notes:

- `index.html`, `Header.png`, and icon resources are bundled into the executable.
- If `icon.png` exists, build scripts auto-generate `icon.ico` and embed it.

---

## Build installer (`.exe` setup wizard)

Requires **Inno Setup 6**.

```powershell
.\build_installer.ps1 -BuildExe -Clean -Version 1.0.0
```

Output:

- `installer\output\CMIP6Studio-Setup.exe`

---

## Credentials (Copernicus CDS)

The app can read/write CDS credentials from:

- `~/.cdsapirc`

Format:

```text
url: https://cds.climate.copernicus.eu/api
key: <your-uid>:<your-api-key>
```

## Distribution

You can distribute either:

- Installer package: `installer\output\CMIP6Studio-Setup.exe`

For public releases, code-signing is recommended to reduce Windows SmartScreen warnings.
