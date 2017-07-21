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
