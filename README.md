# Predominant Race-Based Income Contribution in California Counties (ACS 2017)

This notebook explores the racial composition of income contribution across California counties using American Community Survey (ACS) 2017 data. It applies spatial statistics to analyze how income concentration varies by dominant racial group and identifies significant regional clusters using Local Moran’s I (LISA).

## 🔍 What This Project Does

- Merges U.S. Census ACS data with California county geometries
- Calculates income contribution per race (White, Black, Hispanic, Asian)
- Identifies the **dominant race group** in each county based on income share
- Applies **Global and Local Moran’s I (LISA)** to detect spatial clustering
- Visualizes interactive maps with **Folium** and static versions with **matplotlib**
- Highlights **statistically significant clusters**: High-High, Low-Low, and spatial outliers

## 📁 Files

- `Counties by predominant race income 2017.ipynb`: The full analysis in Jupyter Notebook format
- `data/acs2017_county_data.csv`: Cleaned ACS 2017 county-level data used in the notebook

## 📊 Tools & Libraries

- `pandas`, `geopandas`
- `matplotlib`
- `folium` (interactive maps)
- `esda`, `libpysal` (spatial statistics)

## 🌍 Spatial Concepts Used

- **Dominant Race Group by Income**: calculated as `Income × (%Race / 100)`
- **Moran’s I**: global spatial autocorrelation of income concentration
- **LISA (Local Moran’s I)**: detection of spatial clusters and outliers
- **Cluster Types**:
  - High-High: wealthy counties surrounded by wealthy neighbors
  - Low-Low: poor counties surrounded by poor neighbors
  - High-Low: wealthy outliers in poor regions
  - Low-High: struggling counties in otherwise wealthy areas

## 📌 Example Questions Answered

- Which racial group dominates income contribution in each California county?
- Where are spatial clusters of high or low income contributions?
- Which counties are income outliers compared to their neighbors?

## 📦 Data Sources

- **ACS 2017 Demographics**:  
  📥 [Kaggle Dataset - U.S. Census Demographic Data (muonneutrino)](https://www.kaggle.com/datasets/muonneutrino/us-census-demographic-data?select=acs2017_county_data.csv)

- **California County Geometries**:  
  📥 [California Counties GeoJSON - Click That 'Hood (Code for Germany)](https://github.com/codeforgermany/click_that_hood/)

## 🧠 Author

**Fernando Alonso**  
- GitHub: [@fdo-alo](https://github.com/fdo-alo)  
- Built with Python, spatial love, and a passion for equity in data

## 💬 License

Open for educational, analytical, and portfolio use. Attribution appreciated.
