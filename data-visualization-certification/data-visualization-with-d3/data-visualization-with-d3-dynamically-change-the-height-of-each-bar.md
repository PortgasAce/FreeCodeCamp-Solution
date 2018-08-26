# Data Visualization with D3: Dynamically Change the Height of Each Bar
The height of each bar can be set to the value of the data point in the array, similar to how the x value was set dynamically.

selection.attr("property", (d, i) => {
  /* 
  * d is the data point value
  * i is the index of the data point in the array
  */
})

Change the callback function for the height attribute to return the data value times 3.

Note
Remember that multiplying all data points by the same constant scales the data (like zooming in). It helps to see the differences between bar values in this example.
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
       .attr("y", 0)
       .attr("width", 25)
       .attr("height", (d, i) => {
         // Add your code below this line
         return d * 3;
         
         
         // Add your code above this line
       });
  </script>
</body>
```