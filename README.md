# Intro to Object Oriented JavaScript (ES6) 🔥

## ⚠️ Prerequisites
- [ ] Basic Understanding of **functional JS**
- [ ] **JS Data Types:** Primitive & Non-Primitive
- [ ] Creating **POJOs** (Plain Old JavaScript Objects)

## ✅ SWBAT(s)
- [ ] Explain the need of Object Orientation
- [ ] Drawbacks of conventional JS objects
- [ ] Writing your own class in JS


## 🤔 JS && Object Orientation?

<p align="center">
  <img src="https://i.redd.it/sf50keitkij21.jpg" height=300 />
</p>

### 🗄 Declaring Variables

```js
  const numberOne = 10;
  const numberTwo = new Number(10);

  console.log(numberOne == numberTwo) // Output ????
  console.log(numberOne === numberTwo) // Output ????

```

<p align="left">
  <img src="https://media.tenor.com/images/e9e060b3eed685391ed181b19274f6d9/tenor.gif" height=200 />
</p>

### 😯 Different Ways of creating objects (Plain Old JS Objects)

```js
  const mario = {
    first_name: 'Mario',
    last_name: 'Mario',
    introduce: function (){
      console.log(`Hey There! This is ${this.first_name} ${this.last_name}.`)
    }
  }
```

```js
  const luigi = {
    first_name: 'Luigi',
    last_name: 'Mario',
    introduce: function() {
      console.log(`Hey There! This is ${this.first_name} ${this.last_name}.`)
    }
  }

```

```js
  function createPerson(first_name, last_name){
    const personObject = {
      first_name: first_name,
      last_name: last_name,
      introduce: function(){
        console.log(`Hey There! This is ${this.first_name} ${this.last_name}.`)
      }
    }
    return personObject
  }

  const mario = createPerson('Mario','Mario')
  const luigi = createPerson('Luigi','Mario')
```

### 🤓 Creating a class

```js
  // ES5
  function Person(first_name, last_name){
    this.first_name = first_name
    this.last_name = last_name
  }

  var mario = new Person('Mario','Mario')
  console.log(mario)

  // ES6
  class Person {
    constructor(first_name,last_name){
      this.first_name = first_name
      this.last_name = last_name
    }

    introduce(){
      console.log(`Hey There! This is ${this.first_name} ${this.last_name}.`)
    }
  }

  const luigi = new Person('Luigi','Mario')
  console.log(luigi)
  luigi.introduce()
```

<p align="center">
  <img src="https://media3.giphy.com/media/3knKct3fGqxhK/giphy.gif?cid=ecf05e4774f3104b5de7047c7d2fc04fc5bbe3cf17daca95&rid=giphy.gif" height=200 />
</p>

### 🙌🏻 Exercise

#### Solve it here: [link](https://repl.it/repls/GenerousFlashyPresses#index.js)

```markdown
  # Write a JS class that allows `Ash, Brock & Misty` to create a bank account.

  + An Account should have:
    + Full name of the owner
    + Balance
    + Type of the account (checking || savings)

  + It should have a method that logs the account information.

  ++ Bonus:
    + Implement methods to deposit and withdraw from the account.
```
