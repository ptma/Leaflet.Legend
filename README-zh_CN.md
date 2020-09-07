# Leaflet.Legend 
Leaflet.Legend 是一个 Leaflet 插件， 用于显示图例符号和切换相应的叠加层的显示.  

在线 [demo](https://ptma.gitee.io/leaflet.legend/examples/legend.html).

## 用法示例
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

## 选项
| 选项 | 类型 | 默认值 | 描述 |
|--------|------|---------|-------------|
| position | String | 'topleft' | 图例控件位置。 |
| title | String | 'Legend' | 图例控件的标题。 |
| opacity | Number | 1.0 | 图例面板的透明度。 |
| legends | LegendSymbol[] | [] | [LegendSymbol](#legendsymbol) 图例符号数组。 |
| symbolWidth | Number | 24 | 图例符号的宽度，以像素为单位。 |
| symbolHeight | Number | 24 | 图例符号的高度，以像素为单位。 |
| column | Number | 1 | 图例符号排列的列数。 |
| collapsed | Boolean | false | 图例面板是否默认展开。 |

### LegendSymbol
| 选项 | 类型 | 默认值 | 描述 |
|--------|------|---------|-------------|
| label | String | undefined | 图例符号的文本标签。 |
| type | String | undefined | 图例符号的类型. 可以是 'image'，'circle'，'rectangle'，'polygon' 或 'polyline'。 |
| url | String | undefined | 图里图片的 URL，仅用于 type 为 'image' 时。 |
| radius | Number | undefined | 圆形图例的半径，以像素为单位，仅用于 type 为 'circle' 时。 |
| sides | Number | undefined | 正多边形的边数，仅用于 type 为 'polygon' 时。 |
| layers | Layer\|Layer[]| undefined | 图例符号关联的叠加层. 关联叠加层后可通过点击图例来切换相应叠加层的可见性。 |
| inactive | Boolean | undefined | 图例符号是否为非激活的， 非激活的图例会减淡显示。  |
| stroke              | Boolean  | true       | 是否绘制边框。 |
| color               | String   | '#3388ff' | 边框颜色。 |
| weight              | Number   | 3          | 边框宽度。 |
| opacity             | Number   | 1.0       | 边框透明度。 |
| lineCap             | String   | 'round'    | 指定如何绘制每一条线段末端的属性。有 3 个可能的值，分别是：'butt'，'round' 或 ’square‘。  |
| lineJoin            | String   | 'round'    | 用来设置2个长度不为0的相连部分（线段，圆弧，曲线）如何连接在一起的属性（长度为0的变形部分，其指定的末端和控制点在同一位置，会被忽略）。 |
| dashArray           | String   | null       | 控制用来描边的点划线的图案范式。 |
| dashOffset          | String   | null       | dash模式到路径开始的距离。 |
| fill                | Boolean  | depends    | 是否用颜色填充。 |
| fillColor           | String   | *         | 填充色，默认与边框颜色相同 |
| fillOpacity         | Number   | 0.2       | 填充透明度。 |
| fillRule            | String   | 'evenodd'  | 填充规则。 |
