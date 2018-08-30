Managing Packages with Npm - Use the Caret-Character to Use the Latest Minor Version of a Dependency
Similar to how the tilde (~) we learned about in the last challenge allow npm to install the latest PATCH for a dependency, the caret (^) allows npm to install future updates as well. The difference is that the caret will allow both MINOR updates and PATCHes.

At the moment, your current version of moment should be ~2.10.2 which allows npm to install to the latest 2.10.x-version. If we instead were to use the caret (^) as our version prefix, npm would instead be allowed to update to any 2.x.x-version.

Example

"some-package-name": "^1.3.8" allows updates to any 1.x.x version.

Instructions

Use the caret-character (^) to prefix the version of moment in your dependencies and allow npm to update it to any new MINOR release.

Note that the version numbers themselves not should be changed.