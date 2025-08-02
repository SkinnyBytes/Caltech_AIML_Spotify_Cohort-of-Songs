# 🎸 Spotify Song Clustering Analysis
## Creating Cohorts of Songs - Caltech Machine Learning Lab

A comprehensive machine learning project that analyzes Rolling Stones songs from Spotify's API to create meaningful song cohorts using advanced clustering techniques. This project demonstrates the complete data science pipeline from data acquisition to clustering analysis, with an optional web interface for visualization.

## 📋 Project Overview

### Problem Statement
Music streaming platforms like Spotify aim to enhance user experience through personalized recommendations. This project focuses on creating cohorts (clusters) of similar songs based on audio features to improve recommendation systems. Using Rolling Stones' discography as a case study, we analyze various song characteristics to group similar tracks together.

### Objectives
- Perform comprehensive exploratory data analysis on Spotify audio features
- Apply data preprocessing and feature engineering techniques
- Implement clustering algorithms to create song cohorts
- Evaluate clustering performance using multiple metrics
- Provide insights for music recommendation systems

## 🎯 Key Features

- **Complete ML Pipeline**: From raw data to final clusters
- **Advanced Analytics**: PCA, feature engineering, and statistical analysis
- **Multiple Clustering Approaches**: K-means with optimal cluster selection
- **Rich Visualizations**: Comprehensive plots and cluster analysis
- **Data Quality Management**: Outlier detection and data cleaning
- **Web Interface**: React-based landing page for project presentation

## 📊 Dataset Description

The dataset contains **1,612 Rolling Stones tracks** from Spotify's API with the following audio features:

| Feature | Description | Range |
|---------|-------------|-------|
| `acousticness` | Confidence measure of acoustic content | 0.0 - 1.0 |
| `danceability` | How suitable a track is for dancing | 0.0 - 1.0 |
| `energy` | Perceptual measure of intensity and activity | 0.0 - 1.0 |
| `instrumentalness` | Likelihood track contains no vocals | 0.0 - 1.0 |
| `liveness` | Probability track was performed live | 0.0 - 1.0 |
| `loudness` | Overall loudness in decibels | -60 to 0 dB |
| `speechiness` | Presence of spoken words | 0.0 - 1.0 |
| `tempo` | Estimated tempo in beats per minute | BPM |
| `valence` | Musical positivity/negativity | 0.0 - 1.0 |
| `popularity` | Song popularity score | 0 - 100 |
| `duration_ms` | Track duration in milliseconds | ms |

## 🗂️ Project Structure

```
├── 📚 Jupyter Notebooks/
│   ├── 00_Py_Spotify_Styling.ipynb           # Styling utilities and helper functions
│   ├── 01_Py_Spotify_Data Wrangling.ipynb    # Data cleaning and preprocessing
│   ├── 02_Py_Spotify_Data Analysis and Feature Engineering.ipynb  # EDA and feature engineering
│   └── 04_Py_Spotify_Cluster Analysis.ipynb  # Clustering algorithms and evaluation
│
├── 📊 Datasets/
│   ├── rolling_stones_spotify.csv            # Original raw dataset
│   ├── full_tracks.csv                       # Complete processed dataset
│   ├── clustering_tracks.csv                 # Features prepared for clustering
│   ├── stones_tracks_enriched.csv           # Dataset with additional features
│   ├── stones_tracks_engineered.csv         # Feature-engineered dataset
│   ├── outliers.csv                         # Identified outlier tracks
│   ├── flagged_tracks.csv                   # Tracks requiring attention
│   └── erroneous_entries.csv                # Data quality issues
│
├── 🌐 Web Interface/
│   ├── App.jsx                              # Main React application
│   ├── LandingPage.jsx                      # Project landing page
│   ├── index.css                            # Tailwind CSS styles
│   ├── package.json                         # Node.js dependencies
│   └── postcss.config.js                    # PostCSS configuration
│
├── 📄 Documentation/
│   ├── Data Dictionary - Creating cohorts of songs.xlsx
│   └── 1736848576_creating_cohorts_of_songs_problem_statement.docx
│
└── README.md                                # This file
```

## 🔬 Analysis Workflow

### Phase 1: Data Styling and Setup (`00_Py_Spotify_Styling.ipynb`)
- Environment setup and library imports
- Custom styling functions for consistent visualizations
- Data loading utilities and helper functions

### Phase 2: Data Wrangling (`01_Py_Spotify_Data Wrangling.ipynb`)
- **Data Quality Assessment**: Missing values, duplicates, and inconsistencies
- **Data Cleaning**: Handling erroneous entries and outliers
- **Normalization**: Feature scaling for clustering algorithms
- **Data Validation**: Ensuring data integrity for analysis

### Phase 3: Exploratory Data Analysis & Feature Engineering (`02_Py_Spotify_Data Analysis and Feature Engineering.ipynb`)
- **Comprehensive EDA**: Distribution analysis, correlation studies
- **Feature Relationships**: Understanding audio feature interactions
- **Album Analysis**: Identifying top albums by popularity
- **Dimensionality Reduction**: PCA for feature space understanding
- **Feature Engineering**: Creating derived features for better clustering

