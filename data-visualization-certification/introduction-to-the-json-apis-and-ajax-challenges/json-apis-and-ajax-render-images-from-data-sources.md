JSON APIs and Ajax: Render Images from Data Sources
The last few challenges showed that each object in the JSON array contains an imageLink key with a value that is the URL of a cat's image.

When you're looping through these objects, you can use this imageLink property to display this image in an img element.

Here's the code that does this:
```
html += "<img src = '" + val.imageLink + "' " + "alt='" + val.altText + "'>";
```

Add code to use the imageLink and altText properties in an img tag.

```
<script>
  document.addEventListener('DOMContentLoaded',function(){
    document.getElementById('getMessage').onclick=function(){
      req=new XMLHttpRequest();
      req.open("GET",'/json/cats.json',true);
      req.send();
      req.onload=function(){
        json=JSON.parse(req.responseText);
        var html = "";
        json.forEach(function(val) {
          html += "<div class = 'cat'>";
          // Add your code below this line
          html += "<img src = '" + val.imageLink + "' " + "alt='" + val.altText + "'>";
          
          // Add your code above this line
          html += "</div><br>";
        });
        document.getElementsByClassName('message')[0].innerHTML=html;
      };
     };
  });
</script>
<style>
  body {
    text-align: center;
    font-family: "Helvetica", sans-serif;
  }
  h1 {
    font-size: 2em;
    font-weight: bold;
  }
  .box {
    border-radius: 5px;
    background-color: #eee;
    padding: 20px 5px;
  }
  button {
    color: white;
    background-color: #4791d0;
    border-radius: 5px;
    border: 1px solid #4791d0;
    padding: 5px 10px 8px 10px;
  }
  button:hover {
    background-color: #0F5897;
    border: 1px solid #0F5897;
  }
</style>
<h1>Cat Photo Finder</h1> 
<p class="message box">
  The message will go here
</p>
<p>
  <button id="getMessage">
    Get Message
  </button>
</p>
```