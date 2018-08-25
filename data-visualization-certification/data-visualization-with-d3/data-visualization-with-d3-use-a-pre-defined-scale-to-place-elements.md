Data Visualization with D3: Use a Pre-Defined Scale to Place Elements
With the scales set up, it's time to map the scatter plot again. The scales are like processing functions that turn the x and y raw data into values that fit and render correctly on the SVG canvas. They keep the data within the screen's plotting area.

You set the coordinate attribute values for an SVG shape with the scaling function. This includes x and y attributes for rect or text elements, or cx and cy for circles. Here's an example:

shape
  .attr("x", (d) => xScale(d[0]))
Scales set shape coordinate attributes to place the data points onto the SVG canvas. You don't need to apply scales when you display the actual data value, for example, in the text() method for a tooltip or label.


Use xScale and yScale to position both the circle and text shapes onto the SVG canvas. For the circles, apply the scales to set the cx and cy attributes. Give them a radius of 5 units, too.

For the text elements, apply the scales to set the x and y attributes. The labels should be offset to the right of the dots. To do this, add 10 units to the x data value before passing it to the xScale.
```
<body>
  <script>
    const dataset = [
                  [ 34,     78 ],
                  [ 109,   280 ],
                  [ 310,   120 ],
                  [ 79,   411 ],
                  [ 420,   220 ],
                  [ 233,   145 ],
                  [ 333,   96 ],
                  [ 222,    333 ],
                  [ 78,    320 ],
                  [ 21,   123 ]
                ];
    
    const w = 500;
    const h = 500;
    const padding = 60;
    
    const xScale = d3.scaleLinear()
                     .domain([0, d3.max(dataset, (d) => d[0])])
                     .range([padding, w - padding]);
    
    const yScale = d3.scaleLinear()
                     .domain([0, d3.max(dataset, (d) => d[1])])
                     .range([h - padding, padding]);
    
    const svg = d3.select("body")
                  .append("svg")
                  .attr("width", w)
                  .attr("height", h);
    
    svg.selectAll("circle")
       .data(dataset)
       .enter()
       .append("circle")
       // Add your code below this line
       .attr("cx",(d) => xScale(d[0]))
       .attr("cy",(d) => yScale(d[1]))
       .attr("r","5")
       
       
       // Add your code above this line
       
    svg.selectAll("text")
       .data(dataset)
       .enter()
       .append("text")
       .text((d) =>  (d[0] + ", "
 + d[1]))
       // Add your code below this line
       .attr("x",(d) => xScale(d[0]+10))
       .attr("y",(d) => yScale(d[1]))
       
       
       // Add your code above this line
  </script>
</body>
```