# 🛡️ 311 Service Requests: Differential Privacy Analysis

## 📌 Overview
This project focuses on **Human-Centered Data (HCD)** by analyzing **311 Service Requests** while ensuring user anonymity and data security through **Differential Privacy** techniques. The goal is to extract meaningful insights from public service requests (such as noise complaints, graffiti removal, and sanitation) without compromising the privacy of the individuals submitting them.

## 🔬 Methodology
The analysis leverages Python and various data science libraries (`pandas`, `numpy`, `plotly`, `seaborn`) to preprocess, explore, and apply differential privacy to the dataset.
Key steps include:
- **Data Preprocessing**: Handling missing values, processing timestamps, and standardizing coordinates.
- **Exploratory Data Analysis (EDA)**: Understanding service request types, geographic distributions (ZIP codes, wards), and request statuses.
- **Privacy Preservation**: Implementing differential privacy algorithms to add noise to sensitive fields (like exact coordinates) while preserving aggregate statistical utility.

## 📊 Key Findings
- The most common 311 requests include *Information Only Calls*, *Aircraft Noise Complaints*, and *Graffiti Removal*.
- Geographic analysis reveals concentration of specific request types in certain ZIP codes (e.g., 60612, 60666).
- Applying differential privacy successfully obscured exact locations and personal identifiers while maintaining the overall spatial and categorical trends necessary for city planning and resource allocation.

## 📂 Repository Structure
- `311_DP_Analysis_English.ipynb` - The primary notebook containing data preprocessing, EDA, and differential privacy implementation.
- `IS597.ipynb` - Supplementary analysis and data processing scripts.
- `final/` - Directory containing finalized notebooks and Python scripts (`311_dp_analysis.py`).
- `README.md` - Project documentation.
