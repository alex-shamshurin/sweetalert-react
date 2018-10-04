# react-sweetalert2

[![npm version][npm-image]][npm-url]
[![Downloads][downloads-image]][downloads-url]

> Declarative SweetAlert in React

## Introduction

This is a React SweetAlert wrapper for https://github.com/alex-shamshurin/sweetalert2-react

## Install

```
$ npm install react-sweetalert2
```

## Usage

```js
import React, { Component } from 'react';
import SweetAlert from 'react-sweetalert2';

// ...

render() {
  return (
    <div>
      <button onClick={() => this.setState({ show: true })}>Alert</button>
      <SweetAlert
        show={this.state.show}
        title="Demo"
        text="SweetAlert in React"
        onConfirm={() => this.setState({ show: false })}
      />
    </div>
  );
}
```

Since 0.6, you can wrap your own sweetalert2 (swal) instance:

```js
import React, { Component } from 'react';
import { withSwalInstance } from 'react-sweetalert2';
import swal from 'sweetalert2';

const SweetAlert = withSwalInstance(swal);

// ...

render() {
  return (
    <div>
      <button onClick={() => this.setState({ show: true })}>Alert</button>
      <SweetAlert
        show={this.state.show}
        title="Demo"
        text="SweetAlert in React"
        onConfirm={() => this.setState({ show: false })}
      />
    </div>
  );
}
```

## Tests

Tests were not updated to support sweetalert2. PRs are welcome.

## License

MIT © [C.T. Lin](https://github.com/kessejones/react-sweetalert2)

<!-- 
[npm-url]: https://npmjs.org/package/react-sweetalert2
[npm-image]: https://img.shields.io/npm/v/react-sweetalert2.svg?style=flat-square
[downloads-image]: http://img.shields.io/npm/dm/react-sweetalert2.svg?style=flat-square
[downloads-url]: https://npmjs.org/package/react-sweetalert2
 -->