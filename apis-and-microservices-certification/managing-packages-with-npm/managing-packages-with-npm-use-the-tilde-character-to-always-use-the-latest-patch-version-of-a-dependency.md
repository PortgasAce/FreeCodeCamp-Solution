Managing Packages with Npm - Use the Tilde-Character to Always Use the Latest Patch Version of a Dependency
In the last challenge, we told npm to only include a specific version of a package. That’s a useful way to freeze your dependencies if you need to make sure that different parts of your project stay compatible with each other. But in most use cases you don’t want to miss bug fixes, since they often include important security patches and (hopefully) don’t break things in doing so.

To allow a npm dependency to get updated to the latest PATCH-version, you can prefix the dependency’s version with the tilde-character (~). In package.json, our current rule for how npm may upgrade moment is to use a specific version only (2.10.2), but we want to allow the latest 2.10.x-version.

Example

"some-package-name": "~1.3.8" allows updates to any 1.3.x version.

Instructions

Use the tilde-character (~) to prefix the version of moment in your dependencies and allow npm to update it to any new PATCH release.

Note that the version numbers themselves not should be changed.