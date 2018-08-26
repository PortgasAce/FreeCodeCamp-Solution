JSON APIs and Ajax: Access the JSON Data from an API
In the previous challenge, you saw how to get JSON data from the freeCodeCamp Cat Photo API.

Now you'll take a closer look at the returned data to better understand the JSON format. Recall some notation in JavaScript:

[ ] -> Square brackets represent an array
{ } -> Curly brackets represent an object
" " -> Double quotes represent a string. They are also used for key names in JSON
Understanding the structure of the data that an API returns is important because it influences how you retrieve the values you need.

On the right, click the "Get Message" button to load the freeCodeCamp Cat Photo API JSON into the HTML.

The first and last character you see in the JSON data are square brackets [ ]. This means that the returned data is an array. The second character in the JSON data is a curly { bracket, which starts an object. Looking closely, you can see that there are three separate objects. The JSON data is an array of three objects, where each object contains information about a cat photo.

You learned earlier that objects contain "key-value pairs" that are separated by commas. In the Cat Photo example, the first object has "id":0 where "id" is a key and 0 is its corresponding value. Similarly, there are keys for "imageLink", "altText", and "codeNames". Each cat photo object has these same keys, but with different values.

Another interesting "key-value pair" in the first object is "codeNames":["Juggernaut","Mrs. Wallace","ButterCup"]. Here "codeNames" is the key and its value is an array of three strings. It's possible to have arrays of objects as well as a key with an array as a value.

Remember how to access data in arrays and objects. Arrays use bracket notation to access a specific index of an item. Objects use either bracket or dot notation to access the value of a given property. Here's an example that prints the "altText" of the first cat photo - note that the parsed JSON data in the editor is saved in a variable called json:

console.log(json[0].altText);
// Prints "A white cat wearing a green helmet shaped melon on its head."

For the cat with the "id" of 2, print to the console the second value in the codeNames array. You should use bracket and dot notation on the object (which is saved in the variable json) to access the value.
```

```