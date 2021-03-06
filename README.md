
# Toronto_Potholes
**To access the rendered version of the html file containing an interactive map click [here](https://alsds.github.io/Toronto_Potholes/).**


This is a combination of data mining and data visualization effort with the aim of identifying spatial and temporal information about potholes within the city of Toronto. Although the data is comparative of months within 2018, in the future I hope to conduct analysis spanning multiple years. 

The data was gathered from [Toronto Open Data](https://open.toronto.ca/) in JSON format. The city of Toronto collects information about potholes through service requests and documents pertinent information about each, including the service request code, status, address, longitude, and latitudes of the location requiring service. Each request is uniquely identifiable through its *“service request id”*. 

Querying information about potholes involved making requests by entering parameters such as desired time interval (*start_date*, *end_date*) and the *service request code*. At the time of gathering this information, query sizes were limited to 1,000 records per request. To remain within the query limit, the start and end date parameters had to remain a few days apart. The JSON output of each request was concatenated to form the data representing months, and eventually the entire 2018 year. This data is stored in the JSON directory of this repository. 

![record](https://user-images.githubusercontent.com/61554673/123553950-d6ba8880-d74b-11eb-97d0-69ef8c3b440c.png)

To project the gathered data onto a map, the JSON files were converted to GeoJSON. GeoJSON data is stored in the GeoJSON directory of this repository. 

The GeoJSON coordinates for plotting the map of Toronto and its neighborhoods was obtained from [jasonicarter](https://github.com/jasonicarter/toronto-geojson). 

D3 visualization of potholes and projection onto the map was done using a tutorial from [DUSPviz](http://duspviz.mit.edu/d3-workshop/mapping-data-with-d3/). 


Below, I’ve plotted the distribution of pothole data for the 2018 year using the mined JSON data, which distinguishes pothole information based on the time of the year and neighborhoods in the city of Toronto. 

![months](https://user-images.githubusercontent.com/61554673/123553992-0c5f7180-d74c-11eb-87fc-5f1095a76a93.png)
![areas](https://user-images.githubusercontent.com/61554673/123553997-0e293500-d74c-11eb-92aa-2fc31242f1c2.png)




