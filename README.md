## Name: KEERTHANA S
## Reg No: 212223040092

# Ex04 Simple Calculator - React Project
## Date:

## AIM
To  develop a Simple Calculator using React.js with clean and responsive design, ensuring a smooth user experience across different screen sizes.

## ALGORITHM
### STEP 1
Create a React App.

### STEP 2
Open a terminal and run:
  <ul><li>npx create-react-app simple-calculator</li>
  <li>cd simple-calculator</li>
  <li>npm start</li></ul>

### STEP 3
Inside the src/ folder, create a new file Calculator.js and define the basic structure.

### STEP 4
Plan the UI: Display screen, number buttons (0-9), operators (+, -, *, /), clear (C), and equal (=).

### STEP 5
Create a new file Calculator.css in src/ and add the styling.

### STEP 6
Open src/App.js and modify it.

### STEP 7
Start the development server.
  npm start

### STEP 8
Open http://localhost:3000/ in the browser.

### STEP 9
Test the calculator by entering numbers and operations.

### STEP 10
Fix styling issues and refine content placement.

### STEP 11
Deploy the website.

### STEP 12
Upload to GitHub Pages for free hosting.

## PROGRAM

## Ane.jsx

```
import React, { useState } from "react";
import "./Pm.css"; // Import the CSS

const Calculator = () => {
  const [expression, setExpression] = useState("");
  const [result, setResult] = useState("");

  const handleClick = (value) => {
    if (value === "C") {
      setExpression("");
      setResult("");
    } else if (value === "←") {
      setExpression(expression.slice(0, -1));
    } else if (value === "=") {
      try {
        const res = new Function("return " + expression)();
        setResult(res);
      } catch {
        setResult("Error");
      }
    } else {
      setExpression(expression + value);
    }
  };

  const buttons = [
    "7", "8", "9", "/",
    "4", "5", "6", "*",
    "1", "2", "3", "-",
    "0", ".", "=", "+",
    "C", "←"
  ];

  return (
    <div className="calculator-wrapper">
      <div className="calculator">
        <h2>React Calculator</h2>
        <div className="display">
          <div>{expression || "0"}</div>
          <div className="result">{result !== "" ? "= " + result : ""}</div>
        </div>
        <div className="buttons">
          {buttons.map((btn) => (
            <button key={btn} onClick={() => handleClick(btn)}>
              {btn}
            </button>
          ))}
        </div>
        <footer className="footer">
        <p>Developed by: Keerthana S</p>
        <p>Register Number: 212223040092</p>
      </footer>
      </div>
    </div>
    
  );
};

export default Calculator;
```
## Pm.css
```
/* Full-screen centering */
.calculator-wrapper {
  width: 100vw;
  height: 100vh;
  display: flex;
  flex-direction: column;
  justify-content: center;
  align-items: center;
  background: linear-gradient(to right, #8e9eab, #eef2f3); /* Smooth gradient */
  font-family: 'Segoe UI', Tahoma, Geneva, Verdana, sans-serif;
}

/* Calculator container */
.calculator {
  background: #ffffff;
  border-radius: 20px;
  padding: 30px;
  box-shadow: 0px 8px 30px rgba(0, 0, 0, 0.2);
  width: 320px;
  text-align: center;
  border: 3px solid #4b4b4b;
}

/* Heading */
.calculator h2 {
  margin-bottom: 20px;
  color: #2f2f2f;
}

/* Display area */
.display {
  background: #222;
  color: #0f0;
  padding: 15px;
  font-size: 22px;
  text-align: right;
  border-radius: 10px;
  margin-bottom: 15px;
  border: 2px solid #0f0;
}

/* Result */
.result {
  color: #00ff99;
  font-weight: bold;
  font-size: 20px;
  margin-top: 5px;
}

/* Buttons grid */
.buttons {
  display: grid;
  grid-template-columns: repeat(4, 1fr);
  gap: 12px;
}

/* Button styles */
.buttons button {
  padding: 18px;
  font-size: 18px;
  border: none;
  border-radius: 10px;
  background-color: #6c5ce7;
  color: white;
  cursor: pointer;
  transition: all 0.3s ease;
}

.buttons button:hover {
  background-color: #a29bfe;
  transform: scale(1.05);
}

/* Footer info */
.footer {
  margin-top: 25px;
  text-align: center;
  font-size: 16px;
  color: #2f2f2f;
  font-weight: 600;
}

```

## OUTPUT

![Screenshot 2025-05-16 212224](https://github.com/user-attachments/assets/bcb22b9c-cf5c-49af-a70f-f877cfa49afe)

## RESULT
The program for developing a simple calculator in React.js is executed successfully.
