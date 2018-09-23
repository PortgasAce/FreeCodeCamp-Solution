# Basic HTML and HTML5: Nest an Anchor Element within a Paragraph
You can nest links within other text elements.
```
<p>
Here's a <a target="_blank" href="http://freecodecamp.org"> link to freecodecamp.org</a> for you to follow.
</p>
```
Let's break down the example:

Normal text is wrapped in the p element:
```
<p> Here's a ... for you to follow. </p>
```

Next is the anchor element `<a>` (which requires a closing tag `</a>`):
```
<a> ... </a>
```

target is an anchor tag attribute that specifies where to open the link and the value "_blank" specifies to open the link in a new tab

href is an anchor tag attribute that contains the URL address of the link:
```
<a href="http://freecodecamp.org"> ... </a>
```
The text, "link to freecodecamp.org", within the anchor element called anchor text, will display a link to click:
```
<a href=" ... ">link to freecodecamp.org</a>
```

The final output of the example will look like this:
Here's a link to freecodecamp.org for you to follow.



Now nest your existing a element within a new p element (just after the existing main element). The new paragraph should have text that says "View more cat photos", where "cat photos" is a link, and the rest of the text is plain text.

```
<h2>CatPhotoApp</h2>
<main>
  
  <p>View more <a href="http://freecatphotoapp.com" target="_blank">cat photos</a></p>
  
  <img src="https://bit.ly/fcc-relaxing-cat" alt="A cute orange cat lying on its back.">
  
  <p>Kitty ipsum dolor sit amet, shed everywhere shed everywhere stretching attack your ankles chase the red dot, hairball run catnip eat the grass sniff.</p>
  <p>Purr jump eat the grass rip the couch scratched sunbathe, shed everywhere rip the couch sleep in the sink fluffy fur catnip scratched.</p>
</main>
```
