# learn-react

## React Community
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



## Resources:
[Chapter wise Experiments from Pluralsight](jscomplete.com/playground/rgs1.1) 


### Why React
* React is better because it uses virtual DOM, instead of letting the html structure being pushed out from server, it is dynamically generated from the JS on the page
> Updating DOM is hard, and DOM is the one that makes the html render slow even though js was fast
> Virtual DOM allows to compare for only change and render
> The whole of react library to packaged only takes about 35KB space in the codebase 

* Entry point element
`document.getElementById(‘mountNode’)`

* React uses JSX extension and not HTML. Babel is used to convert JSX to JS on the browser
* Component names must start with Upper case
* useState object to get handle for get and set called a hook in react, initialized with 0
`const [counter, setCounter] = userState(0)`
* Labels rendered can take dynamic value, Example below:

`function Button() {` 
  `const [counter, setCounter] = useState(0);`  
  `return <button onClick={() => setCounter(counter+1)} >{counter}</button>;`  
`}`  

* Use parent function to show multiple components at one display, use <div> tag or <> to create hierarchy
  
  * Props is a parameter that is passed from parent to child component, particularly to send state objects
  
  



