# Making graphs with D3, DC, and Crossfilter
## What are these tools capable of?
[Examples of D3](https://d3js.org/)<br>
[Examples of Crossfilter](http://square.github.io/crossfilter/)<br>
[Examples of DC](https://dc-js.github.io/dc.js/vc/index.html)<br>
[Examples of All 3 working together](https://cdn.rawgit.com/jakobzhao/storymap/48fb6416/examples/dataInteraction/index.html#L2)

## Data in D3
D3 gives us a method to use data in js. the **.data()** command determines what data is being used by D3. Once data is imported into D3,
we must consider how
it is shaped and handled. Data can be shaped as an **array** or an **object**. 

### Arrays
An Array is a bracketed list of data.<br> *Examples:*
<br>  *var names = [Jen, Sam, Beth]*
<br>  *var scores = [12, 67, 35]*

### Objects
Objects, in contrast, are complex in nature having multidimensional observations. <br>
*Example:*
var fruit = {<br>
  kind: "grape"<br>
  color: "red"<br>
  quantity: 12<br>
  tasty: true<br>
  };<br>

Knowing the structure of your data is important to know how to tell D3 what to do with the data.

#### GeoJSON
GeoJSON data is a data object. That is, it is multidimensional and applies multiple elements to a single observation. *Example:*<br>
var geodata = {<br>
    "type": "FeatureCollection",<br>
    "features": [<br>
        {<br>
            "type": "Feature",<br>
            "geometry": {<br>
                "type": "Point",<br>
                "coordinates": [ 150.1282427, -24.471803 ]<br>
            },<br>
            "properties": {<br>
                "type": "town"<br>
            }<br>
        }<br>
    ]<br>
};<br>


## **.append()**
The **.append()** command allows us to dynamically interact with the webpage with creating new elements, such as headings or paragraphs. 
**.append()** changes elements of the page automatically! By defining within the brackets, we tell D3 exactly what it should be modifying,
for example;<br>
.append(div)<br>
*to change a div object*<br>
*or*<br>
.append(svg)<br>
*to change an svg*

## **.attr()**
The **.attr()** command sets the attributes of our D3 objects, such as class, src, id.

## **.style()**
The **.style()** command allows us to change the CSS of our D3 objects without changing the overall page CSS
