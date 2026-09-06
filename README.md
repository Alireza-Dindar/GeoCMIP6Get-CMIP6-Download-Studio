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

<img width="1215" height="693" alt="image" src="https://github.com/user-attachments/assets/e5d2f811-730c-4421-8a0a-67d4b19559ba" /> 
<img width="1280" height="833" alt="image" src="https://github.com/user-attachments/assets/f0d0577f-ed34-4ef1-9197-e2325ee1f536" />
<img width="1221" height="523" alt="image" src="https://github.com/user-attachments/assets/b2d5755a-3f8e-41f0-853a-c702aa739568" />




## Credentials (Copernicus CDS)

The app can read/write CDS credentials from:

- `~/.cdsapirc`

Format:

```text
url: https://cds.climate.copernicus.eu/api
key: <your-uid>:<your-api-key>
```


- Direct Download Link: https://github.com/Alireza-Dindar/GeoCMIP6Get-CMIP6-Download-Studio/releases/download/v1.0.0/CMIP6Studio-Setup.exe
