# reacterview
##### Q: What are the advantages of using React app?
> * is multi-thread; a lot of users can interact with this app in the same time (chat apps)
> * components are modulated, easy to debug and reusable
> * comes with developer tooling and ecosystem

##### Q: What is a component
> * component will be part of the page which will have a specific functionality in react and be reusable

##### Q: How do you decide what goes into a single component
> * Well defined and complete functionality which can be reused in other places

##### Q: Difference between statefull and stateless components
> * https://github.com/mariusbanea/web-developers-toolkit/blob/master/react/react-staless-vs-stateful-components.js

##### Q: difference between states and props
> * State is owned by, and can be updated by a particular component. Props are passed to a component from a parent, and cannot be directly updated by the component which receives them. 
https://github.com/mariusbanea/web-developers-toolkit/blob/master/react/react-props-vs-states.jpg

##### Q: How can you work with state in a component? 
> * creating the initial value in a class component constructor or as an instance property
> * you can read state from the instance property
> * you can merge new state in with the `setState` instance method

##### Q:  Differences between HTML and JSX
> * html cannot have functions and variables whereas JSX can

##### Q: What's your process for building a React app?
> * sketch out the basic design
> * determine the component hierarchy using these steps https://github.com/mariusbanea/web-developers-toolkit/blob/master/react/strategy-of-building-a-react-app.md
> * figure out where state goes
> * pass state as props
> * reverse data flow with callback props

##### Q: describe data lifecycle of a React app
> * The logic description is here: https://raw.githubusercontent.com/mariusbanea/web-developers-toolkit/master/react/react-components-lifecycle-expanded.png
> * Applying that logic into code:
>   * constructor
>   * the dom is updated during the rendering 
>   * componentDidMount
>   * componentWillMount

##### Q: What steps do you need to take in order to make an API request from a component, and then display the information which was fetched?
> * The component should make the API request from a method, either due to user interaction or a lifecycle method being triggered. When the server responds to the request, the component should add the fetched data to its state using this.setState. The update to the state will cause the component to re-render, displaying the fetched information. 

> * Example: https://github.com/mariusbanea/thinkful-google-book-search-react/blob/master/src/App.js

##### Q: What do you use for state-management and how is it helpful?
> * Use Context for state management. It's helpful as a mechanism for passing values through a component tree without using props. Instead of passing props through a bunch of components that won't use it, Context takes data outside the normal flow and makes it available for just the components that need it. Unlike Redux and other state management solutions, Context comes built-in with React, so there's no additional set up.

##### Q: What's the difference between a context Provider and Consumer?
> * A provider can provide a context value to a subtree of components
> * A consumer can read a context value using a render prop or `static contextType`

##### Q: What situations would be good to use context?
> * When you have lots of child components at various levels deep in the tree that all need access to the same data.

##### Q: If you need to pass a prop down 1 or 2 levels, is context necessary?
> * Not necessarily, unless you have a large number of components 1 or 2 levels down that all need that data.

##### Q: Can you pass a component instance as a prop to avoid the need for context?
> * Yes, this is called "component composition". Sometimes this is a more elegant solution.

##### Q: How do you handle multiple views in your React apps?
> * Use React Router to define views based on a given path in the URL.

##### Q: Why should you use the Link component rather than an `a` tag?
> * The Link component avoids a trip to the server to fetch the front-end again. Instead the routing takes place entirely on the client side, replacing components as necessary.

##### Q: How to use the form validation in React
> * Set  this.age = React.createRef()  in your constructor
> * Set the prop  ref={this.age}  on your element
> * Call  this.age.current.focus()

##### Q: What is the difference between a controlled and uncontrolled input?
> * The value of a controlled input is stored in the application's state. Whenever the state is updated, the value in the input is updated (and vice-versa). The value of an uncontrolled input is stored in the DOM. It is accessed through a ref, or events fired by the DOM element.

##### Q: How would you redirect from a registration page to another page when a user successfully logs in?
> * Set a piece of state containing the user information when the user logs in. Then in the registration page component have an if statement which renders a Redirect component if the piece of state has been set.

##### Q: What are the PropTypes and the DefaultProps
> * ‘props-types’ library gives us access to the PropTypes object for validating the props on our component
> * We can define rules for our props e.g. by using Component.propTypes = { myProp: PropTypes.string }
> * DefaultProps can be assigned in a similar way
>   * Component.defaultProps = { foo: bar }
>   * DefaultProps get evaluated before PropTypes and get checked by PropTypes

##### ======== Test Related Questions =====

##### Q: What are smoke tests?
> * Quick tests to check that your code is capable of rendering something. It is preliminary testing to reveal simple failures. 
> * Smoke tests are valuable because they take almost no time to write, and give you some initial assurance during development you haven’t broken your code

##### Q: When would you choose to use shallow and full-DOM rendering?
> * When you shallow render a component, you render just one component
> * Shallow rendering ensures that you are only testing the behavior of a single component, and aren’t indirectly testing the behavior of that component’s children 
> * In full DOM rendering, the entire component including its children are rendered into an in-memory DOM. 
> * If the feature you are trying to test uses the following, use DOM rendering rather than shallow rendering
>   * Refs
>   * Lifecycle methods
>   * Directly interacting with DOM APIs

##### ======== Coding challenges =====
#
##### Challenge 1: create a component which is going to take the props from a child component and display them (check the readme file from the repo bellow for the task details)
> Solution 1: https://github.com/mariusbanea/thinkful-react-change-me-button
#
##### Challenge 2: Write a route which will display the relevant component only when you visit /Home and /Child pages (check the readme file from the repo bellow for the task details)
> Solution 2: https://github.com/mariusbanea/thinkful-react-router-practice
#
##### Challenge 3: Create and implement an app using context (check the readme file from the repo bellow for the task details)
> Solution 3: https://github.com/mariusbanea/thinkful-react-context-practice
