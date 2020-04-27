# learn-react
Resources:
[Chapter wise Experiments from Pluralsight](jscomplete.com/playground/rgs1.1) 

* React is better because it uses virtual DOM, instead of letting the html structure being pushed out from server, it is dynamically generated from the JS on the page

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
  
  



