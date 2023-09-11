# BCG-Zomato-PowerBi
PowerBi Project for BCG Rise 2.0 
This is the individual PowerBi Project for the BCG Rise Course I am currently undertaking.

In this project, we are using the zomato dataset provided by the course.

Restaurant Performance Analysis 

DESCRIPTION

Zomato is a restaurant aggregation and meal delivery service based in India. It is currently operating in several countries across the world. Zomato provides thorough information about numerous eateries as well as consumer reviews. Zomato's owners aim to find hidden irregularities in their company's data. The ultimate goal of this project is to examine the data in such a way that they can accurately assess their business performance.

The data (sample) is currently accessible in the form of a few Excel files, each of which contains information about multiple restaurants operating in a certain continent. The clients want to construct a consolidated and interactive Power BI report that will allow them to do the following:

1.	Derive data on the total number of restaurants worldwide, including continents, countries, and cities 
2.	View data on a global scale with the capacity to drill down to a granular level
3.	Derive data on the restaurants with the highest average customer ratings 
4.	Discover the restaurants with the lowest average costs
5.	Filter and view information on the restaurants based on:
•	Their geographical dimensions such as continent, country, and city.
•	The service they provide, such as online ordering or reservation services
•	The average rating slab by the color.
       6. Identify the restaurants with the most cuisines served.
       7. Design a multi-page report that suits Zomato's theme with easy navigation across sections.
       8. Allow Zomato users to be able to access this information from both a web browser and a mobile device. 
 
Aim of the project:
The aim is to construct a consolidated and interactive PowerBI report that will allow Zomato to quickly assess the required data.
 
Steps that will help in the completion of the project:
1. Import the data from all available Excel files
2. Data transformation: 
•	Make sure the City column names are corrected 
                            For example: 
               “Sí£o Paulo” should be corrected to “São Paulo”
•	Ensure the city name isn't ambiguous
               For example: 
              “Cedar Rapids/Iowa City” should be corrected to “Cedar Rapids”
              “ÛÁstanbul” should be corrected to “Istanbul”
3. Remove any columns that aren't being used 
4. Create two columns to display the Restaurant Name and Restaurant Address
5. Make a separate table for the list of the cuisines that each restaurant serves
6. As it's a dimension table, the Country-Code table must only include unique and non-blank values
7. Create an efficient data model from the tables loaded
 
Steps to use DAX in the project:
1) Add a Rating color column in an appropriate table with the data rows in the format given below
                                                      
Aggregate rating                         	Rating color
Above 4.5  	                              Dark Green
 
4 to 4.4  	                              Green
 
 
2) Create the following measures in the appropriate tables 
a. Restaurant count
b. Average cost
c. Average rating 
d. Cuisine count
3) Create a new column in the Country Code table and name it “Continent” and create the values using the below-mentioned convention
Note: The mapping is continent - country, for example ''Africa – South Africa''

To meet the objectives of the project, I firstly planned out my dashboard into 3 board categories
1. Global View -
   1.1 Showcasing the global reach of Zomato using a Map with number of restaurants as bubble size, ability to drill down into continent,city then restaurant levels.
   1.2 Cards with headline numbers including total restaurants, Average Rating, No. Of cuisines. These intereacted with the map view and would change accordingly
   1.3 Slicers - Ability to filter by continent, country, city, ratings

2. Performance Details -
   2.1 Created a table with restaurant names, Votes Received, Average Spend for 2 (USD) , No. of Cuisines Served, Rating Score. The restaurants selected could be drilled through to a hidden restaurant details page
   2.2 Key factors - 2 Combination charts. 1 for average rating by no of cuisines served ( Testing if More cuisines translate to higher scores), Second chart is the sum of votes and average rating (Does more votes translate to a better rating) both proved not to be the case.
   2.3 2 Pie charts detailing how many restaurants had table booking or online delivery.

3. Restaurant Details -
   3.1 Table with restaurant names, votes, price range
   3.2 Cards with average rating, booking/online delivery, Price Range, City and Country.

4, Key Influencers on Rating -
  Using the inbuilt analysis tool i wanted to see what factors would influence aggregate rating. 


Importing and Cleaning the raw data.
1. After importing all the given csv files, I proceeded to cleaning the data in Power Query. There were missing data in rows and in some cases i chose to omit the entire column (Lat/Long) as the data was unrealiable.
2. Cleaning also involved renaming incorrect cells etc.
3. I also added in columns continent, split the Restaurant Name/Address column into usable columns.
4. I also added in a currency column in the KPI chart and added in the appropriate conversion to USD so that we are better able to compare costs across continents. 
5. After all the cleaning was done i Appended all the country databases together to create a Global database. This was to reduce the number of connections and improve efficency.

Creating Measures/DAX
1. Had little issues creating the required measures and dax.

   
