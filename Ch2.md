### Learn to write in React way

const render = () => {
  document.getElementById('mountNode').innerHTML = `
	<div>
    Hello HTML
<input />
 ${(new Date).toLocaleTimeString()} 
  </div>
`;
  ReactDOM.render(
  React.createElement(
    'div', 
    null, 
    'Hello React',
    React.createElement( 'input', null, null),
    React.createElement ('pre', null, (new Date).toLocaleTimeString() ),
  ),
  document.getElementById('mountNode2'),
);
  
}



// 	currentTime: (new Date).toLocaleTimeString()
 setInterval(render, 1000);


