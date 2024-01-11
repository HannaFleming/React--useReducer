useReducer
![image](https://github.com/HannaFleming/React--useReducer/assets/124400864/9b36eff0-822c-439d-a60c-f3861fb5176b)

```
import { useReducer } from 'react';
import './App.css';


function reducer (state, action){
  switch (action.type){
    case 'ADD':return {count:state.count + 1 };
    case 'SUBSTRACT' : return { count: state.count -1 };
    default: return state;
}}

function App() {

const [state, dispatch] = useReducer(reducer, {count:0})


  return (
    <div className="App">
      <p>{state.count}</p>
      <button onClick={()=>dispatch ({type:'ADD'})}>ADD</button>
      <button onClick={()=>dispatch ({type:'SUBSTRACT'})}>SUBSTRACT</button>

    </div>
  );
 }

export default App;

```
https://github.com/HannaFleming/React--useReducer/assets/124400864/0f308c45-270d-4100-b665-0c8a842e6866



Exaple #2 "Multiply/Divide"

```
import { useReducer } from 'react';
import './App.css';


function reducer (state, action) {
  switch (action.type) {
    case 'multiply':return { count:state.count * 5 };
    case 'divide':return { count:state.count / 5};
    default: return state;
  }
}

function App() {

  const [state, dispatch] = useReducer (reducer, {count: 5 })



  return (
    <div className="App">

      <p>{state.count}</p>
      <button onClick={()=> dispatch({type:"multiply"})}>Multiply</button>
      <button onClick={()=> dispatch({type:"divide"})}>Divide</button>

    </div>
  );
 }

export default App;

```
https://github.com/HannaFleming/React--useReducer/assets/124400864/be15a23f-5964-411b-9715-fcb9c952dbcd


