# Teaching PCD Environmental GIS
## Python, Pandas, GeoPandas, Air Quality, Meteorological Station Matching, and Spatial Statistics for Environmental GIS

[![Google Colab](https://img.shields.io/badge/Google%20Colab-Ready-F9AB00?logo=googlecolab&logoColor=white)](https://colab.research.google.com/)
[![Python](https://img.shields.io/badge/Python-3.x-3776AB?logo=python&logoColor=white)](https://www.python.org/)
[![GeoPandas](https://img.shields.io/badge/GeoPandas-GIS-139C5A)](https://geopandas.org/)
[![GitHub](https://img.shields.io/badge/GitHub-Teaching%20Repository-181717?logo=github)](https://github.com/nattaponm/Teaching_PCD_Environmental_GIS)

Repository นี้จัดทำขึ้นเพื่อใช้ในการเรียนการสอนและฝึกปฏิบัติด้าน **ข้อมูลสิ่งแวดล้อม มลพิษทางอากาศ และระบบสารสนเทศภูมิศาสตร์ (Environmental GIS)** โดยใช้ **Python, Pandas, GeoPandas และ Spatial Statistics** บน **Google Colab**

ชุดบทเรียนออกแบบสำหรับนิสิตระดับ **ปริญญาตรีชั้นปีที่ 3–4 และระดับปริญญาโท** ในสาขาสิ่งแวดล้อม ภูมิศาสตร์ ภูมิสารสนเทศ อุตุนิยมวิทยา และสาขาที่เกี่ยวข้อง รวมถึงผู้เรียนที่ยังไม่มีพื้นฐาน GIS มาก่อน

ข้อมูลหลักที่ใช้ในการฝึกประกอบด้วย

- ข้อมูล **PM₂.₅ รายวันของกรมควบคุมมลพิษ (PCD) / Air4Thai**
- metadata และพิกัดของสถานีตรวจวัดคุณภาพอากาศ PCD/Air4Thai
- metadata ของสถานีอุตุนิยมวิทยา **WMO/OGIMET**
- ขอบเขตการปกครองประเทศไทยระดับ **จังหวัด อำเภอ และตำบล**
- ชุดข้อมูลที่ผ่านกระบวนการตรวจสอบและจัดเตรียมเป็น **canonical teaching dataset**

> **แนวคิดหลักของหลักสูตร**
>
> `Source Data → Reproducible Dataset → QC → Pandas → GIS → CRS → Spatial Join → Distance → Spatiotemporal Analysis → Spatial Statistics → Scientific Interpretation`

---

# Start Here — เริ่มใช้งานจากตรงนี้

สำหรับ **นิสิต/ผู้เรียน** ให้เริ่มจาก Notebook **01** แล้วเรียนตามลำดับ

```text
01 → 02 → 03 → 04 → 05 → 06
```

Notebook **00** เป็น Notebook สำหรับผู้สอนหรือผู้ดูแล repository ใช้สร้างและตรวจสอบ canonical dataset ก่อนเผยแพร่ให้นิสิตใช้

## เปิด Notebook 01 ใน Google Colab

[![Open In Colab](https://colab.research.google.com/assets/colab-badge.svg)](https://colab.research.google.com/github/nattaponm/Teaching_PCD_Environmental_GIS/blob/main/01_get_course_dataset_from_GitHub.ipynb)

เมื่อ Notebook 01 ทำงานสำเร็จ ข้อมูลทั้งหมดจะถูกเตรียมไว้ใน Google Drive และ Notebook 02–06 จะอ่านจากชุดข้อมูลเดียวกันโดยอัตโนมัติ

---

# Course Structure

```text
                 External / Original Sources
        PCD / Air4Thai | OGIMET/WMO | Thailand GIS
                           │
                           ▼
        00 Instructor Dataset Builder & Validation
                           │
                           ▼
                Canonical Teaching Dataset v1
                           │
                           ▼
          01 Download + SHA256 + Data Validation
                           │
                           ▼
             02 Pandas + PM2.5 Foundations
                           │
                           ▼
             03 Map Literacy + CRS + GeoPandas
                           │
                           ▼
       04 Spatial Join + Distance + WMO Matching
                           │
                           ▼
           05 Spatiotemporal PM2.5 Analysis
                           │
                           ▼
        06 Spatial Statistics + Mini Research
                           │
                           ▼
              Environmental Interpretation
```

---

# Notebooks และ Google Colab

| Notebook | ไฟล์ | เนื้อหาหลัก | ผู้ใช้ | Colab |
|---|---|---|---|---|
| **00** | `00_build_and_validate_course_dataset.ipynb` | สร้าง ตรวจสอบ และ package canonical dataset | Instructor | [![Open In Colab](https://colab.research.google.com/assets/colab-badge.svg)](https://colab.research.google.com/github/nattaponm/Teaching_PCD_Environmental_GIS/blob/main/00_build_and_validate_course_dataset.ipynb) |
| **01** | `01_get_course_dataset_from_GitHub.ipynb` | ดาวน์โหลด canonical dataset, SHA256, unzip, validation | Student Start | [![Open In Colab](https://colab.research.google.com/assets/colab-badge.svg)](https://colab.research.google.com/github/nattaponm/Teaching_PCD_Environmental_GIS/blob/main/01_get_course_dataset_from_GitHub.ipynb) |
| **02** | `02_pandas_airquality_data_foundations.ipynb` | Pandas, PCD daily PM₂.₅, QC, missing data, harmonization | Foundation | [![Open In Colab](https://colab.research.google.com/assets/colab-badge.svg)](https://colab.research.google.com/github/nattaponm/Teaching_PCD_Environmental_GIS/blob/main/02_pandas_airquality_data_foundations.ipynb) |
| **03** | `03_map_literacy_CRS_and_geopandas.ipynb` | Point/Polygon, GeoDataFrame, CRS, EPSG:4326, UTM | GIS Foundation | [![Open In Colab](https://colab.research.google.com/assets/colab-badge.svg)](https://colab.research.google.com/github/nattaponm/Teaching_PCD_Environmental_GIS/blob/main/03_map_literacy_CRS_and_geopandas.ipynb) |
| **04** | `04_spatial_join_distance_and_station_matching.ipynb` | Spatial join, point-in-polygon, distance, nearest WMO | Spatial Analysis | [![Open In Colab](https://colab.research.google.com/assets/colab-badge.svg)](https://colab.research.google.com/github/nattaponm/Teaching_PCD_Environmental_GIS/blob/main/04_spatial_join_distance_and_station_matching.ipynb) |
| **05** | `05_spatiotemporal_airquality_analysis.ipynb` | Annual/monthly/seasonal PM₂.₅, completeness, maps, episodes | Spatiotemporal | [![Open In Colab](https://colab.research.google.com/assets/colab-badge.svg)](https://colab.research.google.com/github/nattaponm/Teaching_PCD_Environmental_GIS/blob/main/05_spatiotemporal_airquality_analysis.ipynb) |
| **06** | `06_spatial_statistics_and_mini_research.ipynb` | Moran's I, LISA, spatial weights, FDR, mini research | Advanced | [![Open In Colab](https://colab.research.google.com/assets/colab-badge.svg)](https://colab.research.google.com/github/nattaponm/Teaching_PCD_Environmental_GIS/blob/main/06_spatial_statistics_and_mini_research.ipynb) |

> หากมีการเปลี่ยนชื่อไฟล์ Notebook ภายหลัง ต้องแก้ URL ของปุ่ม **Open in Colab** ให้ตรงกับชื่อไฟล์ใหม่

---

# วัตถุประสงค์การเรียนรู้

เมื่อเรียนครบ Notebook 01–06 ผู้เรียนควรสามารถ

1. เข้าใจโครงสร้างและ provenance ของข้อมูลสิ่งแวดล้อม
2. ใช้ Google Colab และ Google Drive สำหรับ workflow การวิเคราะห์
3. อ่านและตรวจข้อมูล Excel ด้วย Pandas
4. เข้าใจ row, column, observation, variable และ data type
5. ตรวจ missing values, duplicate records และข้อมูลผิดรูปแบบ
6. เข้าใจหลัก **Missing ≠ Zero**
7. เข้าใจว่าค่ามลพิษสูงไม่ควรถูกลบทิ้งเพียงเพราะดูเป็น outlier
8. harmonize ข้อมูลหลายปีอย่างโปร่งใส
9. แปลงข้อมูลจาก matrix/wide format เป็น tidy/long format
10. วิเคราะห์ PM₂.₅ รายวัน รายเดือน รายปี และตามฤดูกาล
11. ตรวจ data completeness ก่อนเปรียบเทียบข้อมูล
12. เข้าใจ latitude, longitude และ geometry
13. สร้าง GeoDataFrame ด้วย GeoPandas
14. เข้าใจ Point, Line และ Polygon
15. เข้าใจ Coordinate Reference System (CRS)
16. ใช้ EPSG:4326 และ projected CRS อย่างเหมาะสม
17. ทำ spatial join ระหว่างสถานีกับจังหวัด อำเภอ และตำบล
18. คำนวณระยะทางระหว่างสถานีอย่างถูกต้อง
19. หา nearest meteorological station
20. เข้าใจว่า **nearest station ≠ representative station**
21. สร้างแผนที่ PM₂.₅ ที่ใช้ scale เดียวกันสำหรับการเปรียบเทียบหลายปี
22. วิเคราะห์ monitoring-network completeness และ spatial coverage
23. เข้าใจ spatial weights
24. คำนวณ Global Moran's I
25. คำนวณ Local Moran / LISA
26. วิเคราะห์ HH, LL, HL และ LH
27. เข้าใจ multiple testing และ FDR correction
28. ทำ sensitivity analysis ต่อ spatial weights
29. แยก spatial association ออกจาก causal interpretation
30. พัฒนา workflow ไปใช้ในโครงงาน วิทยานิพนธ์ หรือการวิจัยด้านสิ่งแวดล้อม

---

# แหล่งข้อมูลและที่มาของข้อมูล

## 1. ข้อมูล PM₂.₅ — PCD / Air4Thai

ข้อมูลคุณภาพอากาศใช้ข้อมูลจาก **กรมควบคุมมลพิษ (Pollution Control Department: PCD)** ผ่านระบบ **Air4Thai**

แหล่งข้อมูลหลัก:

- PCD / Air4Thai: https://air4thai.pcd.go.th/
- Air4Thai Historical Data: https://air4thai.pcd.go.th/webV3/#/History

ข้อมูลที่ใช้ในการสอนช่วงปัจจุบันคือไฟล์รายปี

```text
2021.xlsx
2022.xlsx
2023.xlsx
2024.xlsx
2025.xlsx
```

ไฟล์ PCD ใน course นี้มีโครงสร้างสำคัญคือ `DATA` sheet แบบ matrix เช่น

```text
Date       02T   03T   05T   ...
2024-01-01  21    18    25
2024-01-02  24    20    28
...
```

โดย

```text
row       = วัน
column    = รหัสสถานี
cell      = PM2.5 เฉลี่ย 24 ชั่วโมงที่เผยแพร่ในชุดข้อมูล
```

Notebook 02 แปลงข้อมูลด้วย `melt()` เป็น tidy format

```text
date | station_id | pm25
```

เพื่อให้เหมาะกับการวิเคราะห์ด้วย Pandas และ GIS

### Repository ต้นทางที่ใช้พัฒนาหลักสูตร

- https://github.com/nattaponm/training_PCD_data_GIS
- https://github.com/nattaponm/training_PCD_Ogimet10yr_3provinces_pm25

สอง repository นี้ใช้เป็นฐานของ workflow เดิม และถูกนำมาปรับใหม่ให้เป็นหลักสูตรที่มี canonical dataset, QC และ reproducibility ชัดเจนขึ้น

---

## 2. PCD / Air4Thai Station Metadata

Station metadata ใช้สำหรับ

```text
station ID
station name
station type
latitude
longitude
province
amphoe
tambon
```

และใช้ในงาน

- สร้าง Point geometry
- ตรวจ latitude/longitude
- แสดงสถานีบนแผนที่
- spatial join
- เชื่อม PM₂.₅ กับตำแหน่งสถานี
- วิเคราะห์ monitoring network

canonical files ตัวอย่าง:

```text
pcd_air4thai_stations.csv
pcd_air4thai_stations.geojson
```

จำนวนสถานีอาจเปลี่ยนตาม dataset version จึงควรตรวจจาก `README_DATASET.md`, QC metadata และ `final_build_summary.csv` แทนการ hard-code จำนวนสถานีในงานวิจัย

---

## 3. ข้อมูลสถานีอุตุนิยมวิทยา — WMO / OGIMET

แหล่งข้อมูล:

**OGIMET**  
https://www.ogimet.com/

Canonical meteorological-station metadata ใช้สำหรับ

```text
WMO station ID
station name
latitude
longitude
elevation
nearest-station analysis
```

ไฟล์สำคัญ:

```text
thailand_meteorological_stations_from_course_sources.csv
ogimet_wmo_stations_from_course_sources.csv
```

### ข้อควรระวัง

station metadata ใน repository นี้ใช้เป็น **teaching network / station-matching layer**

ไม่ควรอ้างว่าเป็น authoritative inventory ของสถานีอุตุนิยมวิทยาทั้งหมดในประเทศไทยโดยไม่มีการตรวจสอบกับหน่วยงานหรือฐานข้อมูลทางการเพิ่มเติม

นอกจากนี้ **Core Dataset v1 เน้น station metadata และ spatial matching**

ดังนั้น Notebook 04–05 ที่มี nearest WMO station ยังไม่ได้หมายความว่ามี meteorological time series เช่น

```text
temperature
relative humidity
wind speed
wind direction
rainfall
pressure
```

อยู่ในตารางแล้ว

ขั้นตอน:

```text
PCD station
↓
nearest/candidate WMO station
```

เป็นเพียง spatial relationship ก่อนการนำข้อมูลอุตุนิยมวิทยาตามวันเวลามาเชื่อมในงานขั้นสูง

---

## 4. ข้อมูลขอบเขตการปกครองประเทศไทย

ข้อมูล GIS ระดับ

```text
Province
Amphoe
Tambon
```

ใช้จาก:

**Thailand geographic data (GIS)**  
https://github.com/prasertcbs/thailand_gis

repository ต้นทางระบุข้อมูลเป็น WGS84 latitude/longitude และอธิบายว่าข้อมูลถูกแปลงมาจาก Thailand Common Operational Dataset — Administrative Boundaries (COD-AB)

แหล่ง upstream:

**Thailand COD-AB — Humanitarian Data Exchange**

https://data.humdata.org/dataset/cod-ab-tha

ข้อมูลถูกตรวจและจัดเตรียมใหม่เป็น canonical GeoPackage:

```text
environmental_gis_course.gpkg
```

layers หลัก:

```text
province
amphoe
tambon
pcd_stations
met_stations_thailand
ogimet_stations
```

Canonical CRS:

```text
EPSG:4326 — WGS 84
```

---

# Canonical Teaching Dataset

Repository นี้ใช้แนวคิด **build once, teach many times**

```text
Original sources
      ↓
Instructor build once
      ↓
QC / Validation
      ↓
Freeze dataset version
      ↓
Package
      ↓
GitHub
      ↓
Students download the same dataset
```

ข้อดี:

- ทุกคนใช้ข้อมูล version เดียวกัน
- ลดผลกระทบจากเว็บไซต์/API เปลี่ยน
- ลดปัญหา SSL และ network
- reproducible
- ตรวจ file integrity ด้วย SHA256
- ผลของนิสิตเปรียบเทียบกันได้
- เหมาะกับการเรียนในห้องปฏิบัติการ

---

# Dataset Packages

ไฟล์ข้อมูลหลักที่ root ของ repository:

```text
Teaching_PCD_Environmental_GIS_Core_v1.zip
Teaching_PCD_Environmental_GIS_PCD_Excel_v1.zip
Teaching_PCD_Environmental_GIS_GIS_Source_v1.zip
```

ไฟล์ประกอบ:

```text
dataset_packages.csv
dataset_packages.sha256
final_build_summary.csv
README_DATASET.md
```

## `Teaching_PCD_Environmental_GIS_Core_v1.zip`

เก็บ processed data และ metadata เช่น

```text
PCD station metadata
meteorological station metadata
GeoJSON
GeoPackage
admin lookup
QC reports
provenance
data dictionary
```

## `Teaching_PCD_Environmental_GIS_PCD_Excel_v1.zip`

เก็บ Excel 2021–2025 ที่ใช้สอนการอ่านและ harmonize ข้อมูล PCD

## `Teaching_PCD_Environmental_GIS_GIS_Source_v1.zip`

เก็บ source GIS files ที่ใช้สร้าง canonical boundaries เพื่อให้ตรวจสอบ provenance และทำซ้ำได้

## `dataset_packages.csv`

manifest ของ package เช่น

```text
filename
package type
size
SHA256
student requirement
```

## `dataset_packages.sha256`

SHA256 checksum สำหรับตรวจความสมบูรณ์ของไฟล์

## `final_build_summary.csv`

สรุปผล Instructor Dataset Build

## `README_DATASET.md`

เอกสารเฉพาะด้านข้อมูลและ validation

---

# ทำไมต้องตรวจ SHA256?

ชื่อไฟล์เหมือนกันไม่ได้หมายความว่าไฟล์เหมือนกัน

Notebook 01 คำนวณ

```text
SHA256(downloaded file)
```

แล้วเปรียบเทียบกับ manifest

ถ้าไม่ตรง อาจเกิดจาก

```text
download ไม่ครบ
file ถูกแก้
wrong dataset version
```

ดังนั้น Notebook จะไม่ถือว่าข้อมูลพร้อมใช้เพียงเพราะดาวน์โหลดสำเร็จ

---

# Google Drive Folder Structure

หลังรัน Notebook 01:

```text
MyDrive/
└── Teaching_PCD_Environmental_GIS/
    │
    ├── 01_course_data/
    │   └── v1/
    │       ├── downloads/
    │       └── dataset/
    │
    ├── 02_output/
    │   ├── Notebook_02/
    │   ├── Notebook_03/
    │   ├── Notebook_04/
    │   ├── Notebook_05/
    │   └── Notebook_06/
    │
    ├── 03_figures/
    │   ├── Notebook_02/
    │   ├── Notebook_03/
    │   ├── Notebook_04/
    │   ├── Notebook_05/
    │   └── Notebook_06/
    │
    └── 04_student_work/
```

ข้อมูลและผลลัพธ์จึงคงอยู่ใน Google Drive แม้ runtime ของ Colab จะถูก reset

---

# Notebook 00 — Instructor Dataset Builder

**File:** `00_build_and_validate_course_dataset.ipynb`

[![Open In Colab](https://colab.research.google.com/assets/colab-badge.svg)](https://colab.research.google.com/github/nattaponm/Teaching_PCD_Environmental_GIS/blob/main/00_build_and_validate_course_dataset.ipynb)

สำหรับ **ผู้สอน/ผู้ดูแล dataset**

หน้าที่:

```text
source discovery
download source data
PCD Excel inventory
station metadata extraction
coordinate QC
GIS validation
geometry repair
CRS normalization
provenance
data dictionary
GeoPackage creation
acceptance tests
ZIP packaging
SHA256
```

ควรรันเมื่อสร้าง dataset version ใหม่ ไม่จำเป็นต้องรันทุกครั้งที่เรียน

---

# Notebook 01 — Canonical Dataset Setup

**File:** `01_get_course_dataset_from_GitHub.ipynb`

[![Open In Colab](https://colab.research.google.com/assets/colab-badge.svg)](https://colab.research.google.com/github/nattaponm/Teaching_PCD_Environmental_GIS/blob/main/01_get_course_dataset_from_GitHub.ipynb)

Notebook เริ่มต้นสำหรับนิสิต:

```text
GitHub
↓
dataset_packages.csv
↓
download
↓
SHA256
↓
safe unzip
↓
Excel / station / GeoPackage validation
↓
TEACHING_DATASET_READY
```

---

# Notebook 02 — Pandas and PM₂.₅ Foundations

**File:** `02_pandas_airquality_data_foundations.ipynb`

[![Open In Colab](https://colab.research.google.com/assets/colab-badge.svg)](https://colab.research.google.com/github/nattaponm/Teaching_PCD_Environmental_GIS/blob/main/02_pandas_airquality_data_foundations.ipynb)

เนื้อหา:

- Excel workbook/sheet inspection
- PCD `DATA` matrix
- `melt()`
- tidy data
- datetime
- station ID
- missing values
- duplicates
- QC flags
- attribute join
- PM₂.₅ daily data
- completeness
- annual/monthly statistics
- histogram/boxplot
- 3-province case study

หลัก:

```text
Missing ≠ Zero
High value ≠ Error
Flag first, filter later
```

---

# Notebook 03 — Map Literacy, CRS and GeoPandas

**File:** `03_map_literacy_CRS_and_geopandas.ipynb`

[![Open In Colab](https://colab.research.google.com/assets/colab-badge.svg)](https://colab.research.google.com/github/nattaponm/Teaching_PCD_Environmental_GIS/blob/main/03_map_literacy_CRS_and_geopandas.ipynb)

เนื้อหา:

```text
DataFrame vs GeoDataFrame
Point / Line / Polygon
longitude / latitude
X = longitude
Y = latitude
EPSG:4326
geographic CRS
projected CRS
UTM
geometry QC
bounds QC
station maps
```

กรณีศึกษา:

```text
Saraburi
Lop Buri
Nakhon Nayok
```

สำหรับ metric demonstration ใช้:

```text
EPSG:32647 — WGS 84 / UTM Zone 47N
```

---

# Notebook 04 — Spatial Join, Distance and Station Matching

**File:** `04_spatial_join_distance_and_station_matching.ipynb`

[![Open In Colab](https://colab.research.google.com/assets/colab-badge.svg)](https://colab.research.google.com/github/nattaponm/Teaching_PCD_Environmental_GIS/blob/main/04_spatial_join_distance_and_station_matching.ipynb)

เนื้อหา:

```text
attribute join
spatial join
within / intersects
PCD → province
PCD → amphoe
PCD → tambon
projected distance
geodesic distance
nearest WMO
top-3 WMO candidates
azimuth
national geodesic station matching
```

หลัก:

```text
Nearest station ≠ Representative station
```

ควรพิจารณา:

```text
distance
elevation
terrain
urban/rural
coastal influence
wind exposure
data availability
```

---

# Notebook 05 — Spatiotemporal PM₂.₅ Analysis

**File:** `05_spatiotemporal_airquality_analysis.ipynb`

[![Open In Colab](https://colab.research.google.com/assets/colab-badge.svg)](https://colab.research.google.com/github/nattaponm/Teaching_PCD_Environmental_GIS/blob/main/05_spatiotemporal_airquality_analysis.ipynb)

เนื้อหา:

```text
station-day GeoDataFrame
station-year completeness
station-month completeness
annual variation
monthly variation
seasonal analysis
monitoring-network change
stable five-year panel
annual maps
coverage maps
high-PM2.5 episodes
three-province comparison
```

Teaching season:

```text
Dry        = November–April
Transition = May
Wet        = June–October
```

Annual maps ใช้ scale เดียวกันเพื่อการเปรียบเทียบที่ถูกต้อง

High episode ใช้ percentile-based exploratory definition ไม่ใช่ regulatory exceedance

---

# Notebook 06 — Spatial Statistics and Mini Research

**File:** `06_spatial_statistics_and_mini_research.ipynb`

[![Open In Colab](https://colab.research.google.com/assets/colab-badge.svg)](https://colab.research.google.com/github/nattaponm/Teaching_PCD_Environmental_GIS/blob/main/06_spatial_statistics_and_mini_research.ipynb)

เนื้อหา:

```text
Tobler's First Law
spatial autocorrelation
spatial weights
KNN
distance band
Global Moran's I
permutation tests
Moran scatterplot
Local Moran / LISA
HH / LL / HL / LH
multiple testing
Benjamini–Hochberg FDR
weight sensitivity
mini research
```

หลัก:

```text
Spatial clustering ≠ Source attribution
```

และ:

```text
LISA station map ≠ Continuous pollution hotspot surface
```

---

# Python Libraries

ไลบรารีหลัก:

| Library | บทบาท |
|---|---|
| `numpy` | numerical operations |
| `pandas` | tables, filtering, grouping, aggregation |
| `matplotlib` | plotting |
| `openpyxl` | Excel |
| `geopandas` | GeoDataFrame และ vector GIS |
| `shapely` | geometry |
| `pyproj` | CRS และ geodesic distance |
| `pyogrio` | GIS file I/O |
| `scikit-learn` | numerical/distance tools |
| `libpysal` | spatial weights |
| `esda` | Moran's I และ LISA |
| `pyarrow` | efficient tabular I/O |

Notebook แต่ละบทมี `pip install` สำหรับ Google Colab

---

# กรณีศึกษา 3 จังหวัด

ใช้:

```text
Saraburi
Lop Buri
Nakhon Nayok
```

เพื่อฝึก:

- station selection
- province comparison
- spatial join
- distance analysis
- meteorological-station matching
- annual/monthly/seasonal PM₂.₅
- map interpretation
- monitoring-network limitations

ผู้เรียนสามารถเปลี่ยนพื้นที่ศึกษาได้ภายหลัง

---

# Reproducibility

หลักสำคัญ:

```text
Raw/reference data preserved
Canonical dataset versioned
SHA256 verified
CRS recorded
QC reports saved
Provenance saved
Parameters visible
Outputs written to Drive
No silent deletion of suspicious values
```

เมื่อรายงานผล ควรบันทึก:

```text
dataset version
analysis period
station selection
QC rules
aggregation
CRS
spatial weights
thresholds
permutations
software/library versions
```

---

# Scientific Cautions

## Station observation ≠ Province mean

สถานีเป็น point observation ไม่ใช่ค่าเฉลี่ยทั้งจังหวัดโดยอัตโนมัติ

## Missing ≠ Zero

ไม่มีข้อมูลไม่ใช่ความเข้มข้นศูนย์

## Extreme value ≠ Error

ค่าที่สูงอาจเป็น pollution episode จริง

## Distance ≠ Representativeness

สถานีอุตุนิยมวิทยาที่ใกล้ที่สุดอาจไม่ใช่ตัวแทนที่ดีที่สุด

## Correlation ≠ Causation

ความสัมพันธ์ไม่ได้พิสูจน์สาเหตุ

## Spatial clustering ≠ Source attribution

HH cluster ไม่ได้ระบุตำแหน่งแหล่งกำเนิดโดยตรง

## Monitoring network matters

พื้นที่ station หนาแน่นและ sparse มี spatial support แตกต่างกัน

## One temporal slice for spatial inference

ไม่ควรนำ station เดิมหลายปีมาเป็น independent spatial locations โดยไม่จัดการ temporal dependence

---

# Data Provenance and Attribution

เมื่อใช้ข้อมูลหรือ workflow จาก repository นี้ในรายงาน โครงงาน หรือการวิจัย ควรอ้างแหล่งต้นทาง

## PCD / Air4Thai

Pollution Control Department (PCD), Thailand — Air4Thai

https://air4thai.pcd.go.th/

Historical data:

https://air4thai.pcd.go.th/webV3/#/History

## OGIMET

https://www.ogimet.com/

ควรตรวจเงื่อนไขการใช้งานและการอ้างอิงของ OGIMET ในขณะที่นำข้อมูลจริงไปใช้

## Thailand Administrative Boundaries

https://github.com/prasertcbs/thailand_gis

Upstream COD-AB:

https://data.humdata.org/dataset/cod-ab-tha

## Original Teaching Repositories

https://github.com/nattaponm/training_PCD_data_GIS

https://github.com/nattaponm/training_PCD_Ogimet10yr_3provinces_pm25

---

# Suggested Repository Citation

ตัวอย่างทั่วไป:

```text
nattaponm. (2026). Teaching_PCD_Environmental_GIS:
Python and GIS teaching materials for environmental air-quality analysis.
GitHub repository.
https://github.com/nattaponm/Teaching_PCD_Environmental_GIS
```

หากต้องการใช้ APA หรือ software citation อย่างเป็นทางการ ควรปรับชื่อผู้แต่งและ metadata ให้ตรงกับข้อมูลที่ต้องการเผยแพร่

---

# Data and Code Licensing

ข้อมูลแต่ละชุดยังคงอยู่ภายใต้เงื่อนไขของแหล่งต้นทาง

ผู้ใช้ควร:

1. ตรวจข้อกำหนด PCD/Air4Thai
2. ตรวจข้อกำหนด OGIMET
3. ตรวจ attribution/license ของ GIS source
4. อ้าง original data providers
5. ไม่ถือว่า teaching copy เปลี่ยนสิทธิของ original data

สำหรับ code ของ repository นี้ ควรเพิ่มไฟล์ `LICENSE` ที่ root หากต้องการกำหนดสิทธิการ reuse อย่างชัดเจน

---

# Recommended Research Uses

เหมาะสำหรับ:

```text
environmental GIS laboratory
class exercises
undergraduate projects
master's research preparation
research methods
prototype data analysis
reproducible workflow template
```

ก่อนใช้เพื่อ publication ควรเพิ่มการตรวจตามคำถามวิจัย เช่น:

```text
station representativeness
instrument/data documentation
completeness criteria
meteorological representativeness
emission information
fire hotspots
land use
topography
uncertainty
statistical assumptions
independent validation
```

---

# Possible Extensions

หัวข้อที่สามารถพัฒนาต่อ:

```text
Meteorological time-series integration
Wind rose
ERA5
Radiosonde
Boundary-layer meteorology
Fire hotspots
Satellite AOD
Emission inventory
IDW
Kriging
Spatial regression
GWR
Spatial panel models
Machine learning
HYSPLIT
Health / mortality analysis
```

ควรแยกเป็น Notebook ขั้นสูง เพราะแต่ละหัวข้อมี assumptions และ validation ของตนเอง

---

# Repository Files at a Glance

```text
Teaching_PCD_Environmental_GIS/
│
├── 00_build_and_validate_course_dataset.ipynb
├── 01_get_course_dataset_from_GitHub.ipynb
├── 02_pandas_airquality_data_foundations.ipynb
├── 03_map_literacy_CRS_and_geopandas.ipynb
├── 04_spatial_join_distance_and_station_matching.ipynb
├── 05_spatiotemporal_airquality_analysis.ipynb
├── 06_spatial_statistics_and_mini_research.ipynb
│
├── README.md
├── README_DATASET.md
│
├── Teaching_PCD_Environmental_GIS_Core_v1.zip
├── Teaching_PCD_Environmental_GIS_PCD_Excel_v1.zip
├── Teaching_PCD_Environmental_GIS_GIS_Source_v1.zip
│
├── dataset_packages.csv
├── dataset_packages.sha256
└── final_build_summary.csv
```

---

# Quick Start

สำหรับนิสิต:

```text
1. เปิด Notebook 01 ใน Google Colab
2. Mount Google Drive
3. ดาวน์โหลด canonical packages
4. ตรวจ SHA256
5. รอ TEACHING_DATASET_READY
6. เรียน Notebook 02 → 06
```

[![Open In Colab](https://colab.research.google.com/assets/colab-badge.svg)](https://colab.research.google.com/github/nattaponm/Teaching_PCD_Environmental_GIS/blob/main/01_get_course_dataset_from_GitHub.ipynb)

---

# Acknowledgement

ขอขอบคุณแหล่งข้อมูลและโครงการ open-source ที่สนับสนุนการเรียนรู้และการพัฒนา workflow ได้แก่

- Pollution Control Department (PCD) / Air4Thai
- OGIMET and meteorological observation networks
- Thailand GIS data contributors
- Humanitarian Data Exchange / COD-AB
- Python open-source community
- Pandas
- GeoPandas
- Shapely
- PyProj
- Matplotlib
- PySAL / ESDA

---

# Maintainer

GitHub: [nattaponm](https://github.com/nattaponm)

Repository:

https://github.com/nattaponm/Teaching_PCD_Environmental_GIS

---

> **Educational and scientific-use note**
>
> Repository นี้จัดทำเพื่อการเรียนการสอนและเป็นต้นแบบ workflow การวิเคราะห์ข้อมูลสิ่งแวดล้อม ผลลัพธ์จากแบบฝึกหัดไม่ควรถูกนำไปตีความเป็นข้อสรุปเชิงนโยบาย เชิงสุขภาพ หรือเชิงสาเหตุโดยปราศจากการตรวจสอบข้อมูล วิธีการ และความไม่แน่นอนเพิ่มเติม
