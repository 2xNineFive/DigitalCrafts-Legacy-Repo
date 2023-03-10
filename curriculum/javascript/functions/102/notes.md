# JavaScript Functions 102
## An arrow function expression is more concise than the traditional funciton expression. However, there are caveats (not discussed here).

### Advantages (not a complete list)
The return is considered an _implicit return_, so the `return` keyword is unnecessary.

The `function` keyword is replaced with `=>`'.
```javascript
const someFn = function () {
    return 'Hello World';
}

const anotherFn = () => {
    return 'Hello World';
}
```

The curly braces and the `return` keyword can be removed entirely if everything can fit on one line. 
```javascript
const someFn = function () {
    return 'Hello World';
}

const anotherFn = () => 'Hello World';
```

You can remove paraentheses if there is only one argument. 
```javascript
// one argument 
const greeting = function (name) {
    return `Hello, ${name}`;
}

const newGreeting = name => `Hello, ${name}`;

// more than one argument 
const location = function (city, state) {
    return `The location is ${city}, ${state}.`;
}

const newLocation = (city, state) => `The location is ${city}, ${state}.`;
}
```

A `return` that spans multiple lines can either use an `explicit` return, with curly braces, or an implicit `return`, with parentheses. 
```javascript
// traditional
const studentDetails = function () {
    return {
        name: 'Angel',
        age: 16,
        grade: 91
    }
};

// explicit
const newStudentDetails = () => {
    return {
        name: 'Angel',
        age: 16,
        grade: 91
    }
};

// implicit
const newStudentDetails = () => (
    {
        name: 'Angel',
        age: 16,
        grade: 91
    }
);

```