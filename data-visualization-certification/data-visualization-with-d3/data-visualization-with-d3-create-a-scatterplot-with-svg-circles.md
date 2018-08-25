Data Visualization with D3: Create a Scatterplot with SVG Circles
A scatter plot is another type of visualization. It usually uses circles to map data points, which have two values each. These values tie to the x and y axes, and are used to position the circle in the visualization.

SVG has a circle tag to create the circle shape. It works a lot like the rect elements you used for the bar chart.


Use the data(), enter(), and append() methods to bind dataset to new circle elements that are appended to the SVG canvas.

```
<body>
  <script>
    const dataset = [
                  [ 34,    78 ],
                  [ 109,   280 ],
                  [ 310,   120 ],
                  [ 79,    411 ],
                  [ 420,   220 ],
                  [ 233,   145 ],
                  [ 333,   96 ],
                  [ 222,   333 ],
                  [ 78,    320 ],
                  [ 21,    123 ]
                ];
    
    
    const w = 500;
    const h = 500;
    
    const svg = d3.select("body")
                  .append("svg")
                  .attr("width", w)
                  .attr("height", h);
    
    svg.selectAll("circle")
       // Add your code below this line
       .data(dataset)
       .enter()
       .append("circle")
       
       
       // Add your code above this line
  
  </script>
</body>
```