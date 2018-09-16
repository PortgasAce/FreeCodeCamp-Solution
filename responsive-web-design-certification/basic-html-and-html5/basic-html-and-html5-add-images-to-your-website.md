Basic HTML and HTML5: Add Images to Your Website
You can add images to your website by using the img element, and point to a specific image's URL using the src attribute.

An example of this would be:
````
<img src="https://www.your-image-source.com/your-image.jpg">
```
Note that img elements are self-closing.

All img elements must have an alt attribute. The text inside an alt attribute is used for screen readers to improve accessibility and is displayed if the image fails to load.

Note: If the image is purely decorative, using an empty alt attribute is a best practice.

Ideally the alt attribute should not contain special characters unless needed.

Let's add an alt attribute to our img example above:
```
<img src="https://www.your-image-source.com/your-image.jpg" alt="Author standing on a beach with two thumbs up.">
```

Let's try to add an image to our website:

Insert an img tag, before the h2 element.

Now set the src attribute so that it points to this url:

https://bit.ly/fcc-relaxing-cat

Finally don't forget to give your image an alt text.

```
<img src="https://bit.ly/fcc-relaxing-cat" alt="cat"/>
<h2>CatPhotoApp</h2>
<main>
  
  <p>Kitty ipsum dolor sit amet, shed everywhere shed everywhere stretching attack your ankles chase the red dot, hairball run catnip eat the grass sniff.</p>
  <p>Purr jump eat the grass rip the couch scratched sunbathe, shed everywhere rip the couch sleep in the sink fluffy fur catnip scratched.</p>
</main>
```