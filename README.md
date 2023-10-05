# Javascript-concepts
```
String.prototype.repeatify = function (char) {    
    return this.repeat(char)    
};

    let data = 'hello';
    console.log(data.repeatify(3));
```
#### Objects in javascript 
```
// console.log(z)   //Temporal dead zone
let z;
```

```
const user = {
    name:'Kiran',
    age:31
}
// delete(user.name)
let property = "place";
let value = "Rajur";
user[property] = value;
console.log(user);
````


````
const user1 = {
    name:'Kiran',
    age:31,
    name:'Ritesh',
}

console.log(user1)
```

==========================================================

#### Write function which multiple all numbs value by 2 and return object
```
const nums = {
    a:100,
    b:200,
    c:"My Title"
}


function multipleBy2(obj){
    for(a in obj){
        if(typeof(obj[a]) == 'number'){
            obj[a] *= 2
        }
    }
    return obj;
}

// console.log(multipleBy2(nums))
````


```
const a={};
const b = {key:"b"};
const c = {key:"c"}
a[b] = 123;
a[c]=456;
// console.log(a[b])
```

```
// console.log([..."Kiran"])
```

```
const A = {name:"Kiran", age:31}
const B = {admin:true, ...A}
// console.log(B)
```

```
const shape = {
    radius:10,
    diameter(){
        return this.radius *2
    },
    perimeter :()=> 2 * Math.PI * this.radius
}

// console.log(shape.diameter());
// console.log(shape.perimeter());
```

```
const person1 = {
    name:"Piyush",
    age:24,
    fullName:{
        first:"Hello",
        last:"World"
    }
}

const {fullName:{first}} = person1;
// console.log(first);
// console.log(person1.fullName.first)
```


```
const d = {greeting:"hey"};
const e = d;                 //refrence of object getting copied
const f = Object.assign({}, d);        //simple object .d.d.deep copy
d.greeting = "Hello";

// console.log(e);
// console.log(f);

// console.log({a:1} =={a:1});
// console.log({a:1} === {a:1});

// console.log([1,2] == [1,2]);
// console.log([1,2] === [1,2]);
```

```
let p = {name:"Lynda"};
const member = [p];
p = null;
// console.log(member)


const val = {number:10}
const y = {...val}     //... simple object spread act as deep copy
val.number = 20;
// console.log(y)
```

```
        // {...val} initial value 
const multiply = (x={...val})=>{
    console.log((x.number *= 2));
}

// multiply();   //20
// multiply();    //20
// multiply(val);   //20
// multiply(val);   //40
```

```
var age=10;

var person = {
    name:"Kiran",
    age:24,
    getAge:function(){
        console.log(this.age);
    },
    getArrowAge :()=>{
        console.log(this.age);               //...........arrow function this refers to its parent function scope
    },
    getHello:function(){
        return getArrowAge =()=>{
            console.log(this.age);               //...........arrow function this refers to its parent function scope
        }
    }
    
}
// person.getAge();
// person.getArrowAge();
// person.getHello()();
```

```
let name = "Kiran";


let user2 ={
    name:"Ritesh",
    getName:()=>{
        return this.name;
    }
}

console.log('as');
console.log(user2.getName());

```
