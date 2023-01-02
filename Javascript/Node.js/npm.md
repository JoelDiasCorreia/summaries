
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
Sometimes you might want to **install developer tools globally so that they are accessible anywhere even for code** that is not part of a formal project with a package.json file and a node_modules/ directory. For
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

```bash
$ which eslint
/usr/local/bin/eslint
$ which jest
/usr/local/bin/jest
```

## Uninstalling a Package
npm supports “uninstall” and “update” commands


```bash
$ npm uninstall prettier
removed 1 package and audited 652 packages in 1.99s
found 0 vulnerabilities
```

## Auditing Packages

npm also has an interesting “audit” command that you can use to find and fix security vulnerabilities in your dependencies:

```bash
$ npm audit --fix
=== npm audit security report ===
found 0 vulnerabilities in 876354 scanned packages
```

## Listing Packages

This command will print to stdout all the versions of packages that are installed, as well as their dependencies when --all is specified, in a tree structure.

```bash
npm ls
```

## Run locally installed tools 

Fortunately, npm is bundled with a command known as “npx,” which you can use to run locally installed tools with commands like `npx eslint` or `npx jest`.

## open source packages
The company behind npm also maintains the https://npmjs.com
package repository, which holds hundreds of thousands of open source packages. But you don’t have to use the npm package manager to access this repository of packages. Alternatives include ` yarn` and `pnpm`.

Source: 

- *Javascript: The Definitive Guide, 7th Edition, David Flanagan* chapter 17.4

- [Docs npmjs Version 7 npm-ls](https://docs.npmjs.com/cli/v7/commands/npm-ls?v=true)
