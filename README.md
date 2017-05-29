# \<etools-dexiejs\>

Polymer element that will add Dexies.js to your app and provide access to browser indexedDB database.
Dexie.js is a wrapper library for indexedDB with many features and a very good documentation.
The most important thing it offers is: very fast queries on the indexedDB database.

## Usage

```html
<etools-dexiejs id="dexiejsElement" db-name="etoolsDexieTestDb"></etools-dexiejs>
```

```javascript
// some polymer element
var db = this.$.dexiejsElement.db;
```

Using `db` object you have to define your [database collections](https://github.com/dfahlander/Dexie.js/wiki/Design#database-versioning)
with fields and indexes and then add, delete, update, query, sort data and so on. To see all available features checkout [Dexie.js documentation](https://github.com/dfahlander/Dexie.js/wiki).

## Install
```bash
$ bower install --save etools-dexiejs
```

## Linting the code

Innstall local npm packages (run `npm install`)
Then just run the linting task

```bash
$ npm run lint
```
You should also use polylint. If you don't have Polylint installed run `npm install -g polylint`.
Then just run the linter on each file you wish to check like so

```bash
$ polylint -i filename.html
```
At the moment polylint crashes if it encounters a missing import. If that happens, temporarily comment out such imports and run the command again.

## Preview element locally
Install needed dependencies by running: `$ bower install`.
Make sure you have the [Polymer CLI](https://www.npmjs.com/package/polymer-cli) installed. Then run `$ polymer serve` to serve your element application locally.

## Running Tests

```
$ polymer test
```
