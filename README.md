# @f1stnpm2/magni-iure-dolore

Array quantifier assertions for [Chai](http://chaijs.com/) assertion library.

![main workflow](https://github.com/f1stnpm2/magni-iure-dolore/actions/workflows/main.yml/badge.svg)
[![Coverage Status](https://coveralls.io/repos/github/funny-bytes/@f1stnpm2/magni-iure-dolore/badge.svg?branch=master)](https://coveralls.io/github/funny-bytes/@f1stnpm2/magni-iure-dolore?branch=master)
[![Maintainability](https://api.codeclimate.com/v1/badges/44fb4c780c3f36b0d04f/maintainability)](https://codeclimate.com/github/funny-bytes/@f1stnpm2/magni-iure-dolore/maintainability)
[![node](https://img.shields.io/node/v/@f1stnpm2/magni-iure-dolore.svg)]()
[![code style](https://img.shields.io/badge/code_style-airbnb-brightgreen.svg)](https://github.com/airbnb/javascript)
[![Types](https://img.shields.io/npm/types/@f1stnpm2/magni-iure-dolore.svg)](https://www.npmjs.com/package/@f1stnpm2/magni-iure-dolore)
[![License Status](http://img.shields.io/npm/l/@f1stnpm2/magni-iure-dolore.svg)]()

## Install

```bash
npm install --save-dev chai @f1stnpm2/magni-iure-dolore
```

## Usage

There are three assertions available, applicable to arrays.

* containAll -- Asserts that all array items are true in respect to a predicate.
* containOne -- Asserts that at least one array item is true in respect to a predicate.
* containExactlyOne -- Asserts that exactly one array item is true in respect to a predicate.

A quick example:

```javascript
const chai = require('chai');
const chaiQuantifiers = require('@f1stnpm2/magni-iure-dolore');

chai.use(chaiQuantifiers);

const { expect } = chai;

describe('@f1stnpm2/magni-iure-dolore', () => {
  it('containAll should be true if all items are true', () => {
    expect([0, 1, 2, 3]).to.containAll(item => item < 4);
  });
  it('containOne should be true if at least one item is true', () => {
    expect([0, 1, 2, 3]).to.containOne(item => item >= 2);
  });
  it('containExactlyOne should be true if exactly one item is true', () => {
    expect([0, 1, 2, 3]).to.containExactlyOne(item => item === 2);
  });
});
```

This module also includes types for *TypeScript*.
