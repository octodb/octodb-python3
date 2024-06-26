OctoDB for Python3
==================

This is a wrapper library to use [OctoDB](http://octodb.io) on Python 3

It is based on [pysqlite3](https://github.com/coleifer/pysqlite3)


Installation
------------

### 1. Install the Native Library

You must install the native OctoDB library for this wrapper to work.
It can be either pre-compiled binaries or you can compile it by yourself.
You can start with the [free version](http://octodb.io/en/download.html)

### 2. Install the Wrapper

#### With pip

```
pip install octodb
```

#### Cloning and Building

Optionally you can clone the repo and build it:

```
git clone --depth=1 https://gitlab.com/octodb/octodb-python3
cd octodb-python3
python3 setup.py build install
```


Usage
-----

```python
import octodb
import time

conn = octodb.connect('file:app.db?node=secondary&connect=tcp://server:port')

# check if the db is ready
while not conn.is_ready():
    time.sleep(0.250)

# now we can use the db connection
...
```
