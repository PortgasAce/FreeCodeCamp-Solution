Basic HTML and HTML5: Create a Set of Checkboxes
Forms commonly use checkboxes for questions that may have more than one answer.

Checkboxes are a type of input

Each of your checkboxes can be nested within its own label element. By wrapping an input element inside of a label element it will automatically associate the checkbox input with the label element surrounding it.

All related checkbox inputs should have the same name attribute.

It is considered best practice to explicitly define the relationship between a checkbox input and its corresponding label by setting the for attribute on the label element to match the id attribute of the associated input element.

Here's an example of a checkbox:
```
<label for="loving"><input id="loving" type="checkbox" name="personality"> Loving</label>
```

Add to your form a set of three checkboxes. Each checkbox should be nested within its own label element. All three should share the name attribute of personality.

```

```
