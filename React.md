# React

```javascript
onClick={function() {...}}
onClick={() => ...}
```



props --> properties

```javascript
class Square extends React.Component {
  constructor(props) {
    super(props);
    this.state = {
      value: null,
    };
  }

  render() {
    return (
      <button
        className="square"
        onClick={() => this.setState({value: 'X'})} // replacing () => alert() event handler with () => this...
    // by calling this.setState from onClick, we tell React to re-render that Square whenever its<button> is clicked.
      >
        {this.state.value}
      </button>
    );
  }
}
```

In Javascript classes, you need to always call **super** when defining the constructor of a subclass. All React component classes that hava a constructor should start it iwth a super(props) call.



To collect data from multiple children, or to have two child components communicate with each other, you need to **declare the shared state in their parent component** instead. 

**The parent component can pass the state back down to the children by using props**; this keeps the child components in sync with each other and with the parent component.

In React, function components are a simple way to write components that only contain a render method and don't have their own state.



```javascript
function Square(props) {
  return (
    <button className="square" onClick={props.onClick}>
      {props.value}
    </button>
  );
}
```



X.slice()	--> create a copy of X



In a class, we used an arrow function to access the correct **this** value, but in a fucntion component we don't need to worry about **this**.



```javascript
  handleClick(i) {
    const squares = this.state.squares.slice();
    squares[i] = this.state.xIsNext ? 'X' : 'O';
    this.setState({
      squares: squares,
      xIsNext: !this.state.xIsNext,
    });
  }
```







#### map

```javascript
const numbers = [1, 2, 3];
const doubled = numbers.map(x => x * 2); // [2, 4, 6]
```





### ReactiveX - Observable

####map() v.s. switchMap()

These are used to flatten an observable

say we have a obs(A)

.map((A) => B) => obs(B)

.switchMap((A) => obs<B>) => obs(B)