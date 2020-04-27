Ch1 Codes
` function Hello() {
	return <div>Hello React!</div>;
}

//function Button() {
  //return <button>TEST</button>
//}
function Button(props) {

  return( 
  <button onClick= {props.handleClick} >
    Double
  </button>
    );
}

// function for display
function Display(props) {
  return (
    <div> {props.message} </div>
  );
}

function App() {
  const [counter, setCounter] = useState(1);
  const handleClick = () => setCounter(counter+counter);
  return (
  <>
  <Button handleClick={handleClick} />
    <Display message={counter}/>
    </>
  );
}


ReactDOM.render(
  <App />,
  document.getElementById('mountNode'),
); `
