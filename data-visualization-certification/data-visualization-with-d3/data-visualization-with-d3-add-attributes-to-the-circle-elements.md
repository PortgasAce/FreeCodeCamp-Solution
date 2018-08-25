Data Visualization with D3: Add Attributes to the Circle Elements
The last challenge created the circle elements for each point in the dataset, and appended them to the SVG canvas. But D3 needs more information about the position and size of each circle to display them correctly.

A circle in SVG has three main attributes. The cx and cy attributes are the coordinates. They tell D3 where to position the center of the shape on the SVG canvas. The radius (r attribute) gives the size of the circle.

Just like the rect y coordinate, the cy attribute for a circle is measured from the top of the SVG canvas, not from the bottom.

All three attributes can use a callback function to set their values dynamically. Remember that all methods chained after data(dataset) run once per item in dataset. The d parameter in the callback function refers to the current item in dataset, which is an array for each point. You use bracket notation, like d[0], to access the values in that array.


Add cx, cy, and r attributes to the circle elements. The cx value should be the first number in the array for each item in dataset. The cy value should be based off the second number in the array, but make sure to show the chart right-side-up and not inverted. The r value should be 5 for all circles.
```

```