Data Visualization with D3: Change the Color of an SVG Element
The bars are in the right position, but they are all the same black color. SVG has a way to change the color of the bars.

In SVG, a rect shape is colored with the fill attribute. It supports hex codes, color names, and rgb values, as well as more complex options like gradients and transparency.


Add an attr() method to set the "fill" of all the bars to the color "navy".
```
<body>
  <script>
    const dataset = [12, 31, 22, 17, 25, 18, 29, 14, 9];
    
    const w = 500;
    const h = 100;
    
    const svg = d3.select("body")
                  .append("svg")
                  .attr("width", w)
                  .attr("height", h);
    
    svg.selectAll("rect")
       .data(dataset)
       .enter()
       .append("rect")
       .attr("x", (d, i) => i * 30)
       .attr("y", (d, i) => h - 3 * d)
       .attr("width", 25)
       .attr("height", (d, i) => 3 * d)
       .attr("fill","navy")
       // Add your code below this line
       
       
       
       // Add your code above this line
  </script>
</body>
```