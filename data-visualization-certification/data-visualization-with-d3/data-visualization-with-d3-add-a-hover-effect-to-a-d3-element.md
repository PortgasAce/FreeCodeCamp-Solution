Data Visualization with D3: Add a Hover Effect to a D3 Element
It's possible to add effects that highlight a bar when the user hovers over it with the mouse. So far, the styling for the rectangles is applied with the built-in D3 and SVG methods, but you can use CSS as well.

You set the CSS class on the SVG elements with the attr() method. Then the :hover pseudo-class for your new class holds the style rules for any hover effects.


Use the attr() method to add a class of bar to all the rect elements. This changes the fill color of the bar to brown when you mouse over it.
```

```