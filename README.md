📄 Aerial Network Delay Optimization using Python📌 Project Overview

This project addresses the Aerial Network Delay problem in aeronautical ad-hoc networks (AANETs), where aircraft flying over the North Atlantic must route data efficiently to ground stations.
The goal is to compute optimal routing paths by optimizing end-to-end data transmission rate and end-to-end latency using Python-based simulation and optimization techniques.
The project uses real flight position data, models aircraft-to-aircraft and aircraft-to-ground links, and evaluates both single-objective and multi-objective routing strategies.

🎯 Problem Statement
Thousands of aircraft require continuous internet connectivity while in flight.
Due to high mobility, dynamic topology, and distance-dependent link quality, routing data packets efficiently is challenging.
This project aims to:


Maximize end-to-end data transmission rate


Minimize end-to-end latency


Analyze trade-offs between throughput and delay



🧠 Solution Approach
The project implements a network optimization pipeline:


Load real flight trajectory data (latitude, longitude, altitude)


Convert geographic coordinates to 3D Cartesian space


Compute inter-aircraft and aircraft-to-ground distances


Estimate transmission rate and latency per link


Solve:


Single-objective optimization (maximize throughput)


Multi-objective optimization (maximize throughput & minimize latency)




Export optimal routing paths for analysis



🛠️ Tech Stack


Programming Language: Python


Data Processing: CSV, Pandas


Computation: Math, NumPy


Optimization Logic: Custom routing algorithms


Visualization & Output: Excel (openpyxl)


Environment: Jupyter Notebook



📂 Project Structure
Aerial-Network-Delay/
│
├── ArealNetworDelay.ipynb
├── NA_11_Jun_29_2018_UTC11.CSV
├── optimal_paths.xlsx
├── Aerial Network Delay.pdf
├── README.md
└── requirements.txt (optional)


🔄 Workflow1️⃣ Dataset Loading & Exploration



Load real flight trajectory dataset


Parse flight ID, timestamp, latitude, longitude, altitude


Inspect flight distribution over the North Atlantic



2️⃣ Coordinate Transformation


Convert geographic coordinates to Cartesian coordinates


Enable accurate 3D distance calculations between nodes



3️⃣ Distance & Link Modeling


Compute aircraft-to-aircraft and aircraft-to-ground distances


Model transmission rate as a function of distance


Compute latency using speed-of-light approximation



4️⃣ Single-Objective Optimization
Objective: Maximize end-to-end data transmission rate


Evaluate routing paths to Heathrow (LHR) and Newark (EWR)


Select paths with highest bottleneck transmission rate



5️⃣ Multi-Objective Optimization
Objective: Maximize transmission rate and minimize latency


Evaluate competing routing paths


Select optimal trade-off paths for each aircraft



6️⃣ Result Export & Analysis


Save optimal routing paths to Excel


Separate results for Heathrow and Newark ground stations


Analyze routing efficiency and delay characteristics



📊 Evaluation MetricsThroughput Metric



End-to-end data transmission rate (minimum link rate)


Delay Metric


End-to-end latency (sum of link delays)



✅ Results


Successfully identified optimal routing paths for aircraft


Demonstrated trade-off between latency and throughput


Validated feasibility of optimization-based routing in AANETs


Exported structured results for further analysis



👨💻 Author
Nikhil Sai
B.Tech – Electronics and Computer Engineering
Computer Networks | Optimization | Python
