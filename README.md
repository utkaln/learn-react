# learn-react

### React Community
* Reactiflux - [reactiflux](https://www.reactiflux.com), [github](https://github.com/reactiflux/reactiflux.com)
* Microsoft React Libraries - [github](https://github.com/microsoft/fluentui/wiki/Getting-Started-with-UI-Fabric)
* Material-ui [material-ui](https://material-ui.com)
* React Bootstrap [github](https://react-bootstrap.github.io)
* Awesome react repo on [github](https://github.com/enaqx/awesome-react)

### Ecosystem
* Router - React Router
* Complex Dataflow - Redux, Mobx
* Automated Testing - Jest, Mocha
* Restful API - GraphQL
* Serverside using Node - Next.js
* Http - Fetch, Axios
* I18n - react-intl
* form validation - react-forms
* CLI - create-react-app



### Resources:
[Chapter wise Experiments from Pluralsight](jscomplete.com/playground/rgs1.1) 


### Why React
* React is better because it uses virtual DOM, instead of letting the html structure being pushed out from server, it is dynamically generated from the JS on the page
> Updating DOM is hard, and DOM is the one that makes the html render slow even though js was fast
> Virtual DOM allows to compare for only change and render
> The whole of react library to packaged only takes about 35KB space in the codebase 

  
  
### Tradeoffs (Important for Decision making)

| Others | React |
|--------|-------|
| Framework | Library | 
| Concise | Explicit | 
| Template centric | JS centric |
| Separate Templates | Single File |
| Standard web components | Non-standard | 

  * React is a library not framework, unlike Angular. Framework helps with easy setup, but library has advantage in being smaller size. Being small, it can be changed small component in any existing non-react pages
  * React requires explicit association instead of concise or implicit association as done in angular. Angular code becomes smaller, but React allows more control
  * React is javascript focused compared to that of template centric. Angular has template to enhance the html for dynamism. But React uses power of JS to make html work
  
  Example of IF block (Angular uses template defined for angular where as React uses regular JS)
  > angular
  ```ts
  <h1 *ngIf="isAdmin"> Hi Admin </h1>
  ```
  > react: text within h1 will show only when isAdmin is True
  
  ```JSX
  {isAdmin && <h1>Hi Admin</h1>
  ```
  
 Example of For loop (Angular uses its for loop template, React uses javascript map function and arrow function)
 > angular
 ```ts
  <div *ngFor = "let user of users">{{user.name}}</div>
  ```
  > react
  ```JSX
  users.map(user => <div>{user.name}</div>)
  ```
  *   React uses single file for Model, View and Controller (JS and JSX) in contrast with others. It manages cocerns of separations are taken care by html components such as button, datepicker, accordion and text box etc.

* React is non-standard library as compared to web component standards. the standards comprise of templates, custom elements, shadow DOM for styles, imports. 

### Limitations
* JSX differs from HTML somewhat
* Build step
* Version conflict compared to different versions being compatible with standard web components
* Online content has outdated contents too, so older syntaxes are found often
* Lack of template and with lot of decisions to make with libraries can be exhausting. This can be dealt with following
  * boilerplate projects are available such as <strong> create-react-app, next.js </strong>
* Decision to declar as Class or Function - Function better as syntax is more concise
* Types: prop types, type script, flow
  * prop types - checks types at runtime, more js like syntax (preferred)
  * type script - checks at compile time, more java like syntax (second preferred)
  * flow - type safety via java annotations
* State Management: app's data
  * Plain React: components handle state by themselves, hence most others are options
  * Flux: centralizes state
  * Redux: centralized, and immutable data store
  * Mob X: lightweight, observable state (less code)
* Styling: off the shelf is good enough


### Components
Fundamental units of react. Each component is responsible for an element in DOM.

#### Component | Props | State | Render | Virtual DOM


### Starter Elements
index.js starts looking for the following line to start rendering the DOM. All code should go to a class or function (preferred)
```JSX
ReactDOM.render(<Hello/>, document.getElementById("root"));

```

A starter function description. props is the property through which parameters can be sent encapsulated in an object
```JSX
function Hello(props){
  return <h1> Hello World </h1>;
}

```

### Useful Tips:

* React uses JSX extension and not HTML. Babel is used to convert JSX to JS on the browser
* TypeScript is another language that can 
* Component names must start with Upper case
* Prefer function over class
* Prefer props over state
* Use parent function to show multiple components at one display, use <div> tag or <> to create hierarchy  
* Props is a parameter that is passed from parent to child component, particularly to send state objects
* useState object to get handle for get and set called a hook in react, initialized with 0

```JSX
const [counter, setCounter] = userState(0)
```
* Labels rendered can take dynamic value, Example below:N

```JSX
function Button() { 
  const [counter, setCounter] = useState(0);  
  return <button onClick={() => setCounter(counter+1)} > {counter}</button>; 
}
```


### Mapping of HTML element with JSX
> HTML
```html
  <label for="name" class="header" style="background-color: yellow"> Display Text </label>
```
  
> JSX
```JSX
  <label htmlFor="name" className="highlight" style={{backgroundColor: "yellow"}}> Display Text </label> 
```
  
  * HTML expects a css element for the label <b>style</b>  <b> Vs. </b> JSX expects json like structure for style
  
  
=============
# Getting Started with Create React App

This project was bootstrapped with [Create React App](https://github.com/facebook/create-react-app).

## Available Scripts

In the project directory, you can run:

### `npm start`

Runs the app in the development mode.\
Open [http://localhost:3000](http://localhost:3000) to view it in the browser.

The page will reload if you make edits.\
You will also see any lint errors in the console.

### `npm test`

Launches the test runner in the interactive watch mode.\
See the section about [running tests](https://facebook.github.io/create-react-app/docs/running-tests) for more information.

### `npm run build`

Builds the app for production to the `build` folder.\
It correctly bundles React in production mode and optimizes the build for the best performance.

The build is minified and the filenames include the hashes.\
Your app is ready to be deployed!

See the section about [deployment](https://facebook.github.io/create-react-app/docs/deployment) for more information.

### `npm run eject`

**Note: this is a one-way operation. Once you `eject`, you can’t go back!**

If you aren’t satisfied with the build tool and configuration choices, you can `eject` at any time. This command will remove the single build dependency from your project.

Instead, it will copy all the configuration files and the transitive dependencies (webpack, Babel, ESLint, etc) right into your project so you have full control over them. All of the commands except `eject` will still work, but they will point to the copied scripts so you can tweak them. At this point you’re on your own.

You don’t have to ever use `eject`. The curated feature set is suitable for small and middle deployments, and you shouldn’t feel obligated to use this feature. However we understand that this tool wouldn’t be useful if you couldn’t customize it when you are ready for it.

## Learn More

You can learn more in the [Create React App documentation](https://facebook.github.io/create-react-app/docs/getting-started).

To learn React, check out the [React documentation](https://reactjs.org/).

### Code Splitting

This section has moved here: [https://facebook.github.io/create-react-app/docs/code-splitting](https://facebook.github.io/create-react-app/docs/code-splitting)

### Analyzing the Bundle Size

This section has moved here: [https://facebook.github.io/create-react-app/docs/analyzing-the-bundle-size](https://facebook.github.io/create-react-app/docs/analyzing-the-bundle-size)

### Making a Progressive Web App

This section has moved here: [https://facebook.github.io/create-react-app/docs/making-a-progressive-web-app](https://facebook.github.io/create-react-app/docs/making-a-progressive-web-app)

### Advanced Configuration

This section has moved here: [https://facebook.github.io/create-react-app/docs/advanced-configuration](https://facebook.github.io/create-react-app/docs/advanced-configuration)

### Deployment

This section has moved here: [https://facebook.github.io/create-react-app/docs/deployment](https://facebook.github.io/create-react-app/docs/deployment)

### `npm run build` fails to minify

This section has moved here: [https://facebook.github.io/create-react-app/docs/troubleshooting#npm-run-build-fails-to-minify](https://facebook.github.io/create-react-app/docs/troubleshooting#npm-run-build-fails-to-minify)
=======
