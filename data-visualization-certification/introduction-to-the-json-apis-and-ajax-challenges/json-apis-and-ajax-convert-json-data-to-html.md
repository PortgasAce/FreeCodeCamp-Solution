JSON APIs and Ajax: Convert JSON Data to HTML
Now that you're getting data from a JSON API, you can display it in the HTML.

You can use a forEach method to loop through the data since the cat photo objects are held in an array. As you get to each item, you can modify the HTML elements.

First, declare an html variable with var html = "";.

Then, loop through the JSON, adding HTML to the variable that wraps the key names in strong tags, followed by the value. When the loop is finished, you render it.

Here's the code that does this:
```
json.forEach(function(val) {
  var keys = Object.keys(val);
  html += "<div class = 'cat'>";
  keys.forEach(function(key) {
    html += "<strong>" + key + "</strong>: " + val[key] + "<br>";
  });
  html += "</div><br>";
});
```
Add a forEach method to loop over the JSON data and create the HTML elements to display it.

Here is some example JSON
```
[
  {
    "id":0,
      "imageLink":"https://s3.amazonaws.com/freecodecamp/funny-cat.jpg",
      "altText":"A white cat wearing a green helmet shaped melon on its head. ",
      "codeNames":[ "Juggernaut", "Mrs. Wallace", "Buttercup"
    ]
  }
]
```

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
        // Add your code below this line
        json.forEach(function(val) {
        var keys = Object.keys(val);
        html += "<div class = 'cat'>";
        keys.forEach(function(key) {
        html += "<strong>" + key + "</strong>: " + val[key] + "<br>";
  });
        html += "</div><br>";
});
        
        
        // Add your code above this line
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