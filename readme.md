# sort-ids [![unstable](https://img.shields.io/badge/stability-unstable-green.svg)](http://github.com/badges/stability-badges) [![Build Status](https://travis-ci.org/dy/sort-ids.svg?branch=master)](https://travis-ci.org/dy/sort-ids)

Sort input array, but return sorted ids of the initial array numbers, keeping the initial array unchanged.

Useful to make linked sorting of multiple arrays, where the second (n-th) array should be sorted the same way as the first one.

This package is ~ 6 times faster compared to sorting function.

[![npm install sort-ids](https://nodei.co/npm/sort-ids.png?mini=true)](https://npmjs.org/package/sort-ids/)

```js
var sort = require('sort-ids')
var reorder = require('array-rearrange')

var rates = [.12, .47, .52, .97, ...sourceNumbers]
var names = ['John', 'Alexa', 'Jimmy', 'Kate', ...linkedArray]

var ids = sortIds(rates)

var sortedRates = reorder(a, ids)
var sortedNames = reorder(b, ids)
```

See also [array-rearrange](https://ghub.io/array-rearrange) for reordering input array based on a list of ids.

## Acknowledgement

The idea was proposed by [Robert Monfera](https://github.com/monfera) for [snap-points-2d](https://ghub.io/snap-points-2d), which was eventually implemented. But turned out there are the other applications, like sorting colors etc.

## License

(c) 2018 Dmitry Yv. MIT License
