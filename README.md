# Extracting-Building-Footprints-From-GHSL-Data-and-Estimating-Building-Height



The process of extracting building footprints from GHSL data and estimating building height involves several steps, each essential for proper data extraction, processing, and visualization. Here's a detailed description of my workflow: <br>

1. Extract Building Footprints for Specific Region Using OSM <br>
•	The first step is to use OpenStreetMap (OSM) data to extract building footprints for the desired region. This is typically done by defining the geographical area of interest (AOI) for the building footprints extraction. The extracted data includes information such as building polygons, which are essential for subsequent analysis.<br>
2. Visualize Downloaded Data<br>
•	After downloading the building footprint data, the next step is to visualize the extracted building footprints. This allows you to ensure that the correct region has been selected, and that the building data is properly captured. Visualizing the data helps in verifying that the footprints align with the real-world map.<br>
3. Calculate Building Area & Generate Centroids<br>
•	Once the building footprints are extracted, it is necessary to calculate the area of each building polygon. This can be done by calculating the area in square meters for each polygon. Additionally, centroids for each building footprint are generated. These centroids will later be used to calculate geographical coordinates (latitude and longitude) for the buildings.<br>
4. Download GHSL Data from Google Earth Engine (GEE) Using Kolkata Shapefile<br>
•	To estimate building heights, you will download GHSL (Global Human Settlement Layer) data from Google Earth Engine. The data is usually available as raster files representing different building-related parameters, including height. You will use a Kolkata shapefile as your AOI for extracting the relevant GHSL data from GEE.<br>
5. Reproject Data to EPSG:4326 (WGS 1984)<br>
•	The downloaded GHSL data may be in a different projection, so it is necessary to reproject it to EPSG:4326 (WGS 1984). This ensures that all spatial data is in a consistent coordinate reference system (CRS) and aligns correctly with other geospatial data, such as building footprints.<br>
6. Fetch Building Height from Reprojected Raster Data<br>
•	After reprojecting the GHSL data, you will extract building height information from the raster data. This height data represents the elevation of each building and is a crucial part of the analysis for understanding building dimensions.<br>
7. Add 'height_m' Column to Data<br>
•	Once the building height data has been extracted from the GHSL raster, you will create a new column, 'height_m', to store the height values for each building. This column will be added to the building footprint dataset, providing a clear representation of each building's height.<br>
8. Calculate Latitude and Longitude Based on Centroids<br>
•	Using the centroid points generated earlier, you will calculate the corresponding latitude and longitude values for each building. These values will be derived from the spatial coordinates of the centroids and will help in locating each building geographically.<br>
9. Generate Final Shapefile with Building Footprint and Height Data<br>
•	After calculating the height and obtaining the latitude and longitude for each building, you will generate a final shapefile that contains all the relevant information. This shapefile will include building footprints, height data, and coordinates for each building, making it a comprehensive dataset for further analysis.<br>
10. Visualize Final Building Footprints with Height Data<br>
•	At this point, you can visualize the final building footprints, now enriched with height data. This visualization will show both the geographic location of the buildings and their heights, providing a clearer understanding of the building distribution and urban landscape.<br>
11. Export Final Data to Excel and CSV Files<br>
•	Finally, you will export the dataset containing building footprints, height data, and latitude/longitude values into both Excel and CSV formats. These files can then be used for further analysis, reporting, or sharing with stakeholders.<br>
Conclusion<br>
This process provides a detailed and structured approach to extracting building footprints from GHSL data, estimating building heights, and generating a comprehensive dataset with geographic and building-related information. The entire workflow is implemented in the buildingFootprintExtraction.ipynb code file.

