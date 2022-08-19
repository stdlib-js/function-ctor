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

<!-- eslint-disable stdlib/no-redeclare -->

```javascript
import Function from 'https://cdn.jsdelivr.net/gh/stdlib-js/function-ctor@v0.0.1-esm/index.mjs';
```

#### Function( \[...argNames,] body )

Returns a new [function][mdn-function] object.

<!-- eslint-disable stdlib/no-redeclare -->

```javascript
var greet = new Function( 'name', 'return "Hello, "+name+"!"' );

var v = greet( 'Jane' );
// returns 'Hello, Jane!'
```

Argument names must be strings corresponding to valid JavaScript parameters (i.e., a plain identifier, or, in environments supporting such parameters, a rest parameter or destructured parameter, optionally with a default).

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

<!-- eslint-disable stdlib/no-redeclare -->

```html
<!DOCTYPE html>
<html lang="en">
<body>
<script type="module">

import Function from 'https://cdn.jsdelivr.net/gh/stdlib-js/function-ctor@v0.0.1-esm/index.mjs';

var add = new Function( 'x', 'y', 'return x + y' );

var v = add( 1, 2 );
// returns 3

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

This package is part of [stdlib][stdlib], a standard library with an emphasis on numerical and scientific computing. The library provides a collection of robust, high performance libraries for mathematics, statistics, streams, utilities, and more.

For more information on the project, filing bug reports and feature requests, and guidance on how to develop [stdlib][stdlib], see the main project [repository][stdlib].

#### Community

[![Chat][chat-image]][chat-url]

---

## License

See [LICENSE][stdlib-license].


## Copyright

Copyright &copy; 2016-2022. The Stdlib [Authors][stdlib-authors].

</section>

<!-- /.stdlib -->

<!-- Section for all links. Make sure to keep an empty line after the `section` element and another before the `/section` close. -->

<section class="links">

[npm-image]: http://img.shields.io/npm/v/@stdlib/function-ctor.svg
[npm-url]: https://npmjs.org/package/@stdlib/function-ctor

[test-image]: https://github.com/stdlib-js/function-ctor/actions/workflows/test.yml/badge.svg?branch=v0.0.1
[test-url]: https://github.com/stdlib-js/function-ctor/actions/workflows/test.yml?query=branch:v0.0.1

[coverage-image]: https://img.shields.io/codecov/c/github/stdlib-js/function-ctor/main.svg
[coverage-url]: https://codecov.io/github/stdlib-js/function-ctor?branch=main

<!--

[dependencies-image]: https://img.shields.io/david/stdlib-js/function-ctor.svg
[dependencies-url]: https://david-dm.org/stdlib-js/function-ctor/main

-->

[chat-image]: https://img.shields.io/gitter/room/stdlib-js/stdlib.svg
[chat-url]: https://gitter.im/stdlib-js/stdlib/

[stdlib]: https://github.com/stdlib-js/stdlib

[stdlib-authors]: https://github.com/stdlib-js/stdlib/graphs/contributors

[umd]: https://github.com/umdjs/umd
[es-module]: https://developer.mozilla.org/en-US/docs/Web/JavaScript/Guide/Modules

[deno-url]: https://github.com/stdlib-js/function-ctor/tree/deno
[umd-url]: https://github.com/stdlib-js/function-ctor/tree/umd
[esm-url]: https://github.com/stdlib-js/function-ctor/tree/esm
[branches-url]: https://github.com/stdlib-js/function-ctor/blob/main/branches.md

[stdlib-license]: https://raw.githubusercontent.com/stdlib-js/function-ctor/main/LICENSE

[mdn-function]: https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Function

</section>

<!-- /.links -->
