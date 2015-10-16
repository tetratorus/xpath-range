# XPath Range [![Coverage Status](https://coveralls.io/repos/openannotation/xpath-range/badge.svg?branch=master&service=github)](https://coveralls.io/github/openannotation/xpath-range?branch=master)
[![Sauce Test Status](https://saucelabs.com/browser-matrix/xpath-range.svg)](https://saucelabs.com/u/xpath-range)

This module is for describing and resolving a DOM `Range` using XPath.

## Installation

Use `npm install xpath-range`.

## Usage

### `XPathRange.fromRange(range, [root])`

Convert a `Range` to a pair of XPath expressions and offsets.

If the optional parameter `root` is supplied, the computed XPath expressions
will be relative to it.

Returns an object with the following properties:

  - start
  - startOffset
  - end
  - endOffset

### `XPathRange.toRange(root, startPath, startOffset, endPath, endOffset)`

Construct a `Range` from the given XPath expressions and offsets.

If the optional parameter `root` is supplied, the XPath expressions are
evaluated as relative to it.

Returns a `Range` object.

## Compatibility

This library should work with any browser implementing basic `Range` support.

### Internet Explorer version 8

- Basic support can be achieved with the [rangy][rangy] shim.
- There is no support for namespaces in X(HT)ML documents (issue #17).

## Community

Originally, this code was part of the
[Annotator](http://annotatorjs.org/) project.

Any discussion should happen on the
[annotator-dev](https://lists.okfn.org/mailman/listinfo/annotator-dev) mailing
list.

## Development

To contribute, fork this repository and send a pull request with your changes,
including any necessary test and documentation updates.

## Testing

You can run the command-line test suite by executing `npm test`.

To run the test suite in a browser, install the karma test runner

    npm install -g karma-cli

and then run `karma start` and it will print directions for debugging.

[rangy] https://github.com/timdown/rangy
