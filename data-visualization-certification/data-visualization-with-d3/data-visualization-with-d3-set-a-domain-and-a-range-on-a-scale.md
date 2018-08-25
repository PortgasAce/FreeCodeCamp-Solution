Data Visualization with D3: Set a Domain and a Range on a Scale
By default, scales use the identity relationship - the input value maps to the output value. But scales can be much more flexible and interesting.

Say a data set has values ranging from 50 to 480. This is the input information for a scale, and is also known as the domain.

You want to map those points along the x axis on the SVG canvas, between 10 units and 500 units. This is the output information, which is also known as the range.

The domain() and range() methods set these values for the scale. Both methods take an array of at least two elements as an argument. Here's an example:

// Set a domain
// The domain covers the set of input values
scale.domain([50, 480]);
// Set a range
// The range covers the set of output values
scale.range([10, 500]);
scale(50) // Returns 10
scale(480) // Returns 500
scale(325) // Returns 323.37
scale(750) // Returns 807.67
d3.scaleLinear()
Notice that the scale uses the linear relationship between the domain and range values to figure out what the output should be for a given number. The minimum value in the domain (50) maps to the minimum value (10) in the range.


Create a scale and set its domain to [250, 500] and range to [10, 150].

Note
You can chain the domain() and range() methods onto the scale variable.
```
<body>
  <script>
    // Add your code below this line
    const scale = d3.scaleLinear();
    scale.domain([250,500]);
    scale.range([10,150]);
    
    
    // Add your code above this line
    const output = scale(50);
    d3.select("body")
      .append("h2")
      .text(output);
  </script>
</body>
```