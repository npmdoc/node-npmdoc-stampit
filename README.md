# api documentation for  [stampit (v3.1.2)](https://github.com/stampit-org/stampit#readme)  [![npm package](https://img.shields.io/npm/v/npmdoc-stampit.svg?style=flat-square)](https://www.npmjs.org/package/npmdoc-stampit) [![travis-ci.org build-status](https://api.travis-ci.org/npmdoc/node-npmdoc-stampit.svg)](https://travis-ci.org/npmdoc/node-npmdoc-stampit)
#### Create objects from reusable, composable behaviors.

[![NPM](https://nodei.co/npm/stampit.png?downloads=true)](https://www.npmjs.com/package/stampit)

[![apidoc](https://npmdoc.github.io/node-npmdoc-stampit/build/screenCapture.buildNpmdoc.browser._2Fhome_2Ftravis_2Fbuild_2Fnpmdoc_2Fnode-npmdoc-stampit_2Ftmp_2Fbuild_2Fapidoc.html.png)](https://npmdoc.github.io/node-npmdoc-stampit/build/apidoc.html)

![npmPackageListing](https://npmdoc.github.io/node-npmdoc-stampit/build/screenCapture.npmPackageListing.svg)

![npmPackageDependencyTree](https://npmdoc.github.io/node-npmdoc-stampit/build/screenCapture.npmPackageDependencyTree.svg)



# package.json

```json

{
    "author": {
        "name": "Eric Elliott",
        "url": "https://ericelliottjs.com"
    },
    "bugs": {
        "url": "https://github.com/stampit-org/stampit/issues"
    },
    "dependencies": {},
    "description": "Create objects from reusable, composable behaviors.",
    "devDependencies": {
        "babel-cli": "^6.10.1",
        "babel-preset-es2015": "^6.16.0",
        "benchmark": "^2.1.1",
        "check-compose": "^3.2.0",
        "dependency-check": "^2.5.0",
        "eslint": "^3.7.0",
        "eslint-config-airbnb-base": "^11.0.0",
        "eslint-plugin-import": "^2.0.1",
        "istanbul": "^1.1.0-alpha.1",
        "lodash": "^4.16.1",
        "magic-string": "^0.19.0",
        "nsp": "^2.1.0",
        "require-all": "^2.0.0",
        "rimraf": "^2.3.4",
        "rollup": "^0.41.1",
        "rollup-plugin-buble": "^0.15.0",
        "rollup-plugin-filesize": "^1.0.0",
        "rollup-plugin-uglify": "^1.0.0",
        "tape": "^4.2.2",
        "watch": "^1.0.1"
    },
    "directories": {},
    "dist": {
        "shasum": "8bd956b2f1ccbdb1ed2bec4af4fce4a0120a0388",
        "tarball": "https://registry.npmjs.org/stampit/-/stampit-3.1.2.tgz"
    },
    "gitHead": "be8d00a6eec289f2f0d94e81cdb3c7efbfd2b4d9",
    "homepage": "https://github.com/stampit-org/stampit#readme",
    "jsnext:main": "dist/stampit.mjs",
    "keywords": [
        "object",
        "prototype",
        "object oriented",
        "browser",
        "inheritance",
        "oop",
        "node",
        "factory",
        "class",
        "stamp"
    ],
    "license": "MIT",
    "main": "dist/stampit.full.js",
    "maintainers": [
        {
            "name": "koresar",
            "email": "kore.sar@gmail.com"
        }
    ],
    "name": "stampit",
    "npmFileMap": [
        {
            "basePath": "/dist/",
            "files": [
                "stampit.full.js",
                "stampit.full.min.js"
            ]
        }
    ],
    "npmName": "stampit",
    "optionalDependencies": {},
    "readme": "ERROR: No README data found!",
    "repository": {
        "type": "git",
        "url": "git+ssh://git@github.com/stampit-org/stampit.git"
    },
    "scripts": {
        "audit": "nsp check",
        "build": "babel-node --presets=es2015 build",
        "check": "npm run audit && npm run deps",
        "clean": "rimraf dist/*",
        "cov": "npm run cov:clean && npm run cov:generate",
        "cov:clean": "rimraf ./coverage/",
        "cov:generate": "babel-node --presets=es2015 ./node_modules/.bin/istanbul cover test",
        "deps": "npm run deps:missing && npm run deps:extra",
        "deps:extra": "dependency-check package.json --extra --no-dev --ignore",
        "deps:missing": "dependency-check package.json",
        "lint": "eslint src && eslint test",
        "posttest": "node test/benchmark",
        "prebuild": "npm run clean",
        "precheck": "npm test",
        "prepublish": "npm run check",
        "pretest": "npm run build",
        "test": "babel-node --presets=es2015 test && npm run lint",
        "watch": "watch 'clear && npm -s test' test/ src/"
    },
    "version": "3.1.2"
}
```



# <a name="apidoc.tableOfContents"></a>[table of contents](#apidoc.tableOfContents)

#### [module stampit](#apidoc.module.stampit)
1.  [function <span class="apidocSignatureSpan">stampit.</span>compose ()](#apidoc.element.stampit.compose)
1.  [function <span class="apidocSignatureSpan">stampit.</span>composers ()](#apidoc.element.stampit.composers)
1.  [function <span class="apidocSignatureSpan">stampit.</span>conf ()](#apidoc.element.stampit.conf)
1.  [function <span class="apidocSignatureSpan">stampit.</span>configuration ()](#apidoc.element.stampit.configuration)
1.  [function <span class="apidocSignatureSpan">stampit.</span>deepConf ()](#apidoc.element.stampit.deepConf)
1.  [function <span class="apidocSignatureSpan">stampit.</span>deepConfiguration ()](#apidoc.element.stampit.deepConfiguration)
1.  [function <span class="apidocSignatureSpan">stampit.</span>deepProperties ()](#apidoc.element.stampit.deepProperties)
1.  [function <span class="apidocSignatureSpan">stampit.</span>deepProps ()](#apidoc.element.stampit.deepProps)
1.  [function <span class="apidocSignatureSpan">stampit.</span>deepStatics ()](#apidoc.element.stampit.deepStatics)
1.  [function <span class="apidocSignatureSpan">stampit.</span>init ()](#apidoc.element.stampit.init)
1.  [function <span class="apidocSignatureSpan">stampit.</span>initializers ()](#apidoc.element.stampit.initializers)
1.  [function <span class="apidocSignatureSpan">stampit.</span>methods ()](#apidoc.element.stampit.methods)
1.  [function <span class="apidocSignatureSpan">stampit.</span>properties ()](#apidoc.element.stampit.properties)
1.  [function <span class="apidocSignatureSpan">stampit.</span>propertyDescriptors ()](#apidoc.element.stampit.propertyDescriptors)
1.  [function <span class="apidocSignatureSpan">stampit.</span>props ()](#apidoc.element.stampit.props)
1.  [function <span class="apidocSignatureSpan">stampit.</span>refs ()](#apidoc.element.stampit.refs)
1.  [function <span class="apidocSignatureSpan">stampit.</span>staticDeepProperties ()](#apidoc.element.stampit.staticDeepProperties)
1.  [function <span class="apidocSignatureSpan">stampit.</span>staticProperties ()](#apidoc.element.stampit.staticProperties)
1.  [function <span class="apidocSignatureSpan">stampit.</span>staticPropertyDescriptors ()](#apidoc.element.stampit.staticPropertyDescriptors)
1.  [function <span class="apidocSignatureSpan">stampit.</span>statics ()](#apidoc.element.stampit.statics)



# <a name="apidoc.module.stampit"></a>[module stampit](#apidoc.module.stampit)

#### <a name="apidoc.element.stampit.compose"></a>[function <span class="apidocSignatureSpan">stampit.</span>compose ()](#apidoc.element.stampit.compose)
- description and source-code
```javascript
compose = function () { [native code] }
```
- example usage
```shell
...
  getMyProp() {
    return this.myProp;
  }
})
.init(function ({value}) {      // add initializers to your future objects
  this.myProp = value || this.myProp;
})
.compose(AnotherStamp);         // add other stamp behaviours to your objects

console.log(typeof MyStamp);                            // 'function'
console.log(MyStamp());                                 // { myProp: 'default value' }

console.log(typeof MyStamp().getMyProp);                // 'function'
console.log(MyStamp().getMyProp());                     // default value
...
```

#### <a name="apidoc.element.stampit.composers"></a>[function <span class="apidocSignatureSpan">stampit.</span>composers ()](#apidoc.element.stampit.composers)
- description and source-code
```javascript
function composers() {
  var args = [], len = arguments.length;
  while ( len-- ) args[ len ] = arguments[ len ];

  return ((this && this.compose) || stampit).call(this, {
    composers: extractFunctions.apply(void 0, args)
  });
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.stampit.conf"></a>[function <span class="apidocSignatureSpan">stampit.</span>conf ()](#apidoc.element.stampit.conf)
- description and source-code
```javascript
function composeUtil() {
  var i = arguments.length, argsArray = Array(i);
  while ( i-- ) argsArray[i] = arguments[i];

  return ((this && this.compose) || stampit).call(this, ( obj = {}, obj[propName] = action.apply(void 0, [ {} ].concat( argsArray
 )), obj ));
  var obj;
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.stampit.configuration"></a>[function <span class="apidocSignatureSpan">stampit.</span>configuration ()](#apidoc.element.stampit.configuration)
- description and source-code
```javascript
function composeUtil() {
  var i = arguments.length, argsArray = Array(i);
  while ( i-- ) argsArray[i] = arguments[i];

  return ((this && this.compose) || stampit).call(this, ( obj = {}, obj[propName] = action.apply(void 0, [ {} ].concat( argsArray
 )), obj ));
  var obj;
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.stampit.deepConf"></a>[function <span class="apidocSignatureSpan">stampit.</span>deepConf ()](#apidoc.element.stampit.deepConf)
- description and source-code
```javascript
function composeUtil() {
  var i = arguments.length, argsArray = Array(i);
  while ( i-- ) argsArray[i] = arguments[i];

  return ((this && this.compose) || stampit).call(this, ( obj = {}, obj[propName] = action.apply(void 0, [ {} ].concat( argsArray
 )), obj ));
  var obj;
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.stampit.deepConfiguration"></a>[function <span class="apidocSignatureSpan">stampit.</span>deepConfiguration ()](#apidoc.element.stampit.deepConfiguration)
- description and source-code
```javascript
function composeUtil() {
  var i = arguments.length, argsArray = Array(i);
  while ( i-- ) argsArray[i] = arguments[i];

  return ((this && this.compose) || stampit).call(this, ( obj = {}, obj[propName] = action.apply(void 0, [ {} ].concat( argsArray
 )), obj ));
  var obj;
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.stampit.deepProperties"></a>[function <span class="apidocSignatureSpan">stampit.</span>deepProperties ()](#apidoc.element.stampit.deepProperties)
- description and source-code
```javascript
function composeUtil() {
  var i = arguments.length, argsArray = Array(i);
  while ( i-- ) argsArray[i] = arguments[i];

  return ((this && this.compose) || stampit).call(this, ( obj = {}, obj[propName] = action.apply(void 0, [ {} ].concat( argsArray
 )), obj ));
  var obj;
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.stampit.deepProps"></a>[function <span class="apidocSignatureSpan">stampit.</span>deepProps ()](#apidoc.element.stampit.deepProps)
- description and source-code
```javascript
function composeUtil() {
  var i = arguments.length, argsArray = Array(i);
  while ( i-- ) argsArray[i] = arguments[i];

  return ((this && this.compose) || stampit).call(this, ( obj = {}, obj[propName] = action.apply(void 0, [ {} ].concat( argsArray
 )), obj ));
  var obj;
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.stampit.deepStatics"></a>[function <span class="apidocSignatureSpan">stampit.</span>deepStatics ()](#apidoc.element.stampit.deepStatics)
- description and source-code
```javascript
function composeUtil() {
  var i = arguments.length, argsArray = Array(i);
  while ( i-- ) argsArray[i] = arguments[i];

  return ((this && this.compose) || stampit).call(this, ( obj = {}, obj[propName] = action.apply(void 0, [ {} ].concat( argsArray
 )), obj ));
  var obj;
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.stampit.init"></a>[function <span class="apidocSignatureSpan">stampit.</span>init ()](#apidoc.element.stampit.init)
- description and source-code
```javascript
function initializers() {
  var args = [], len = arguments.length;
  while ( len-- ) args[ len ] = arguments[ len ];

  return ((this && this.compose) || stampit).call(this, {
    initializers: extractFunctions.apply(void 0, args)
  });
}
```
- example usage
```shell
...
  myProp: 'default value'
})
.methods({                      // add methods to your future objects
  getMyProp() {
    return this.myProp;
  }
})
.init(function ({value}) {      // add initializers to your future objects
  this.myProp = value || this.myProp;
})
.compose(AnotherStamp);         // add other stamp behaviours to your objects

console.log(typeof MyStamp);                            // 'function'
console.log(MyStamp());                                 // { myProp: 'default value' }
...
```

#### <a name="apidoc.element.stampit.initializers"></a>[function <span class="apidocSignatureSpan">stampit.</span>initializers ()](#apidoc.element.stampit.initializers)
- description and source-code
```javascript
function initializers() {
  var args = [], len = arguments.length;
  while ( len-- ) args[ len ] = arguments[ len ];

  return ((this && this.compose) || stampit).call(this, {
    initializers: extractFunctions.apply(void 0, args)
  });
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.stampit.methods"></a>[function <span class="apidocSignatureSpan">stampit.</span>methods ()](#apidoc.element.stampit.methods)
- description and source-code
```javascript
function composeUtil() {
  var i = arguments.length, argsArray = Array(i);
  while ( i-- ) argsArray[i] = arguments[i];

  return ((this && this.compose) || stampit).call(this, ( obj = {}, obj[propName] = action.apply(void 0, [ {} ].concat( argsArray
 )), obj ));
  var obj;
}
```
- example usage
```shell
...
## Simplest Example

'''js
const MyStamp = stampit()       // create new empty stamp
.props({                        // add properties to your future objects
  myProp: 'default value'
})
.methods({                      // add methods to your future objects
  getMyProp() {
    return this.myProp;
  }
})
.init(function ({value}) {      // add initializers to your future objects
  this.myProp = value || this.myProp;
})
...
```

#### <a name="apidoc.element.stampit.properties"></a>[function <span class="apidocSignatureSpan">stampit.</span>properties ()](#apidoc.element.stampit.properties)
- description and source-code
```javascript
function composeUtil() {
  var i = arguments.length, argsArray = Array(i);
  while ( i-- ) argsArray[i] = arguments[i];

  return ((this && this.compose) || stampit).call(this, ( obj = {}, obj[propName] = action.apply(void 0, [ {} ].concat( argsArray
 )), obj ));
  var obj;
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.stampit.propertyDescriptors"></a>[function <span class="apidocSignatureSpan">stampit.</span>propertyDescriptors ()](#apidoc.element.stampit.propertyDescriptors)
- description and source-code
```javascript
function composeUtil() {
  var i = arguments.length, argsArray = Array(i);
  while ( i-- ) argsArray[i] = arguments[i];

  return ((this && this.compose) || stampit).call(this, ( obj = {}, obj[propName] = action.apply(void 0, [ {} ].concat( argsArray
 )), obj ));
  var obj;
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.stampit.props"></a>[function <span class="apidocSignatureSpan">stampit.</span>props ()](#apidoc.element.stampit.props)
- description and source-code
```javascript
function composeUtil() {
  var i = arguments.length, argsArray = Array(i);
  while ( i-- ) argsArray[i] = arguments[i];

  return ((this && this.compose) || stampit).call(this, ( obj = {}, obj[propName] = action.apply(void 0, [ {} ].concat( argsArray
 )), obj ));
  var obj;
}
```
- example usage
```shell
...
Stamps are [standardised](https://github.com/stampit-org/stamp-specification) composable factory functions. **Stampit** is an [infected
 compose](https://medium.com/@koresar/fun-with-stamps-episode-8-tracking-and-overriding-composition-573aa85ba622) featuring friendly
 handy API.


## Simplest Example

'''js
const MyStamp = stampit()       // create new empty stamp
.props({                        // add properties to your future objects
  myProp: 'default value'
})
.methods({                      // add methods to your future objects
  getMyProp() {
    return this.myProp;
  }
})
...
```

#### <a name="apidoc.element.stampit.refs"></a>[function <span class="apidocSignatureSpan">stampit.</span>refs ()](#apidoc.element.stampit.refs)
- description and source-code
```javascript
function composeUtil() {
  var i = arguments.length, argsArray = Array(i);
  while ( i-- ) argsArray[i] = arguments[i];

  return ((this && this.compose) || stampit).call(this, ( obj = {}, obj[propName] = action.apply(void 0, [ {} ].concat( argsArray
 )), obj ));
  var obj;
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.stampit.staticDeepProperties"></a>[function <span class="apidocSignatureSpan">stampit.</span>staticDeepProperties ()](#apidoc.element.stampit.staticDeepProperties)
- description and source-code
```javascript
function composeUtil() {
  var i = arguments.length, argsArray = Array(i);
  while ( i-- ) argsArray[i] = arguments[i];

  return ((this && this.compose) || stampit).call(this, ( obj = {}, obj[propName] = action.apply(void 0, [ {} ].concat( argsArray
 )), obj ));
  var obj;
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.stampit.staticProperties"></a>[function <span class="apidocSignatureSpan">stampit.</span>staticProperties ()](#apidoc.element.stampit.staticProperties)
- description and source-code
```javascript
function composeUtil() {
  var i = arguments.length, argsArray = Array(i);
  while ( i-- ) argsArray[i] = arguments[i];

  return ((this && this.compose) || stampit).call(this, ( obj = {}, obj[propName] = action.apply(void 0, [ {} ].concat( argsArray
 )), obj ));
  var obj;
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.stampit.staticPropertyDescriptors"></a>[function <span class="apidocSignatureSpan">stampit.</span>staticPropertyDescriptors ()](#apidoc.element.stampit.staticPropertyDescriptors)
- description and source-code
```javascript
function composeUtil() {
  var i = arguments.length, argsArray = Array(i);
  while ( i-- ) argsArray[i] = arguments[i];

  return ((this && this.compose) || stampit).call(this, ( obj = {}, obj[propName] = action.apply(void 0, [ {} ].concat( argsArray
 )), obj ));
  var obj;
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.stampit.statics"></a>[function <span class="apidocSignatureSpan">stampit.</span>statics ()](#apidoc.element.stampit.statics)
- description and source-code
```javascript
function composeUtil() {
  var i = arguments.length, argsArray = Array(i);
  while ( i-- ) argsArray[i] = arguments[i];

  return ((this && this.compose) || stampit).call(this, ( obj = {}, obj[propName] = action.apply(void 0, [ {} ].concat( argsArray
 )), obj ));
  var obj;
}
```
- example usage
```shell
n/a
```



# misc
- this document was created with [utility2](https://github.com/kaizhu256/node-utility2)
