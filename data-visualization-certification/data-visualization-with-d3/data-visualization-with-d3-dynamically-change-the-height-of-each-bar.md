Data Visualization with D3: Dynamically Change the Height of Each Bar
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

```