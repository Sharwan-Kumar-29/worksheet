1) Dynamic vs static typing

denug question1 


function calculateArea(length, width) {
    return length * width;
}
console.log(calculateArea(10, "5")); // Expected: Error-free calculation

ans There is no error in this code because type coercion take place

question 3)

let arr=["10",20,"30"]

const result=arr.reduce((acc,ele)=>(acc+Number(ele)),0)
console.log(result)

question 4) 

Ans) dynamic typing: refers to js ability to allow variable to hold values of any types and those types can change over time
time

type of variable is determined at runtime and can be reassigned to values of different types without error
eg
let variable=42//Number
variable="Hello"//String
variable=true // bollean

Type coercion : it refers to js ability to convert the data type to another when an operation required it
let result="10"-5

2)String Concatination::

error based debugging
let a = "10";
let b = "5";
console.log(+a + +b); // Expected Output: 15
we have to use uniary plus operator for the type conversion from string to number because add
operation concate the string no any type coercion happen

question3)
 ans) let arr=["Hello", 42, true]
function stringconv(arr){
    return arr.map(String).join('')
}
console.log(stringconv(arr))

question4) Discuss how type coercion differs in equality checks (== vs. ===). Provide an example.
ans) in case of loose equality(==) it will not check the datatype of the comparision components/variable
in case of strict Equality(===) it will check the datatype also if the datatype as well as value
is same it will return true else false


3) Functions: Declarative, Expression, Anonymous, Arrow
question1) debug
const multiply = (a, b) => {
    return a * b 
};
console.log(multiply(2, 3)); // Expected Output: 6

wwe have to specify the return statement because curly bracies takes two or more statements

question 3) 
ans function applyToArray(array, callback) {
    return array.map(callback);
}


const result1 = applyToArray([1, 2, 3], function(value) {
    return value * 2;
});
console.log(result1);

// Usage with an arrow function
const result2 = applyToArray([1, 2, 3], value => value * 2);
console.log(result2); 

question4)
ans
arrow function is different from the expression function in case of the scope because expression function refers to the
value of object like if we want to acces the object name inside the function we can use this.name
but in case of the arrow function scope of this is globally or returning undefined


4)Function vs arrow function and this
question1) debug
const obj = {
    name: "JavaScript",
    getName:function(){
        const arrow=()=>this.name
        return arrow()
        
    }
};

we have to use arrow function inside the function and return it

question4)

regular function pros
rugular function have its own this context
regular function have fuction declaration hosting we can call the function before its declaration

cons 
syntax is longer compared to arrow function

pros of arrow function 
syntax short it has some time one line syntax
single line arrow function can automatically return 

cons
it cant be used as constructor


vidoe link: https://drive.google.com/drive/folders/1xWMNgs6t4hNFQVIOo6m6xZ6FO2p3meuN?usp=sharing



