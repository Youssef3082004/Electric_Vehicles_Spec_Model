# Electric Vehicles Specification Model
<div align="center">

[![Python](https://img.shields.io/badge/Python-3.13+-3776AB?style=for-the-badge&logo=python&logoColor=white)](https://python.org)
[![Pandas](https://img.shields.io/badge/Pandas-2.2.3+-3776AB?style=for-the-badge&logo=pandas&logoColor=white)](https://python.org)
[![NumPy](https://img.shields.io/badge/NumPy-1.26+-013243?style=for-the-badge&logo=numpy&logoColor=white)](https://numpy.org)
[![scikit-learn](https://img.shields.io/badge/scikit--learn-1.4+-F7931E?style=for-the-badge&logo=scikit-learn&logoColor=white)](https://scikit-learn.org)
[![Matplotlib](https://img.shields.io/badge/Matplotlib-3.9+-11557C?style=for-the-badge&logo=matplotlib&logoColor=white)](https://matplotlib.org)
[![Seaborn](https://img.shields.io/badge/Seaborn-0.13+-4C72B0?style=for-the-badge&logo=python&logoColor=white)](https://seaborn.pydata.org)


</div>

## 📑 Description
This project analyzes and processes a dataset of 2025 electric vehicle specifications. It includes a Jupyter Notebook (`Model.ipynb`) that performs data cleaning, preprocessing, and feature engineering to prepare the data for analysis or machine learning modeling.

## 📂 Project Structure

* **`Model.ipynb`**: The main Jupyter Notebook containing the Python code for data loading, cleaning, and preprocessing.
* **`electric_vehicles_spec_2025.csv`**: The dataset containing detailed specifications for various electric vehicle models.

## 📊 Dataset Overview

The dataset (`electric_vehicles_spec_2025.csv`) provides a comprehensive list of electric vehicles with the following key features:

* **Performance:** `top_speed_kmh`, `torque_nm`, `acceleration_0_100_s`
* **Battery & Charging:** `battery_capacity_kWh`, `efficiency_wh_per_km`, `range_km`, `fast_charging_power_kw_dc`
* **Physical Specs:** `length_mm`, `width_mm`, `height_mm`, `towing_capacity_kg`, `seats`, `cargo_volume_l`
* **Categorical Info:** `brand`, `drivetrain` (FWD/RWD/AWD), `segment`, `car_body_type`

## 🛠️ Features & Workflow

The `Model.ipynb` notebook implements the following data processing pipeline:

1. **Data Loading**: Imports the dataset using Pandas.
2. **Exploratory Data Analysis (EDA)**:
* Displays dataset structure and statistics (`info()`, `describe()`).
* Checks for duplicated records.


3. **Data Cleaning**:
* Identifies null values across columns.
* **Imputation**: Fills missing values in `number_of_cells`, `towing_capacity_kg`, and `torque_nm` with the integer mean of their respective columns.
* Drops rows with remaining missing values to ensure data integrity.


4. **Feature Selection**:
* Removes non-essential or redundant columns: `source_url`, `model`, `battery_type`, and `fast_charge_port`.


5. **Data Transformation**:
* **Label Encoding**: Converts categorical text columns (e.g., `brand`, `drivetrain`, `segment`) into numerical format using Scikit-Learn's `LabelEncoder` for model compatibility.



## 🚀 Getting Started

### Prerequisites

To run this project, you need Python installed along with the following libraries:

* pandas
* numpy
* seaborn
* matplotlib
* scikit-learn

### Installation

1. Clone the repository:
```bash
git clone https://github.com/youssef3082004/electric_vehicles_spec_model.git

```


2. Navigate to the project directory:
```bash
cd electric_vehicles_spec_model

```


3. Install the required packages:
```bash
pip install pandas numpy seaborn matplotlib scikit-learn

```



### Usage

1. Open the Jupyter Notebook:
```bash
jupyter notebook Model.ipynb

```


2. Run the cells sequentially to reproduce the data processing steps.
