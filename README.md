# Weather Data Interpolation

This repository contains implementations of different interpolation techniques for handling missing values in weather data. The dataset used is `weather_report.csv`, and the methods explored include:

- **Pandas Interpolation (`interpolate.ipynb`)**: Uses `interpolate()` to estimate missing values.
- **K-Nearest Neighbors (`knn_imputer.ipynb`)**: Utilizes `KNNImputer` from `sklearn.impute` to fill missing values.
- **Long Short-Term Memory Network (`lstm.ipynb`)**: Uses an LSTM model to predict missing values in time-series data.
- **Rolling Window Interpolation (`rolling.ipynb`)**: Applies a rolling mean to smooth data and fill gaps.

## Installation

Ensure you have Python installed, then install dependencies using:

```bash
pip install -r requirements.txt
```

If using Jupyter Notebook, you may also need:

```bash
pip install notebook
```

## Usage

Clone the repository:

```bash
git clone https://github.com/YOUR_USERNAME/weather-data-interpolation.git
cd weather-data-interpolation
```

Open Jupyter Notebook:

```bash
jupyter notebook
```

Navigate to the `notebooks/` directory and run the desired `.ipynb` file.

## Dataset

The dataset `weather_report.csv` contains weather-related measurements with missing values. If the dataset is not included, update `data/` with your own weather dataset or download it from a provided link.

## Interpolation Methods

### 1. Pandas Interpolation (`interpolate.ipynb`)
- Uses the `interpolate()` function from Pandas to fill missing values.
- Suitable for datasets with smooth transitions.
- Supports different interpolation methods such as linear, polynomial, and spline.

### 2. K-Nearest Neighbors (`knn_imputer.ipynb`)
- Uses `KNNImputer` from `sklearn.impute` to estimate missing values.
- Fills gaps based on similar observations using K-nearest neighbors.
- Works well if missing values are correlated with nearby data points.

### 3. LSTM (`lstm.ipynb`)
- Uses a deep learning model (Long Short-Term Memory network) to predict missing values.
- Processes time-series data and learns temporal dependencies.
- Computationally intensive but suitable for complex trends.

### 4. Rolling Window (`rolling.ipynb`)
- Applies a rolling mean to fill missing values.
- Useful for smoothing fluctuations in the dataset.
- Not ideal for datasets with sharp variations.

## Results

Each method has its own advantages and limitations. The effectiveness depends on the dataset structure and the nature of missing data. Below is a general comparison:

| Method            | Best For                         | Complexity | Computational Cost |
|------------------|--------------------------------|------------|--------------------|
| Pandas Interpolation | Simple missing data patterns | Low        | Low |
| KNN Imputer | Data with correlated features | Medium | Medium |
| LSTM | Complex time-series patterns | High | High |
| Rolling Window | Smoothing fluctuations | Low | Low |

## Repository Structure

```plaintext
weather-data-interpolation  
│-- notebooks  
│   │-- interpolate.ipynb  
│   │-- knn_imputer.ipynb  
│   │-- lstm.ipynb  
│   │-- rolling.ipynb  
│-- data  
│   │-- weather_report.csv  
│-- README.md  
│-- requirements.txt  
│-- .gitignore  
|-- .gitattributes
│-- LICENSE  
```

## License

This project is licensed under the MIT License. See the `LICENSE` file for details.
