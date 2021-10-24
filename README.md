# SoftwareDevelopmentBestPractices

## Avoid nested code
Example
```js
if (someCondition) {
  if (someCondition) {
    if (someCondition) {
      promise
        .then(a => {
          console.log('I am bad code');
        })
    }
  }
}
```

Instread write all conditions in one line and use async to avoid `.then` call
