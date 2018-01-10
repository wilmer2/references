# React

## List Rendering
```js
{users.map(user => <UserProfile user={user} />)}
```
## Event Handling
```js
<button onClick={eventHandler} />
```

## LifeCycle Methods
```js
componentWillMount()
componentDidMount()
componentWillReceiveProps(nextProps)
shouldComponentUpdate(nextProps, nextState)
componentWillUpdate(nextProps, nextState)
componentDidUpdate(prevProps, prevState)
componentWillUnmount()
```

## Refs
```js
<input ref={ref => { this.myInput = ref }}
```

## Fragment
```js
import { Fragment } from 'react';

<Fragment>
  <Component1 />
  <Component2 />
</Fragment>
```

## Error Handling
```js
componentDidCatch(error, info)
```

## High Order Components
### Proxy Pass
```js
function ppHOC(WrappedComponent) {
  return class PP extends React.Component {
    render() {
      return <WrappedComponent {...this.props} />
    }
  }
}
```

### Inheritance Inversion
```js
function iiHOC(WrappedComponent) {
  return class Enhancer extends WrappedComponent {
      render() {
        super.render();
      }
  }
}
```
