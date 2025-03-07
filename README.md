# Synthea Healthcare Graph Analytics

## Overview
Synthea Healthcare Graph Analytics is a powerful tool for analyzing patient interactions, identifying high-risk individuals, and simulating disease spread in a healthcare network. Using graph-based techniques, this system transforms patient data into an interactive graph model that helps healthcare professionals derive insights efficiently.

## Features
- **Graph-based Patient Analytics**: Converts patient records and encounters into a graph structure.
- **Interactive Visualization**: Displays patient interactions dynamically using PyVis.
- **Risk Analysis**: Identifies high-risk individuals using PageRank.
- **Disease Spread Simulation**: Models infection spread over patient encounters.
- **Real-time Dashboard**: Allows users to explore patient risk levels and detect anomalies via Streamlit.

## Dataset
The system uses **Synthea Synthetic Patient Records**, which include:
- **patients.csv** - Details on patient demographics and health records.
- **encounters.csv** - Records of patient interactions with healthcare providers.

## Installation
### **1️⃣ Setup Environment**
```sh
pip install pandas networkx pyvis streamlit
```

### **2️⃣ Load Dataset**
```python
import pandas as pd
patients_df = pd.read_csv("synthea_data/csv/patients.csv")
encounters_df = pd.read_csv("synthea_data/csv/encounters.csv")
```

### **3️⃣ Build Graph**
```python
synthea_graph = build_graph(patients_df, encounters_df)
```

### **4️⃣ Visualize Graph**
```python
visualize_graph(synthea_graph)
```

### **5️⃣ Identify High-Risk Patients**
```python
pagerank_scores = pagerank(synthea_graph)
top_patients = sorted(pagerank_scores.items(), key=lambda x: x[1], reverse=True)[:5]
print("Top Influential Patients:", top_patients)
```

### **6️⃣ Simulate Disease Spread**
```python
infected_patients = simulate_disease_spread(synthea_graph, initial_infected=5, spread_prob=0.7, steps=10)
```

### **7️⃣ Run Interactive Dashboard**
```sh
streamlit run app.py
```
![Screenshot 2025-03-07 023156](https://github.com/user-attachments/assets/fd9603e5-bd2b-4297-bb8b-f20396bc8286)

## Usage
- **Load patient and encounter data** to construct a healthcare network.
- **Analyze patient relationships** using graph analytics.
- **Detect high-risk individuals** based on encounter history.
- **Simulate disease spread** to predict healthcare outcomes.
- **Interact with a Streamlit dashboard** for real-time insights.

## Future Enhancements
- **Integration with real hospital data** for real-world impact.
- **Machine learning models** to predict patient risks more accurately.
- **Dynamic graph updates** based on new patient interactions.

## License
This project is open-source under the MIT License.

## Contact
For more details, contact 
**Linkedin** : **www.linkedin.com/in/sayantichy**.

---
🚀 **Empowering Healthcare with Graph Analytics!**

