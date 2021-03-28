// To briefly understand what setTimeout() could be used for

# Explain the settimeout function with example

SetTime out function allows you to trigger another action in a particular minute of time. it has many uses in javascript, such as delaying tasks, finds its application in animations, notifications and functional execution delay. however, because javascript is a single threaded,translative language, one task can only be performed at a time.

The setTimeout method is a built in method that takes call back function as an argument and executes it after a given amount of time.
**syntax:**
setTimeout (callbackFunction, delay,arguments)
```
//Example of setTimeout function 

setTimeout(()=>{
  console.log('Welcome to the world of setTimeout function')
}, 3000); //logs out welcome to the world of setTimeout Function after 3seconds
```