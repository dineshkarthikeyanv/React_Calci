# Ex04 Simple Calculator - React Project
## Date:02-09-2026
## Name : V DINESHKARTHIKEYAN
## Reg No :212225230060

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
index.html
```h
<!DOCTYPE html>
<html lang="en">
<head>
<meta charset="UTF-8">
<meta name="viewport" content="width=device-width, initial-scale=1.0">
<title>Simple Calculator</title>
<link rel="stylesheet" href="style.css">
</head>
<body>
  <h1>Simple Calculator</h1>
  <div class="calculator">
    <input type="text" class="screen" id="screen" readonly>
    <div class="buttons">
      <button onclick="press('7')">7</button>
      <button onclick="press('8')">8</button>
      <button onclick="press('9')">9</button>
      <button onclick="press('/')">/</button>
      <button onclick="press('4')">4</button>
      <button onclick="press('5')">5</button>
      <button onclick="press('6')">6</button>
      <button onclick="press('*')">*</button>
      <button onclick="press('1')">1</button>
      <button onclick="press('2')">2</button>
      <button onclick="press('3')">3</button>
      <button onclick="press('-')">-</button>
      <button onclick="press('0')">0</button>
      <button class="clear" onclick="clearScreen()">C</button>
      <button class="equal" onclick="calcEqual()">=</button>
      <button onclick="press('+')">+</button>
    </div>
  </div>

  <script src="script.js"></script>
</body>
</html>
```
style.css
```c
body {
  background: #0a0a0a;
  margin: 0;
  font-family: Arial, sans-serif;
}

h1 {
  text-align: center;
  color: #ff1a1a;
  background: #0a0a0a;
  padding: 20px 0;
  margin: 0;
  letter-spacing: 1px;
}

.calculator {
  width: 320px;
  margin: 40px auto;
  background: #111;
  border: 1px solid #b30000;
  border-radius: 16px;
  padding: 20px;
  box-shadow: 0 8px 28px rgba(255, 0, 0, 0.25);
}

.screen {
  width: 100%;
  height: 60px;
  font-size: 28px;
  text-align: right;
  padding: 10px 15px;
  box-sizing: border-box;
  border: 1px solid #660000;
  border-radius: 8px;
  background: #000;
  color: #ff3333;
  margin-bottom: 15px;
}

.buttons {
  display: grid;
  grid-template-columns: repeat(4, 1fr);
  gap: 10px;
}

.buttons button {
  padding: 20px 0;
  font-size: 18px;
  border: 1px solid #330000;
  border-radius: 10px;
  background: #1c1c1c;
  color: #fff;
  cursor: pointer;
  transition: 0.2s ease;
}

.buttons button:hover {
  background: #b30000;
  border-color: #ff1a1a;
}

.buttons button:active {
  background: #ff1a1a;
  border-color: #fff;
  transform: scale(0.94);
}

.buttons button.equal {
  background: #cc0000;
  border-color: #ff1a1a;
}

.buttons button.equal:hover {
  background: #ff1a1a;
}

.buttons button.equal:active {
  background: #ff4d4d;
  transform: scale(0.94);
}

.buttons button.clear {
  background: #330000;
  color: #ff4d4d;
}

.buttons button.clear:hover {
  background: #4d0000;
}

.buttons button.clear:active {
  background: #ff1a1a;
  color: #fff;
  transform: scale(0.94);
}

@media (max-width: 400px) {
  .calculator {
    width: 90%;
  }
  .buttons button {
    padding: 16px 0;
    font-size: 16px;
  }
}
```
script.js
```j
const screen = document.getElementById('screen');

function press(value) {
  screen.value += value;
}

function clearScreen() {
  screen.value = '';
}

function calcEqual() {
  try {
    screen.value = eval(screen.value).toString();
  } catch (error) {
    screen.value = 'Error';
  }
}
```
## OUTPUT
<img width="1920" height="1080" alt="Screenshot (394)" src="https://github.com/user-attachments/assets/2cbf041f-745b-40f1-a9d1-480af2662024" />


## RESULT
The program for developing a simple calculator in React.js is executed successfully.
