# PROJECT-1--BENGALURU-ROAD-INFRASTRUCTURE-INFRA-GAP-ANALYSIS

## Project Overview
Project Overview: Bengaluru road infrastructure analysis involves the systematic evaluation of urban connectivity, repair life cycles, and traffic performance for chosen 4 wards (Kormangala, Whitefield, Jayanagar, Yeshwanthpur). This project focuses on analyzing the "Investment-Impact Gap" using historical expenditure data, ward-level metadata, and real-time congestion metrics across key urban hubs. The project provides data-driven insights and recommendations for optimizing budget allocation, enhancing road durability, and improving travel time indices (TTI). By correlating repair cycles with modern congestion levels, the analysis supports strategic decision-making in areas like urban planning, resource prioritization, and infrastructure longevity.

### **Objectives**
1. Analyze Investment-Impact Correlation
2. Identify Infrastructure Gaps
3. Engineered Durability Metrics
4. Optimize Budget Allocation
5. Isolate Congestion Bottlenecks

### **Dataset overview**
<img width="1000" height="766" alt="image" src="https://github.com/user-attachments/assets/1e622f1e-fc2a-48b4-ae69-153730d6374b" />

### **Data Modelling**
<img width="1369" height="675" alt="image" src="https://github.com/user-attachments/assets/fdca108a-0fa3-4269-b874-619971672584" />

SCHEMA: STAR SCHEMA

-FACT TABLE: a. BANGLORE_TRAFFIC_DATASET

-DIMENSION TABLE:

a. BBMP 2014 Ward Delimitation Details

b. BBMP Road repair data 2017

c. BBMP Ward Area & Road Length

d. Calendar table

### **Challenges faced**

1) Data Fragmentation & Silos: Consolidating eight years of disparate data from multiple sources (Government repair logs, historical investment records, and modern traffic APIs) into a single, unified Star Schema.
2) The "Messy String" Problem: The “BBMP road repair 2017” data wasn't in a standard format; it was written as natural language (e.g., "from KH Road to Vivekananda Nagara"). Used Power Query to separate messy strings to get cleaned data.
3) Quantifying "Soft" Metrics: Developing the Durability Index from scratch—translating qualitative road conditions and repair cycles into a quantifiable numerical scale for statistical modeling.
4) The "Many-to-Many" Conflict: Initially, Excel refused to connect your tables because "Indiranagar" appeared multiple times in both. Connected these tables with Bridge tables.
5) Data Typos: During the splitting process, you encountered fragments and typos (like "Joncition") that required the Replace Values and Trim functions to ensure they would match the traffic dataset names.

### **Key KPI Metrics**
1. Total Ward Coverage: 4 Key Hubs (Koramangala, Jayanagar, Yeshwanthpur, and Whitefield).
2. Average Congestion Level: 78.17% (The primary baseline for traffic saturation across focus wards).
3. Average Speed: 39.75 km/hr (Used to correlate infrastructure quality with mobility efficiency).
4. Durability Index: 0.07K (A custom-modeled metric representing the structural health and longevity of the road network).
5. Investment vs. Impact ROI: Identified Yeshwanthpur as the high-ROI zone with 26.91% Speed Contribution despite only 2.97% City Investment. 
6. Repair Lifecycle Peak: Identified 2016 as the peak maintenance year with 481 Km of road repaired, followed by a sharp decline.
7.Travel Time Index (TTI) by Area: Comparative analysis showing Yeshwanthpur (1.36) vs. Whitefield (1.26) to measure delay severity. 
8. Avg. Public Transport Usage: 45.11%
9. Avg. Parking Usage: 75.01%
10. Pedestrian/Cyclist Count: 129 (Highlights the multi-modal nature of road usage).
11. Incident Frequency: Longitudinal tracking of incidents per location (e.g., Koramangala peaking at 9 reports in 2023).



