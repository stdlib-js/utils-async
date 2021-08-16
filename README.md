<!--

@license Apache-2.0

Copyright (c) 2018 The Stdlib Authors.

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

# Async

[![NPM version][npm-image]][npm-url] [![Build Status][test-image]][test-url] [![Coverage Status][coverage-image]][coverage-url] [![dependencies][dependencies-image]][dependencies-url]

> Standard library async utilities.

<section class="installation">

## Installation

```bash
npm install @stdlib/utils-async
```

</section>

<section class="usage">

## Usage

```javascript
var ns = require( '@stdlib/utils-async' );
```

#### ns

Standard library async utilities.

```javascript
var o = ns;
// returns {...}
```

<!-- <toc pattern="*"> -->

<div class="namespace-toc">

-   <span class="signature">[`anyByRightAsync( collection, [options,] predicate, done )`][@stdlib/utils/async/any-by-right]</span><span class="delimiter">: </span><span class="description">test whether at least one element in a collection passes a test implemented by a predicate function, iterating from right to left.</span>
-   <span class="signature">[`anyByAsync( collection, [options,] predicate, done )`][@stdlib/utils/async/any-by]</span><span class="delimiter">: </span><span class="description">test whether at least one element in a collection passes a test implemented by a predicate function.</span>
-   <span class="signature">[`bifurcateByAsync( collection, [options,] predicate, done )`][@stdlib/utils/async/bifurcate-by]</span><span class="delimiter">: </span><span class="description">split values into two groups according to a predicate function.</span>
-   <span class="signature">[`composeAsync( ...fcn )`][@stdlib/utils/async/compose]</span><span class="delimiter">: </span><span class="description">function composition.</span>
-   <span class="signature">[`countByAsync( collection, [options,] indicator, done )`][@stdlib/utils/async/count-by]</span><span class="delimiter">: </span><span class="description">group values according to an indicator function and return group counts.</span>
-   <span class="signature">[`doUntilAsync( fcn, predicate, done[, thisArg ] )`][@stdlib/utils/async/do-until]</span><span class="delimiter">: </span><span class="description">invoke a function until a test condition is true.</span>
-   <span class="signature">[`doWhileAsync( fcn, predicate, done[, thisArg ] )`][@stdlib/utils/async/do-while]</span><span class="delimiter">: </span><span class="description">invoke a function while a test condition is true.</span>
-   <span class="signature">[`everyByRightAsync( collection, [options,] predicate, done )`][@stdlib/utils/async/every-by-right]</span><span class="delimiter">: </span><span class="description">test whether all elements in a collection pass a test implemented by a predicate function, iterating from right to left.</span>
-   <span class="signature">[`everyByAsync( collection, [options,] predicate, done )`][@stdlib/utils/async/every-by]</span><span class="delimiter">: </span><span class="description">test whether all elements in a collection pass a test implemented by a predicate function.</span>
-   <span class="signature">[`forEachRightAsync( collection, [options,] fcn, done )`][@stdlib/utils/async/for-each-right]</span><span class="delimiter">: </span><span class="description">invoke a function once for each element in a collection, iterating from right to left.</span>
-   <span class="signature">[`forEachAsync( collection, [options,] fcn, done )`][@stdlib/utils/async/for-each]</span><span class="delimiter">: </span><span class="description">invoke a function once for each element in a collection.</span>
-   <span class="signature">[`functionSequenceAsync( ...fcn )`][@stdlib/utils/async/function-sequence]</span><span class="delimiter">: </span><span class="description">function sequence.</span>
-   <span class="signature">[`groupByAsync( collection, [options,] indicator, done )`][@stdlib/utils/async/group-by]</span><span class="delimiter">: </span><span class="description">group values according to an indicator function.</span>
-   <span class="signature">[`ifelseAsync( predicate, x, y, done )`][@stdlib/utils/async/if-else]</span><span class="delimiter">: </span><span class="description">if a predicate function returns a truthy value, return `x`; otherwise, return `y`.</span>
-   <span class="signature">[`ifthenAsync( predicate, x, y, done )`][@stdlib/utils/async/if-then]</span><span class="delimiter">: </span><span class="description">if a predicate function returns a truthy value, invoke `x`; otherwise, invoke `y`.</span>
-   <span class="signature">[`inmapRightAsync( collection, [options,] fcn, done )`][@stdlib/utils/async/inmap-right]</span><span class="delimiter">: </span><span class="description">invoke a function for each element in a collection and update the collection in-place, iterating from right to left.</span>
-   <span class="signature">[`inmapAsync( collection, [options,] fcn, done )`][@stdlib/utils/async/inmap]</span><span class="delimiter">: </span><span class="description">invoke a function for each element in a collection and update the collection in-place.</span>
-   <span class="signature">[`mapFunAsync( fcn, n, [options,] done )`][@stdlib/utils/async/map-function]</span><span class="delimiter">: </span><span class="description">invoke a function `n` times and return an array of accumulated function return values.</span>
-   <span class="signature">[`mapKeysAsync( obj, [options,] transform, done )`][@stdlib/utils/async/map-keys]</span><span class="delimiter">: </span><span class="description">map keys from one object to a new object having the same values.</span>
-   <span class="signature">[`mapValuesAsync( obj, [options,] transform, done )`][@stdlib/utils/async/map-values]</span><span class="delimiter">: </span><span class="description">map values from one object to a new object having the same keys.</span>
-   <span class="signature">[`noneByRightAsync( collection, [options,] predicate, done )`][@stdlib/utils/async/none-by-right]</span><span class="delimiter">: </span><span class="description">test whether all elements in a collection fail a test implemented by a predicate function, iterating from right to left.</span>
-   <span class="signature">[`noneByAsync( collection, [options,] predicate, done )`][@stdlib/utils/async/none-by]</span><span class="delimiter">: </span><span class="description">test whether all elements in a collection fail a test implemented by a predicate function.</span>
-   <span class="signature">[`reduceRightAsync( collection, initial, [options,] reducer, done )`][@stdlib/utils/async/reduce-right]</span><span class="delimiter">: </span><span class="description">apply a function against an accumulator and each element in a collection and return the accumulated result, iterating from right to left.</span>
-   <span class="signature">[`reduceAsync( collection, initial, [options,] reducer, done )`][@stdlib/utils/async/reduce]</span><span class="delimiter">: </span><span class="description">apply a function against an accumulator and each element in a collection and return the accumulated result.</span>
-   <span class="signature">[`waterfall( fcns, clbk[, thisArg] )`][@stdlib/utils/async/series-waterfall]</span><span class="delimiter">: </span><span class="description">execute functions in series, passing the results of one function as arguments to the next function.</span>
-   <span class="signature">[`someByRightAsync( collection, n, [options,] predicate, done )`][@stdlib/utils/async/some-by-right]</span><span class="delimiter">: </span><span class="description">test whether a collection contains at least `n` elements which pass a test implemented by a predicate function, iterating from right to left.</span>
-   <span class="signature">[`someByAsync( collection, n, [options,] predicate, done )`][@stdlib/utils/async/some-by]</span><span class="delimiter">: </span><span class="description">test whether a collection contains at least `n` elements which pass a test implemented by a predicate function.</span>
-   <span class="signature">[`tabulateByAsync( collection, [options,] indicator, done )`][@stdlib/utils/async/tabulate-by]</span><span class="delimiter">: </span><span class="description">generate a frequency table according to an indicator function.</span>
-   <span class="signature">[`trycatchAsync( x, y, done )`][@stdlib/utils/async/try-catch]</span><span class="delimiter">: </span><span class="description">if a function does not return an error, invoke a callback with the function result; otherwise, invoke a callback with a value `y`.</span>
-   <span class="signature">[`trythenAsync( x, y, done )`][@stdlib/utils/async/try-then]</span><span class="delimiter">: </span><span class="description">if a function does not return an error, invoke a callback with the function result; otherwise, invoke a second function.</span>
-   <span class="signature">[`untilAsync( predicate, fcn, done[, thisArg ] )`][@stdlib/utils/async/until]</span><span class="delimiter">: </span><span class="description">invoke a function until a test condition is true.</span>
-   <span class="signature">[`whileAsync( predicate, fcn, done[, thisArg ] )`][@stdlib/utils/async/while]</span><span class="delimiter">: </span><span class="description">invoke a function while a test condition is true.</span>

