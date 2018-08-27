Managing Packages with Npm - How to Use package.json, the Core of Any Node.js Project or npm Package
The file package.json is the center of any Node.js project or npm package. It stores information about your project just like the -section in a HTML document describes the content of a webpage. The package.json consists of a single JSON-object where information is stored in "key": value-pairs. There are only two required fields in a minimal package.json - name and version - but it’s a good practice to provide additional information about your project that could be useful to future users or maintainers.

The author-field

If you go to the Glitch project that you set up previously and look at on the left side of your screen, you’ll find the file tree where you can see an overview of the various files in your project. Under the file tree’s back-end section, you’ll find package.json - the file that we’ll be improving in the next couple of challenges.

One of the most common pieces of information in this file is the author-field that specifies who’s the creator of a project. It can either be a string or an object with contact details. The object is recommended for bigger projects but in our case, a simple string like the following example will do.

"author": "Jane Doe",

Instructions

Add your name to the author-field in the package.json of your Glitch project.

Remember that you’re writing JSON.

All field-names must use double-quotes ("), e.g. "author"

All fields must be separated with a comma (,)

```
- fork [glitch boilerplate-npm](https://glitch.com/#!/import/github/freeCodeCamp/boilerplate-npm)

- add`"author": "Jane Doe",` to package.json

- click share，copy the `Share your App` url
```