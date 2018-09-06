# Bootcamp

## Purpose

The purpose of this bootcamp note is to gain practice in fullstack JavaScript developing included:

- Basic javascript language skills and functional patterns
- React application development
- Node development
- Rest service development in node
- Unit testing
- Docker basics
- Mongo basics
- AWS basics
- Continuous integration

This way we will create a simple web application. After then we will create a node rest api with MongoDB, which could be used by the application. When the app and the api are ready, they will move in docker containers, and they well be able to deploy to AWS ECS.

## Javascript

Javascript is a single threaded asynchronous script language run by interpreters, such as V8 or Chakra. The popularity of javascript based on that it's running on many platforms: in every browsers, on server side by NodeJS, in mobile applications by React Native, in IOT devices, etc. The other important benefit of javascript is its functional nature. The functional features, such as high order functions, allow us to implement asynchronous behaviour easy, eg.: `onClick` callbacks, HTTP request handlers, etc.

**Check your javascript skills by our [questionaire](https://community.risingstack.com/repatch-the-simplified-redux/)!**

### The ECMAScript standards

In accordance with the popularity of Javascript, this is a dynamically evolving language. The ECMAScript is the Javascript standard by the ECMA international. The association publishes an extension of the language in every year. You can always check the [kangax compatibility table](http://kangax.github.io/compat-table/es2016plus/) to ensure which features are supported in your chosen platform.

### Babel

Javascript feature-supporting is very diverse, but convergent caused of the ECMAScript standard. Usually you need to compile Javascript to Javascript in a lower version. This makes a babelian chaos, and it is not easy to wrap your mind around. There is some tool to make this transpilations, such as [Babel](http://babeljs.io/) or the ultimate [TypeScript](https://www.typescriptlang.org/). This latter is a typed superset of Javascript and it also includes the newest features of ECMAScript.

## Functional programming

This topic is too wide to explain in a brief paragraph. As I mentioned above javascript is a very functional-powered language. Although this is not a [pure functional language](https://en.wikipedia.org/wiki/Purely_functional_programming), it has a lot of features that allow us to follow functional patterns. There are many articles and blog posts about functional patterns in javascript, I can also suggest one.

**Check our suggested [book](https://github.com/getify/Functional-Light-JS) about functional patterns!**

### Determinism

Functional programming's primary trait is the determinism. What does it mean? If I have a function, which provides always the same output on the same input independently of its environment, we call this function as pure function, and pure functions are deterministic.

The biggest part of a code is data transformation, and data transformations could be easily deterministic. I have some input data, and I want to create some output data. It is a simple projection between two data manifestation. The most simple computer program is a data transformation, and we can describe it as an data transformation or data projection. And the functions do this exactly:

![](stateless_projection.png)

Of course we are thinking in short functions, so a program cannot be a big giant functions. This is much more a function composition:

![](stateless_projections.png)

### Immutability

The base requirement of the deterministic behaviour is immutability. That means **we just create things in memory, but never change them!** If I create a variable

```js
let a = 1
```

and I modify this

```js
a = 2
```

then I changed its value in the memory. If any part of our code relies on this variable I influenced its running, and I can cause some unexpected behaviour of the program. And unexpected behaviour does not match with definition of determinism. In a strongly asynchronous environment I can never be sure which kind of tasks are running in what order. **Undeterminism and unexpected behaviour is the devil himself and causes the most of bugs!**

If I create an object

```js
const user = { name: 'John', age: 28 }
```

and I change a property

```js
user.age = 30
```

or I remove a property

```js
delete user.age
```

then I did the same. I changed something in the memory and I may caused unexpected crashes.

If I create an array

```js
const numbers = [10, 20, 30]
```

and I push something within it

```js
numbers.push(40)
```

or I replace an item

```js
numbers[2] = 40
```

or I delete an item

```js
delete numbers[2]
```

then I changed this array, and somebody might hate me.

I do the same when I create a `Date` object

```js
const date = new Date()
```

and I change it

```js
date.setHours(14)
```

There are some practice to handle data immutable:

#### Variables against constants

We never use `var` or `let`. We use only `const`. So we can say, we **do not deal with variables**. We **work only with constants**. Only in very-very sparse cases, when we use `let`. For example when we create some state in a closure. Notice, that redux's store is this case, where the `state` is defined by `let`.

#### Deal with objects

We do not change object properties. And we never delete any of them. Rather than it, we assign a new one:

```js
const user = { name: 'John', age: 28 }
const modifiedUser = { ...user, age: 30, gender: 'male' }
```

If I want to delete an item, I reduce a new one without this:

```js
Object.keys(object).reduce(
  (acc, key) => key !== unnecessaryKey ? { ...acc, [key]: object[key] } : acc
  , {}
)
```

#### Deal with arrays

We do not push anything into arrays, and we never replace items or delete any kind of them. Rather than it, we assign a new one:

```js
const numbers = [10, 20, 30]
const extendedArray = [...numbers, 40]
```

For replacing an item we can use the `.map()` function:

```js
const numbers = [10, 20, 30, 40]
const replacedArray = numbers.map((number, i) => i === 2 ? 42 : number)
```

or

```js
users.map(user => user.id === 'abc' ? { ...user, age: 32 } : user)
```

For deleting an item we can use the `.filter()` function:

```js
users.filter(user => user.id !== 'abc')
```

For slicing arrays do not use `.splice()`. Rather than it just use `.slice()`:

```js
const firstTwoItems = [10, 20, 30, 40].slice(0, 2)
```

or use the rest operator:

```js
const [first, second, ...rest] = [10, 20, 30, 40]
```

#### Other useful array methods

##### `.map()`

Maybe the most often used array method, that projects an array to an other array. The `.map()` returns a new array with the same length. With using `.map()`, you can change type of the elements, but it keeps the length.

```js
const usernames = users.map(user => user.name)
```

##### `.filter()`

An other often used array method. The `.filter` keeps the type of the elements, but it does not with the length. This method also returns a new array.

```js
const permittedUsers = users.filter(user => user.role === 'SOME_ROLE')
```

##### `.find()`

The `.find()` allows you to find an element in arrays with a predicate function:

```js
const user = users.find(user => user.id === 'abc')
```

##### `.findIndex()`

The `.findIndex()` is very similar to `.find()`, but rather than it, the `.findIndex()` returns the index of the matched element.

```js
const userIndex = users.findIndex(user => user.id === 'abc')
```

##### `.includes()`

A very good alternative of `.indexOf()`, but it returns with boolean value, so you do not need to check `index > -1` typically. Against of `.find()` or `.findIndex()` it searches by exact value matching, so is often useful for checking primitives in arrays.

```js
['SOME_PERMISSION', 'AN_OTHER_PERMISSION'].includes('SOME_PERMISSION') // true
```

##### `.flatten()`

This method converts multi-dimensional arrays to one-dimensional arrays.

```js
const letters = ['a', 'b', 'c']
const numbers = [1, 2, 3]
const matrix = letters.map(letter => numbers.map(number => ({ letter, number })))
const pairs = matrix.flatten()

/*
[
  { letter: 'a', number: 1 },
  { letter: 'a', number: 2 },
  { letter: 'a', number: 3 },
  { letter: 'b', number: 1 },
  { letter: 'b', number: 2 },
  { letter: 'b', number: 3 },
  { letter: 'c', number: 1 },
  { letter: 'c', number: 2 },
  { letter: 'c', number: 3 }
]
*/
```

##### `.some()`

The `.some()` implements a simple OR behavior on items with a predicate function:

```js
const numbers = [null, null, 10, null, 30]
const isThereValidNumbers = numbers.some(Number.isFinite) // true
```

##### `.every()`

The `.every()` implements a simple AND behavior on items with a predicate function:

```js
const numbers = [null, null, 10, null, 30]
const everyNumberIsValid = numbers.every(Number.isFinite) // false
```

### The state

Why can we say, this is true only on the simple programs. Because in these cases the program has no state. The state brings the complication, and every application has some state. A web application obviously has state. A REST data service has definitely not, but only in an optimistic world. The real life always works with states.

Then how can we adapt our functional projecting pattern including the state. We can curve our previous figure to this:

![](stateful_program.png)

We separate our **STATE** from the program logic (**REDUCER**). We has an initial state: this is the initial input of the reducer, and in every turn the reducers output will be the next state of the application.

### Reducers

Of course this closed system does nothing on its own. It needs some triggering action from the outside world, such as a user click or a HTTP request, etc. So a reducer's signature is:

```
(state, action) -> nextState
```

>All of us know well the [redux](https://redux.js.org/)'s [reducers](https://redux.js.org/basics/reducers). Its pattern is the same. We have a global application state (this is the [store](https://redux.js.org/basics/store)), and we have a reducer. This is just one reducer. Every other reducer is combined within this one.

Generally true, that a reducer makes from the current state a next state by an action. So a reducer always has two input argument:

- the currently accumulated state
- and an action

#### Reducing arrays

Javascript arrays has a `.reduce()` method, which accepts two argument. The first one is a required reducer, and the second one is an optional initial state. If there is no initial state as the second argument, the initial state will be the first item of the array, and the reducing starts at the second item. The `.reduce()` method can transform an array to anything we want against the rest of array methods, such as `.map()` or `.filter()`. Using `.reduce()` method can replace any kind of `for` loops. So we can say, we can avoid using `for` loops. Think in reducer!

Check this example of summing array of numbers:

```js
const sum = [10, 20, 30].reduce((sum, num) => sum + num, 0)
```

The initial state is `0`. The `.reduce()` starts the reducing at the first item, if we have initial state. The rounds are:

| # | state | item | nextState |
|:-:|:-----:|:----:|:---------:|
| 1 |   0   |  10  |     10    |
| 2 |   10  |  20  |     30    |
| 3 |   30  |  30  |     60    |

The first state will be the initial state, and the last next state will be the result of the `.reduce()` method, so the result is `60`.

I can do the same without initial state:

```js
const sum = [10, 20, 30].reduce((sum, num) => sum + num)
```

Then the initial state will be the first item of the array and the reducing starts at the second item of the array:

| # | state | item | nextState |
|:-:|:-----:|:----:|:---------:|
| 1 |   10  |  20  |     30    |
| 2 |   30  |  30  |     60    |

There are some commonly useful reduce implementation, such as:

```js
const max = [42, 7, 13, 56].reduce((max, num) => num > max ? num : max);
```

```js
const min = [42, 7, 13, 56].reduce((min, num) => num < min ? num : min);
```

### Curry

In many cases we need to bind one or more argument from a function before we call it. Look at this example. We have a callback to handle various items:

```js
handleClick = (id, evt) => { ... }

...

users.map(({id, name}) => (
  <input value={name} onClick={(e) => this.handleClick(id, e)} />
))
```

But if we define handleClick with this signature:

```js
handleClick = id => evt => { ... }
```

We have a bit simpler callbacks in jsx:

```js
users.map(({id, name}) => (
  <input value={name} onClick={this.handleClick(id)} />
))
```

We can also use the `.bind()` method on functions:

```js
handleClick = (id, evt) => { ... }

...

users.map(({id, name}) => (
  <input value={name} onClick={this.handleClick.bind(id)} />
))
```

### Closures

To understand closures first you need to understand what means capturing and bindid variables. If I have an expression, something like this:

```js
const f = a => b => a + b
```

then the `b => a + b` expression is an open expression, because `a` does not appears in this expression. The `b` is a *bound variable* and `a` is a *free variable* here. But if you give some value to `a` by `f(10)`, then the `a` will a captured variable in the inner expression.

The inner scope definitely access its value, but you can not from outside. This is the *closure*, when a set of variables are hidden, and there is no way to modify them directly. Let's see a simple example:

```js
const createIncrementalIdGenerator = () => {
  let id = 0
  return () => ++id
}

const getId = createIncrementalIdGenerator()
console.log(getId) // 1
console.log(getId) // 2
```

In this example you can not decrease its value, just increase.

Closures makes safety to protect variables (states) from the incompetent use. Redux's store is a closure and you can not access the store's state without the `getState()` function. But you never can modify by overriding its value, like `store.state = ...`

### Side-effects

A functional code is always deterministic, but in the real world there are indeterministic stuffs such as:
- network interaction
- filesystem interaction
- working with the current time
- randomness

Indeterministic resources are not able to unit-testing. To writing smart code you have to separate them from the strictly functional parts logic.

**Check this [post](https://github.com/jaystack/blog-posts/blob/master/side-effect/index.md) to getting around this topic.**

## React as a functional library

I do not have to introduce React, because you might know it. But maybe I can tell some interesting fact about the library generally. React is a universal paradigm to creating view functionally. The basic principle is simple: **Convert the data to view!** Or a bit differently: **Convert props to virtual dom.** Of course, React is more sophisticated, but the basic principle is this. So, every React component is just a pure function, that accepts the data as arguments (`props`) and returns the virtual dom. The virtual dom is a serialisable descriptor of the view.

### JSX

What happens exactly when you write [JSX](https://reactjs.org/docs/introducing-jsx.html) code:

```jsx
const element = <div className="hello"><h1>Hello, World!</h1></div>
```

JSX transpilers compile this code into:

```js
const element = React.createElement('div', {
  className: 'hello',
  children: React.createElement('h1', {
    children: 'Hello, World!'
  })
})
```

### The virtual dom and bootstrapping

The `React.createElement` always returns virtual dom. Virtual dom is a simple serializable object hierarchy, that describes the entire view. And React finishes here its work. Rendering to DOM must applied by [react-dom](https://www.npmjs.com/package/react-dom). ReactDOM is a render engine for rendering to DOM. There are several render engines, for example to PDF, Canvas, native mobile view, LED display or something else.

So the virtual dom is an environment independent input of the rendering engines. The React library performs only this part of the entire react flow, and the core functions of this moment is the `React.createElement`, which renders the virtual dom actually.

If any state of any component changes, React will rerender the component, and also the child components and their child components below that, etc.

The render engine (eg. react-dom) listens the changes in the virtual dom. That means when the virtual dom changes, the render engine determines which part of the dom changed actually by difference of the previous and the current virtual dom. If you type some text in an input field, the virtual dom only changes at this point, so the render engine only updates only this input value in the html dom.

### Functional components

The simples way to implement a react component is writing a function, which takes the props as argument and returns the virtual dom.

Something like:

```jsx
const Title = ({ name }) => <div>Hello {name}!</div>
```

The first argument is the `props`, the same as `this.props` in the class-based components. It also has a second argument: `context`, but this is an advanced feature and usually we don't need it to use.

We call them functional components, because they written as simple pure functions. Functional components' common property is that they don't have any inner state. If we need some state in the components, we must define them as classes.

### Importance of immutable data-handling

The virtual dom is an immutable data structure as the `React.createElement` is a pure immutable function. So if you have not thought so far, rendering is a computationally job.

Therefore in a well-written react application we try to avoid unnecessary rerenders. The principle is simple: needed to know in every component when the input data - props (and state) - really changes.

Suppose that we have a simple state in a component:

```jsx
class NameInput extends React.Component {
  state = {
    name: 'World'
  }

  handleChange = evt => {
    // ...
  }

  render() {
    return <input
      value={this.state.name}
      onChange={this.handleChange}
    />
  }
}
```

What if we update the state by mutating the state:

```js
handleChange = evt => {
  this.state.name = evt.target.value
}
```

The state instance wasn't change, we didn't create a new one. We just override the old value. React tries to determines the difference of the previous and current state. But the previous state is lost, because we modified that directly. Then the difference between the previous and the current state is nothing. React won't render.

So if you update the state always immutable, react has always the previous and the current state at all times, because in this case we created a new instance of the state object. Then react can observe the difference and rerender the component.

Mutability also can cause unnecessary rerenders. Always take care to handle the data immutable!

#### The `PureComponent`

We know functional components, `React.Component` and now we meet `React.PureComponent`. `PureComponent` is almost the same like the regular `Component` baseclass, except that `PureComponent` has a builtin shallow compare for the changing `props` and `state`. It's really useful and advisable to use, so **check this [documentation](https://reactjs.org/docs/react-api.html#reactpurecomponent) to understand it**.

### How Redux works

#### Creating the store

For understanding how redux works, let's implement a simple redux store!

```js
const createStore = reducer => {
  let state
  let listeners = []

  subscribe = listener => {
    listeners = [ ...listeners, listener ]
    const unsubscribe = () => listeners = listeners.filter(
      l => l !== listeners
    )
    return unsubscribe
  }

  dispatch = action => {
    state = reducer(state, action)
    listeners.forEach(listener => listener())
  }

  getState = () => state

  return {
    subscribe
    dispatch
    getState
  }
}
```

Notice that the real redux implementation is a bit smarter. But the essential part is almost the same. After creating the store, redux dispatches a special init action, which ensures taking the initial state. How it works? It's simple. Your reducers won't react on a `@@redux/INIT` action, therefore they return the previous state. Because there is no previous state, the reducer automatically takes the default argument.

#### Reducers

Okay. Now we need a reducer.

```js
const reducer = (state = '', action) =>
  action === 'UPDATE_NAME' ? action.name : state
```

Of course usually you write a bit more complicated reducers with `switch-case` statement. It's practical if you react on multiple actions.

#### Combining reducers

What if we'd like to combine multiple reducers into one root reducer? Suppose that we have the following state:

```js
{
  inProgress: Boolean,
  name: String
}
```

We'd like to separate them into two reducers. One for `inProgress` and one for `name`. Then we have an `inProgress` reducer and a `nameReducer`. Redux provides a `combineReducers` function, you probably know it already.

```js
const rootReducer = combineReducers({
  inProgress: inProgressReducer,
  name: nameReducer
})
```

How it works? There is no magic. You can imagine like that:

```js
const rootReducer = (state, action) => ({
  inProgress: inProgressReducer(state.inProgress, action),
  name: nameReducer(state.name, action)
})
```

The slices of the state and the related reducers take the proper substate, what they need, and the action as arguments. Of course they get every action, but they will react on those action, in which they are interested. If they get disinterested actions, they return the same (previous) state. So just those reducers will work, which should react on the action.

#### Connecting components to the state

The simplest way to connect the application to the store's state is subscribe the entire application to the store, and pass the whole state there:

```jsx
store.subscribe(() => ReactDOM.render(<App state={store.getState()}/>))
```

But it's not too efficient. The entire application need to rerender on every state change. Of course you can avoid unnecessary rerenders in the components with `shouldComponentUpdate` lifecycle method, but it's still really inefficient.

The best way to connect the state to the components is that every component - which needs some state - will be connected to the store separately.

```js
import { connect } from 'redux'

connect(state => ({ name: state.name }), { updateName })(NameInput)
```

Notice, that the `connect` function's signature is a decorator-like signature:

```
(mapStateToProps, mapDispatchToProps) => component => container
```

So the reason behind the curry is this consideration, that we can use them as decorators.

```js
@connect(state => ({ name: state.name }), { updateName })
class NameInput extends React.Component {
  ...
}
```

How it works? The `connect` function wraps your component into an outer component and returns this container. The container wraps your actions with the `dispatch` function and pass them to your component as props. It subscribes to the store change and persists the return value of the `mapStateToProps` into its local state, which is forwarded to your component as props.

#### StoreProvider

These containers takes the store instance from the [context](https://reactjs.org/docs/context.html) provided by the `react-redux`'s [Provider](https://github.com/reduxjs/react-redux/blob/HEAD/docs/api.md#provider-store) component, which ensures the store instance to the context for its child components below.

```jsx
<Provider store={store}>
  <App />
</Provider>
```

### Selectors

Selectors are pure functions which takes the store's state as argument and return some data. Selectors usually select a slice of the state, but they are also available to make some computation on the state, eg. some transformation, aggregation, etc.

Very important, that components must be free from any business logic computation or transformation, and also they must be independent from the raw state. The best is when your components take ready-to-display data in their props.

Selectors are the bridge between the application state and the components' input. They also have other advantages, such as:

- They are reusable for building complex selectors.
- They are suitable for unit-testing, because they are pure functions.
- Memoized selectors can avoid unnecessary computations and rerenders.
- They can save us from refactoring components when state structure changes.

Redux developers say, that the business logic live in the reducers, and also in the selectors. Selectors are the opposite way from the data instead of like reducers do, and usually we implement them in a separated file or folder.

Selectors are used mostly at `mapStateToProps`, but we can use them also in thunks.

Suppose, that we have the following state

```js
{
  me: {
    firstName: 'John',
    lastName: 'Smith'
  },
  items: [ 10, 20, 30, 40 ]
}
```

Then we can write the following selectors:

```js
const getMe = state => state.me
const getItems = state => state.items
const getMyName = state => {
  const { firstName, lastName } = getMe(state)
  return `${firstName} ${lastName}`
}
const getSumOfItems = state => {
  const items = getItems(state)
  return items.reduce((sum, item) => sum + item)
}
```

And then we can connect them into components:

```jsx
import { getMyName, getItems, getSumOfItems } from '../selectors'

@connect(state => ({
  name: getMyName(state),
  items: getItems(state),
  sum: getSumOfItems(state)
}))
class extends React.PureComponent {
  render() {
    const { name, items, sum } = this.props
    return <div>
      <h1>My name is: {name}</h1>
      <h2>Sum is: {sum}</h2>
      <ul>
        {items.map((item, i) => <li key={i}>{item}</li>)}
      </ul>
    </div>
  }
}
```

What if the name changes? The container invokes the `mapStateToProps` and it invokes our selectors. The `getMyName` will return the new name, this is ok. But unfortunately `getSumOfItems` will be also invoked and unnecessarily computes the sum of the items again. It does not seem like a big effort, but if the selector does some harder computation, then it could be really inefficient.

#### Reselect

For this purpose the react team provides the [reselect](https://www.npmjs.com/package/reselect) package. How it works?

```js
import { createSelector } from 'reselect'

const getMe = state => state.me
const getItems = state => state.items
const getMyName = createSelector(
  getMe,
  ({ firstName, lastName }) => `${firstName} ${lastName}`
)
const getSumOfItems = createSelector(
  getItems,
  items => items.reduce((sum, item) => sum + item)
)
```

Selectors created by `createSelector` will be memoized selectors, which means they persist the previous return value of their input selectors. If the input selectors do not produce any change, the selector will return the previous value. Therefore the selector runs only when the input data changes.

If you'd like to use more selectors as input data, then you shall use an array of selectors as the first argument:

```js
const getSurface = createSelector(
  [getWidth, getHeight],
  (width, height) => width * height
)
```

#### Parameterized selectors

It seems obvious, that if we need free parameters in our selectors then we make a curry:

```js
const getSumFrom = index => createSelector(
  getItems,
  items => items.slice(index).reduce((sum, item) => sum + item)
)
```

And then:

```js
@connect((state, { index }) => ({ sum: getSumFrom(index)(state) }))
```

But if you look at this a bit deeper, then you could find that this solution misfits the selectors power: the memoization, because this curry will create always a new selector won't keep the previous selector's state.

So how can we deal with this problem? Notice that the signature of `mapStateToProps` looks like this:

```
(state, props) => finalProps
```

So we can use directly the `props` as parameters, or we can pass to the selectors false props as second argument.

```js
const getSumFrom = createSelector(
  [getItems, (_, index) => index],
  (items, index) => items.slice(index).reduce((sum, item) => sum + item)
)
```

And then

```js
@connect((state, { index }) => ({ sum: getSumFrom(state, index) }))
```

or just

```js
@connect((state) => ({ sum: getSumFrom(state, 2) }))
```

If we need more parameters than one, we can use parameter objects.

```js
@connect((state) => ({ sum: getSumFrom(state, { from: 2, to : 7 }) }))
```

### Thunks

#### The extra arguments

### How Repatch works

### The state

Ide vajon mit akartam írni?

## Creating an offline react app

### Testing repatch actions

## Running Docker containers

## Creating a NodeJS app

### Express basics

#### Handlers

#### Middlewares

### Configs

### Graceful startup

### A basic authentication and authorization

### Platfrom-independent services and side-effect handling

### Unit-testing services

#### Mocks and spies

## Creating an online react app

### react-router

### Creating a simple api interface

### Thunks and side-effect handling

### Typing-timer

### Strong- and weak binding

### Unit-testing thunks

## Creating Docker images

## Docker-composing

## AWS

### Deploy containers to ECS

### Continous integration

### Serverless environments and lambdas

## Isomorph React applications

### Next.js

Check the [tutorial](https://learnnextjs.com/) of [Next.js](https://github.com/zeit/next.js/).
