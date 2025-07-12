This repository includes the final project submission for Georgetown University's PPOL 5202: Data Visualization for Data Science, Fall 2024.

<h1 align="center"> China's Global Development Finance: A Geospatial and Economic Analysis</h1>
<h3 align="center"> Visualizing Investment Distribution, Lending Terms, and Strategic Priorities (2000–2021)</h3>

<p align="center">
By Irene Chen, Gabriel Soto, Tian Tong, Vaishnavi Singh, Yixin Luo | Instructor: Prof. Rebecca Johnson
</p>


<!-- Introduction -->
<h2 id="abstract">Introduction</h2>
This project analyzes China's expanding role in global development finance from 2000-2021, examining strategic investments across 165 low-to-middle income countries. Through analysis of over 20,985 projects valued at approximately $1.34 trillion, this research provides insights into China's development financing patterns and their socioeconomic impacts in recipient nations.

<!-- Data Source -->
<h2 id="abstract">Data Source</h2>
Our analysis draws on the <strong>AidData Global Chinese Development Finance Dataset (Version 3.0)</strong>, curated by the Global Research Institute at William & Mary. This dataset is constructed using the <strong>Tracking Underreported Financial Flows (TUFF)</strong> methodology, which integrates cross-validation from approximately fifty independent sources per project. These sources span a range of institutions, including academic organizations (e.g., Duke University, Harvard University), multilateral development banks (e.g., the World Bank, Asian Development Bank, Inter-American Development Bank), and local entities such as government agencies, media outlets, and think tanks. This rigorous, multi-source verification process enhances the reliability and comprehensiveness of the dataset, making it well-suited for analyzing China’s development finance activities on a global scale.

The full dataset is publicly available via AidData’s <a href="https://www.aiddata.org/data/aiddatas-geospatial-global-chinese-development-finance-dataset-version-3-0">official website</a> and <a href="https://github.com/aiddata/gcdf-geospatial-data">GitHub repository</a>. The filtered datasets used in our analysis—<code>df_filtered</code> and <code>combined_geojson</code>—are available in this project’s repository.

<!-- Methodology -->
<h2 id="abstract">Methodology</h2>
This research examines a targeted subset of the AidData dataset, focusing on high-value Chinese development projects with significant socioeconomic impact potential and geospatial precision. By establishing a monetary threshold of $10 million, we concentrate on substantial investments that typically generate measurable socioeconomic effects in recipient countries. Additionally, we restrict our analysis to projects classified under Official Development Assistance (ODA) and Other Official Flows (OOF) definitions, enabling us to examine how China's diplomatic strategy manifests through its development finance initiatives.

## Scripts
</p>
The following structure outlines the organization of scripts, data files, and documentation used throughout the project.
</p>

---

<h3>main-amd-python</h3>

| Script                         | Language   | Purpose                                                                                       |
| ------------------------------ | ---------- | --------------------------------------------------------------------------------------------- |
| `ppol5205_final_project.ipynb` | Python     | Interest rate trends, time series analysis, exploratory data summary (uses `df_filtered.csv`) |
| `ppol5202_final_project.qmd`   | R / Quarto | Data cleaning, geospatial merging, full visualization, and dashboard development              |


<h3>data</h3>

| File                                                       | Description                                                           |
| ---------------------------------------------------------- | --------------------------------------------------------------------- |
| `AidDatasGlobalChineseDevelopmentFinanceDataset_v3.0.xlsx` | Original raw dataset from AidData Global Chinese Development Finance Dataset (Version 3.0)                                      |
| `df_filtered.csv`                                          | Cleaned dataset: filtered to projects ≥ \$10M and relevant categories |
| `combined_geojson.rds`                                     | Merged project-geography data for mapping (used in Shiny apps)        |

<h3>docs</h3>

| File                                         | Description                                                                                                       |
| -------------------------------------------- | ----------------------------------------------------------------------------------------------------------------- |
| `Field Definitions_GCDF 3.0.pdf`             | Official data dictionary from AidData defining all variables used in the GCDF dataset for coding schemes and understanding                           |
| `TUFF Methodology 3.0.pdf`                   | Technical overview of the TUFF (Tracking Underreported Financial Flows) data collection and verification process. |
| `report-china-development-12-2-24.pdf`       | Final written report summarizing methodology, findings, and policy implications of our analysis                  |
| `presentation-china-development-12-2-24.pdf` | Slide deck used for the final project presentation, highlighting key visualizations and insights                 |



<!-- Data Processing and Visualization -->
<h2 id="abstract">Data Processing and Visualization</h2>
Data Processing and Visualization</h2>
The analysis leverages R for data processing and visualization, using packages such as <code>sf</code> for geospatial analysis, <code>leaflet</code> for interactive mapping, and <code>shiny</code> for dashboard development. The R workflow produces two interactive Shiny dashboards and three standalone plots that explore key financial characteristics of China's development lending.

Archived versions of the interactive plots are also available via the <a href="https://ppol5202-final-project.netlify.app/">Netlify archive</a>.

#### 1. Comprehensive Overview Dashboard
- Interactive map displaying project locations with detailed popup information
- Sector-wise distribution analysis showing investment patterns across industries
- Project status visualization revealing completion and implementation stages
- Regional variation analysis highlighting geographic investment patterns
- Comprehensive data table with custom filtering options

#### 2. OECD ODA Income Group Dashboard
- Investment distribution visualization by recipient country income groups
- Geographic distribution of projects through interactive mapping
- Temporal analysis showing investment trends over time
- Custom filtering options for detailed regional and temporal analysis

Both dashboards are available at the <a href="https://yt583-tian.shinyapps.io/china-development/">Shiny app deployment</a>.

#### 3. Interest Rate and Grace Period Analysis
- Interactive line plot tracking loan terms from 2000-2020
- Comparison between project interest rates and China's domestic rates
- Visualization of grace period evolution showing increased flexibility
- Clear display of convergence between international and domestic rates (2008-2009)
- Trend analysis revealing shift from strict to accommodating lending terms

#### 4. Interest Rate Distribution Analysis
- Dynamic box plot showing interest rate distributions by year
- Outlier identification and temporal pattern analysis
- Visualization of lending term variations across projects
- Annual distribution patterns revealing risk assessment strategies
- Comparison tools for cross-year rate distribution analysis

#### 5. Project Status and Financial Health Analysis
- Linked scatter plots showing financial distress and completion status
- Time series analysis of total project volumes
- Interactive visualization of project status correlations
- Temporal clustering analysis (2010-2017 focus period)
- Integration of financial health indicators with completion rates

<!-- Req -->
<h2 id="abstract">Requirements</h2>

- **R** version 4.0 or higher  
  - Required packages: `shiny`, `leaflet`, `dplyr`, `plotly`, `DT`, `sf`, `tidyr`, `ggplot2`
- **Python** version 3.8 or higher  
  - Required packages: `pandas`, `numpy`, `bokeh`, `plotly`
- At least 8 GB of RAM is recommended for processing spatial files such as `combined_geojson.rds`
- Active internet connection is required to render interactive base maps in Shiny applications

<!-- CONTRIBUTORS -->
<h2 id="contributors">Contributors</h2>

<p>
This replication study was completed as part of the Final Project for 
the course PPOL 5202: Data Visualization for Data Science(Fall 2024)
 at 
<a href="https://mccourt.georgetown.edu/">Georgetown University, McCourt School of Public Policy</a>.
</p>

We gratefully acknowledge the original authors for publicly sharing their data, which made this replication possible. We also appreciate Professor Rebecca Johnson for her invaluable guidance and support throughout the project.
