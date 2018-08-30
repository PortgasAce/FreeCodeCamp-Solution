Managing Packages with Npm - Manage npm Dependencies By Understanding Semantic Versioning
Versions of the npm packages in the dependencies-section of your package.json follow what’s called Semantic Versioning (SemVer), an industry standard for software versioning aiming to make it easier to manage dependencies. Libraries, frameworks or other tools published on npm should use SemVer in order to clearly communicate what kind of changes that projects who depend on the package can expect if they update.

SemVer doesn’t make sense in projects without public APIs - so unless your project is similar to the examples above, use another versioning format.

So why do you need to understand SemVer?

Knowing SemVer can be useful when you develop software that use external dependencies (which you almost always do). One day, your understanding of these numbers will save you from accidentally introducing breaking changes to your project without understanding why things “that worked yesterday” suddenly doesn’t.

This is how Semantic Versioning works according to the official website:

Given a version number MAJOR.MINOR.PATCH, increment the:

MAJOR version when you make incompatible API changes,

MINOR version when you add functionality in a backwards-compatible manner, and

PATCH version when you make backwards-compatible bug fixes.

This means that PATCHes are bug fixes and MINORs add new features but neither of them break what worked before. Finally, MAJORs add changes that won’t work with earlier versions.

Example

A semantic version number: 1.3.8

Instructions

In the dependencies-section of your package.json, change the version of moment to match MAJOR version 2, MINOR version 10 and PATCH version 2