### Phase 4: Cluster Analysis (`04_Py_Spotify_Cluster Analysis.ipynb`)
- **Optimal Cluster Selection**: Elbow method and silhouette analysis
- **K-means Clustering**: Implementation with multiple cluster counts
- **Cluster Evaluation**: Silhouette scores, Davies-Bouldin index
- **Cluster Interpretation**: Understanding song cohorts characteristics
- **Results Visualization**: Comprehensive cluster analysis plots

## 🚀 Getting Started

### Prerequisites
```bash
# Python Requirements
python >= 3.8
pandas >= 1.3.0
numpy >= 1.21.0
matplotlib >= 3.4.0
seaborn >= 0.11.0
scikit-learn >= 1.0.0
scipy >= 1.7.0

# For Web Interface
node >= 16.0.0
npm >= 8.0.0
```

### Installation

1. **Clone the repository**
```bash
git clone <repository-url>
cd Caltech_AIML_Spotify\ Lab
```

2. **Python Environment Setup**
```bash
# Create virtual environment
python -m venv spotify_analysis
source spotify_analysis/bin/activate  # On Windows: spotify_analysis\Scripts\activate

# Install Python dependencies
pip install pandas numpy matplotlib seaborn scikit-learn scipy jupyter
```

3. **Web Interface Setup**
```bash
# Install Node.js dependencies
npm install
```

### Running the Analysis

#### Jupyter Notebooks
```bash
# Start Jupyter server
jupyter notebook

# Run notebooks in order:
# 1. 00_Py_Spotify_Styling.ipynb
# 2. 01_Py_Spotify_Data Wrangling.ipynb  
# 3. 02_Py_Spotify_Data Analysis and Feature Engineering.ipynb
# 4. 04_Py_Spotify_Cluster Analysis.ipynb
```

#### Web Interface
```bash
# Development server
npm start

# Production build
npm run build
```

## 📈 Key Results & Insights

### Data Quality Findings
- **Dataset Size**: 1,612 unique Rolling Stones tracks
- **Data Completeness**: High-quality dataset with minimal missing values
- **Outlier Analysis**: Systematic identification of unusual tracks
- **Feature Distributions**: Comprehensive understanding of audio characteristics

### Clustering Results
- **Optimal Clusters**: Data-driven determination of ideal cluster count
- **Cluster Characteristics**: Distinct cohorts based on musical features
- **Performance Metrics**: Quantitative evaluation of clustering quality
- **Song Groupings**: Meaningful categorization for recommendation systems

### Business Implications
- **Recommendation Enhancement**: Improved song suggestion algorithms
- **User Experience**: Better playlist generation based on mood/style
- **Content Strategy**: Insights for music curation and discovery

## 🛠️ Technologies Used

### Data Science Stack
- **Python 3.8+**: Core programming language
- **Pandas**: Data manipulation and analysis
- **NumPy**: Numerical computing
- **Scikit-learn**: Machine learning algorithms
- **Matplotlib/Seaborn**: Data visualization
- **Jupyter**: Interactive development environment

### Web Technologies
- **React 18**: Frontend framework
- **Tailwind CSS 3**: Utility-first CSS framework
- **PostCSS**: CSS processing
- **Node.js**: JavaScript runtime

### Analysis Techniques
- **K-means Clustering**: Primary clustering algorithm
- **Principal Component Analysis (PCA)**: Dimensionality reduction
- **Feature Standardization**: Data preprocessing
- **Silhouette Analysis**: Cluster validation
- **Davies-Bouldin Index**: Clustering performance metric

## 📊 Generated Outputs

The analysis produces several refined datasets:

- **`full_tracks.csv`**: Complete processed dataset ready for analysis
- **`clustering_tracks.csv`**: Standardized features optimized for clustering
- **`stones_tracks_engineered.csv`**: Enhanced dataset with derived features
- **`outliers.csv`**: Tracks identified as statistical outliers
- **`flagged_tracks.csv`**: Songs requiring special attention

## 🔍 Next Steps & Extensions

### Potential Improvements
- **Additional Algorithms**: DBSCAN, hierarchical clustering
- **Feature Engineering**: Advanced audio feature combinations
- **Cross-Artist Analysis**: Expanding beyond Rolling Stones
- **Temporal Analysis**: Evolution of musical styles over time
- **Interactive Dashboard**: Web-based cluster exploration tool

### Research Applications
- **Music Information Retrieval**: Advanced audio analysis
- **Recommendation Systems**: Production-ready implementations  
- **Genre Classification**: Automatic music categorization
- **Mood Detection**: Emotion-based music analysis

## 👥 Contributors

**Caltech AIML Course Project**
- Academic Institution: California Institute of Technology
- Course: Machine Learning
- Project Focus: Clustering Analysis and Recommendation Systems

## 📄 License

This project is created for educational purposes as part of the Caltech Machine Learning course. Please refer to the course guidelines for usage and distribution terms.

## 🤝 Acknowledgments

- **Spotify API**: For providing comprehensive audio feature data
- **Rolling Stones**: For their extensive musical catalog
- **Caltech AIML Program**: For the structured learning framework
- **Open Source Community**: For the amazing tools and libraries used

---

**🎵 "You can't always get what you want, but if you try sometimes, you just might find you get what you need" - The Rolling Stones**

*This project demonstrates how machine learning can help us find exactly what we need in music recommendation systems.*