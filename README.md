**NOTICE**: If you're reading this on GitHub.com please be aware this is a mirror of the primary remote located at https://code.richard.do/explore/projects.
Please direct issues and pull requests there.

# persistent-dict

[![PyPI](https://img.shields.io/pypi/v/persistent-dict.svg)](https://pypi.python.org/pypi/persistent-dict)
[![Python Versions](https://img.shields.io/pypi/pyversions/persistent-dict.svg)](https://pypi.python.org/pypi/persistent-dict)
[![Build Status](https://travis-ci.org/richardasaurus/persistent-dict.png?branch=master)](https://travis-ci.org/richardasaurus/persistent-dict)

A Python Dict which stores data in Redis.

You can use ``RedisDict`` exactly like a normal ``dict``. As long as all the keys and values in it are [picklable](https://docs.python.org/3/library/pickle.html).

## Installation

To install, simply:

```bash
pip install persistent-dict
```

## How to use

```python
import redis
from persistentdict import RedisDict

mydict = RedisDict(persistence=redis.StrictRedis())

# with a specific storage key in redis
mydict = RedisDict(persistence=redis.StrictRedis(), key='stuff')

mydict['hello'] = 'world'

print(mydict)
{'hello': 'world'}
```

## Future plans

- Support for other storage backends other than Redis.
