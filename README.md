# map671-f26-final-madisonhigh
## **MAP 671 final project - Potential Threats to Blackside Dace Habitat in Whitley County, Kentucky (EPSG:3089)**
### **Project data:**
Data for this project was downloaded from the [KyGovMaps Open Data Portal](https://opengisdata.ky.gov/). Data for this project includes [Blackside Dace Streams in Kentucky (2009)](https://opengisdata.ky.gov/datasets/713e12641f934b438827cba8e6100d15_0/explore?location=36.736097%2C-83.692123%2C9), [Incorporated City Boundaries in Kentucky (Polygons)](https://opengisdata.ky.gov/datasets/2c3b574f960c48719ded987025445397_0/explore?location=36.912134%2C-84.104514%2C13), [Existing Industry in Kentucky](https://opengisdata.ky.gov/datasets/d4d3ec0a590d434fb9e239fbca84db44_0/explore?location=36.921036%2C-84.073784%2C13), [Permitted Mine Boundaries in Kentucky](https://opengisdata.ky.gov/datasets/733bd4425aeb407ab0e702e33349f6d7_0/explore?location=36.765287%2C-83.806946%2C11), [State-Maintained Roads in Kentucky](https://opengisdata.ky.gov/datasets/08acf66a47b54110b7fd4510c9721e86_0/explore?location=37.801450%2C-85.738791%2C7), and [Kentucky County Polygons](https://opengisdata.ky.gov/datasets/ad52760b298b4f2b8879233fecd1acd1_0/explore?location=37.822402%2C-85.768000%2C7).
### **Background**
I created this map because I found the Blackside Dace Streams dataset while I was browsing the data portal for data to use for my project. I thought it was interesting and specific enough that I could definitely build off of it.

![Blackside dace](https://encrypted-tbn0.gstatic.com/images?q=tbn:ANd9GcQsB34uUvFwavND1mAGmBWqA5lVlkTqnDbq7uG9ZlcBOVyVZ8JVxIkY6V0&s=10) 

Blackside dace are small minnows with a red underbelly and a black stripe down their sides. These fish are endemic to two river basins across Kentucky, Tennessee, and Virginia. According to the [U.S. Fish & Wildlife Service](https://ecos.fws.gov/ecp/species/4775), blackside dace are considered threatened under the 1987 U.S. Endangered Species Act. Since their habitat is constrained to such a narrow area, I was interested to see if there was anything around their habitats that could pose a threat to their survival.
### **Map creation**
To make the map, I downloaded all of the previously linked from the KyGovMaps Open Data Portal and loaded it all into QGIS. This data was originally exported as Pseudo-Mercator (EPSG:3857), so I used a ballpark transform to convert it to NAD83/Kentucky Single Zone (ftUS) (EPSG:3089). Some of the files had data for all of Kentucky, while the dace habitat only covered a few counties in Kentucky and Tennessee. I decided to make a map of only one county to show more detail. I wanted to find 3 different sources of potential threat to the habitats, which ended up being industrial sites, state-maintained roads, and permitted mines. I chose all of these because improperly managed wastewater from the industrial sites and mines could pollute the streams, and runoff from salted roads during the wintertime (or even litter year-round) could also pollute the streams.

I added all of this data to the map, and clipped the KY county polygons layer to just show Whitley County. After this, I clipped all of the data to the extent of Whitley County since all of the layers were at least state-wide data. The mine boundary polygon was especially important to clip because it was so detailed and was taking a while to render after zooming.

<img width="1371" height="822" alt="image" src="https://github.com/user-attachments/assets/bf8465b1-cafe-4f96-a47e-f946a8b50808" />

_Map before clipped and formatted data_

After clipping all of the data, I edited the symbology. I made sure to color everything in a way that was intuitive (ex: blue streams, gray roads), resized the points for industrial sites so they stuck out more, and removed the border around the mine polygons because it was making the map feel too cluttered. 

<img width="1360" height="809" alt="image" src="https://github.com/user-attachments/assets/ce067f3e-194f-4883-8592-9091a4fce4bf" />

_Map after clipped and formatted data_

If I were to take this map further, I would try to rank the streams by threat level and consider how many potential threats are near each section of stream.
