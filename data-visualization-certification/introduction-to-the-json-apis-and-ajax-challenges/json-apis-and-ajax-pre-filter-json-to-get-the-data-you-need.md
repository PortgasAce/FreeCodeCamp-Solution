JSON APIs and Ajax: Pre-filter JSON to Get the Data You Need
If you don't want to render every cat photo you get from the freeCodeCamp Cat Photo API, you can pre-filter the JSON before looping through it.

Given that the JSON data is stored in an array, you can use the filter method to filter out the cat whose "id" key has a value of 1.

Here's the code to do this:

json = json.filter(function(val) {
  return (val.id !== 1);
});

Add code to filter the json data to remove the cat with the "id" value of 1.

```

```