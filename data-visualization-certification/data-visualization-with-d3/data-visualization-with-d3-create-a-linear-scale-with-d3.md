Data Visualization with D3: Create a Linear Scale with D3
The bar and scatter plot charts both plotted data directly onto the SVG canvas. However, if the height of a bar or one of the data points were larger than the SVG height or width values, it would go outside the SVG area.

In D3, there are scales to help plot data. Scales are functions that tell the program how to map a set of raw data points onto the pixels of the SVG canvas.

For example, say you have a 100x500-sized SVG canvas and you want to plot Gross Domestic Product (GDP) for a number of countries. The set of numbers would be in the billion or trillion-dollar range. You provide D3 a type of scale to tell it how to place the large GDP values into that 100x500-sized area.

It's unlikely you would plot raw data as-is. Before plotting it, you set the scale for your entire data set, so that the x and y values fit your canvas width and height.

D3 has several scale types. For a linear scale (usually used with quantitative data), there is the D3 method scaleLinear():

const scale = d3.scaleLinear()

By default, a scale uses the identity relationship. The value of the input is the same as the value of the output. A separate challenge covers how to change this.


Change the scale variable to create a linear scale. Then set the output variable to the scale called with an input argument of 50.
```

```