</div>

<!-- </toc> -->

</section>

<!-- /.usage -->

<section class="examples">

## Examples

<!-- TODO: better examples -->

<!-- eslint no-undef: "error" -->

```javascript
var objectKeys = require( '@stdlib/utils-keys' );
var ns = require( '@stdlib/utils-async' );

console.log( objectKeys( ns ) );
```

</section>

<!-- /.examples -->


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

Copyright &copy; 2016-2021. The Stdlib [Authors][stdlib-authors].

</section>

<!-- /.stdlib -->

<!-- Section for all links. Make sure to keep an empty line after the `section` element and another before the `/section` close. -->

<section class="links">

[npm-image]: http://img.shields.io/npm/v/@stdlib/utils-async.svg
[npm-url]: https://npmjs.org/package/@stdlib/utils-async

[test-image]: https://github.com/stdlib-js/utils-async/actions/workflows/test.yml/badge.svg
[test-url]: https://github.com/stdlib-js/utils-async/actions/workflows/test.yml

[coverage-image]: https://img.shields.io/codecov/c/github/stdlib-js/utils-async/main.svg
[coverage-url]: https://codecov.io/github/stdlib-js/utils-async?branch=main

[dependencies-image]: https://img.shields.io/david/stdlib-js/utils-async.svg
[dependencies-url]: https://david-dm.org/stdlib-js/utils-async/main

