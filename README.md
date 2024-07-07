# # Orphan Wells Analysis in Texas

## Overview

This repository contains an analysis of the distribution and regulatory performance of orphan wells in Texas. The analysis focuses on:

1. The spatial distribution of plugged and unplugged orphan wells.
2. The inspection and violation history of these wells to understand regulatory performance across different districts and district offices.

## Data Sources

The analysis utilizes the following data sources:

- **Well Data**: Information about wells including their API number, operator, lease name, completion date, and plug date.
- **Well Shapes**: Geospatial data of wells.
- **Orphaned Wells Shape**: Information about orphaned wells including a unique identifier (`well_ident`).
- **Inspections**: Details about inspections including `inspection_date`, `operator_name`, `district`, and `district_office_inspecting`.
- **Violations**: Details about violations including `violation_disc_date`.
- **Well Inspections**: Maps wells to their inspections.
- **Well Violations**: Maps wells to their violations.

## Key Steps and Analysis

### 1. Data Preparation

- **Standardized API Numbers**: Extracted 8-digit API numbers from the `well_ident` field in the orphaned wells dataset.
- **Merged Data**: Combined well data with shapes and orphaned wells data to create a detailed dataset of orphan wells.
- **Filtered Data**: Separated the dataset into plugged and unplugged wells for focused analysis.

### 2. Inspection and Violation Data

- **Merged Inspection and Violation Data**: Incorporated inspection and violation dates into the orphan wells dataset.
- **Handled Missing/Invalid Dates**: Cleaned the data to ensure valid dates for meaningful analysis.

### 3. Visualization

- **Distribution of Plugged and Unplugged Wells**: Created maps to visualize the spatial distribution of plugged and unplugged orphan wells in Texas.
- **Inspection and Violation Analysis**: Analyzed the most recent inspection and violation dates, and visualized the data by district and district office.

## Summary of Findings

### Spatial Distribution

- **Plugged Wells**: A small number of orphan wells have been plugged.
- **Unplugged Wells**: A significant number of orphan wells remain unplugged, indicating a potential area for regulatory focus.

### Inspection and Violation History

- **Inspection Dates**: The distribution of the most recent inspection dates varies across different districts and district offices, with some areas showing more recent activity.
- **Violation Dates**: The distribution of violation dates also varies, highlighting areas where regulatory enforcement may be more active.



## Repository Structure

- `data/`: Contains the datasets used for the analysis.
- `notebooks/`: Jupyter notebooks containing the analysis code.
- `notebook_summaries/`: Jupyter notebooks saved as .html with extensive notations
- `figures/`: Visualizations generated from the analysis.
- `README.md`: This file providing an overview of the project.

## How to Use

1. **Clone the repository**:
   
   ```sh
   git clone https://github.com/your-username/orphan-wells-texas.git
   cd orphan-wells-texas
   ```

2. **Install dependencies**:
    Ensure you have the necessary Python packages installed. You can create a virtual environment and install dependencies using:
   
   ```sh
   python -m venv env
   source env/bin/activate  # On Windows use `env\Scripts\activate`
   pip install -r requirements.txt
   ```

3. **Run the notebooks**:
    Open the Jupyter notebooks in the `notebooks/` directory to explore the analysis.
   
   ```sh
   jupyter notebook notebooks/
   ```

## Contributions

Contributions to this project are welcome. Please open an issue or submit a pull request with your suggestions or improvements.

## License

This project is licensed under the MIT License. See the [LICENSE](LICENSE) file for details.
