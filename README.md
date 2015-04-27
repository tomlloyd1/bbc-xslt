A variant of the package [node-libxslt](https://github.com/albanm/node-libxslt) that works with Node version 0.12.2.

The compatible version of libxmljs can used with it like so: 

```js
var libxmljs = require('bbc-xslt').libxmljs;
```

bbc-xslt
============

[![Build status](https://travis-ci.org/albanm/node-libxslt.svg)](https://travis-ci.org/albanm/node-libxslt)
[![Code Climate](https://codeclimate.com/github/albanm/node-libxslt/badges/gpa.svg)](https://codeclimate.com/github/albanm/node-libxslt)
[![NPM version](https://badge.fury.io/js/libxslt.svg)](http://badge.fury.io/js/libxslt)

Node.js bindings for [libxslt](http://xmlsoft.org/libxslt/) compatible with [libxmljs](https://github.com/polotek/libxmljs/issues/226).

Installation
------------
```
npm install bbc-xslt
```

Basic usage
-----------

```js
var bbc-xslt = require('bbc-xslt');

bbc-xslt.parse(stylesheetString, function(err, stylesheet){
  var params = {
    MyParam: 'my value'
  };

  // 'params' parameter is optional
  stylesheet.apply(documentString, params, function(err, result){
    // err contains any error from parsing the document or applying the stylesheet
    // result is a string containing the result of the transformation
  });  
});
```

