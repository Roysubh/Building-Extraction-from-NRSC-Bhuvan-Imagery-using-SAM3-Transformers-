<h1 align="center"><b>🛰️ Building Extraction from NRSC’s Bhuvan High-Resolution Imagery (1 m) using SAM3 (Transformers)</b></h1>

<p align="center">
Prompt-based building footprint extraction from high-resolution Indian satellite imagery using SAM3
</p>

## 🌍 About This Project:
This repository demonstrates how to extract **building footprints automatically** from **NRSC’s Bhuvan high-resolution (1 m) base map** using **SAM3 (Segment Anything Model v3)** powered by the **Transformers backend** for prompt-based semantic segmentation.

<h3 align="center">✔ Workflow Characteristics</h3>

<p align="center">
✅ <b>Simple</b> &nbsp;|&nbsp;
✅ <b>Reproducible</b> &nbsp;|&nbsp;
✅ <b>Annotation-free</b> &nbsp;|&nbsp;
✅ <b>GIS-friendly</b>
</p>

### 🧠 How SAM3 Understands the Scene
Instead of manual labels, SAM3 is guided using a simple **text prompt**: 'buildings'

## ✨ Highlights:
- 🧠 **SAM3** powered by the **Transformers backend**
- 🛰️ High-resolution imagery from **NRSC Bhuvan (1 m)**
- 🗺️ End-to-end workflow: **QGIS → Jupyter → GeoTIFF**
- 🔍 **Prompt-based semantic segmentation** (no annotations)
- 📊 **Multiple output samples** for visual evaluation
- 🇮🇳 A focused **GeoAI use case for India**

## 🧰 Tech Stack:
| Category | Tool |
|--------|------|
| 🧠 **Segmentation** | **SAM3 (Transformers)** |
| 📦 **Library** | **segment-geospatial[samgeo3]** |
| 🛰️ **Imagery** | **NRSC Bhuvan (1 m)** |
| 🗺️ **GIS** | **QGIS** |
| 🐍 **Language** | **Python** |
| 📓 **Platform** | **Jupyter Notebook** |
| 🤗 **Model Hub** | **Hugging Face** |

## 🔧 Installation:
📦 Step 1: Install Required Library:
    Install the latest version of **segment-geospatial** with **SAM3** support: **'pip install -U segment-geospatial[samgeo3]'**
🤗 Step 2: Login to Hugging Face:
    **SAM3** models are downloaded from **Hugging Face**, so authentication is required (only once).

## 🗺️ Data Preparation (QGIS):
1️⃣ Load **Bhuvan high-resolution imagery** in QGIS  
2️⃣ Clip the **AOI**  
3️⃣ Export as **GeoTIFF**
✔ **RGB (3-band)**  
✔ **CRS preserved**  
✔ **Optimized tile size**

## 🧠 SAM3 Mask Generation (Core Idea):
The building extraction workflow is driven by **SAM3** using a simple text prompt and high-resolution satellite imagery.

### 🔹 Configuration
- 🧠 **Backend**: **Transformers**
- 🏷️ **Prompt**: **`"buildings"`**
- 🛰️ **Input**: **NRSC Bhuvan RGB GeoTIFF**
- 🧾 **Output**: **Binary building mask (GeoTIFF)**
---
### 🔄 Raster to Vector Conversion (GeoTIFF → SHP)
The generated building mask (**.tif**) can be converted to **vector polygons (.shp)** for GIS analysis.

- 🗺️ Convert raster mask to **building footprints**
- 📐 Enables **area, count, and spatial analysis**
- 🔗 Fully compatible with **QGIS / ArcGIS**
✔ Final Output: **Building footprint Shapefile (.shp)**

## 🧪 Output Samples:
Here are example outputs generated using **SAM3** on **NRSC Bhuvan 1 m resolution imagery** using the prompt **`buildings`**.

| Sample | SAM3 Building Mask Output |
|------|---------------------------|
| **Sample 1** | ![](https://raw.githubusercontent.com/Roysubh/Building-Extraction-from-NRSC-Bhuvan-Imagery-using-SAM3-Transformers-/main/Sample1.png) |
| **Sample 2** | ![](https://raw.githubusercontent.com/Roysubh/Building-Extraction-from-NRSC-Bhuvan-Imagery-using-SAM3-Transformers-/main/Sample2.png) |
| **Sample 3** | ![](https://raw.githubusercontent.com/Roysubh/Building-Extraction-from-NRSC-Bhuvan-Imagery-using-SAM3-Transformers-/main/Sample3.png) |

## ⚠️ Notes & Limitations:
Performance may vary depending on:

- 🏠 **Roof contrast**
- 🌥️ **Shadow conditions**
- 🏙️ **Urban density**

Additional considerations:
- 🔧 **Dense urban areas may require post-processing** to refine building boundaries
- 👁️ This repository focuses on **visual and practical demonstration** rather than quantitative accuracy evaluation

## 📜 Disclaimer:
This repository is provided strictly for **research and educational use**.  
All **NRSC Bhuvan imagery** is the property of **ISRO / NRSC**, and users are responsible for adhering to the official **Bhuvan data usage policies**.

## 🙌 Acknowledgements:
This work acknowledges the contributions of the following platforms and communities:

- **NRSC / ISRO** for the Bhuvan high-resolution imagery platform  
- **Meta AI** for the Segment Anything Model  
- **Hugging Face** for the Transformers framework and model hosting  
- **QGIS Open Source Community** for GIS tools and support

<h3 align="center">✍️ Author</h3>

<p align="center">
<b>© Subham Roy</b><br><br>
📧 subhamofficwork@gmail.com | subhamroygeospatialai@gmail.com <br>
🔗 <a href="https://github.com/Roysubh">GitHub</a> |
<a href="https://scholar.google.com/citations?user=bTxDrQgAAAAJ&hl=en">Google Scholar</a> |
<a href="https://www.researchgate.net/profile/Subham-Roy-14">ResearchGate</a> |
<a href="https://orcid.org/0009-0007-6704-2781">ORCID</a> |
<a href="https://www.linkedin.com/in/subham-roy-601867167/">LinkedIn</a>
</p>




