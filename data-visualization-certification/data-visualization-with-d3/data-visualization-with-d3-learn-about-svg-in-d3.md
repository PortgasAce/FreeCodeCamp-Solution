Data Visualization with D3: Learn About SVG in D3
SVG stands for Scalable Vector Graphics.

Here "scalable" means that, if you zoom in or out on an object, it would not appear pixelated. It scales with the display system, whether it's on a small mobile screen or a large TV monitor.

SVG is used to make common geometric shapes. Since D3 maps data into a visual representation, it uses SVG to create the shapes for the visualization. SVG shapes for a web page must go within an HTML svg tag.

CSS can be scalable when styles use relative units (such as vh, vw, or percentages), but using SVG is more flexible to build data visualizations.


Add an svg node to the body using append(). Give it a width attribute set to the provided w constant and a height attribute set to the provided h constant using the attr() method for each. You'll see it in the output because there's a background-color of pink applied to it in the style tag.

Note
Width and height attributes do not have units. This is the building block of scaling - the element will always have a 5:1 width to height ratio, no matter what the zoom level is.
```

```