# OFI_SERVICES

## WOAS — Warehouse Optimization & Anomaly System

### Overview

WOAS (Warehouse Optimization & Anomaly System) is an AI-driven logistics tool built to analyze warehouse inventory and detect inefficiencies before they escalate.
It helps operations teams balance stock levels, propose transfers, and identify unusual inventory behaviors using unsupervised machine learning (Isolation Forest).

⸻

### Features

	
• **AI Insights (Anomaly Detection):**  
Detects abnormal inventory behavior such as sudden stock drops, delayed restocks, or high storage costs.

• **Warehouse Optimization:**  
Calculates surplus and deficit per warehouse and proposes efficient transfer strategies.

• **Data Preview:**  
Displays a quick look at current inventory to verify correctness.

• **Interactive Streamlit Dashboard:**  
Run, analyze, and download results in an easy-to-use interface.

____

### Project Structure

| Folder / File Path                         | Description |
|--------------------------------------------|-------------|
| `warehouse_optimizer/`                     | Root project directory |
| ├── `app.py`                               | Main Streamlit application script |
| ├── `anomaly_detection.py`                 | Contains ML-based anomaly detection logic |
| ├── `optimizer.py`                         | Handles surplus/deficit analysis and transfer proposal logic |
| ├── `requirements.txt`                     | Python dependencies for the project |
| ├── `README.md`                            | Project documentation and usage guide |
| ├── `data/`                                | Folder containing dataset CSV files |
| │ ├── `warehouse_inventory.csv`            | Warehouse-level inventory data |
| │ ├── `vehicle_fleet.csv`                  | Vehicle specifications and efficiency data |
| │ ├── `orders.csv`                         | Orders and delivery information |
| │ ├── `routes_distance.csv`                | Distance and route mapping data |
| │ ├── `cost_breakdown.csv`                 | Operational cost data |
| │ ├── `customer_feedback.csv`              | Feedback and sentiment data |
| │ ├── `delivery_performance.csv`           | Delivery performance metrics |
| ├── `outputs/`                             | Generated output files (transfer proposals, anomalies) |
| │ ├── `transfer_proposals.csv`             | Recommended inter-warehouse transfers |
| │ ├── `warehouse_anomalies.csv`            | Flagged anomalies in inventory data |
| └── `venv/`                                | Virtual environment folder (optional, for isolated dependencies) |

### How It Works 

	1.	Loads warehouse data (e.g., stock, reorder level, and storage cost).
	2.	Computes surplus and deficit across warehouses.
	3.	Generates transfer proposals to rebalance inventory efficiently.
	4.	Runs Isolation Forest (unsupervised ML) to detect anomalies in stock, cost, or restock timing.
	5.	Displays results interactively with options to export findings.

____

Setup Instructions (Plain Text)
	1.	Clone the repository
Open your terminal and run:
git clone https://github.com/<your-username>/warehouse-optimizer.git
cd warehouse-optimizer
	2.	Create and activate a virtual environment
	•	On macOS/Linux:
python3 -m venv venv
source venv/bin/activate
	•	On Windows:
python -m venv venv
venv\Scripts\activate
	3.	Install the required packages
Run:
pip install -r requirements.txt
	4.	Add your datasets
Place all .csv files (like warehouse_inventory.csv) inside the data/ folder
or specify their folder path in the Streamlit sidebar input.
	5.	Launch the Streamlit app
Run this command in the terminal:
streamlit run app.py
	6.	Access the dashboard
Open your browser and go to:
http://localhost:8501

____

  ### Tech Stack
  
	•	Python 3.12+
	•	Streamlit — Interactive UI
	•	Pandas, NumPy — Data wrangling
	•	Scikit-Learn (Isolation Forest) — ML-based anomaly detection

____

### Author

Name: Vaibhav Simhaj
Role: AI & Data Engineering Intern
Organization: NexGen Logistics Pvt. Ltd.
Project: Warehouse Optimization & AI Insights System
