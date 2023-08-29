# DEFORESTATION-ANALYSIS-USING-SQL
 
# **INTRODUCTION**
This analysis is focused on the manipulation of sql query and its operators to determine the deforestation of countries of several continents. Three dataset was provided for this analysis, this will be solved using sql aggregate functions, joins and even subquerys.

# **ACTIVITY**
1. To determine the total number of countries involved in deforestation.
2. To determine the income groups of countries having total area ranging from 75,000 to 150,000
3. The retrieval of country names that have a forest area(in Square Kilometers) greater than the average forest area of all countries in the 'high Income' income group
4. To calculate the average total area (in square miles) for countries in the 'upper middle income' income group, then compare the result with the rest of the income categories.
5. To detemine the total forst area( in square kilometers) for countries in the 'high Income' income group, alos compare with the other income categories
6. What are the countries from each region or continent having the highest forest area?

# **SKILL DEMONSTRATED**

1). Creating a new database and the importation of three datasets into the table section of the new.
2). The use of operational keywords. 
3). Joins and subquerys

# **DATA IMPORTATION AND DATA QUERY

A new database was created on my SQL server management by cliking on 'New Query', this activated a work interface where I wrote the code 'CREATE DATABASE DEFORESTATION;' then I clicked 'Execute' to executed the code, this developed a database accessed on the left-handside of the work interface. Then I imported the three dataset names; Forest, Land and Regions by right-clicking on 'importing flat-file' on my newly created deforestation database, This loaded the files into the table section of the deforestation database, the three tables have matching column that made it easy to join the tables together, view a screenshot of the raw data imported.

![Deforestation raw data](https://github.com/Jessie-Watt/DEFORESTATION-ANALYSIS-USING-SQL/assets/140435577/b1511cbb-172f-48e1-95cf-e781aab36d70)


To achieve the activity of the total number of countries involved in the deforestation I joined the three datasets on matching columns of 'country_name' then I used the aggregate function of 'count' to determine the countries involved the deforestation, then I renamed the new column as 'total country'. The screeshot can be seen below.

 ![Total countries](https://github.com/Jessie-Watt/DEFORESTATION-ANALYSIS-USING-SQL/assets/140435577/ba29d691-6531-4cec-9297-0c17a7805a81)


To determine the income groups of countries having total area ranging from 75,000 to 150,000, I used the inner join operator to join the land and regions table togther on matching 'column_name' then the 'where' operator was used to generate total area of countries between the range of 75,000 and 150,000.
![Countries with tot_area btw 75k and 150k](https://github.com/Jessie-Watt/DEFORESTATION-ANALYSIS-USING-SQL/assets/140435577/1da8b92f-d22a-41bd-b7d0-047f5ef17167)

The retrieval of country names that have a forest area(in Square Kilometers) greater than the average forest area of all countries in the 'high Income' income group was achieved by first calculating the average 'forest area' in the forest table using the aggregate function, then the forest and regions table were inner joinned on the 'where' operator conditioning the 'forest area' to produce an output of all countries greater the subqueried 'average forest_area' and and also streamlining it to only the 'high income' on the income group. Please see the screenshot below.

![Countries with greater forest area high income](https://github.com/Jessie-Watt/DEFORESTATION-ANALYSIS-USING-SQL/assets/140435577/a2055d94-26d3-455c-8805-dd7d8ed06003)

To calculate the average total area (in square miles) for countries in the 'upper middle income' income group, then compare the result with the rest of the income categories. This was achieved using the aggreagte function to calculate the average total area first, then the 'forest' and 'regions' tables were joined on matching columns of country_name conditioning the income group of all countries to calculate for only the 'uppermiddle income'. Incase where countries having total area greater than average total this was also considered in the second screenshot.
    

![avg Total Area of countries in the upper middle income](https://github.com/Jessie-Watt/DEFORESTATION-ANALYSIS-USING-SQL/assets/140435577/acb81197-5356-4231-84a4-417da9f36ea7)

![avg total area of countries greater than average total area](https://github.com/Jessie-Watt/DEFORESTATION-ANALYSIS-USING-SQL/assets/140435577/44d24118-66e4-459c-a5a6-8b177f94d733)

To evaluate the total forest area (in square kilometers) of countries in the 'high Income' income group, the sum of the forest_area_sqkm was calculated, then I joined  'regions' and 'forest' tables comparing the individual forest area to the aggregated summation of the forest areas conditioning it to the 'high income' of the income group.

![Total forest area of countries in high income](https://github.com/Jessie-Watt/DEFORESTATION-ANALYSIS-USING-SQL/assets/140435577/d2cd809b-e6d3-41b3-8b89-33551caee829)

The countries from each region or continent having the highest forest area. The max country was first determined

![Max Forest are sqkm](https://github.com/Jessie-Watt/DEFORESTATION-ANALYSIS-USING-SQL/assets/140435577/259611eb-fcf8-4057-bf4c-1855d42e2497)

![Countries with highest forest area](https://github.com/Jessie-Watt/DEFORESTATION-ANALYSIS-USING-SQL/assets/140435577/e684856a-ccd1-4b32-a3a4-8b33ea36f79e)


# CONCLUSION
This task exposed and enlighted my understanding in the use of SQL keywords, its operators, clauses and constraints to filter, sort and retrieve required data through dedicated thinking to resolve problems.  
