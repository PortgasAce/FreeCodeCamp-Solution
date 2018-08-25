Data Visualization with D3: Change the Presentation of a Bar Chart
The last challenge created a bar chart, but there are a couple of formatting changes that could improve it:

1) Add space between each bar to visually separate them, which is done by adding a margin to the CSS for the bar class

2) Increase the height of the bars to better show the difference in values, which is done by multiplying the value by a number to scale the height


First, add a margin of 2px to the bar class in the style tag. Next, change the callback function in the style() method so it returns a value 10 times the original data value (plus the "px").

Note
Multiplying each data point by the same constant only alters the scale. It's like zooming in, and it doesn't change the meaning of the underlying data.
```

```