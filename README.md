# Leaflet.Legend 
Leaflet.Legend is a plugin for Leaflet that display legend symbols and toggle overlays.  

Check out the [demo](https://ptma.github.io/Leaflet.Legend/examples/legend.html).

## Example
```javascript
var map = L.map("map", {
        center: [29, 120],
    });
    
L.control.Legend({
    position: "bottomleft",
    legends: [{
        label: "Marker1",
        type: "image",
        url: "marker/marker-red.png",
    }]
}).addTo(map);
```

## Options
| Option | Type | Default | Description |
|--------|------|---------|-------------|
| position | String | 'topleft' | The position of the control. |
| title | String | 'Legend' | The title of the control. |
| opacity | Number | 1.0 | Opacity of the container. |
| legends | LegendSymbol[] | [] | Array of [legend symbols](#legendsymbol) that will be added to the container. |
| symbolWidth | Number | 24 | Symbol width of the legend, in pixels. |
| symbolHeight | Number | 24 | Symbol width of the legend, in pixels. |
| column | Number | 1 | The number of columns arranged in the legend. |
| collapsed | Boolean | false | If true, the control will be collapsed into an icon and expanded on mouse hover or touch. |

### LegendSymbol
| Option | Type | Default | Description |
|--------|------|---------|-------------|
| label | String | undefined | The label of the legend symbol. |
| type | String | undefined | The type of the legend symbol. Possible values are 'image', 'circle', 'rectangle', 'polygon' or 'polyline' |
| url | String | undefined | The url of the symbol image, only used when type is 'image' |
| radius | Number | undefined | The radius of the circle, in pixels, only used when type is 'circle' |
| sides | Number | undefined | The number of sides of a regular polygon, only used when type is 'polygon' |
| layers | Layer\|Layer[]| undefined | Legend symbol associated layers. While associating the layers, the display state of the layers can be toggled. |
| inactive | Boolean | undefined | Is the legend symbol inactive |
| stroke              | Boolean  | true       | Whether to draw stroke along the path\. Set it to false to disable borders on polygons or circles\. |
| color               | String   | '\#3388ff' | Stroke color |
| weight              | Number   | 3          | Stroke width in pixels |
| opacity             | Number   | 1\.0       | Stroke opacity |
| lineCap             | String   | 'round'    | A string that defines shape to be used at the end of the stroke\. |
| lineJoin            | String   | 'round'    | A string that defines shape to be used at the corners of the stroke\. |
| dashArray           | String   | null       | A string that defines the stroke dash pattern. Doesn't work on Canvas\-powered layers in some old browsers\. |
| dashOffset          | String   | null       | A string that defines the distance into the dash pattern to start the dash\. Doesn't work on Canvas-powered layers in some old browsers\. |
| fill                | Boolean  | depends    | Whether to fill the path with color. Set it to false to disable filling on polygons or circles\. |
| fillColor           | String   | \*         | Fill color. Defaults to the value of the color option |
| fillOpacity         | Number   | 0.2       | Fill opacity. |
| fillRule            | String   | 'evenodd'  | A string that defines how the inside of a shape is determined\. |
