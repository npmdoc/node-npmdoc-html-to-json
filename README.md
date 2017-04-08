# api documentation for  [html-to-json (v0.6.0)](https://github.com/prolificinteractive/node-html-to-json#readme)  [![npm package](https://img.shields.io/npm/v/npmdoc-html-to-json.svg?style=flat-square)](https://www.npmjs.org/package/npmdoc-html-to-json) [![travis-ci.org build-status](https://api.travis-ci.org/npmdoc/node-npmdoc-html-to-json.svg)](https://travis-ci.org/npmdoc/node-npmdoc-html-to-json)
#### Parses HTML strings into objects using flexible, composable filters.

[![NPM](https://nodei.co/npm/html-to-json.png?downloads=true)](https://www.npmjs.com/package/html-to-json)

[![apidoc](https://npmdoc.github.io/node-npmdoc-html-to-json/build/screenCapture.buildApidoc.browser.%252Fhome%252Ftravis%252Fbuild%252Fnpmdoc%252Fnode-npmdoc-html-to-json%252Ftmp%252Fbuild%252Fapidoc.html.png)](https://npmdoc.github.io/node-npmdoc-html-to-json/build/apidoc.html)

![npmPackageListing](https://npmdoc.github.io/node-npmdoc-html-to-json/build/screenCapture.npmPackageListing.svg)

![npmPackageDependencyTree](https://npmdoc.github.io/node-npmdoc-html-to-json/build/screenCapture.npmPackageDependencyTree.svg)



# package.json

```json

{
    "author": {
        "name": "Eric Weber"
    },
    "bugs": {
        "url": "https://github.com/prolificinteractive/node-html-to-json/issues"
    },
    "dependencies": {
        "bluebird": "^3.0.6",
        "cheerio": "^0.19.0",
        "lodash": "^3.10.1",
        "request": "^2.67.0"
    },
    "description": "Parses HTML strings into objects using flexible, composable filters.",
    "devDependencies": {
        "express": "^4.10.4",
        "mocha": "^2.3.4",
        "should": "^7.1.1"
    },
    "directories": {},
    "dist": {
        "shasum": "718db295f3de0a9262d4528fac1a85837e6e06b1",
        "tarball": "https://registry.npmjs.org/html-to-json/-/html-to-json-0.6.0.tgz"
    },
    "gitHead": "3fc462625525b6d67b2f4c5cc2e04b564d463fec",
    "homepage": "https://github.com/prolificinteractive/node-html-to-json#readme",
    "license": "MIT",
    "main": "index.js",
    "maintainers": [
        {
            "name": "prolificeric",
            "email": "eric@prolificinteractive.com"
        }
    ],
    "name": "html-to-json",
    "optionalDependencies": {},
    "readme": "ERROR: No README data found!",
    "repository": {
        "type": "git",
        "url": "git+https://github.com/prolificinteractive/node-html-to-json.git"
    },
    "scripts": {
        "test": "jshint ./lib/* ./test/*; node_modules/.bin/mocha"
    },
    "version": "0.6.0"
}
```



# <a name="apidoc.tableOfContents"></a>[table of contents](#apidoc.tableOfContents)

#### [module html-to-json](#apidoc.module.html-to-json)
1.  [function <span class="apidocSignatureSpan">html-to-json.</span>ParseContext (options)](#apidoc.element.html-to-json.ParseContext)
1.  [function <span class="apidocSignatureSpan">html-to-json.</span>Parser (filter)](#apidoc.element.html-to-json.Parser)
1.  [function <span class="apidocSignatureSpan">html-to-json.</span>batch (html, dictionary, callback)](#apidoc.element.html-to-json.batch)
1.  [function <span class="apidocSignatureSpan">html-to-json.</span>createMethod (filter)](#apidoc.element.html-to-json.createMethod)
1.  [function <span class="apidocSignatureSpan">html-to-json.</span>createParser (filter)](#apidoc.element.html-to-json.createParser)
1.  [function <span class="apidocSignatureSpan">html-to-json.</span>parse (html, filter, callback)](#apidoc.element.html-to-json.parse)
1.  [function <span class="apidocSignatureSpan">html-to-json.</span>request (options, filter, callback)](#apidoc.element.html-to-json.request)
1.  object <span class="apidocSignatureSpan">html-to-json.</span>ParseContext.prototype
1.  object <span class="apidocSignatureSpan">html-to-json.</span>Parser.prototype

#### [module html-to-json.ParseContext](#apidoc.module.html-to-json.ParseContext)
1.  [function <span class="apidocSignatureSpan">html-to-json.</span>ParseContext (options)](#apidoc.element.html-to-json.ParseContext.ParseContext)

#### [module html-to-json.ParseContext.prototype](#apidoc.module.html-to-json.ParseContext.prototype)
1.  [function <span class="apidocSignatureSpan">html-to-json.ParseContext.prototype.</span>_filterWithArray ()](#apidoc.element.html-to-json.ParseContext.prototype._filterWithArray)
1.  [function <span class="apidocSignatureSpan">html-to-json.ParseContext.prototype.</span>_filterWithConstant ()](#apidoc.element.html-to-json.ParseContext.prototype._filterWithConstant)
1.  [function <span class="apidocSignatureSpan">html-to-json.ParseContext.prototype.</span>_filterWithFunction ()](#apidoc.element.html-to-json.ParseContext.prototype._filterWithFunction)
1.  [function <span class="apidocSignatureSpan">html-to-json.ParseContext.prototype.</span>_filterWithObject ()](#apidoc.element.html-to-json.ParseContext.prototype._filterWithObject)
1.  [function <span class="apidocSignatureSpan">html-to-json.ParseContext.prototype.</span>get (key)](#apidoc.element.html-to-json.ParseContext.prototype.get)
1.  [function <span class="apidocSignatureSpan">html-to-json.ParseContext.prototype.</span>map (selector, filter)](#apidoc.element.html-to-json.ParseContext.prototype.map)
1.  [function <span class="apidocSignatureSpan">html-to-json.ParseContext.prototype.</span>parse (callback)](#apidoc.element.html-to-json.ParseContext.prototype.parse)

#### [module html-to-json.Parser](#apidoc.module.html-to-json.Parser)
1.  [function <span class="apidocSignatureSpan">html-to-json.</span>Parser (filter)](#apidoc.element.html-to-json.Parser.Parser)

#### [module html-to-json.Parser.prototype](#apidoc.module.html-to-json.Parser.prototype)
1.  [function <span class="apidocSignatureSpan">html-to-json.Parser.prototype.</span>method ()](#apidoc.element.html-to-json.Parser.prototype.method)
1.  [function <span class="apidocSignatureSpan">html-to-json.Parser.prototype.</span>parse (html, callback)](#apidoc.element.html-to-json.Parser.prototype.parse)
1.  [function <span class="apidocSignatureSpan">html-to-json.Parser.prototype.</span>request (options, callback)](#apidoc.element.html-to-json.Parser.prototype.request)



# <a name="apidoc.module.html-to-json"></a>[module html-to-json](#apidoc.module.html-to-json)

#### <a name="apidoc.element.html-to-json.ParseContext"></a>[function <span class="apidocSignatureSpan">html-to-json.</span>ParseContext (options)](#apidoc.element.html-to-json.ParseContext)
- description and source-code
```javascript
function ParseContext(options) {
  var context = this;

  _.defaults(this, options, {
    $container: null,
    $: null,
    filter: {},
    parent: null
  });

  this.promises = Object.create(this.parent? this.parent.promises: {});
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.html-to-json.Parser"></a>[function <span class="apidocSignatureSpan">html-to-json.</span>Parser (filter)](#apidoc.element.html-to-json.Parser)
- description and source-code
```javascript
function Parser(filter) {
  this.filter = filter;
}
```
- example usage
```shell
...
var parseFoo = htmlToJson.createMethod({
'foo': function ($doc) {
  return $doc.find('#foo').bar();
}
});
'''

## htmlToJson.createParser(filter), new htmlToJson.Parser(filter)

For the sake of reusability, creates an object with '.parse' and '.request' helper methods, which use the passed filter. For example
:

'''javascript
var linkParser = htmlToJson.createParser(['a[href]', {
'text': function ($a) {
  return $a.text();
...
```

#### <a name="apidoc.element.html-to-json.batch"></a>[function <span class="apidocSignatureSpan">html-to-json.</span>batch (html, dictionary, callback)](#apidoc.element.html-to-json.batch)
- description and source-code
```javascript
function batch(html, dictionary, callback) {
  var promise;
  var $ = cheerio.load(html);
  var context = new ParseContext({
    $: $,
    $container: $.root()
  });

  promise = Promise.props(_.mapValues(dictionary, function (filter) {
    // Filter is wrapped by .createParser or .createMethod
    if (filter.filter) {
      filter = filter.filter;
    }

    context.filter = filter;

    return context.parse();
  }));

  return callbackify(promise, callback);
}
```
- example usage
```shell
...
    return $img.attr('src');
  }]
}, function (err, result) {
  console.log(result);
});
'''

## htmlToJson.batch(html, dictionary, [callback]) -> promise

Performs many parsing operations against one HTML string. This transforms the HTML into a DOM only once instead of for each filter
 in the dictionary, which can quickly get expensive in terms of processing. This also allows you to break your filters up into more
 granular components and mix and match them as you please.

The values in the dictionary can be 'htmlToJson.Parser' objects, generated methods from 'htmlToJson.createMethod', or naked filters
 that you might normally pass into 'htmlToJson.parse'. For example:

'''javascript
return getProlificHomepage().then(function (html) {
...
```

#### <a name="apidoc.element.html-to-json.createMethod"></a>[function <span class="apidocSignatureSpan">html-to-json.</span>createMethod (filter)](#apidoc.element.html-to-json.createMethod)
- description and source-code
```javascript
createMethod = function (filter) {
  return method(filter);
}
```
- example usage
```shell
...
  'name': function ($section) {
    return $section.text();
  },
  'link': function ($section) {
    return $section.attr('href');
  }
}]),
offices: htmlToJson.createMethod(['.office', {
  'location': function ($office) {
    return $office.find('.location').text();
  },
  'phone': function ($office) {
    return $office.find('.phone').text();
  }
}]),
...
```

#### <a name="apidoc.element.html-to-json.createParser"></a>[function <span class="apidocSignatureSpan">html-to-json.</span>createParser (filter)](#apidoc.element.html-to-json.createParser)
- description and source-code
```javascript
createParser = function (filter) {
  return new this.Parser(filter);
}
```
- example usage
```shell
...
Performs many parsing operations against one HTML string. This transforms the HTML into a DOM only once instead of for each filter
 in the dictionary, which can quickly get expensive in terms of processing. This also allows you to break your filters up into more
 granular components and mix and match them as you please.

The values in the dictionary can be 'htmlToJson.Parser' objects, generated methods from 'htmlToJson.createMethod', or naked filters
 that you might normally pass into 'htmlToJson.parse'. For example:

'''javascript
return getProlificHomepage().then(function (html) {
return htmlToJson.batch(html, {
  sections: htmlToJson.createParser(['#primary-nav a', {
    'name': function ($section) {
      return $section.text();
    },
    'link': function ($section) {
      return $section.attr('href');
    }
  }]),
...
```

#### <a name="apidoc.element.html-to-json.parse"></a>[function <span class="apidocSignatureSpan">html-to-json.</span>parse (html, filter, callback)](#apidoc.element.html-to-json.parse)
- description and source-code
```javascript
function parse(html, filter, callback) {
  var isCheerioObject = typeof html === 'object' && html._root._root;

  if (typeof html !== 'string' && !isCheerioObject) {
    throw new Error('HTML string required');
  }

  var $ = cheerio.load(html);

  var parseContext = new ParseContext({
    $: $,
    $container: isCheerioObject? html: $.root(),
    filter: filter
  });

  return callbackify(parseContext.parse(), callback);
}
```
- example usage
```shell
...

Parses HTML strings into objects using flexible, composable filters.

## Installation

'npm install html-to-json'

## htmlToJson.parse(html, filter, [callback]) -> promise

The 'parse()' method takes a string of HTML, and a filter, and responds with the filtered data. This supports both callbacks and
 promises.

'''javascript
var promise = htmlToJson.parse('<div>content</div>', {
'text': function ($doc) {
  return $doc.find('div').text();
...
```

#### <a name="apidoc.element.html-to-json.request"></a>[function <span class="apidocSignatureSpan">html-to-json.</span>request (options, filter, callback)](#apidoc.element.html-to-json.request)
- description and source-code
```javascript
request = function (options, filter, callback) {
  var promise;

  promise = new Promise(function (resolve, reject) {
    request(options, function (err, response) {
      if (err) {
        return reject(err);
      }

      resolve(response);
    });
  });

  promise = promise.then(function (response) {
    return parse(response.body, filter);
  });

  return callbackify(promise, callback);
}
```
- example usage
```shell
...
});

promise.done(function (result) {
//Works as well
});
'''

## htmlToJson.request(requestOptions, filter, [callback]) -> promise

The 'request()' method takes options for a call to the [request](https://github.com/request/request) library and a filter, then
returns the filtered response body.

'''javascript
var promise = htmlToJson.request('http://prolificinteractive.com/team', {
'images': ['img', function ($img) {
  return $img.attr('src');
...
```



# <a name="apidoc.module.html-to-json.ParseContext"></a>[module html-to-json.ParseContext](#apidoc.module.html-to-json.ParseContext)

#### <a name="apidoc.element.html-to-json.ParseContext.ParseContext"></a>[function <span class="apidocSignatureSpan">html-to-json.</span>ParseContext (options)](#apidoc.element.html-to-json.ParseContext.ParseContext)
- description and source-code
```javascript
function ParseContext(options) {
  var context = this;

  _.defaults(this, options, {
    $container: null,
    $: null,
    filter: {},
    parent: null
  });

  this.promises = Object.create(this.parent? this.parent.promises: {});
}
```
- example usage
```shell
n/a
```



# <a name="apidoc.module.html-to-json.ParseContext.prototype"></a>[module html-to-json.ParseContext.prototype](#apidoc.module.html-to-json.ParseContext.prototype)

#### <a name="apidoc.element.html-to-json.ParseContext.prototype._filterWithArray"></a>[function <span class="apidocSignatureSpan">html-to-json.ParseContext.prototype.</span>_filterWithArray ()](#apidoc.element.html-to-json.ParseContext.prototype._filterWithArray)
- description and source-code
```javascript
_filterWithArray = function () {
  var selector = this.filter[0];
  var eachFilter = this.filter[1];
  var afterFilter = this.filter[2];
  var result = this.map(selector, eachFilter);

  if (afterFilter) {
    return result.then(afterFilter);
  }

  return result;
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.html-to-json.ParseContext.prototype._filterWithConstant"></a>[function <span class="apidocSignatureSpan">html-to-json.ParseContext.prototype.</span>_filterWithConstant ()](#apidoc.element.html-to-json.ParseContext.prototype._filterWithConstant)
- description and source-code
```javascript
_filterWithConstant = function () {
  return Promise.resolve(this.filter);
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.html-to-json.ParseContext.prototype._filterWithFunction"></a>[function <span class="apidocSignatureSpan">html-to-json.ParseContext.prototype.</span>_filterWithFunction ()](#apidoc.element.html-to-json.ParseContext.prototype._filterWithFunction)
- description and source-code
```javascript
_filterWithFunction = function () {
  return Promise.resolve(this.filter.call(this, this.$container, this.$));
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.html-to-json.ParseContext.prototype._filterWithObject"></a>[function <span class="apidocSignatureSpan">html-to-json.ParseContext.prototype.</span>_filterWithObject ()](#apidoc.element.html-to-json.ParseContext.prototype._filterWithObject)
- description and source-code
```javascript
_filterWithObject = function () {
  var _this;
  var filter = this.filter;
  var parent = this.parent;
  var $ = this.$;
  var $container = this.$container;
  var promises = this.promises;
  var propertyMap = {};

  if (filter.$container) {
    $container = this.$(filter.$container);
    delete filter.$container;
  }

  _.each(filter, function (subfilter, key) {
    var subcontext = new ParseContext({
      $container: $container,
      $: $,
      filter: subfilter,
      parent: this
    });

    promises['key:' + key] = propertyMap[key] = new Promise(function (resolve, reject) {
      process.nextTick(function () {
        subcontext.parse().done(resolve, reject);
      });
    });
  }, this);

  return Promise.props(propertyMap);
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.html-to-json.ParseContext.prototype.get"></a>[function <span class="apidocSignatureSpan">html-to-json.ParseContext.prototype.</span>get (key)](#apidoc.element.html-to-json.ParseContext.prototype.get)
- description and source-code
```javascript
get = function (key) {
  return Promise.resolve(this.promises['key:' + key]);
}
```
- example usage
```shell
...
    },
    'image': function ($product) {
      return $product.find('img').attr('src');
    },
    'colors': function ($product) {
      // This is where we use a promise to get the colors asynchronously
      return this
        .get('id')
        .then(function (id) {
          return getProductDetails(id).get('colors');
        });
    }
  }], callback);
}
'''
...
```

#### <a name="apidoc.element.html-to-json.ParseContext.prototype.map"></a>[function <span class="apidocSignatureSpan">html-to-json.ParseContext.prototype.</span>map (selector, filter)](#apidoc.element.html-to-json.ParseContext.prototype.map)
- description and source-code
```javascript
map = function (selector, filter) {
  var _this = this;
  var $ = this.$;
  var $els = this.$container.find(selector);

  var promises = _.map($els, function (el) {
    var subcontext = new ParseContext({
      $container: $(el),
      $: $,
      filter: filter,
      parent: this
    });

    return subcontext.parse();
  }, this);

  return Promise.all(promises);
}
```
- example usage
```shell
...
    return $doc.find('#foo').text(); //foo
  }
}, callback);
'''

### Arrays

Arrays of data can be parsed out by either using the .map() method within a filter function or using the shorthand [selector, filter
] syntax:

#### .map(selector, filter)

A filter is applied incrementally against each matched element, and the results are returned within an array.

'''javascript
var html = '<div id="items"><div class="item">1</div><div class="item">2</div></div>';
...
```

#### <a name="apidoc.element.html-to-json.ParseContext.prototype.parse"></a>[function <span class="apidocSignatureSpan">html-to-json.ParseContext.prototype.</span>parse (callback)](#apidoc.element.html-to-json.ParseContext.prototype.parse)
- description and source-code
```javascript
parse = function (callback) {
  var promise;

  _.every(['Function', 'Array', 'Object'], function (type) {
    if (_['is' + type](this.filter)) {
      promise = this['_filterWith' + type]();
      return false;
    }

    return true;
  }, this);

  if (!promise) {
    promise = this._filterWithConstant();
  }

  return callbackify(promise, callback);
}
```
- example usage
```shell
...

Parses HTML strings into objects using flexible, composable filters.

## Installation

'npm install html-to-json'

## htmlToJson.parse(html, filter, [callback]) -> promise

The 'parse()' method takes a string of HTML, and a filter, and responds with the filtered data. This supports both callbacks and
 promises.

'''javascript
var promise = htmlToJson.parse('<div>content</div>', {
'text': function ($doc) {
  return $doc.find('div').text();
...
```



# <a name="apidoc.module.html-to-json.Parser"></a>[module html-to-json.Parser](#apidoc.module.html-to-json.Parser)

#### <a name="apidoc.element.html-to-json.Parser.Parser"></a>[function <span class="apidocSignatureSpan">html-to-json.</span>Parser (filter)](#apidoc.element.html-to-json.Parser.Parser)
- description and source-code
```javascript
function Parser(filter) {
  this.filter = filter;
}
```
- example usage
```shell
...
var parseFoo = htmlToJson.createMethod({
'foo': function ($doc) {
  return $doc.find('#foo').bar();
}
});
'''

## htmlToJson.createParser(filter), new htmlToJson.Parser(filter)

For the sake of reusability, creates an object with '.parse' and '.request' helper methods, which use the passed filter. For example
:

'''javascript
var linkParser = htmlToJson.createParser(['a[href]', {
'text': function ($a) {
  return $a.text();
...
```



# <a name="apidoc.module.html-to-json.Parser.prototype"></a>[module html-to-json.Parser.prototype](#apidoc.module.html-to-json.Parser.prototype)

#### <a name="apidoc.element.html-to-json.Parser.prototype.method"></a>[function <span class="apidocSignatureSpan">html-to-json.Parser.prototype.</span>method ()](#apidoc.element.html-to-json.Parser.prototype.method)
- description and source-code
```javascript
method = function () {
  var _this = this;

  return function (html, callback) {
    return _this.parse(html, callback);
  };
}
```
- example usage
```shell
...

The former allows you to easily reuse the filter (and make it testable), while that latter is a one-off.

### parser.parse(html, [callback])

Parses the passed html argument against the parser's filter.

### parser.method(html, [callback])

Returns a method that wraps 'parser.parse()'

### parser.request(requestOptions, [callback])

Makes a request with the request options, then runs the response body through the parser's filter.
...
```

#### <a name="apidoc.element.html-to-json.Parser.prototype.parse"></a>[function <span class="apidocSignatureSpan">html-to-json.Parser.prototype.</span>parse (html, callback)](#apidoc.element.html-to-json.Parser.prototype.parse)
- description and source-code
```javascript
parse = function (html, callback) {
  return methods.parse(html, this.filter, callback);
}
```
- example usage
```shell
...

Parses HTML strings into objects using flexible, composable filters.

## Installation

'npm install html-to-json'

## htmlToJson.parse(html, filter, [callback]) -> promise

The 'parse()' method takes a string of HTML, and a filter, and responds with the filtered data. This supports both callbacks and
 promises.

'''javascript
var promise = htmlToJson.parse('<div>content</div>', {
'text': function ($doc) {
  return $doc.find('div').text();
...
```

#### <a name="apidoc.element.html-to-json.Parser.prototype.request"></a>[function <span class="apidocSignatureSpan">html-to-json.Parser.prototype.</span>request (options, callback)](#apidoc.element.html-to-json.Parser.prototype.request)
- description and source-code
```javascript
request = function (options, callback) {
  return methods.request(options, this.filter, callback);
}
```
- example usage
```shell
...
});

promise.done(function (result) {
//Works as well
});
'''

## htmlToJson.request(requestOptions, filter, [callback]) -> promise

The 'request()' method takes options for a call to the [request](https://github.com/request/request) library and a filter, then
returns the filtered response body.

'''javascript
var promise = htmlToJson.request('http://prolificinteractive.com/team', {
'images': ['img', function ($img) {
  return $img.attr('src');
...
```



# misc
- this document was created with [utility2](https://github.com/kaizhu256/node-utility2)
