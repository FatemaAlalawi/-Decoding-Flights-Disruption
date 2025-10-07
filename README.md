#  Decoding Flights Disruption

## 📊 Project Overview
This Power BI dashboard analyzes US airline flight delays and cancellations from August 2019 to August 2023 (3M+ flights) to identify root causes and provide data-driven recommendations for improving operational efficiency.

## 🎯 Business Problem
US flight delays and cancellations have caused passenger complaints to increase by 252% compared to 2019 levels, highlighting significant operational inefficiencies in airline operations.

## 📁 Dataset
- **Source**: US Bureau of Transportation Statistics & Department of Transportation
- **Period**: August 2019 - August 2023
- **Records**: 3M+ flights
- **Airlines**: 18 major US carriers

## 🔧 Technical Implementation

### Power BI Features Used
- **DAX Measures**: Custom calculations for delay analysis, performance metrics, and categorization
- **Calculated Columns**: Data transformation and categorization
- **Interactive Visuals**: Scatter plots, bar charts, time series, and custom maps
- **Data Modeling**: Star schema with relationships between fact and dimension tables

### Key DAX Measures & Columns
- `Delay Recovery` = Arrival Delay - Departure Delay
- `Taxi-Out Category` = Categorized gate-to-runway times (Normal, Concerning, Severe, Critical)
- `Time Status` = Classified flights as Delayed, Early, or On-Time
- `Flight Duration Category` = Grouped flights by length (Short, Medium, Long, Very Long)
- `Realistic Departure Delay` = Filtered outlier delays for accurate analysis
- `Arrived Delayed %` = Percentage of flights arriving more than 15 minutes late
- `Arrived Early %` = Percentage of flights arriving before scheduled time
- `Arrived On-Time %` = Percentage of flights arriving within 15 minutes of schedule
- `Cancelled %` = Percentage of cancelled flights
- `Significant Delay Rate` = Percentage of delays longer than 15 minutes
- `Departure Hour` = Extracted hour from departure time
- `Month Name` = Full month name from date
- `Day of Week` = Full weekday name from date
- `Official Delay Category` = Categorized delays as Minor, Significant, or Extreme
- `Route` = Origin and destination airport codes combined
- `Overall Status` = Final flight status (Cancelled, Delayed, Early, On-Time)
- `Total Flights` = Count of all flights in dataset
- `Operated Flights` = Count of flights that were not cancelled
- `Delayed Arrivals` = Count of flights arriving more than 15 minutes late
- `On-Time Flights` = Count of flights departing and arriving within 15 minutes of schedule

## 📈 Key Insights

### Performance Metrics
- **33%** of flights arrived delayed
- **64%** arrived early (indicating inefficient scheduling)
- **3%** cancellation rate
- Average departure delay: **10.12 minutes**
- Average arrival delay: **4.26 minutes**

### Critical Findings
1. **Short flights (0-60 min)** are most vulnerable to delays with poor recovery capability
2. **Peak hours** (7-9 AM, 5-7 PM) experience severe congestion
3. **Friday operations** show the worst performance across all metrics
4. **Regional airports** suffer from infrastructure limitations
5. **Holiday seasons** (June & December) see significant disruption spikes

## 🗺️ Dashboard Structure

### 1. Overall Performance
- Flight status distribution (Delayed, Early, On-Time, Cancelled)
- Airline performance comparison
- Annual trends and COVID impact analysis

### 2. Location & Routes Analysis
- High-delay routes (LAS-MDW, LAS-DAL, DEN-MDW)
- Regional airport challenges
- Geographic delay patterns

### 3. Time Contribution
- Hourly, daily, and seasonal delay patterns
- Peak period identification
- Holiday season impact

### 4. Operational Efficiency
- Gate-to-runway time analysis
- Delay recovery by flight distance
- Scheduled vs. actual time performance

## 💡 Recommendations

### Strategic Improvements
1. **Optimize Schedules**
   - Add buffers to short-haul routes
   - Tighten long-haul schedules
   - Implement dynamic scheduling

2. **Fortify Operations**
   - Strategic staffing during peak hours
   - Boost Friday operations
   - Mandate contingency plans

3. **Target Infrastructure**
   - Upgrade regional airport resources
   - Optimize arrival sequencing
   - Reduce taxiway congestion

## 🚀 How to Use
1. Open `Flight_Disruption_Analysis.pbix` in Power BI Desktop
2. Refresh data connection if needed
3. Use interactive filters to explore specific airlines, time periods, or routes
4. Hover over visuals for detailed tooltips and insights

## 📋 Requirements
- Power BI Desktop
- Basic understanding of airline operations terminology
- Familiarity with delay analysis concepts

## 👥 Audience
- Airline Operations Management

---

*This analysis provides actionable insights to reduce flight disruptions and improve passenger satisfaction through data-driven operational improvements.*
