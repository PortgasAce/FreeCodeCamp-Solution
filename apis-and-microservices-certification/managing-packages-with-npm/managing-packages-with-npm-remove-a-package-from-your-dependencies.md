Managing Packages with Npm - Remove a Package from Your Dependencies
Now you’ve tested a few ways you can manage dependencies of your project by using the package.json's dependencies-section. You’ve included external packages by adding them to the file and even told npm what types of versions you want by using special characters as the tilde (~) or the caret (^).

But what if you want to remove an external package that you no longer need? You might already have guessed it - Just remove the corresponding "key": value-pair for that from your dependencies.

This same method applies to removing other fields in your package.json as well

Instructions

Remove the package moment from your dependencies.

Make sure you have the right amount of commas after removing it.