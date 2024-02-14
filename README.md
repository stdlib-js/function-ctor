<!--

@license Apache-2.0

Copyright (c) 2022 The Stdlib Authors.

Licensed under the Apache License, Version 2.0 (the "License");
you may not use this file except in compliance with the License.
You may obtain a copy of the License at

   http://www.apache.org/licenses/LICENSE-2.0

Unless required by applicable law or agreed to in writing, software
distributed under the License is distributed on an "AS IS" BASIS,
WITHOUT WARRANTIES OR CONDITIONS OF ANY KIND, either express or implied.
See the License for the specific language governing permissions and
limitations under the License.

-->


<details>
  <summary>
    About stdlib...
  </summary>
  <p>We believe in a future in which the web is a preferred environment for numerical computation. To help realize this future, we've built stdlib. stdlib is a standard library, with an emphasis on numerical and scientific computation, written in JavaScript (and C) for execution in browsers and in Node.js.</p>
  <p>The library is fully decomposable, being architected in such a way that you can swap out and mix and match APIs and functionality to cater to your exact preferences and use cases.</p>
  <p>When you use stdlib, you can be absolutely certain that you are using the most thorough, rigorous, well-written, studied, documented, tested, measured, and high-quality code out there.</p>
  <p>To join us in bringing numerical computing to the web, get started by checking us out on <a href="https://github.com/stdlib-js/stdlib">GitHub</a>, and please consider <a href="https://opencollective.com/stdlib">financially supporting stdlib</a>. We greatly appreciate your continued support!</p>
</details>

# Function

[![NPM version][npm-image]][npm-url] [![Build Status][test-image]][test-url] [![Coverage Status][coverage-image]][coverage-url] <!-- [![dependencies][dependencies-image]][dependencies-url] -->

> [Function][mdn-function] constructor.

<!-- Section to include introductory text. Make sure to keep an empty line after the intro `section` element and another before the `/section` close. -->

<section class="intro">

</section>

<!-- /.intro -->

<!-- Package usage documentation. -->



<section class="usage">

## Usage

To use in Observable,

```javascript
Function = require( 'https://cdn.jsdelivr.net/gh/stdlib-js/function-ctor@v0.2.0-umd/browser.js' )
```

To vendor stdlib functionality and avoid installing dependency trees for Node.js, you can use the UMD server build:

```javascript
var Function = require( 'path/to/vendor/umd/function-ctor/index.js' )
```

To include the bundle in a webpage,

```html
<script type="text/javascript" src="https://cdn.jsdelivr.net/gh/stdlib-js/function-ctor@v0.2.0-umd/browser.js"></script>
```

If no recognized module system is present, access bundle contents via the global scope:

```html
<script type="text/javascript">
(function () {
    window.Function;
})();
</script>
```

#### Function( \[...argNames,] body )

Returns a new [function][mdn-function] object.

```javascript
var greet = new Function( 'name', 'return "Hello, "+name+"!"' );

var v = greet( 'Jane' );
// returns 'Hello, Jane!'
```

Argument names must be strings corresponding to valid JavaScript parameters (i.e., a plain identifier, or, in environments supporting such parameters, a rest parameter or destructured parameter, optionally with a default).

* * *

### Properties

<a name="prop-length"></a>

#### Function.prototype.length

A number representing the number of arguments expected by the function.

```javascript
var greet = new Function( 'name', 'return "Hello, "+name+"!"' );
var v = greet.length;
// returns 1
```

<a name="prop-name"></a>

#### Function.prototype.name

**Read-only** property representing the name of the function.

```javascript
function greet( name ) {
    return 'Hello, '+name+'!';
}
var v = greet.name;
// returns 'greet'

// Functions created with the Function constructor are anonymous:
var fcn = new Function( 'name', 'return "Hello, "+name+"!"' );
v = fcn.name;
// returns 'anonymous'
```

<a name="prop-prototype"></a>

#### Function.prototype.prototype

**Read-only** property representing the prototype of the function.

```javascript
function greet( name ) {
    return 'Hello, '+name+'!';
}
var proto = greet.prototype;
// returns {}
```

* * *

### Methods

<a name="method-apply"></a>

#### Function.prototype.apply( thisArg, args )

Calls the specified function with the given `this` argument and arguments provided as an array-like object.

<!-- eslint-disable no-invalid-this -->

```javascript
function add( x, y ) {
    return this.initial + x + y;
}

var ctx = {
    'initial': 10
};

var v = add.apply( ctx, [ 1, 2 ] );
// returns 13
```

<a name="method-bind"></a>

#### Function.prototype.bind( thisArg\[, arg1\[, arg2\[, ...]]] )

Returns a new function which invokes the original function with the given `this` value and arguments.

```javascript
function add( x, y ) {
    return x + y;
}
var add1 = add.bind( null, 1 );

var v = add1( 2 );
// returns 3
```

<a name="method-call"></a>

#### Function.prototype.call( thisArg\[, arg1\[, arg2\[, ...]]] )

Calls the specified function with the given `this` value and arguments.

