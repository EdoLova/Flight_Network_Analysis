# Flight Network Analysis

This project performs a comprehensive analysis of the US flight network using Apache Spark and GraphFrames.  
The goal is to explore flight patterns, airport connectivity, and hub importance by modeling the airline network as a graph and computing several graph-theoretic metrics.

---

## Objectives
- Transform US flight data (2018) into a graph structure:  
  - Nodes represent airports  
  - Edges represent flights connecting airports
- Compute network statistics and metrics:
  - Node degree (in-degree, out-degree, total degree)  
  - Local and total triangle counts  
  - Eigenvector centrality  
  - PageRank scores
- Identify the most connected and structurally important airports
- Validate results against GraphFrames built-in functions
- Optional visualization of network structure and flight volume heatmaps

---

## Tools and Technologies
- Python  
- Apache Spark  
- PySpark DataFrames and RDD API  
- GraphFrames  
- Pandas, Matplotlib, iGraph  
- Docker-based Spark environment for reproducibility  

**Dataset:** `flights_2018.csv` (US flights including origin, destination, delays, and counts)  

**Architecture:**  
CSV Dataset → Spark DataFrame → GraphFrames → Graph Analysis → Visualization

---

## Main Results
- The US airport network exhibits a hub-and-spoke, scale-free architecture.
- **Atlanta (ATL)** and **Chicago O’Hare (ORD)** are the busiest hubs by flight volume (weighted degree) and PageRank.
- **Minneapolis (MSP)** and **Charlotte (CLT)** rank higher in Eigenvector centrality than in volume-based metrics, highlighting strategic connections to other major hubs.
- Total triangle count: **24,120**, reflecting the robustness and alternative routing potential in the network.
- PageRank and Eigenvector centrality provide nuanced insights into airport importance beyond raw flight counts.
- Visualizations reveal a dense core-periphery structure and a flight volume heatmap highlighting key corridors.

---

## Project Structure
Each task is implemented in a dedicated Jupyter notebook (`TP3_Lovato_Markhovski_Piccoli.ipynb`), following the project assignment structure:

### Tasks
1. **Node Statistics** – Compute in-degree, out-degree, total degree  
2. **Single Triangles Count** – Count triangles per node  
3. **Total Triangle Count** – Aggregate global triangle metrics  
4. **Eigenvector Centrality** – Compute influence of airports  
5. **PageRank Algorithm** – Compute weighted PageRank  
6. **Most Connected Airports** – Identify top airports by total degree  
7. **Most Important Airports** – Identify key hubs using PageRank and Eigenvector  
8. **Validation** – Compare manual implementations with GraphFrames built-in functions  
9. **Visualization (Bonus)** – Graph layout and flight volume heatmaps  

---

## Usage
1. **Environment Setup:**  
   Start Docker container with Spark and Jupyter: Start Docker container with Spark and Jupyter:  
   "docker-compose up", then access the Jupyter URL (usually `http://127.0.0.1:8888`) and select the PySpark kernel.  
2. **Run Notebook:**  
   Set the year variable if needed, then run all cells sequentially.  
3. **Install Missing Libraries:**  
   "!pip install python-igraph matplotlib pandas"
4. **Visualization:**
   Execute optional cells for network graph and flight heatmap visualizations.

---

## Authors

Edoardo Lovato

Julia Markhovski

Leonardo Arduino Piccoli

Université Claude Bernard Lyon 1
Data Processing and Analytics (DPA)
Academic Year 2025–2026
   
