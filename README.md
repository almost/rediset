# rediset

**Composable, cachable, lazy trees of Redis set operations**

**Author:** Jamie Matthews. [Follow me on Twitter](http://twitter.com/j4mie).

## Documentation

Full documentation is available at [http://j4mie.github.com/rediset](http://j4mie.github.com/rediset).

## Changelog

#### 0.12.0

* Split huge rediset.py file into a package

#### 0.11.0

* Fix broken SortedSet slicing behaviour and broken tests.

#### 0.10.0

* Range views now support more operations, eg len(), proxied through to their parent SortedSet

#### 0.9.0

* Rename "reversed" range view to "descending"

#### 0.8.0

* Add support for range views on sorted sets; ss.reversed and ss.withscores

#### 0.7.0

* Correct argument ordering bug in SETEX call.

#### 0.6.0

* All keys that are automatically generated by Rediset (to store the results
  of operations, etc) are now prefixed to distinguish them from user data.
* Rediset can now (optionally) MD5 hash all of the keys it generates.

#### 0.5.0

* Refactoring to remove internal Redis wrapper class
* Add support for zremrangebyrank and zremrangebyscore to sorted sets

#### 0.4.0

* Rework documentation, now at http://j4mie.github.com/rediset
* Add initial support for sorted sets

#### 0.3.0

* Ensure empty sets are cached correctly

#### 0.2.0

* Add support for operation between sets, eg `s1.intersection(s2)`

#### 0.1.0

* Initial release. Very experimental.

## Installation

You can install Rediset from PyPI:

    pip install rediset

## Overview

Rediset is an abstraction of Redis sets and set operations.

## Requirements

 - Python 2.7.X
 - Redis 2.4.X or later
 - Python modules as specified in requirements.txt

## Development

To contribute: fork the repository, make your changes, add some tests, commit,
push to a feature branch, and open a pull request.

### How to run the tests

Rediset is tested with [nose](http://nose.readthedocs.org). Clone the repository,
create a virtualenv (with Python 2.7), then run `pip install -r requirements.txt`. Then, simply type
`nosetests` to find and run all the tests. A Redis Server version 2.4.0 or later must be running for the tests.

## (Un)license

This is free and unencumbered software released into the public domain.

Anyone is free to copy, modify, publish, use, compile, sell, or distribute this
software, either in source code form or as a compiled binary, for any purpose,
commercial or non-commercial, and by any means.

In jurisdictions that recognize copyright laws, the author or authors of this
software dedicate any and all copyright interest in the software to the public
domain. We make this dedication for the benefit of the public at large and to
the detriment of our heirs and successors. We intend this dedication to be an
overt act of relinquishment in perpetuity of all present and future rights to
this software under copyright law.

THE SOFTWARE IS PROVIDED "AS IS", WITHOUT WARRANTY OF ANY KIND, EXPRESS OR
IMPLIED, INCLUDING BUT NOT LIMITED TO THE WARRANTIES OF MERCHANTABILITY, FITNESS
FOR A PARTICULAR PURPOSE AND NONINFRINGEMENT. IN NO EVENT SHALL THE AUTHORS BE
LIABLE FOR ANY CLAIM, DAMAGES OR OTHER LIABILITY, WHETHER IN AN ACTION OF
CONTRACT, TORT OR OTHERWISE, ARISING FROM, OUT OF OR IN CONNECTION WITH THE
SOFTWARE OR THE USE OR OTHER DEALINGS IN THE SOFTWARE.

For more information, please refer to <http://unlicense.org/>
