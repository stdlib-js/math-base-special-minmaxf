<!--

@license Apache-2.0

Copyright (c) 2025 The Stdlib Authors.

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

# minmaxf

[![NPM version][npm-image]][npm-url] [![Build Status][test-image]][test-url] [![Coverage Status][coverage-image]][coverage-url] <!-- [![dependencies][dependencies-image]][dependencies-url] -->

> Return the minimum and maximum of two single-precision floating-point numbers.

<!-- Section to include introductory text. Make sure to keep an empty line after the intro `section` element and another before the `/section` close. -->

<section class="intro">

</section>

<!-- /.intro -->

<!-- Package usage documentation. -->



<section class="usage">

## Usage

```javascript
import minmaxf from 'https://cdn.jsdelivr.net/gh/stdlib-js/math-base-special-minmaxf@esm/index.mjs';
```

You can also import the following named exports from the package:

```javascript
import { assign } from 'https://cdn.jsdelivr.net/gh/stdlib-js/math-base-special-minmaxf@esm/index.mjs';
```

#### minmaxf( x, y )

Returns the minimum and maximum of two single-precision floating-point numbers in a single pass.

```javascript
var v = minmaxf( 4.2, 3.14 );
// returns [ 3.14, 4.2 ]

v = minmaxf( +0.0, -0.0 );
// returns [ -0.0, +0.0 ]
```

If any argument is `NaN`, the function returns `NaN` for both the minimum value and the maximum value.

```javascript
var v = minmaxf( 4.2, NaN );
// returns [ NaN, NaN ]

v = minmaxf( NaN, 3.14 );
// returns [ NaN, NaN ]
```

#### minmaxf.assign( x, y, out, stride, offset )

Returns the minimum and maximum of two single-precision floating-point numbers in a single pass and assigns results to a provided output array.

```javascript
import Float32Array from 'https://cdn.jsdelivr.net/gh/stdlib-js/array-float32@esm/index.mjs';

var out = new Float32Array( 2 );

var v = minmaxf.assign( 5.0, -2.0, out, 1, 0 );
// returns <Float32Array>[ -2.0, 5.0 ]

var bool = ( v === out );
// returns true
```

</section>

<!-- /.usage -->

<!-- Package usage notes. Make sure to keep an empty line after the `section` element and another before the `/section` close. -->

<section class="notes">

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
<script type="module">

import logEachMap from 'https://cdn.jsdelivr.net/gh/stdlib-js/console-log-each-map@esm/index.mjs';
import discreteUniform from 'https://cdn.jsdelivr.net/gh/stdlib-js/random-array-discrete-uniform@esm/index.mjs';
import minmaxf from 'https://cdn.jsdelivr.net/gh/stdlib-js/math-base-special-minmaxf@esm/index.mjs';

var opts = {
    'dtype': 'float32'
};
var x = discreteUniform( 100, -100, 100, opts );
var y = discreteUniform( 100, -100, 100, opts );

logEachMap( 'minmaxf(%d, %d) = [%s]', x, y, minmaxf );

</script>
</body>
</html>
```

</section>

<!-- /.examples -->

<!-- C interface documentation. -->



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

Copyright &copy; 2016-2026. The Stdlib [Authors][stdlib-authors].

</section>

<!-- /.stdlib -->

<!-- Section for all links. Make sure to keep an empty line after the `section` element and another before the `/section` close. -->

<section class="links">

[npm-image]: http://img.shields.io/npm/v/@stdlib/math-base-special-minmaxf.svg
[npm-url]: https://npmjs.org/package/@stdlib/math-base-special-minmaxf

[test-image]: https://github.com/stdlib-js/math-base-special-minmaxf/actions/workflows/test.yml/badge.svg?branch=v0.1.1
[test-url]: https://github.com/stdlib-js/math-base-special-minmaxf/actions/workflows/test.yml?query=branch:v0.1.1

[coverage-image]: https://img.shields.io/codecov/c/github/stdlib-js/math-base-special-minmaxf/main.svg
[coverage-url]: https://codecov.io/github/stdlib-js/math-base-special-minmaxf?branch=main

<!--

[dependencies-image]: https://img.shields.io/david/stdlib-js/math-base-special-minmaxf.svg
[dependencies-url]: https://david-dm.org/stdlib-js/math-base-special-minmaxf/main

-->

[chat-image]: https://img.shields.io/badge/zulip-join_chat-brightgreen.svg
[chat-url]: https://stdlib.zulipchat.com

[stdlib]: https://github.com/stdlib-js/stdlib

[stdlib-authors]: https://github.com/stdlib-js/stdlib/graphs/contributors

[umd]: https://github.com/umdjs/umd
[es-module]: https://developer.mozilla.org/en-US/docs/Web/JavaScript/Guide/Modules

[deno-url]: https://github.com/stdlib-js/math-base-special-minmaxf/tree/deno
[deno-readme]: https://github.com/stdlib-js/math-base-special-minmaxf/blob/deno/README.md
[umd-url]: https://github.com/stdlib-js/math-base-special-minmaxf/tree/umd
[umd-readme]: https://github.com/stdlib-js/math-base-special-minmaxf/blob/umd/README.md
[esm-url]: https://github.com/stdlib-js/math-base-special-minmaxf/tree/esm
[esm-readme]: https://github.com/stdlib-js/math-base-special-minmaxf/blob/esm/README.md
[branches-url]: https://github.com/stdlib-js/math-base-special-minmaxf/blob/main/branches.md

[stdlib-license]: https://raw.githubusercontent.com/stdlib-js/math-base-special-minmaxf/main/LICENSE

<!-- <related-links> -->

<!-- </related-links> -->

</section>

<!-- /.links -->
