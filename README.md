# **Uber Trip Analytics Dashboard**

## **Project Overview**
This project analyzes Uber trip data to uncover booking patterns, revenue performance, trip efficiency, and demand behavior across time, locations, and vehicle types. Using Power BI, the solution delivers an end-to-end analytical workflow  transforming raw trip records into insights that support operational optimization, pricing decisions, and rider experience improvements.

<img width="1047" height="587" alt="Overview Analysis" src="https://github.com/user-attachments/assets/1e777664-27c1-457a-b48e-808181c1b2ee" />


---

## **Problem Statement**
Uber requires a clear understanding of how customers book rides, how revenue is generated, and how trip distance/time vary across the day, week, and city locations.  
The goal is to enable stakeholders to:

- Identify booking and revenue trends  
- Evaluate operational efficiency (distance, duration, idle hours)  
- Understand temporal demand (hourly, daily, day-of-week)  
- Optimize driver allocation, pricing models, and resource planning  
- Improve customer satisfaction through data-backed decision-making

---

## **Analytical Objectives**
- Analyze **Total Bookings**, **Revenue**, **Trip Distance**, and **Trip Duration**.
- Compare trip behavior by **time of day**, **day of week**, and **location**.
- Identify **peak demand windows** for operational optimization.
- Evaluate vehicle type performance to guide **fleet and resource distribution**.
- Assess customer preference across **payment types** and **trip types**.
- Enable drill-through into granular records for audits and deeper analysis.

---

## **Workflow Summary**
This project follows a complete BI lifecycle:

### **1. Data Ingestion**
- Imported Uber trip dataset into Power BI  
- Initial structural review of fields (payment type, vehicle, date/time, distance, location)

### **2. Data Cleaning – Power Query**
- Standardized payment types and vehicle categories  
- Cleaned inconsistent pickup/drop-off labels  
- Created proper Date/Time fields  
- Removed duplicates and corrected empty or invalid trip records  

<img width="1305" height="657" alt="Trip Details Table" src="https://github.com/user-attachments/assets/cbf3af19-9d76-4865-8d56-debeddd8df28" />


### **3. Data Modeling**
- Built a star schema with:
  - **Fact Table:** Trip Details  
  - **Dimensions:** Date, Time, City, Location, Vehicle Type, Payment Type  
- Created **inactive relationship** for switching between pickup and drop-off analysis  
- Added Calender table for Time Intelligence

<img width="1188" height="593" alt="Star Schema Data Model" src="https://github.com/user-attachments/assets/92059bf8-354a-426d-b95b-aa62a095a959" />

### **4. DAX Calculations**
- I implemented DAX calculations to analyze key metrics, including total bookings, total and average booking value, total and average trip distance, and trip duration in minutes. Additional measures aggregate data by hour, day, and day of the week, complemented by a dynamic selector that allows toggling between different KPIs.

#### Furthest Trip DAX:

<img width="973" height="500" alt="Furthest Trip DAX" src="https://github.com/user-attachments/assets/73550502-8010-4a3b-8bdf-ff83944fd048" />

#### Most Frequent Drop off Point DAX:

<img width="970" height="500" alt="Most Frequent Drop off Point DAX" src="https://github.com/user-attachments/assets/a5a82184-1fec-4695-a324-1dcdb3c77757" />


### **5. Dashboard Development**
- **Dashboard 1: Overview Analysis**  
- **Dashboard 2: Time Analysis**  
- **Dashboard 3: Details View (Drill-through)**  
- Added bookmarks, slicers, dynamic titles, conditional formatting, and user-friendly interactions  

---

## **Dashboards & Visualizations**

### **Dashboard 1: Overview Analysis**
Provides an overview of Uber trip activity, focusing on bookings, revenue, distances, trip and payment types, vehicle performance, and location insights. Key visuals include KPI cards for core metrics, breakdowns by payment and trip type, daily booking trends, vehicle performance grids, and analyses of top pickup/drop-off points, most popular booking locations, and preferred vehicles per location.

<img width="1047" height="587" alt="Overview Analysis" src="https://github.com/user-attachments/assets/18d6abb1-ebc9-4d36-8d27-d407b79a0e4b" />


---

### **Dashboard 2: Time Analysis**
Focuses on time-based analysis, highlighting hourly, daily, and weekly demand patterns. Key visuals include bookings by 10-minute pickup intervals, daily trends, an hour-by-day-of-week heatmap, and a dynamic measure selector to switch between bookings, revenue, and distance metrics.

<img width="1047" height="581" alt="Time Analysis" src="https://github.com/user-attachments/assets/d9f45fa5-440d-4636-8843-8cbb669792a1" />


---

### **Dashboard 3: Details Tab**
Provides a detailed trip-level view, offering a complete data table with trip ID, date, time, vehicle, payment type, passengers, distance, fares, and pickup location. It includes drill-through functionality from charts to filtered records and bookmarks to toggle between full and filtered data views.

<img width="1046" height="587" alt="Details Dashboard" src="https://github.com/user-attachments/assets/4d5d367a-2034-4ff1-a9a0-cfe51486fb26" />


---

## **Key Insights**
The Key insights I drew were:

1️⃣ **UberX dominates customer preference**, generating the highest ride volume and revenue — guiding fleet prioritization.  
2️⃣ **Uber Pay leads as the primary payment method**, indicating strong adoption of digital payments and requiring reliable system uptime.  
3️⃣ **Night trips contribute ~65% of all bookings**, signaling higher demand during late hours and the need for increased driver availability.  
4️⃣ **Peak demand occurs between 7AM–10AM and 4PM–9PM**, ideal windows for dynamic pricing and driver surge allocation.  
5️⃣ **Sunday shows the highest booking volume (19.2K)**, while Thursday has the lowest — useful for weekly driver scheduling.  
6️⃣ **Penn Station / Madison Sq West is the top pickup hub**, highlighting a major transit-driven cluster requiring high driver density.  
7️⃣ **Farthest trip spans 144 miles**, revealing outlier long-distance demand useful for fare optimization and potential regional service improvements.

---

## **Recommendations**
- **Enhance driver allocation** during peak windows (AM & PM rush hours, weekends).  
- **Strengthen digital payment systems** since Uber Pay drives the majority of transactions.  
- **Boost nighttime driver incentives** because night trips dominate demand.  
- **Leverage dynamic pricing** in high-volume locations like Penn Station and Upper East Side.  
- **Promote UberX and Comfort vehicles** to maximize revenue in high-traffic zones.  
- **Use weekly insights** to optimize driver schedules, especially increasing coverage on Sundays.

---

## **Tools & Technologies**
- **Power BI** – Data modeling, DAX, dashboard design  
- **Power Query** – ETL transformation and cleaning  
- **DAX** – KPI creation, time intelligence, dynamic measures  
- **Excel** – Data source and initial preprocessing  
- **Bookmarks & Drill-through** – Enhanced user experience  
- **Conditional Formatting & Slicers** – Visual clarity and interactivity  

---

