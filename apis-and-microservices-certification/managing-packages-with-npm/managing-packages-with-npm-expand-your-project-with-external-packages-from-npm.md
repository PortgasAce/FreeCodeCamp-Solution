Managing Packages with Npm - Expand Your Project with External Packages from npm
One of the biggest reasons to use a package manager is their powerful dependency management. Instead of manually having to make sure that you get all dependencies whenever you set up a project on a new computer, npm automatically installs everything for you. But how can npm know exactly what your project needs? Meet the dependencies-section of your package.json.

In the dependencies-section, packages your project require are stored using the following format:

"dependencies": {

"package-name": "version",

"express": "4.14.0"

}

Instructions

Add version 2.14.0 of the package moment to the dependencies-field of your package.json

Moment is a handy library for working with time and dates.