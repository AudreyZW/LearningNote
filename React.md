#React



## JSX

A syntax extension to Javascript.

e.g. 

```typescript
const element = <h1>Hello world!</h1>;
```

using it with React to describe what UI should look like, instead of putting markup and logic in separate files.

JSX produces React "elements" which can be rendered to the DOM.



### Embedding expression in JSX

```javascript
const name = 'Josh Perez';
const element = <h1>Hello, {name}</h1>;

ReactDOM.render(
  element,
  document.getElementById('root')
);
```

