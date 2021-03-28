# Explain promises with examples

Promise is similar in meaning to dictionary terms of what promise is defined... this is outrightly guaaranteeing that we are going to do something in the future.

Promises works on three principles of accept,reject and pending states.

chaining is one of the best features of Promise, here callbacks are attach rather than passing them.

based on a logic of thinking or process, statement are executed choosing if it is either true or false (i.e Accept or Reject). it also gives out error output incase an error is found using a more defined error catch exception.

Promise can be applied in various ways such as fetching data from the web server and so on.

we have some types of Promise, Promise all and promise race. when these are used with setTimeoutput function,it really makes programming planning an efffective ones, execution is carried out in a more precise and logical manner. this can be achieved by making use of promise syntax of Promise.all()
and Promise.race()
Promises are one of the ways we can deal with asynchronous operations in javascript.

**Examples of how Promise works are shown below:**
```
//Promise 

let allGoods = true;

const accessingGoods = new Promise ((resolve, reject)=>{
  if (!allGoods){
    reject ('error Accessing Goods!');
  } else {
    resolve ('nice work!')
  }  
})

accessingGoods.then ((message)=> {
  console.log (message)}).catch((message)=>{
    console.log (message)
  }); // it displays nice work, this is as a result of setting the variable declaration of let to be true, it will display error Accessing Goods if allGoods was initiated to false.
```
```
//Another example of Promise function

let numberLogic = new Promise((resolve, reject)=>{
  let spinNumber1 = 0
  if (spinNumber1 == 0){;
  resolve ('success');
}else {
  reject('failed');
}
});

numberLogic.then (message => alert (message), error => alert (error)
). catch((message) => {
  console.log('This is the catch' + message)
}); // it displays success because the condition spinNumber equals to 0, if this condition is set to any number aside zero, failed shall be displayed.
```
```
//using Promise with a setTimeout function

let numberCounter = new Promise ((resolve, reject)=>{
  
    setTimeout(()=> resolve ('success'),2000);
});

numberCounter.then(messages => alert(messages), error => alert (error)
); // it displays success after 2 seconds
```
```
// Promise.all

const promise1 = new Promise ((resolve, reject)=>{
  resolve ('Hello World!');
});
const promise2 = new Promise((resolve,reject)=>{
  setTimeout(()=>{
    resolve ('Goodbye,', 2000);
  });
  resolve ('10');
});
const promise3 = new Promise ((resolve, reject)=>{
  setTimeout(()=>{
    resolve ('Goodbye,', 3000);
  });
});

Promise.all ([
  promise1,
  promise2,
  promise3,
]).then((values)=>{
  console.log(values);
}); //display array ['Hello World!', '10', 'Goodbye' ]
```