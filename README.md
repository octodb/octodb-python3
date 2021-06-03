LiteSync for Python3
====================

This library takes [pysqlite3](https://github.com/coleifer/pysqlite3) and makes
some small modifications so it is suitable for use with
[LiteSync](http://litesync.io).

Additional features:

* User-defined window functions (requires SQLite >= 3.25)
* Flags and VFS an be specified when opening connection
* Incremental BLOB I/O, [bpo-24905](https://github.com/python/cpython/pull/271)
* Improved error messages, [bpo-16379](https://github.com/python/cpython/pull/1108)
* Simplified detection of DML statements via `sqlite3_stmt_readonly`.
* Sqlite native backup API (also present in standard library 3.7 and newer).

Building with pre-installed LiteSync
------------------------------------

To build `litesync` linked against the pre-installed library, run:

```
$ python setup.py build
```
