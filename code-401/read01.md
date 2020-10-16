- **Array map()**
1. return a new array have the same length ,this method does not change the original array.
1. provided function for each element in an array, in order.
- syntax array.map(function(item , index){})

- **Array reduce()**
1. reduces the array to a single value.
1. executes a provided function for each value of the array .
1. the return value of the function is stored in an accumulator.
1. does not change the original array.
- syntax array.reduce(function(accumulator  ,item , index){})

- **Superagent**
- Promise.then() syntax.
```
function(){
  superagent.get(URL)
    .then((result)=>{
      return result.body
    })
}
```
- async/await syntax.
```
async function(){
  let result = await superagent.get(URL)
  return result
}
```
- JavaScript Promises
It allows you to associate handlers with an asynchronous action's eventual success value or failure reason. This lets asynchronous methods return values like synchronous methods: instead of immediately returning the final value, the asynchronous method returns a promise to supply the value at some point in the future.
```
function isEven(num){
  return new Promise((resolve , reject)=>{
    if(num % 2 == 0){
      resolve(num)
    }else{
      reject("not a even number")
    }
  })
}
let numArray = [1,2,3,4,5,6,7,8,9]
numArray.forEach(num=>{
  isEven(num)
  .then(data=>{
    console.log(data)
  })
  .catch(err=>{
    console.log(err)
  })
})
```
- Are all callback functions considered to be Asynchronous? Why or Why Not?
No , not every call back considerred as asynchronous. 
for examply the forEach consider as a call back function but not a asynchronous.


## npm
npm is the world’s largest software registry. Open source developers from every continent use npm to share and borrow packages, and many organizations use npm to manage private development as well.

npm consists of three distinct components:

- the website
- the Command Line Interface (CLI)
- the registry

Use npm to :
- Adapt packages of code for your apps, or incorporate packages as they are.
- Download standalone tools you can use right away.
- Run packages without downloading using npx.
- Share code with any npm user, anywhere.
- Restrict code to specific developers.
- Create Orgs (organizations) to coordinate package maintenance, coding, and developers.
- Form virtual teams by using Orgs.
- Manage multiple versions of code and code dependencies.
- Update applications easily when underlying code is updated.
- Discover multiple ways to solve the same puzzle.