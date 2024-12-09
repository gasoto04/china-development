# China's Development Finance Projects Analysis
#### Irene Chen,Yixin Crystal Luo, Vaishnavi Singh, Gabriel Soto, Tian Tong

## Introduction
This project analyzes China's expanding role in global development finance from 2000-2021, examining strategic investments across 165 low-to-middle income countries. Through analysis of over 20,985 projects valued at approximately $1.34 trillion, this research provides insights into China's development financing patterns and their socioeconomic impacts in recipient nations.

## Data Source
Our analysis utilizes AidData's Global Chinese Development Finance Dataset (Version 3.0) from William & Mary's Global Research Institute. This dataset employs the TUFF (Tracking Underreported Financial Flows) methodology, incorporating rigorous verification from approximately fifty distinct sources per project. These sources include academic institutions like Duke and Harvard universities, multilateral organizations such as the World Bank, Asian Development Bank, and Inter-American Development Bank, as well as local stakeholders including think tanks, government agencies, and media outlets.
This multi-layered verification process ensures the dataset's reliability for analyzing China's global development finance initiatives. The dataset can be accessed through AidData's official website and GitHub repository, with our filtered analysis datasets (df_filtered and combined_geojson) available in our project repository.

AidData Website: https://www.aiddata.org/data/aiddatas-geospatial-global-chinese-development-finance-dataset-version-3-0

GitHub Repository: https://github.com/aiddata/gcdf-geospatial-data 

## Methodology
This research examines a targeted subset of the AidData dataset, focusing on high-value Chinese development projects with significant socioeconomic impact potential and geospatial precision. By establishing a monetary threshold of $10 million, we concentrate on substantial investments that typically generate measurable socioeconomic effects in recipient countries. Additionally, we restrict our analysis to projects classified under Official Development Assistance (ODA) and Other Official Flows (OOF) definitions, enabling us to examine how China's diplomatic strategy manifests through its development finance initiatives.

## Scripts
### `main-amd-python` folder
#### Python Analysis Files
1. `ppol5205_final_project.ipynb`
   - Purpose: Jupyter notebook containing Python analysis code
   - Rendered HTML output: `ppol5205_final_project_Python.html`

#### R Analysis Files
1. `ppol5202_final_project.qmd`
   - Purpose: Quarto document containing R analysis code
   - Rendered HTML output: `ppol5202_final_project.html`

### `data` folder
#### Raw data 
`AidDatasGlobalChineseDevelopmentFinanceDataset_v3.0.xlsx`
   - Original dataset from AidData Global Chinese Development Finance Dataset (Version 3.0)
   - Contains comprehensive record of Chinese development projects worldwide

#### Processed Data Files
1. `df_filtered.csv`
   - Filtered version of the original dataset, containing projects meeting the $10 million threshold criteria
   - Used for main analysis in both R and Python scripts

2. `combined_geojson.rds`
   - R data file containing geographical information, used for mapping visualizations
   - Combines project data with geographical coordinates
  
### `docs` folder
#### Dataset Documentation
1. `Field Definitions_GCDF 3.0.pdf`
   - Contains detailed definitions of all variables in the AidData Global Chinese Development Finance Dataset
   - Essential reference for understanding data fields and coding schemes

2. `TUFF Methodology 3.0.pdf`
   - Documentation of the Tracking Underreported Financial Flows (TUFF) methodology
   - Explains data collection and verification processes used in the dataset

#### Project Deliverables
1. `report-china-development-12-2-24.pdf`
2. `presentation-china-development-12-2-24.pdf`
   - Project presentation slides and written report of the project

## Data Processing and Visualization
The analysis utilizes R for data processing and visualization, employing packages such as sf for geospatial analysis, leaflet for interactive mapping, and Shiny for dashboard creation. The visualization consists of two main interactive dashboards over shiny apps and three interactive plots of financial terms:
For interactive plots, it can be archived: https://ppol5202-final-project.netlify.app/

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

Both available at: https://yt583-tian.shinyapps.io/china-development/

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

## Requirements
- R version 4.0 or higher
- Required R packages: shiny, leaflet, dplyr, plotly, DT, sf, tidyr, ggplot2
- Sufficient RAM for processing GeoJSON files
- Internet connection for base map rendering

