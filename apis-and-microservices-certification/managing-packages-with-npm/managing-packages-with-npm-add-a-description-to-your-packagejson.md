Managing Packages with Npm - Add a Description to Your package.json
The next part of a good package.json is the description-field, where a short but informative description about your project belongs.

If you some day plan to publishing a package to npm, remember that this is the string that should sell your idea to the user when they decide whether to install your package or not. However, that’s not the only use case for the description: Since it’s a great way to summarize what a project does, it’s just as important for your normal Node.js-projects to help other developers, future maintainers or even your future self understand the project quickly.

Regardless of what you plan for your project, a description is definitely recommended. Let’s add something similar to this:

"description": "A project that does something awesome",

Instructions

Add a description to the package.json in your Glitch project.

Remember to use double-quotes for field-names (") and commas (,) to separate fields.