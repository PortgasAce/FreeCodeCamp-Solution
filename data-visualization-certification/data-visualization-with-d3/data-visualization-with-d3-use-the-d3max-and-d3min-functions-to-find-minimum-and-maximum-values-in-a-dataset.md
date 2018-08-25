Data Visualization with D3: Use the d3.max and d3.min Functions to Find Minimum and Maximum Values in a Dataset
The D3 methods domain() and range() set that information for your scale based on the data. There are a couple methods to make that easier.

Often when you set the domain, you'll want to use the minimum and maximum values within the data set. Trying to find these values manually, especially in a large data set, may cause errors.

D3 has two methods - min() and max() to return this information. Here's an example:

const exampleData = [34, 234, 73, 90, 6, 52];
d3.min(exampleData) // Returns 6
d3.max(exampleData) // Returns 234
A dataset may have nested arrays, like the [x, y] coordinate pairs that were in the scatter plot example. In that case, you need to tell D3 how to calculate the maximum and minimum.

Fortunately, both the min() and max() methods take a callback function.

In this example, the callback function's argument d is for the current inner array. The callback needs to return the element from the inner array (the x or y value) over which you want to compute the maximum or minimum. Here's an example for how to find the min and max values with an array of arrays:

const locationData = [[1, 7],[6, 3],[8, 3]];
// Returns the smallest number out of the first elements
const minX = d3.min(locationData, (d) => d[0]);
// minX compared 1, 6, and 8 and is set to 1

The positionData variable holds a 3-dimensional (3D) array. Use a D3 method to find the maximum value of the z coordinate (the third value) from the arrays and save it in the output variable.

Note
Fun fact - D3 can plot 3D arrays.
```

```