[chat-image]: https://img.shields.io/gitter/room/stdlib-js/stdlib.svg
[chat-url]: https://gitter.im/stdlib-js/stdlib/

[stdlib]: https://github.com/stdlib-js/stdlib

[stdlib-authors]: https://github.com/stdlib-js/stdlib/graphs/contributors

[stdlib-license]: https://raw.githubusercontent.com/stdlib-js/utils-async/main/LICENSE

<!-- <toc-links> -->

[@stdlib/utils/async/any-by-right]: https://github.com/stdlib-js/utils-async-any-by-right

[@stdlib/utils/async/any-by]: https://github.com/stdlib-js/utils-async-any-by

[@stdlib/utils/async/bifurcate-by]: https://github.com/stdlib-js/utils-async-bifurcate-by

[@stdlib/utils/async/compose]: https://github.com/stdlib-js/utils-async-compose

[@stdlib/utils/async/count-by]: https://github.com/stdlib-js/utils-async-count-by

[@stdlib/utils/async/do-until]: https://github.com/stdlib-js/utils-async-do-until

[@stdlib/utils/async/do-while]: https://github.com/stdlib-js/utils-async-do-while

[@stdlib/utils/async/every-by-right]: https://github.com/stdlib-js/utils-async-every-by-right

[@stdlib/utils/async/every-by]: https://github.com/stdlib-js/utils-async-every-by

[@stdlib/utils/async/for-each-right]: https://github.com/stdlib-js/utils-async-for-each-right

[@stdlib/utils/async/for-each]: https://github.com/stdlib-js/utils-async-for-each

[@stdlib/utils/async/function-sequence]: https://github.com/stdlib-js/utils-async-function-sequence

[@stdlib/utils/async/group-by]: https://github.com/stdlib-js/utils-async-group-by

[@stdlib/utils/async/if-else]: https://github.com/stdlib-js/utils-async-if-else

[@stdlib/utils/async/if-then]: https://github.com/stdlib-js/utils-async-if-then

[@stdlib/utils/async/inmap-right]: https://github.com/stdlib-js/utils-async-inmap-right

[@stdlib/utils/async/inmap]: https://github.com/stdlib-js/utils-async-inmap

[@stdlib/utils/async/map-function]: https://github.com/stdlib-js/utils-async-map-function

[@stdlib/utils/async/map-keys]: https://github.com/stdlib-js/utils-async-map-keys

[@stdlib/utils/async/map-values]: https://github.com/stdlib-js/utils-async-map-values

[@stdlib/utils/async/none-by-right]: https://github.com/stdlib-js/utils-async-none-by-right

[@stdlib/utils/async/none-by]: https://github.com/stdlib-js/utils-async-none-by

[@stdlib/utils/async/reduce-right]: https://github.com/stdlib-js/utils-async-reduce-right

[@stdlib/utils/async/reduce]: https://github.com/stdlib-js/utils-async-reduce

[@stdlib/utils/async/series-waterfall]: https://github.com/stdlib-js/utils-async-series-waterfall

[@stdlib/utils/async/some-by-right]: https://github.com/stdlib-js/utils-async-some-by-right

[@stdlib/utils/async/some-by]: https://github.com/stdlib-js/utils-async-some-by

[@stdlib/utils/async/tabulate-by]: https://github.com/stdlib-js/utils-async-tabulate-by

[@stdlib/utils/async/try-catch]: https://github.com/stdlib-js/utils-async-try-catch

[@stdlib/utils/async/try-then]: https://github.com/stdlib-js/utils-async-try-then

[@stdlib/utils/async/until]: https://github.com/stdlib-js/utils-async-until

[@stdlib/utils/async/while]: https://github.com/stdlib-js/utils-async-while

<!-- </toc-links> -->

</section>

<!-- /.links -->
