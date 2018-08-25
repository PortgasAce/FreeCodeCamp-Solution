Data Visualization with D3: Change Styles Based on Data
D3 is about visualization and presentation of data. It's likely you'll want to change the styling of elements based on the data. You can use a callback function in the style() method to change the styling for different elements.

For example, you may want to color a data point blue if has a value less than 20, and red otherwise. You can use a callback function in the style() method and include the conditional logic. The callback function uses the d parameter to represent the data point:

selection.style("color", (d) => {
  /* Logic that returns the color based on a condition */
});
The style() method is not limited to setting the color - it can be used with other CSS properties as well.


Add the style() method to the code in the editor to set the color of the h2 elements conditionally. Write the callback function so if the data value is less than 20, it returns "red", otherwise it returns "green".

Note
You can use if-else logic, or the ternary operator.
```
<body>
  <script>
    const dataset = [12, 31, 22, 17, 25, 18, 29, 14, 9];
    
    d3.select("body").selectAll("h2")
      .data(dataset)
      .enter()
      .append("h2")
      .text((d) => (d + " USD"))
      // Add your code below this line
      .style("color",(data)=>{
        return data<20?"red":"green"
      })
      
      
      // Add your code above this line
  </script>
</body>
```