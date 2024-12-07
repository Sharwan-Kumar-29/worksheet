Promises and Callbacks

question1)

function fetchUser(callback) {
    setTimeout(() => {
        const user = null; // Should fetch a valid user object
        callback(user.name); // Bug: Cannot read property 'name'
    }, 1000);
}

fetchUser((name) => console.log(name));

ans) user is null so we can't access user.name


question 3) fetch two api simultaniously

ans)
const api1 = 'https://jsonplaceholder.typicode.com/posts/1';
const api2 = 'https://jsonplaceholder.typicode.com/users/1';

const fetchApi1 = fetch(api1).then(response => response.json());
const fetchApi2 = fetch(api2).then(response => response.json());

    Promise.all([fetchApi1, fetchApi2])
    .then(([data1, data2]) => {
        console.log('Data from API 1:', data1); // Result from API 1
        console.log('Data from API 2:', data2); // Result from API 2
    })
    .catch(error => {
        console.error('Error fetching data:', error);
    });

in this we first fetch both the api's and then store into the variable and then use the promise.all to resolve all the promises if either of the promise will not resolved promise all will reject entire prosises and give the reason it will not provide results for the promise that resolved successfully


question3)
How can we use async await with promises to simplify asynchronous code write an example
ans) 
async function fetchTwoAPIs(api1, api2) {
    try {
        
        const response1 = await fetch(api1);
        const data1 = await response1.json();

        /
        const response2 = await fetch(api2);
        const data2 = await response2.json();

        
        return { api1Data: data1, api2Data: data2 };
    } catch (error) {
        console.error('Error fetching APIs:', error);
        throw error; // Rethrow error if needed
    }
}

MAP,Filter,Reduce and method Chaining:

Error Handling

const nums = [10, 20, 30];
const result = nums.map((n) => n / 0).filter((n) => n > 0); // Bug: Improper math operation
console.log(result.reduce());

0 division error:

question 3)
ans) 
const input = [1, 2, 3, 4, 5];

const result = input
    .filter(num => num % 2 === 0) 
    .map(num => num * 2)          
    .reduce((sum, num) => sum + num, 0); 

console.log(result);

3)Frequency Creation in Objects Using Reduce....

question 1) Error-Based Debugging:Fix this code


const chars = "aabbc";
const freq = chars.split("").reduce((acc, char) => {
    acc[char]=(acc[char]||0)+1
    return acc; 
}, {});
console.log(freq);

if char is present in acc it will +1 in the existing frequency if not it will return last falsy value + 1

question3) Output based question

let arr=[1,2,3,4,5]
let obj=arr.reduce((acc,char)=>{
    if(char%2==0){
        acc['even']=(acc['even']||0)+1
    }
    else{
        acc['odd']=(acc['odd']||0)+1
    }
    return acc
},{})
console.log(obj)



question 4) difference between reduce and for loop in the context of frequency calculation


ans: Both reduce and for loop iterate over the array once (O(n)), so their time complexity is the same
for small datasets 
the performance difference is negligible

for large datasets:
A for loop may have slightly better performance because it avoids the overhead of higher order function calls used by reduce


4)) Error debug:

const nums = [1, 10, 2];
nums.sort((a,b)=>a-b); 
console.log(nums);

for sort function sort the data lexciographhically order
for number or integer we have to write down the function


question 2)
ans)
const people = [
  { name: "Alice", age: 25 },
  { name: "Bob", age: 30 }
];

const sortedPeople = people.sort((a, b) => b.age - a.age);

console.log(sortedPeople);


question 3)

let words = ['banana', 'apple', 'cherry', 'Éclair', 'apple', 'éclair'];

let sortedWords = words.sort((a, b) => a.localeCompare(b));

console.log(sortedWords);





























