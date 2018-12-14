#ES6

####Let

is only accessible in the block level it is defined



#### Const

is used to assign a constant value to the variable and the value cannot be changed. It's fixed



#### Arrow Function

```javascript
// Old Syntax
function oldOne() {
 console.log("Hello World..!");
}
// New Syntax
var newOne = () => {
 console.log("Hello World..!");
}
```

```javascript
let Func = (a, b = 10) => {
 return a + b; 
}
Func(20); // 20 + 10 = 30

let NotWorkingFunction = (a = 10, b) => {
 return a + b;
}
NotWorkingFunction(20); // NAN. Not gonna work.
// the first value gets assigned to the first parameter ...
```

#### For of Loop

```javascript
let arr = [2,3,4,1];
for (let value of arr) {
 console.log(value);
}
Output:
2
3
4
1
```

#### Spread Attributes

```javascript
let SumElements = (arr) => {
 console.log(arr); // [10, 20, 40, 60, 90]
let sum = 0;
 for (let element of arr) {
 sum += element;
 }
 console.log(sum); // 220. 
}
SumElements([10, 20, 40, 60, 90]);


let SumElements = (...arr) => {
 console.log(arr); // [10, 20, 40, 60, 90]
let sum = 0;
 for (let element of arr) {
 sum += element;
 }
 console.log(sum); // 220. 
}
SumElements(10, 20, 40, 60, 90); // Note we are not passing array here. Instead we are passing the elements as arguments.
```

```javascript
let arr = [10, 20, 60];
Math.max(arr); // Shows error. Doesn't accept an array.

let arr = [10, 20, 60];
Math.max(...arr); // 60
```



#### Maps

```javascript
var NewMap = new Map();
NewMap.set('name', 'John'); 
NewMap.set('id', 2345796);
NewMap.set('interest', ['js', 'ruby', 'python']);
NewMap.get('name'); // John
NewMap.get('id'); // 2345796
NewMap.get('interest'); // ['js', 'ruby', 'python']
```



``` javascript
NewMap.keys();
NewMap.values();

for (let [key, value] in NewMap) {
    console.log(key + " - " + value);
}
```



#### Sets

```javascript
var sets = new Set();
sets.add('a');
sets.has('a');	//returns true
```



#### Static methods

assign methods to the class function, not to its "prototype"





#### Getters and Setters

```javascript
class People {
constructor(name) {
 this.name = name;
 }
 get Name() {
 return this.name;
 }
 set Name(name) {
 this.name = name;
 }
}
let person = new People("Jon Snow");
console.log(person.Name);
person.Name = "Dany";
console.log(person.Name);
```





