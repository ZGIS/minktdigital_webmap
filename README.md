# MINKT DIGITAL Web Map

The MINKT DIGITAL web map is an open layers web application that integrates data collected in Survey123 as a WFS. The application includes pop-ups, geolocation, an interactive gallery, and layer switchers ([walkermatt-layerswitcher](https://github.com/walkermatt/ol-layerswitcher)).

**See the Web Map Result:** <br/>
[https://zgis.github.io/minktdigital_webmap/](https://zgis.github.io/minktdigital_webmap/)

**View the MINKT Stories Platform:** <br/>
[https://minkt-digital.zgis.at/](https://minkt-digital.zgis.at/)


<br/>


**Recent Updates:** 

<br/>

| _Date_  | Issue / Edit |
| ------------- | ------------- |
| _21.12.2021_  | **ol.proj.transform()**: The features from the WFS no longer showed up on the map today. Upon investigation it turns out the coordinates of each point was being coverted completely wrong (some points had invalid coordinates, some were in Canada, and some were in Antarctica). Only after removing the ol.proj.transform function from the point geometries wsa the issue resolved and the points again appear in their correct location. Oddly, the geolocation and the home position still function properly with the transformation function. Note: no changes were made to the survey, the WFS, or the source code of this web map when I noticed the missing features.  | 
| _07.12.2021_  | Legend updated with improved icons and css styling. |
| _01.12.2021_  | Legend added. Some stylistic improvements. |
|  _30.11.2021_  | Added to the map: autoPan function for the pop-ups, on-hover highlighting of the individual features, and an on-hover opening and closing of the layer switcher menu were added.  |

<br/>
