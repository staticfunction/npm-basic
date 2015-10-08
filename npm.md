# NPM

---

## What is NPM?
 * A package manager for Javascript
 * Makes it easy for JavaScript developers to share and reuse code

Note: npm makes it easy for JavaScript developers to share and reuse code, and it makes it easy to update the code that you're sharing.

---

## General Idea
> Create small packages which solves one problem and solves it well

---

## Getting Started

```shell 
npm init 
```

Note: This will create a package.json

---

## Install Dependencies

```shell
npm install your-dependency
```

Note: There are at least 2 kinds of dependencies that are commonly used

---

## dependecies

```json
"dependencies": {
	"random-movie": "~1.4.3"
}
```
OR

```shell
npm install random-movie --save
```

Note: This kind of dependencies is needed for your project to run.

---

## devDependencies

```json
"devDependencies": {
	"browserify": "~11.2.0",
    "http-server": "~0.8.5"
}
```
OR

```shell
npm install browserify http-server --save-dev
```

Note: This kind of dependecies are use to help you build your project

---

## Semantic Versioning

Major.Minor.Patch | 1.2.3

> NPM follows [Semantic versioning v2.0.0](http://semver.org/)

---

## Custom Scripts

```json
"scripts": {
	"build": "browserify movie.js --standalone movie --outfile bundle.js",
	"launch": "http-server . -a localhost -o"
}
```

And you can run them by:

```shell
npm run launch
```

---

## Publishing

```shell
npm publish
```

* When publishing a commonjs library be sure to set your main:

```json
"main": "index.js"
```

---