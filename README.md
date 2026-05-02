**Car Purchase Analysis Dashboard**
An interactive business intelligence dashboard built for the INI8 Labs Data Analytics Engineer assessment — uncovering buyer behavior, sales trends, and geographic insights across 999 car purchases.

**Project Structure**
Car_Purchase_Analysis.pbix — Main Power BI dashboard file
car_data.csv — Cars fact table with brand, price, make year
buyer_details.csv — Buyer demographics, country, salary, department
README.md — Project documentation (this file)

**✨ Key Features & Visuals**

**📅 Purchase Trend Over Time**
Line chart showing monthly car purchase count — reveals seasonality and demand spikes.

**🏆 Top 5 Brands by Sales**
Horizontal bar chart ranking Ford, Chevrolet, Toyota, GMC by total sales value.
**🌍 Buyers by Country**
Bar chart showing buyer distribution — Russia and Brazil lead buyer count.

**💰 Avg Salary by Country**
Pie chart comparing average salaries — Netherlands, Saudi Arabia, Norway highlighted.

**⚥ Gender vs Car Make Year**
Bar chart revealing gender-wise preference trends across car manufacture years (1960–2020).

**🏢 Avg Car Price by Dept**
Column chart identifying which department purchases the most expensive cars on average.

**📋 Gender × Brand Matrix**
Cross-tab table showing brand preference per gender — Acura, Audi most popular among males.

**🔵 Repeat vs Single Buyers**
Donut chart identifying buyer type — 100% of the dataset currently flagged as new buyers.

**DAX Measures & Calculated Columns**

**Latest Car Bought Date** — Calculated column on Cars table using MAX of purchase date per buyer ID, joined via Buyer Details.

**Avg Car Price by Year** — Measure to identify the year with the highest average car price using AVERAGEX over a date table.

**Buyer Type Flag** — Calculated column classifying buyers as Repeat or Single-time based on purchase count per buyer ID.

**Avg Salary by Country** — CALCULATE + AVERAGE measure filtered by country dimension.

**🗃️ Data Model**

A Date table was created using DAX CALENDAR() and linked to the Cars fact table on the purchase date field.
Relationships: Cars table → Date table (many-to-one on date key), Cars table → Buyer Details (many-to-one on buyer ID).
A Date slicer (slider) is connected to the Date table and filters all visuals on the dashboard simultaneously.

**Key Insights**
Ford leads all brands in total sales value, followed by Chevrolet and Toyota.
Russia has the highest number of car buyers, suggesting a strong market presence.
Netherlands buyers earn the highest average salary (~₹7.68K/month equivalent).
Males show strong preference for Acura and Audi; females lean toward Acura and Audi as well but with lower volume.
Car purchases peaked in the early 2000s based on make year trends.
Avg car price is relatively consistent across departments, ranging around ₹20K–₹35K.
