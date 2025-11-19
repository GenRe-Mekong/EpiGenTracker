# 🧬 EpiGenTracker — Map · Timeline · Charts · Genetic Tree

> Visualise data across **space**, **time**, and **category** — right in your browser.
> Zero installation. Designed for malaria genetic epidemiology data but suitable for any data.
>
> <b> Launch App Here: </b> https://genre-mekong.github.io/EpiGenTracker/
> 

[![Version: v0.6](https://img.shields.io/badge/prototype-v0.6-blue)](#)
[![Run: Browser only](https://img.shields.io/badge/run-browser_only-brightgreen)](#)
[![License: MIT](https://img.shields.io/badge/license-MIT-lightgrey)](#)

### Table of Contents
-- [✨ What it is](#-what-it-is) 
-- [⚡ Quick Start](#-quick-start) 
-- [📁 Input File Formats](#-input-file-formats) 
-- [🧭 Full User guide](#-full-user-guide) 
-- [📚 Citation & Author](#-citation--author) --




## ✨ What it is
EpiGenTracker turns tabular data (.csv) into an interactive map–timeline–chart visualisation.  
Load your **sample CSV**, play through time, compare **two regions**, and (optionally) explore a **genetic similarity tree**.

- **Map:** plots samples by administrative region.  
- **Timeline player:** animate sample appearances by collection date.  
- **Charts:** compare two regions (Area A/B) over time, grouped and coloured by assigned labels.  
- **Genetic Tree (optional):** visualize pairwise similarity from a `.tab` distance matrix.  
- **No backend needed:** works entirely offline in your browser.

<img src="assets/images/Demo-20sec.gif" width="800" alt="Demo">

## ⚡ Quick Start
1. **Access App:** https://genre-mekong.github.io/EpiGenTracker/  
2. **Load Map:** Click **Load eastern GMS map (KH, LA, TH, VN)** or **upload your own GeoJSON layers (ADM0–ADM2)** <p> - (Details on how to prepare your own map will be updated soon).</p>  
3. **Load Sample Data (.csv)** → the map animates over time. <p> - (Details on how to prepare your data will be updated soon) </p>
4. **😀 Explore Data!** → Aggregate temporal trend by region, zoom in and out, track specific labels. <p></p>
5. *(Optional)* Load **Genetic Distance (.tab)** to enable the similarity tree.

## 📁 Input File Formats

### 🗺️ GeoJSON (maps)
- ADM2 required (districts); ADM1/ADM0 optional (borders/labels).  
- Auto-detects IDs like `GID_2`, `ADM2_PCODE`, or `NAME_2`.
You can download geojson files for any countries from https://gadm.org/download_country.html 

### 🧬 CSV (samples)
CSV, UTF-8, comma-separated, one header row, one sample per row.

**Required columns:**
- `GID_2` — Administrative division 2 ID matching your GeoJSON, which can be found at https://gadm.org/download_country.html
- `CollectionDate` in `YYYY-MM-DD` or just `Month` and `Year` columns
- 
**Optional columns:**
- `Group` or `Cluster` — sample group/cluster name will be used for colour and labelling
- `Latitude`, `Longitude` — for jittered placement of samples within polygons (to be able to see overlapping samples in the same area)
- Any columns can be added. This will allow you to colour the markers with these column. For example, you may wish to have 'species' or 'drug resistance' column

**Minimal Example:**
```csv
GID_2,CollectionDate,Group
KHM.1.1_1,2023-01-14,ClusterA
KHM.1.1_1,2023-02-02,ClusterB
VNM.2.3_1,2023-02-10,Unclustered
```

## 🧭 Full User guide
Coming soon!


## 📚 Citation & Author
✨ Developed by **Varanya Wasakul** with support from AI-assisted development tools

If you use EpiGenTracker in your work, please cite:
> GenRe-Mekong. EpiGenTracker: An interactive browser app for genetic epidemiology data visualization. 2025. https://github.com/GenRe-Mekong/EpiGenTracker



