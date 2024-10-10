this is (html )file, that you can make it.
<!DOCTYPE html>
<html lang="en">
<head>
    <link rel="stylesheet" href="clac.css">
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Mosawer Mansour calculator</title>
    
</head>
<body>
<footer></footer>
<div class="calculator">
    <input type="text" id="display" disabled>
    <div class="row">
        <button onclick="appendToDisplay('1')">1</button>
        <button onclick="appendToDisplay('2')">2</button>
        <button onclick="appendToDisplay('3')">3</button>
        <button onclick="appendToDisplay('Math.sqrt(')">√</button>
       
    </div>
    <div class="row">
        <button onclick="appendToDisplay('4')">4</button>
        <button onclick="appendToDisplay('5')">5</button>
        <button onclick="appendToDisplay('6')">6</button>
        <button onclick="appendToDisplay('(')">(</button>
    </div>
    <div class="row">
  
        <button onclick="appendToDisplay('7')">7</button>
        <button onclick="appendToDisplay('8')">8</button>
        <button onclick="appendToDisplay('9')">9</button>
        <button class="operator" onclick="appendToDisplay('**2')">x²</button>
    </div>
    <div class="row">
        <button class="operator" onclick="appendToDisplay('*')">×</button>
        <button onclick="appendToDisplay('0')">0</button>
        <button class="operator" onclick="appendToDisplay('-')">−</button>
        <button onclick="appendToDisplay(')')">)</button>
        
    </div>
    <div class="row">
        <button onclick="appendToDisplay('Math.sin(')">sin</button>
        <button onclick="appendToDisplay('Math.cos(')">cos</button>
        <button onclick="appendToDisplay('Math.tan(')">tan</button>
    
        <button class="operator" onclick="appendToDisplay('/')">÷</button>
       
      
        </div>
        <div class="row">
        <button class="operator" onclick="appendToDisplay('+')">+</button>
        <button class="operator" onclick="calculateResult()">=</button>
            <button class="operator" onclick="clearDisplay()">C</button>
            <button onclick="appendToDisplay('Math.log(')">log</button>
      
         
        </div>

<script>
    function clearDisplay() {
        document.getElementById('display').value = '';
    }

    function appendToDisplay(value) {
        document.getElementById('display').value += value;
    }

    function calculateResult() {
        const display = document.getElementById('display');
        try {
            const result = eval(display.value.replace(/×/g, '*').replace(/÷/g, '/'));
            display.value = result;
        } catch (error) {
            display.value = 'Error';
        }
    }
</script>

</body>
</html>









this is (css) file:
body {
    font-family: Arial, sans-serif;
    background-color: #2c3e50;
    color: #ecf0f1;
    margin: 0;
    padding: 20px;
    justify-self: center;
    align-items: center;
}

.container {
    max-width: 800px;
    margin: auto;
    text-align: center;
}

h1 {
    margin-bottom: 20px;
}

.member {
    background-color: #34495e;
    padding: 15px;
    margin: 10px 0;
    border-radius: 5px;
}

button {
    padding: 10px 15px;
    background-color: #e74c3c;
    border: none;
    color: white;
    border-radius: 5px;
    cursor: pointer;
}

button:hover {
    background-color: #c0392b;
}











