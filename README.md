# Global Temperature Change — Data Exploration

A data exploration project examining global temperature change trends from **1961 to 2020**, using NASA GISS surface temperature data sourced via FAO/FAOSTAT. The analysis investigates climate change indicators across countries, continents, and development status.

\---

## Table of Contents

* [Overview](#overview)
* [Dataset](#dataset)
* [Research Questions](#research-questions)
* [Key Findings](#key-findings)
* [Installation](#installation)
* [Usage](#usage)
* [Project Structure](#project-structure)
* [Recommendations](#recommendations)
* [References](#references)

\---

## Overview

Global temperature is a widely used measure of the Earth's overall climate condition. This project explores temperature anomalies (deviations from a 1951–1980 baseline) to understand how climate change manifests across different regions, development stages, and time periods — including the impact of COVID-19 on emissions and temperature trends in OECD countries.

\---

## Dataset

|File|Description|
|-|-|
|`Environment\_Temperature\_change\_E\_All\_Data\_NOFLAG.csv`|Annual surface temperature change by country (1961–2019), including monthly, seasonal, and annual anomalies with standard deviations|
|`FAOSTAT\_data\_1-10-2022.csv`|Long-format FAO temperature change data covering 1961–2020|
|`FAOSTAT\_data\_11-24-2020.csv`|Country code reference table (ISO codes, M49 codes)|

**Source:** [NASA GISS Global Surface Temperature Change via Kaggle](https://www.kaggle.com/datasets/sevgisarac/temperature-change?group=bookmarked)

**Coverage:** 284 countries/regions | Monthly, seasonal \& annual anomalies | Baseline: 1951–1980

\---

## Research Questions

1. How has the average global temperature changed over the years (1961–2019)?
2. How does temperature change vary in OECD countries before and after COVID-19 (2016–2020)?
3. What is the overall seasonal variation of temperature around the world?
4. Are there noticeable differences in temperature trends between developed and developing countries?
5. How does temperature change vary between continents over the past two decades?
6. What are the temperature variations across different regions of Africa in the last 20 years?
7. Which countries or regions have experienced the fastest temperature increase?

\---

## Key Findings

### Global Trend

* Global average temperature has risen at a rate of **+0.03°C per year** from 1961 to 2019.

### OECD Countries \& COVID-19

* Despite a \~7% drop in carbon emissions in 2020 due to COVID-19, OECD average temperature change **peaked at \~2.01°C** in 2020 vs. 1.54°C in 2016 — suggesting temperature change is not immediately responsive to short-term emission reductions.

### Seasonality

* Significant seasonal temperature variation was detected globally, with **Palestine, Antarctica, Libya, Gibraltar, and Qatar** showing the strongest seasonal trends.

### Developed vs. Developing Countries

* Prior to 2010, developing countries (Non-Annex I) occasionally experienced higher temperature changes than developed nations.
* **Post-2010**, developed countries (Annex I) have consistently shown higher temperature changes across all years.

### Continents (2000–2019)

|Continent|Avg. Temperature Change|
|-|-|
|Europe|1.57°C|
|Northern America|1.15°C|
|Asia|1.06°C|
|Africa|\~0.95°C|
|South America|\~0.89°C|
|Australia|0.83°C|
|Antarctica|0.52°C|

### African Regions (2000–2019)

* **Highest average temperature change:** Northern Africa (1.21°C), Western Africa (1.10°C)
* **Lowest average temperature change:** Southern Africa (0.84°C), Middle Africa (0.87°C)
* **Highest temperature variability (std dev):** Southern Africa (0.63), indicating the least stable temperatures

### Fastest Rising Temperatures (Mann-Kendall Test)

Top countries with the strongest increasing temperature trends:

1. Saint Pierre and Miquelon
2. Morocco
3. India
4. Nepal
5. Bangladesh
6. Greenland
7. Tunisia
8. Liberia
9. Samoa
10. Sierra Leone

\---

## Installation

```bash
# Clone the repository
git clone https://github.com/deepa14315/deepa-dataexploration.git
cd deepa-dataexploration

# Install dependencies
pip install pandas numpy seaborn plotly matplotlib statsmodels pymannkendall
```

> \*\*Note:\*\* Some functions require `numpy<1.24` for compatibility with `pymannkendall`.
> ```bash
> pip install "numpy<1.24"
> ```

\---

## Usage

Open and run the Jupyter notebook:

```bash
jupyter notebook "Data Exploration.ipynb"
```

Ensure the three CSV data files are placed in a `data/` subdirectory relative to the notebook.

\---

## Project Structure

```
├── data/
│   ├── Environment\_Temperature\_change\_E\_All\_Data\_NOFLAG.csv
│   ├── FAOSTAT\_data\_1-10-2022.csv
│   └── FAOSTAT\_data\_11-24-2020.csv
├── Data Exploration.ipynb
└── README.md
```

\---

## Recommendations

1. **Mitigate emissions** — accelerate transition to renewable energy and sustainable practices globally.
2. **Adaptation strategies** — Northern and Western Africa should prioritise climate-resilient infrastructure and water management.
3. **Conservation** — protect polar and fragile ecosystems, especially Antarctica.
4. **Data sharing** — enhance global climate monitoring and collaborative research.
5. **Climate education** — raise awareness among the public, businesses, and policymakers.
6. **International cooperation** — strengthen commitments to frameworks like the Kyoto Protocol.

\---

## References

* Brohan, P. et al. (2006). Uncertainty estimates in regional and global observed temperature changes. *J. Geophys. Res.*, 111(D12106).
* Hansen, J. et al. (2010). Global surface temperature change. *Rev. Geophys.*, 48.
* IPCC (2018). *Special Report on Global Warming of 1.5°C*. https://www.ipcc.ch/sr15/
* IPCC (2021). *Climate Change 2021: The Physical Science Basis*. Cambridge University Press.
* OECD (2023). *Climate change*. OECD iLibrary.
* Rahmstorf, S. \& Coumou, D. (2011). Increase of extreme events in a warming world. *PNAS*, 108, 17905–17909.
* World Meteorological Organization (2022). *State of Climate in Africa*.
* Shepard, D. (2019). Global warming: severe consequences for Africa. UN Africa Renewal.

