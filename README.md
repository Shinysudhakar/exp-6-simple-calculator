# EXP 06 - SIMPLE CALCULATOR USING REACT JS

## AIM:
To create a simple calculator using react js

## SOFTWARE:
Visual Studio Code

## ALGORITHM:

1) Set up the React environment: Install Node.js and create a new React project using create-react-app. Open your terminal or command prompt and run the following commands
2) Open the project in your preferred code editor.
3) Replace the contents of 'src/App.js" with the following code
4) Replace the contents of "src/App.css" with the following CSS styles
5) Start the development server: In the terminal, run npm start to start the React development server.
6) Open your browser and visit http://localhost:3000 to see the calculator.

## PROGRAM:

### APP.JS
```
java
import React, { useState } from 'react';
import './App.css';

function App() {
  const [result, setResult] = useState('');

  const handleClick = (value) => {
    setResult(result + value);
  };

  const calculate = () => {
    try {
      setResult(eval(result).toString());
    } catch (error) {
      setResult('Error');
    }
  };

  const clear = () => {
    setResult('');
  };

  return (
    <div className="App">
      <br></br>
      <br></br>
      <h2><u>SIMPLE CALCULATOR</u></h2>
      <br></br>
      <div className="calculator">
        <input type="text" value={result} readOnly />
        <div className="keypad">
          <button onClick={() => handleClick('9')}>9</button>
          <button onClick={() => handleClick('8')}>8</button>
          <button onClick={() => handleClick('7')}>7</button>
          <button onClick={() => handleClick('6')}>6</button>
          <button onClick={() => handleClick('5')}>5</button>
          <button onClick={() => handleClick('4')}>4</button>
          <button onClick={() => handleClick('3')}>3</button>
          <button onClick={() => handleClick('2')}>2</button>
          <button onClick={() => handleClick('1')}>1</button>
          <button onClick={() => handleClick('+')}>+</button>
          <button onClick={() => handleClick('0')}>0</button>
          <button onClick={() => handleClick('-')}>-</button>
          <button onClick={() => handleClick('*')}>*</button>
          <button onClick={clear}>C</button>
          <button onClick={() => handleClick('/')}>/</button>
          <button onClick={() => handleClick('.')}>.</button>
          <button onClick={calculate}>=</button>
        </div>
      </div>
    </div>
  );
}

export default App;
```
### APP.CSS:
```
java
.App {
  text-align: center;
}

.calculator {
  width: 200px;
  margin: 0 auto;
  padding: 35px;
  border: 2px solid #f77e7e;
  border-radius: 5px;
  
}

input[type='text'] {
  width: 100%;
  margin-bottom: 20px;
  padding: 5px;
  font-size: 16px;
}

.keypad button {
  width: 50px;
  height: 30px;
  margin: 2px;
  font-size: 16px;
  cursor: pointer;
}
```

## OUTPUT:

### IDLE:

<img width="362" alt="image" src="https://github.com/Monisha-11/SIMPLE-CALCULATOR-USING-REACT-JS/assets/93427240/12a41534-ca5f-479d-b65f-b1930ec3c788">

### CALCLUTION:

<img width="340" alt="image" src="https://github.com/Monisha-11/SIMPLE-CALCULATOR-USING-REACT-JS/assets/93427240/f976d357-0f63-4b0a-a0f5-6f337aa50db3">

<img width="325" alt="image" src="https://github.com/Monisha-11/SIMPLE-CALCULATOR-USING-REACT-JS/assets/93427240/55fb6cf8-e0ec-4e88-bc2c-6765fa5459cd">

## RESULT:
Thus the simple calculator using react js.
