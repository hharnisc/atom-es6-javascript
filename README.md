# es6-javascript
A collection of commands and ES6 focused snippets for optimizing modern Javascript development productivity. It aims to be compliant with [AirBnB's mostly reasonable approach to Javascript](https://github.com/airbnb/javascript).

*Note: this is a fork of [turbo-javascript](https://github.com/extrabacon/atom-turbo-javascript) that uses arrow functions by default and adds a few more snippets for chai and classes for convenience.*

## Changelog

**Version 1.0.0**

- Uses single quotes to comply with AirBnB guidelines

If you need double quotes please downgrade `apm install es6-javascript@0.7.0`

## Commands

Use the following keymaps to speed up your development. You can quickly terminate lines with semicolons or manipulate blocks of code with ease.

#### End Line `CTRL-;`
Terminates the current line with a semicolon.

#### End Line with a comma `CTRL-,`
Terminates the current line with a comma (great for object literals).

#### End New Line `CTRL-ENTER`
Terminates the current line with a colon or semicolon, followed with a new line. A comma is inserted when the cursor is inside an object literal, otherwise a semicolon is inserted.

#### Easy Blocks `CTRL-B`
Creates a statement block `{ ... }` with the selected text placed inside and properly indented. If the selection is already wrapped with a block, the block is removed and its content is unindented.

## Snippets

Snippets are optimized to be short and easy to remember. Some snippets are "chainable" and render differently when preceded by a ".".

For example, `.fe` renders a chain-friendly version of the forEach snippet, while `fe` renders a full code block.

### Declarations

#### `v⇥` var statement
```js
var ${1:name};
```

#### `ve⇥` var assignment
```js
var ${1:name} = ${2:value};
```

#### `l⇥` let statement
```js
let ${1:name};
```

#### `le⇥` let assignment
```js
let ${1:name} = ${2:value};
```

#### `co⇥` const statement
```js
const ${1:name};
```

#### `coe⇥` const assignment
```js
const ${1:name} = ${2:value};
```

#### `cos⇥` const symbol
```js
const ${1:name} = Symbol('${1:name}');
```


### Flow Control

#### `if⇥` if statement
```js
if (${1:condition}) {
  ${0}
}
```

#### `el⇥` else statement
```js
else {
  ${0}
}
```

#### `ife⇥` else statement
```js
if (${1:condition}) {
  ${2}
} else {
  ${3}
}
```

#### `ei⇥` else if statement
```js
else if (${1:condition}) {
  ${0}
}
```

#### `fl⇥` for loop
```js
for (let ${1:i} = 0; ${1:i} < ${2:iterable}${3:.length}; ${1:i}++) {
  ${4}
}
```

#### `fi⇥` for in loop
```js
for (let ${1:key} in ${2:source}) {
  if (${2:source}.hasOwnProperty(${1:key})) {
    ${0}
  }
}
```

#### `fo⇥` for of loop (ES6)
```js
for (let ${1:key} of ${2:source}) {
  ${0}
}
```

#### `wl⇥` while loop
```js
while (${1:condition}) {
  ${0}
}
```

#### `tc⇥` try/catch
```js
try {
  ${1}
} catch (${2:err}) {
  ${3}
}
```

#### `tf⇥` try/finally
```js
try {
 ${1}
} finally {
 ${2}
}
```

#### `tcf⇥` try/catch/finally
```js
try {
  ${1}
} catch (${2:err}) {
  ${3}
} finally {
  ${4}
}
```

### Functions

#### `f⇥` anonymous function
```js
function (${1:arguments}) {${0}}
```

#### `fn⇥` named function
```js
function ${1:name}(${2:arguments}) {
  ${0}
}
```

#### `iife⇥` immediately-invoked function expression (IIFE)
```js
((${1:arguments}) => {
  ${0}
})(${2});
```

#### `fa⇥` function apply
```js
${1:fn}.apply(${2:this}, ${3:arguments})
```

#### `fc⇥` function call
```js
${1:fn}.call(${2:this}, ${3:arguments})
```

#### `fb⇥` function bind
```js
${1:fn}.bind(${2:this}, ${3:arguments})
```

#### `af⇥` arrow function (ES6)
```js
${1:(arguments)} => ${2:statement}
```

#### `afb⇥` arrow function with body (ES6)
```js
${1:(arguments)} => {
\t${0}
}
```

#### `gf⇥` generator function (ES6)
```js
function* (${1:arguments}) {
  ${0}
}
```

#### `gfn⇥` named generator function (ES6)
```js
function* ${1:name}(${1:arguments}) {
  ${0}
}
```

### Iterables

#### `fe⇥` forEach loop (chainable)
```js
${1:iterable}.forEach((${2:item}) => {
  ${0}
});
```

#### `map⇥` map function (chainable)
```js
${1:iterable}.map((${2:item}) => {
  ${0}
});
```

#### `reduce⇥` reduce function (chainable)
```js
${1:iterable}.reduce((${2:previous}, ${3:current}) => {
  ${0}
}${4:, initial});
```

#### `filter⇥` filter function (chainable)
```js
${1:iterable}.filter((${2:item}) => {
  ${0}
});
```

#### `find⇥` ES6 find function (chainable)
```js
${1:iterable}.find((${2:item}) => {
  ${0}
});
```

### Objects and classes

#### `c⇥` class (ES6)
```js
class ${1:name} {
  constructor(${2:arguments}) {
    ${0}
  }
}
```

#### `cex⇥` child class (ES6)
```js
class ${1:name} extends ${2:base} {
  constructor(${2:arguments}) {
    super(${2:arguments})
    ${0}
  }
}
```

#### `cf⇥` class function (ES6)

```js
{$1:name}({$2:arguments}) {
  ${0}
}
```

#### `kv⇥` key/value pair
Javascript:
```js
${1:key}: ${2:'value'}
```

#### `m⇥` method (ES6 syntax)
```js
${1:method}(${2:arguments}) {
  ${0}
}
```

#### `get⇥` getter (ES6 syntax)
```js
get ${1:property}() {
  ${0}
}
```

#### `set⇥` setter (ES6 syntax)
```js
set ${1:property}(${2:value}) {
  ${0}
}
```

#### `gs⇥` getter and setter (ES6 syntax)
```js
get ${1:property}() {
  ${0}
}
set ${1:property}(${2:value}) {

}
```

#### `proto⇥` prototype method (chainable)
```js
${1:Class}.prototype.${2:methodName} = function (${3:arguments}) {
  ${0}
};
```

### Returning values

#### `r⇥` return
```js
return ${0};
```

#### `rth⇥` return this
```js
return this;
```

#### `rn⇥` return null
```js
return null;
```

#### `rt⇥` return true
```js
return true;
```

#### `rf⇥` return false
```js
return false;
```

#### `r0⇥` return 0
```js
return 0;
```

#### `r-1⇥` return -1
```js
return -1;
```

#### `rp⇥` return Promise (ES6)
```js
return new Promise((resolve, reject) => {
  ${0}
});
```

### Types

#### `S⇥` String
#### `N⇥` Number
#### `O⇥` Object
#### `A⇥` Array
#### `D⇥` Date
#### `Rx⇥` RegExp

#### `tof⇥` typeof comparison
```js
typeof ${1:source} === '${2:undefined}'
```

#### `iof⇥` instanceof comparison
```js
${1:source} instanceof ${2:Object}
```

### Promises

#### `p⇥` new Promise (ES6)
```js
new Promise((resolve, reject) => {
  ${0}
})
```

#### `then⇥` Promise.then (chainable)
```js
${1:promise}.then((${2:value}) => {
  ${0}
});
```

#### `catch⇥` Promise.catch (chainable)
```js
${1:promise}.catch((${2:err}) => {
  ${0}
});
```

### ES6 modules

#### `ex⇥` module export
```js
export ${1:member};
```

#### `im⇥` module import
```js
import ${1:*} from '${2:module}';
```

#### `ima⇥` module import as
```js
import ${1:*} as ${2:name} from '${3:module}';
```

#### `imn⇥` named module import
```js
import \{ ${1:name} \} from '${2:module}';
```

### BDD testing (Mocha, Jasmine, etc.)

#### `desc⇥` describe
```js
describe('${1:description}', () => {
  ${0}
});
```

#### `its⇥` synchronous "it"
```js
it('${1:description}', () => {
  ${0}
});
```

#### `ita⇥` asynchronous "it"
```js
it('${1:description}', (done) => {
  ${0}
});
```

#### `bef⇥` before
```js
before(() => {
  ${0}
});
```

#### `befe⇥` beforeEach
```js
beforeEach(() => {
  ${0}
});
```

#### `aft⇥` after
```js
after(() => {
  ${0}
});
```

#### `afte⇥` afterEach
```js
afterEach(() => {
  ${0}
});
```

### Console

#### `cl⇥` console.log
```js
console.log('${1:title}', ${2:$1}$0);
```

#### `cll⇥` console.log (text only)
```js
console.log(${0});
```

#### `ce⇥` console.error
```js
console.error(${0});
```

#### `cw⇥` console.warn
```js
console.warn(${0});
```

### Timers

#### `st⇥` setTimeout
```js
setTimeout(() => {
  ${0}
}, ${1:delay});
```

#### `si⇥` setInterval
```js
setTimeout(() => {
  ${0}
}, ${1:delay});
```

#### `sim⇥` setInterval
```js
setImmediate(() => {
  ${0}
});
```


### DOM specifics

#### `ae⇥` addEventListener
```js
${1:document}.addEventListener('${2:event}', function (e) {
  ${0}
});
```

#### `gi⇥` getElementById
```js
${1:document}.getElementById('${2:id}')
```

#### `gc⇥` getElementsByClassName
```js
Array.from(${1:document}.getElementsByClassName('${2:class}'))
```
`Array.from` polyfill required for ES5

#### `gt⇥` getElementsByTagName
```js
Array.from(${1:document}.getElementsByTagName('${2:tag}'))
```
`Array.from` polyfill required for ES5

#### `qs⇥` querySelector
```js
${1:document}.querySelector('${2:selector}')
```

#### `qsa⇥` querySelectorAll
```js
Array.from(${1:document}.querySelectorAll('${2:selector}'))
```
`Array.from` polyfill required for ES5

### Node.js specifics

#### `cb⇥` Node.js style callback
```js
(err${1:, value}) => {${0}}
```

#### `re⇥` require a module
```js
require('${1:module}');
```

#### `em⇥` export member
```js
exports.${1:name} = ${2:value};
```

#### `me⇥` module.exports
```js
module.exports = ${1:name};
```

#### `on⇥` attach an event handler (chainable)
```js
${1:emitter}.on('${2:event}', (${3:arguments}) => {
  ${0}
});
```

### Miscellaneous

#### `us⇥` use strict
```js
'use strict';
```

# License

The MIT License (MIT)
