# SoftwareDevelopmentBestPractices

Bunch of best practice for software development I follow and encourage others to follow so new devs can easily understand the code base and you feel better about the code. 

NOTE: I know that `console.log` is considered bad practice but it is just for demo in this file.

## Avoid nested code
Example
```js
if (someCondition1) {
  if (someCondition2) {
    if (someCondition3) {
      promise
        .then(a => {
          console.log('I am bad code');
        })
    }
  }
}
```

Instread write all conditions in one line and use async to avoid `.then` call
 
```js
if (someCondition1 && someCondition2 && someCondition3) {
 const result = await promise;
 console.log('I am good code');
}
```
