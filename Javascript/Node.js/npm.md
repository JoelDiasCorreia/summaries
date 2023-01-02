
# Package Management with npm
In modern software development, it is common for any nontrivial
**program that you write to depend on third-party software libraries**.

> A package manager makes it easy to find and install third-party packages. 

Just as importantly, **a package manager keeps track of what packages your code depends** on  and saves this information into a file so that when someone else wants to try your program, they can download your code and your list of dependencies, then use their own package manager to install all the third-party packages that your code needs.

> npm is the package manager that is bundled with Node

## Installing a Package
To install a package, you use the `npm install` command.

> This reads the dependencies listed in the package.json file and downloads the third-party packages that the project needs and saves them in a node_modules/ directory.

## Dev Dependencies
The other kind of dependency is on developer tools that are needed by developers who want to work on your project, but aren’t actually needed to run the code.

```
npm install --save-dev prettier
```

## Global dependencies
Sometimes you might want to install developer tools globally so that they are accessible anywhere even for code that is not part of a formal project with a package.json file and a node_modules/ directory. For
that you can use the -g (for global) option:

```bash
$ npm install -g eslint jest
/usr/local/bin/eslint ->
/usr/local/lib/node_modules/eslint/bin/eslint.js
/usr/local/bin/jest ->
/usr/local/lib/node_modules/jest/bin/jest.js
+ jest@24.9.0
+ eslint@6.7.2
added 653 packages from 414 contributors in 25.596s
```


Source: 

*Javascript: The Definitive Guide, 7th Edition, David Flanagan*
- chapter 17.4