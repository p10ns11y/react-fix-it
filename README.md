[![Build Status](https://travis-ci.org/MicheleBertoli/react-fix-it.svg?branch=master)](https://travis-ci.org/MicheleBertoli/react-fix-it)

# React Fix It
Automagically generate tests from errors.

Follow the flow:

- Enhance your components with `fixIt`
- Write some bugs (or wait for your components to fail)
- Open the console and copy the test snippet
- Paste the code to reproduce the error
- Fix the bugs and celebrate

:warning: This package uses [react-component-errors](https://github.com/staxmanade/react-component-errors) to wrap the lifecycle methods into a try...catch block, which affects the performance of your components. Therefore it should **not** be used in production.

## Demo

![Demo](demo.gif)

## Installation

```
yarn add --dev react-fix-it
```

## Usage

```jsx
import React, { Component } from 'react'
import fixIt from 'react-fix-it'

class MyComponent extends Component {
  render() {
    return <div>Hello ⚛</div>
  }
}

export default fixIt(MyComponent)
```

## Test

```
yarn test
```