<!-- eslint-disable no-invalid-this -->

```javascript
function add( x, y ) {
    return this.initial + x + y;
}

var ctx = {
    'initial': 10
};

var v = add.call( ctx, 1, 2 );
// returns 13
```

<a name="method-to-string"></a>

#### Function.prototype.toString()

Returns a string representing the function.

```javascript
function add( x, y ) {
    return x + y;
}
var v = add.toString();
// e.g., returns 'function add( x, y ) {\n    return x + y;\n}'
```

</section>

<!-- /.usage -->

<!-- Package usage notes. Make sure to keep an empty line after the `section` element and another before the `/section` close. -->

<section class="notes">

## Notes

-   In pre-ES2015 environments, only plain identifiers (without defaults) are valid JavaScript parameters.
-   Creating `Function` objects with the `Function` constructor is less efficient than declaring a function via a function expression or a function statement.
-   The `Function` constructor can be invoked without the `new` operator (using `new` and not using `new` both return a new `Function` object).
-   The `Function` constructor creates functions which execute in the **global scope**. Hence, created functions **cannot** access variables local to the scope in which functions were created.  

</section>

<!-- /.notes -->

<!-- Package usage examples. -->

<section class="examples">

## Examples

<!-- eslint no-undef: "error" -->

```html
<!DOCTYPE html>
<html lang="en">
<body>
<script type="text/javascript" src="https://cdn.jsdelivr.net/gh/stdlib-js/function-ctor@v0.2.0-umd/browser.js"></script>
<script type="text/javascript">
(function () {

var add = new Function( 'x', 'y', 'return x + y' );

var v = add( 1, 2 );
// returns 3

})();
</script>
</body>
</html>
```

</section>

<!-- /.examples -->

<!-- Section to include cited references. If references are included, add a horizontal rule *before* the section. Make sure to keep an empty line after the `section` element and another before the `/section` close. -->

<section class="references">

</section>

<!-- /.references -->

<!-- Section for related `stdlib` packages. Do not manually edit this section, as it is automatically populated. -->

<section class="related">

</section>

<!-- /.related -->

<!-- Section for all links. Make sure to keep an empty line after the `section` element and another before the `/section` close. -->


<section class="main-repo" >

* * *

## Notice

This package is part of [stdlib][stdlib], a standard library for JavaScript and Node.js, with an emphasis on numerical and scientific computing. The library provides a collection of robust, high performance libraries for mathematics, statistics, streams, utilities, and more.

For more information on the project, filing bug reports and feature requests, and guidance on how to develop [stdlib][stdlib], see the main project [repository][stdlib].

#### Community

[![Chat][chat-image]][chat-url]

---

## License

See [LICENSE][stdlib-license].


## Copyright

Copyright &copy; 2016-2024. The Stdlib [Authors][stdlib-authors].

</section>

<!-- /.stdlib -->

<!-- Section for all links. Make sure to keep an empty line after the `section` element and another before the `/section` close. -->

<section class="links">

[npm-image]: http://img.shields.io/npm/v/@stdlib/function-ctor.svg
[npm-url]: https://npmjs.org/package/@stdlib/function-ctor

[test-image]: https://github.com/stdlib-js/function-ctor/actions/workflows/test.yml/badge.svg?branch=v0.2.0
[test-url]: https://github.com/stdlib-js/function-ctor/actions/workflows/test.yml?query=branch:v0.2.0

[coverage-image]: https://img.shields.io/codecov/c/github/stdlib-js/function-ctor/main.svg
[coverage-url]: https://codecov.io/github/stdlib-js/function-ctor?branch=main

<!--

[dependencies-image]: https://img.shields.io/david/stdlib-js/function-ctor.svg
[dependencies-url]: https://david-dm.org/stdlib-js/function-ctor/main

-->

[chat-image]: https://img.shields.io/gitter/room/stdlib-js/stdlib.svg
[chat-url]: https://app.gitter.im/#/room/#stdlib-js_stdlib:gitter.im

[stdlib]: https://github.com/stdlib-js/stdlib

[stdlib-authors]: https://github.com/stdlib-js/stdlib/graphs/contributors

[umd]: https://github.com/umdjs/umd
[es-module]: https://developer.mozilla.org/en-US/docs/Web/JavaScript/Guide/Modules

[deno-url]: https://github.com/stdlib-js/function-ctor/tree/deno
[deno-readme]: https://github.com/stdlib-js/function-ctor/blob/deno/README.md
[umd-url]: https://github.com/stdlib-js/function-ctor/tree/umd
[umd-readme]: https://github.com/stdlib-js/function-ctor/blob/umd/README.md
[esm-url]: https://github.com/stdlib-js/function-ctor/tree/esm
[esm-readme]: https://github.com/stdlib-js/function-ctor/blob/esm/README.md
[branches-url]: https://github.com/stdlib-js/function-ctor/blob/main/branches.md

[stdlib-license]: https://raw.githubusercontent.com/stdlib-js/function-ctor/main/LICENSE

[mdn-function]: https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Function

</section>

<!-- /.links -->
