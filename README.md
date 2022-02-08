![Capture3](https://user-images.githubusercontent.com/81073205/152939922-2dc2d2c5-208f-4eef-807f-2048b539101b.PNG)

The MINKT DIGITAL web map hosted here is the central element of a map-based platform with which the [iDEAS:lab](https://ideaslab.plus.ac.at/) in Salzburg, Austria hosts workshops to **build digial skills with young citizen scientists**.

The web map is an open layers web application that integrates data collected in Survey123 as a WFS. The application includes pop-ups, geolocation, an interactive gallery, and layer switchers ([walkermatt-layerswitcher](https://github.com/walkermatt/ol-layerswitcher)). 


**See the Live Web Map:** <br/>
[https://zgis.github.io/minktdigital_webmap/](https://zgis.github.io/minktdigital_webmap/)

**View the MINKT DIGITAL Platform:** <br/>
[https://minkt-digital.zgis.at/](https://minkt-digital.zgis.at/)


<br/>

## The Concept and Spatial Data Infrastructure behind the Web Map

![concept](https://user-images.githubusercontent.com/81073205/152962979-aa3da3a2-02f3-4e6c-ad19-668407fb8b52.png)


## The Web Map

The inital view of the web map upon opening it shows the clustered features:

![Capture5](https://user-images.githubusercontent.com/81073205/152940001-65e11f41-3453-48bf-be26-7ed5cf137f8e.PNG)

<br/>
<br/>

When the user zooms in (via mouse scroll or the home button at the top-right) the individual icons for the features become visible:

![Capture6](https://user-images.githubusercontent.com/81073205/152940014-3ee5c3f8-863d-4906-b74f-5fe91f68d6bb.PNG)
<br/>
<br/>

If the user clicks on any icon, a popup is generated showing the image and the story. The same can be done via the interactive gallery at the bottom of the map.
![Capture7](https://user-images.githubusercontent.com/81073205/152940030-168f6fda-b0f3-47b6-b574-68191d4db34d.PNG)
<br/>
<br/>

If the web map is loaded on a phone screen, the layout automatically adjusts. Notably the gallery disappears.
<img align="center" src="https://user-images.githubusercontent.com/81073205/152957551-b3e630c1-4cdc-4121-9fef-1bf5dda1e12d.PNG" height="400">


## Recent Updates

<br/>

| _Date_  | Issue / Edit |
| ------------- | ------------- |
| _21.12.2021_  | **ol.proj.transform()**: The features from the WFS no longer showed up on the map today. Upon investigation it turns out the coordinates of each point was being coverted completely wrong (some points had invalid coordinates, some were in Canada, and some were in Antarctica). Only after removing the ol.proj.transform function from the point geometries wsa the issue resolved and the points again appear in their correct location. Oddly, the geolocation and the home position still function properly with the transformation function. Note: no changes were made to the survey, the WFS, or the source code of this web map when I noticed the missing features.  | 
| _07.12.2021_  | Legend updated with improved icons and css styling. |
| _01.12.2021_  | Legend added. Some stylistic improvements. |
|  _30.11.2021_  | Added to the map: autoPan function for the pop-ups, on-hover highlighting of the individual features, and an on-hover opening and closing of the layer switcher menu were added.  |

<br/>

## Reproducibility

The web map hosted here can be reproduced by you with your own data, for your own applications! 

Please note that the data that flows into the web map is created in the [ESRI](https://www.esri.com/en-us/home) environment, specifically ArcGIS Online and Survey123. These are **commercial products**. 

