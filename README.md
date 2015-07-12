# react-dimensions

React [higher-order component](https://gist.github.com/sebmarkbage/ef0bf1f338a7182b6775) to get dimensions of container


### `undefined`

eslint-disable no-irregular-whitespace


### `undefined([options.getHeight], [options.getWidth])`

Wraps a react component and adds properties `containerHeight` and
`containerWidth`. Useful for responsive design. Properties update on
window resize. **Note** that the parent element must have a height, or else
nothing will be rendered.

Can be used as an [ES7 class decorator](https://github.com/wycats/javascript-decorators) or a
[higher-order component](http://babeljs.io/blog/2015/06/07/react-on-es6-plus/#property-initializers)
(see examples)

### Parameters

| parameter             | type     | description                                                                                                                         |
| --------------------- | -------- | ----------------------------------------------------------------------------------------------------------------------------------- |
| `[options.getHeight]` | function | _optional:_ `getHeight(element)` should return element height, where element is the wrapper div. Defaults to `element.clientHeight` |
| `[options.getWidth]`  | function | _optional:_ `getWidth(element)` should return element width, where element is the wrapper div. Defaults to `element.clientWidth`    |


### Example

```js
import Dimensions from 'react-dimensions'

class MyComponent {
  render() (
    <div>
      {`containerWidth=${this.props.containerWidth},`}
      {`containerHeight=${$this.props.containerHeight}`}
    </div>
  )
}

export default Dimensions()(MyComponent) // Enhanced component
```


```js
// with [ES7 Decorators](https://github.com/wycats/javascript-decorators)
import Dimensions from 'react-dimensions'

​@Dimensions()
class MyComponent {
  render() (
    <div>
      {`containerWidth=${this.props.containerWidth},`}
      {`containerHeight=${$this.props.containerHeight}`}
    </div>
  )
}

export default MyComponent
```


**Returns** `function`, Returns a decorator that can be used to enhance a react component `Enhance(MyComponent)`


### `Dimensions`

eslint-enable no-irregular-whitespace

## Installation

Requires [nodejs](http://nodejs.org/).

```sh
$ npm install react-dimensions
```

## Tests

```sh
$ npm test
```


