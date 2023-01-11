# How to test JavaScript code using 'jest'
without wasting your time to testing the JavaScript code. Use this fantastic tool to test your code and save yourself 100s of hours.

## Jest
Jest is a testing framework developed by Facebook for testing JavaScript code.
It is a fast and has a powerful feature set, including the ability to mock dependencies and simulate events.

The greate thing about this framework is it works with projects that use Node,React,Angular, and Vue.

## How it works
In here I use a small Project to show you how it works

### Step 1: makes package.json 
open the project folder in vs code or your favourite IDE
then run this command 

```
npm init -y
```

### Step 2: install jest

```
npm install --save-dev jest
```

### Step 3: create a file sum.js that calculates sum

```
const sum = (a,b) =>{
  return a+b;
}

module.exports = sum;
```

### Step 4: create a file named sum.test.js this will contain our actual test

```
const sum = require('./sum');

test('adds 1 + 2 to equal 3', () =>{
  expect(sum(1,2)).toBe(3);
});
```

### Step 5: add the following section to your package.json

```
{
  "scripts": {
    "test": "jest"
  }
}
```

### Step 6: open the terminal run this command

```
npm test

or

yarn test
```

congrats! jest will print this message

```
> test@1.0.0 test
> jest

 PASS  ./sum.test.js
  ✓ adds 1 + 2 to equal 3 (5 ms)

Test Suites: 1 passed, 1 total
Tests:       1 passed, 1 total
Snapshots:   0 total
Time:        0.901 s, estimated 1 s
Ran all test suites.
```
