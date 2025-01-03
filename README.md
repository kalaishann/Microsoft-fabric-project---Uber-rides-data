
# Uber Rides-Dashboard - Using Microsoft Fabric, POWER BI

https://github.com/user-attachments/assets/eaa3b70a-8960-482c-9619-cdbb37fb741d

## Problem Statement

This dashboard helps the Uber Rides understand their customers better and increase their revenue. It helps the Uber Rides know if their customers are satisfied with their services. Through divers ratings, they get to know their improvement area, & thus they can improve their services by identifying these area. It also let them know in which location have to increase the vehicle availability & driver availability, thus since by using this dashboard they have identified this problem, they can further work on factors responsible for these unwanted delays.


Also since customer preferrence for long & short distance drive is comparably low for electric fuel type vehicle than the petrol and disel fuel type vehicles.

This dashboard will help them to figure out total number of ride taken on weekdays as well as weekend also what is the revenue status for prime hrs & normal hrs.


### Steps i followed 

- Step 1 : Created a Gateway: 
      - Installed and configured the On-premises Gateway in (Standard mode - for collaborating with team). To pull data from on premises from folder files as well as SQL DB, etc.(here i have used Microsoft fabric as my platform).
![Connecting SQL DB to Fabric ](https://github.com/user-attachments/assets/714ac744-a962-4b80-a120-aa119d6dd53d)
- Step 2 : Created workspace:
      - Created an uber workspace in fabric to keep Lakehouse,Warehouse,Data pipeline, Data flows, Sematic model as well as POWERBI report.

- Step 3 : Data Storage:

     - Lakehouse – Created a Lakehouse to store all kind of raw data files including JSON, XML, CSV, EXCEL, SQL data.
     - ![Establishing connecting between on prem to Fabric using Data pipeline](https://github.com/user-attachments/assets/2d932ba2-0b38-45fa-b486-ee26d64f8417)
     ![Diverse files stored in lakehouse](https://github.com/kalaishann/Test/blob/96408a73f64d65fd3696368369d561646ce003e8/Lakehouse%20storage.png)

     - Warehouse – Created a Warehouse to store structured data in tabular format for SQL analysis.

- Step 4 : Data Transformation:
     - Dataflow – Created Dataflow Gen 2 for each files in Lakehouse and implement complex data calculation using DAX, Calculated columns and measures to transform raw data in to structured data in tabular format.
     - Created a strong data model that can handle uncertainties, changes without compromising the data quality to
support (OLAP – Online analytical processing).

- Step 4 : Data pipelines:
     -  Pipeline 1 – for on premises to LH
     -  Pipeline 2 – SQL DB to LH
     -  Final pipeline – To invoke PL1 and PL2 one after other to streamline the data flow.
     -  ![LH -On premises Raw data upload](https://github.com/user-attachments/assets/746d6713-69b8-451a-93bb-aa49b16d982d)
- step 5: Reporting:
     - Designed an interactive dashboard in Power BI Desktop, connected via One Lake Data Hub – to bring sematic
model from warehouse in the fabric environment.
     - Created a Date Master Table to streamline reporting across all datasets.
     - Build a Three pages report – Summary, Driver, User.
### Summary View:
- Key KPIs - Total Location, Total Users, Total Drivers, Total Distance, Total Duration, Total Fare, Total Revenue.
- Slicers – Year, Month, Day.
Dynamic summary view based on model.
- Flow of Revenue based on Prime/ normal hours, Pickup location and drop off location.
- Revenue (Min, Avg, Max) based on hours (Prime/Normal) breaking in to day of the week.
- User Trend on each Quarter by Day of the week.
- Revenue based on Fare per Month.
- Page navigator for Driver and User view and info button.
### Driver View:
- KPIs – Total Locations, Total Trips, Revenue based on Ride Category (Long Travel, Medium Travel and Short Travel).
- Slicers – Driver Id, Vehicle Id, Year, Month, Day.
- Average fare and Average distance based on Month.
- Drivers availability based on Fuel type, breaking in to ride category and days (weekday and weekend).
- Driver Performance table based on no of rides and average driver ratings.
- Revenue by capacity and fuel type.
- Page navigator for summary view and User view.
- Back button and info button.
### User View:
- Revenue by User category break down by model.
- Total revenue by User category break down by model and ride category.
- No of Rides by Ride category breaking in to days (weekday / weekend) also by Fuel type.
- User performance table shows User id, No of rides, User category, Ride category, Days.
- Page navigator for Summary view and Driver view.
- Back button and info button.
 

### ETL Process:

- Step 1 : Open power query editor & in view tab under Data preview section, check "column distribution", "column quality" & "column profile" options.
- Step 2 : Also since by default, profile will be opened only for 1000 rows so you need to select "column profiling based on entire dataset".
- Step 3 : In USERS dataset i have added the calculated columns to .
- 
           Although, by default, while calculating average, blank values are ignored.


  
  

       
        
 
         


 
