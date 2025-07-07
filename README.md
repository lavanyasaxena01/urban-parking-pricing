# 🅿️ Dynamic Pricing for Urban Parking Lots
A real-time pricing simulation using Pathway and Python to optimize urban parking using demand and competition-based models.

## 📘 Overview

This project aims to build a smart pricing engine for urban parking lots using historical and real-time data. The system adapts parking prices based on occupancy, demand, traffic conditions, vehicle type, and nearby competitor lots.

The solution is implemented using:
- 3 Pricing Models: Linear, Demand-Based, and Competitive
- Real-time simulation using Pathway
- Bokeh and Matplotlib for visualization

## 🧰 Tech Stack

| Component      | Technology       |
|----------------|------------------|
| Language       | Python 🐍         |
| Real-time Engine | [Pathway](https://github.com/pathwaycom/pathway) ⚡ |
| Data Format    | JSONL, CSV        |
| Visualization  | Bokeh, Matplotlib |
| Platform       | Google Colab      |
| Version Control| Git + GitHub      |

## Architecture Diagram
[User Data]
     ↓
[Data Cleaning & Feature Engineering (Pandas)]
     ↓
[Pricing Models (Linear, Demand, Competitive)]
     ↓
[Streaming Output (Pathway)]
     ↓
[JSONL Output + Visualization (Matplotlib/Bokeh)]

## 🔁 Workflow & Architecture Explanation

1. **Data Ingestion**: Historical parking data (CSV) is cleaned and encoded.
2. **Feature Engineering**: Occupancy ratio, traffic level, queue length, and vehicle weights are computed.
3. **Pricing Models**:
   - Linear Pricing: Based only on occupancy.
   - Demand-Based Pricing: Uses weighted factors (occupancy, queue, traffic, etc.)
   - Competitive Pricing: Adjusts prices based on nearby parking lots within 1 km.
4. **Streaming Simulation**:
   - The dataset is converted to a JSONL stream.
   - Pathway reads the stream and applies the pricing logic row by row in real-time.
5. **Output**:
   - Computed prices are written to `realtime_output.jsonl`
   - Plotted using Matplotlib/Bokeh for time-based trends.

## ▶️ How to Run This Project

1. Clone the repository:
   ```bash
   git clone https://github.com/lavanyasaxena01/urban parking pricing.git
   cd urban parking pricing

pip install -r requirements.txt

python pathway_simulation.py

tail realtime_output.jsonl

## 👥 Contributors

- [Lavanya Saxena](https://github.com/lavanyasaxena01)

