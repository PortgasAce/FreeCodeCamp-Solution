JSON APIs and Ajax: Render Images from Data Sources
The last few challenges showed that each object in the JSON array contains an imageLink key with a value that is the URL of a cat's image.

When you're looping through these objects, you can use this imageLink property to display this image in an img element.

Here's the code that does this:

html += "<img src = '" + val.imageLink + "' " + "alt='" + val.altText + "'>";


Add code to use the imageLink and altText properties in an img tag.
```
```