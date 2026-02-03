# GIS-Based Spatial Suitability Analysis – Kythnos Island (QGIS)

## Overview
This project presents a GIS-based spatial suitability analysis conducted on the island of Kythnos, Greece.  
The analysis combines constraint-based analysis and weighted overlay techniques to identify candidate areas suitable for development.

The project was implemented entirely in QGIS and follows a structured multi-criteria decision analysis (MCDA) workflow, demonstrating how GIS can support spatial decision-making through transparent and reproducible methods.

---

## Study Area
The study area is the island of Kythnos, located in the Cyclades complex of Greece.

Kythnos is characterized by:
- Complex topography
- Environmentally sensitive areas
- Limited developable land
- Strong spatial constraints related to settlements, hydrography, and protected zones

These characteristics make it an appropriate case study for GIS-based suitability and site selection analysis.

---

## Data Used
The analysis was based on publicly available spatial datasets, including:
- Digital Elevation Model (DEM)
- Slope (derived from DEM)
- Hydrographic network
- Settlements and built-up areas
- Protected areas (e.g. Natura 2000)
- Geological or land-use data
- Administrative boundaries (study area mask)

All datasets were preprocessed to ensure:
- A common Coordinate Reference System (EGSA ’87)
- Consistent spatial resolution and extent
- Appropriate vector-to-raster conversion

---

## Methodology

### 1. Constraint-Based Analysis
Spatial constraints were applied to exclude unsuitable areas from further consideration. These included:
- Buffer zones around settlements
- Buffer zones around hydrographic features
- Environmentally protected areas
- Areas exceeding slope thresholds
- Geologically or land-use restricted zones

Each constraint layer was converted to raster format and reclassified into binary values (suitable / unsuitable).  
All constraint rasters were combined using raster calculation to produce a final exclusion mask.

---

### 2. Weighted Overlay Analysis
A weighted overlay analysis was applied to the remaining suitable areas using evaluation criteria such as:
- Slope classes
- Distance from infrastructure
- Land characteristics
- Environmental suitability factors

Each criterion was:
- Reclassified into suitability scores
- Assigned a relative weight based on its importance
- Combined using raster algebra to generate a continuous suitability index.

---

### 3. Scenario-Based Analysis
Two different
