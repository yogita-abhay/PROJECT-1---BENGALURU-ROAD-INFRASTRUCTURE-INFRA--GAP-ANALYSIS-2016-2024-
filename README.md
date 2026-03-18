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

### **EXCEL DASHBOARD**
<img width="1954" height="951" alt="image" src="https://github.com/user-attachments/assets/c96ee421-e02c-4b0e-b41c-bfc4b3b76e79" />

### **POWER BI DASHBOARD**
<img width="1485" height="824" alt="image" src="https://github.com/user-attachments/assets/acb63904-1e7e-4e48-b457-42338edd57b2" />

### **TAKEAWAYS**
1. Investment-Efficiency Mismatch: The data reveals a significant "Investment Gap." While Jayanagar received 77.8% of the city’s infrastructure investment, it only contributed 24.65% to speed improvements, whereas Yeshwanthpur showed much higher ROI with minimal funding.

2. Critical Congestion Threshold: Across the four focus wards, the average congestion level sits at a critical 78.17%, indicating that current road capacity is nearly saturated despite the 481 Km of repairs completed during the 2016 peak.

3. The "Maintenance-Delay" Correlation: Spatial analysis proves that areas with the oldest repair cycles (pre-2015) currently exhibit the highest Travel Time Index (TTI), particularly in Koramangala, proving that infrastructure "health" is a direct predictor of traffic flow.
   
4. Diminishing Returns on Repairs: The sharp decline in road repaired length from 481 Km (2016) to 189 Km (2017) correlates with the rising incident reports in subsequent years, highlighting the need for a preventative rather than reactive maintenance model.

5. Predictive Value of the Durability Index: By utilizing the custom 0.07K Durability Index, urban planners can now predict which wards will hit "gridlock status" (TTI > 1.5) before the structural failure actually occurs.

### **STRATEGIC RECCOMENDATIONS**

1.Implement ROI-Based Budgeting: Move away from the current high-investment model in saturated zones like Jayanagar (77.8% investment). Instead, reallocate funds toward high-impact, low-cost "quick wins" identified in Yeshwanthpur, where small investments yielded a 26.91% speed contribution.

2. Transition to Predictive Maintenance: The sharp rise in incidents following the 2016 repair peak indicates a reactive cycle. Use the Durability Index to trigger road maintenance before the index drops below a critical threshold, preventing the 78.17% congestion spikes caused by surface failures.

3. Targeted Bottleneck Interventions: Focus engineering resources on Koramangala and Whitefield, which show the highest Travel Time Index (TTI). Since these areas have lower speed contributions relative to investment, physical interventions like "Tactical Urbanism" or signal synchronization are needed over simple repaving.

4. Multi-Modal Integration: With Pedestrian/Cyclist counts at only 129, there is a massive opportunity to reduce the 75.01% Parking Usage and road congestion by investing in non-motorized transport (NMT) lanes, particularly in high-density wards.

5. Digital Twin & Real-Time Monitoring: Upgrade the current historical analysis into a "Live Infra-Gap Tracker." By integrating real-time traffic APIs with the existing Star Schema SQL database, planners can receive automated alerts when TTI exceeds 1.5 in any ward.


