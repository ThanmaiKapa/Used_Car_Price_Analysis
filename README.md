## Used Car Price Analysis
### Problem Statement
The used car market is characterized by significant variability in pricing due to numerous influencing factors such as make, model, year, mileage, condition, and geographical location. This complexity often results in challenges for buyers and sellers in determining fair market values, leading to uncertainty and inefficiency in transactions. The objective of this project is to develop a comprehensive data analytics solution to accurately analyse used car prices by collecting and cleaning data from reliable sources, identifying key features, and employing statistical analysis and visualization techniques.
- Car price variation based on various cars brands.
- Best cars with good quality with less price.

### Steps followed

- Step 1 : Extract the data from the web by web scraping using python libraries(BeautifulSoup).
- Step 2: Clean the data and convert it into csv file.
- Step 3: Load the csv file into Power BI Desktop.
- Step 4 : Open power query editor & in view tab under Data preview section, check "column distribution", "column quality" & "column profile" options.
- Step 5 : It was observed that in none of the columns errors & empty values were present.
- Step 6 : For changing format like capitalizing words go to transform tab and click on format which is present in the ribbon and then select capitalize each word.
- Step 7 : For converting price into numerical form select New column option which is present in the home tab in the Table view ribbon.
for creating new column following DAX expression was written;
       
        Price Value = 
          var pricevalue='Used Cars Data'[Price]
          Return
           VALUE(LEFT(pricevalue, LEN(pricevalue)-4))*100000
- Step 8 : For changing format of the currency select the column and then select format option in column tools and change it to currency and change the currency symbol to Indian rupee symbol.

Snap of new calculated column,

![Screenshot 2024-05-28 191002](https://github.com/user-attachments/assets/51825800-95a1-4d84-81e9-9ac093a35166)
- Step 9 : A tooltip is added with a pie chart, donut chart and a card visual.
Snap of the tooltip,

![Screenshot 2024-05-30 204749](https://github.com/user-attachments/assets/d8d1bfbd-55b6-4ecc-9528-525d88cb7c0e)
- Step 10 : Report on car brand page is created by adding a table, 2 card visuals, funnel chart, pie chart with a tooltip and a treemap.
snap of the visual page,

![Screenshot 2024-05-30 204704](https://github.com/user-attachments/assets/a13e2fe6-3210-4b33-b014-51a5c9be584f)
- Step 11 : A table is added in a car details table page with a slicer containing car company names.
snap of the visual page,

![Screenshot 2024-05-30 204352](https://github.com/user-attachments/assets/b7898745-7c70-4206-810d-bff58071a2af)
- Step 12 : Comparision page is created by adding a horizontal bar graph, scatter chart and a decomposition tree.
snap of the visual page,

![Screenshot 2024-05-30 204523](https://github.com/user-attachments/assets/19e791c1-9d6b-458a-a1a4-dece640a6309)
- Step 13 : Top cars page is created by adding a location map, funnel chart, table, pie chart, donut chart, multi-row card and a slicer with locations.
snap of the visual page,

![Screenshot 2024-05-30 205033](https://github.com/user-attachments/assets/a687789e-18a0-46c6-b450-78092c1c0f43)
- Step 14 : Visual filters (Slicers) were added for various report pages.
