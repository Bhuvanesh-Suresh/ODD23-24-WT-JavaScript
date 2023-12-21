# Exp-09 JavaScript
## Exp-09:(i)
## AIM:
To create a form with java script code to calculate electricity bill.
## PROCEDURE:
### STEP 1:
Start define the document as HTML.
### STEP 2:
Open the HTML structure with necessary head and body .Give the script type as text/javascript.
### STEP 3:
Define the function for the program as calc().
### STEP 4:
Give the necessary input that is required for calculating the electricity bill like var prev,curr,units,amt. Get the number for input using document.getElementById.
### STEP 5:
Give the necessary condition using if-else condition. Close the script and head tags.
### STEP 6:
Give the input type in the body of the HTML.
### STEP 7:
End the HTML structure.
## PROGRAM:
```
<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8">
  <meta name="viewport" content="width=device-width, initial-scale=1.0">
  <title>Electricity Bill Calculator</title>
  <style>
    body {
      font-family: Arial, sans-serif;
      margin: 20px;
    }
    form {
      max-width: 400px;
      margin: 0 auto;
    }
  </style>
</head>
<body>

  <h2>Electricity Bill Calculator</h2>

  <form id="electricityForm">
    <label for="units">Enter Units Consumed:</label>
    <input type="number" id="units" name="units" required>

    <label for="rate">Enter Rate per Unit:</label>
    <input type="number" id="rate" name="rate" required>

    <button type="button" onclick="calculateBill()">Calculate Bill</button>
  </form>

  <h3>Result:</h3>
  <p id="result"></p>

  <script>
    function calculateBill() {
      // Get input values
      var units = parseFloat(document.getElementById('units').value);
      var rate = parseFloat(document.getElementById('rate').value);

      // Calculate bill
      var billAmount = units * rate;

      // Display result
      document.getElementById('result').innerHTML = "Your electricity bill is: ₹" + billAmount.toFixed(2);
    }
  </script>

</body>
</html>
```
## OUTPUT:
![1 html js ss](https://github.com/Bhuvanesh-Suresh/ODD23-24-WT-JavaScript/assets/145742661/b3e30705-e9c0-46c2-93e3-203e8f9b4a90)
## RESULT:
Thus the java code executed to calculate the electricity bill.
## Exp-09:(ii)
## AIM:
To create a form with java script code to compute the factorial of a given number without recursion.
## PROCEDURE:
### STEP 1:
Start define the document as HTML.
### STEP 2:
Open the HTML structure with necessary head and body .Give the script type as text/javascript.
### STEP 3:
Define the function for the program as show().
### STEP 4:
Give the necessary input that is require to compute the factorial like var i, n, fact. Get the number for input using document.getElementById.
### STEP 5:
Using for-loop condition calculate the factorial. Close the script and head tags.
### STEP 6:
Give the input type in the body of the HTML.
### STEP 7:
End the HTML structure.
## PROGRAM:
```
<!DOCTYPE html>
<html lang="en">
<head>
 <meta charset="UTF-8">
 <meta name="viewport" content="width=device-width, initial-scale=1.0">
 <title>Factorial Calculator</title>
</head>
<body>

 <h2>Factorial Calculator</h2>

 <form>
   <label for="number">Enter a Number:</label>
   <input type="number" id="number" required>

   <button type="button" onclick="calculateFactorial()">Compute Factorial</button>
 </form>

 <h3>Result:</h3>
 <p id="result"></p>

 <script>
   function calculateFactorial() {
     var number = parseInt(document.getElementById('number').value);

     if (isNaN(number)) {
       alert("Please enter a valid number.");
       return;
     }

     var factorial = 1;
     for (var i = 2; i <= number; i++) {
       factorial *= i;
     }

     document.getElementById('result').innerHTML = "Factorial: " + factorial;
   }
 </script>

</body>
</html>
```
## OUTPUT:
![2 html js ss](https://github.com/Bhuvanesh-Suresh/ODD23-24-WT-JavaScript/assets/145742661/28640dda-0f78-4ce4-b27e-74457d8f530f)
## RESULT:
Thus the java code executed to compute the factorial of a given number without recursion.
## Exp-09:(iii)
## AIM:
To construct a JavaScript code to generate ‘N’ prime numbers.
## PROCEDURE:
### STEP 1:
Start define the document as HTML.
### STEP 2:
Open the HTML structure with necessary head and body .Give the script type as text/javascript.
### STEP 3:
Define the function for the program as show().
### STEP 4:
Give the necessary input that is required to construct a java code to generate ‘N’ prime numbers . Get the number for input using document.getElementById.
### STEP 5:
Using for-loop condition generate ‘N’ prime numbers. Close the script and head tags.
### STEP 6:
Give the input type in the body of the HTML.
### STEP 7:
End the HTML structure.
## PROGRAM:
```
<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8">
  <meta name="viewport" content="width=device-width, initial-scale=1.0">
  <title>Prime Number Generator</title>
</head>
<body>

  <h2>Prime Number Generator</h2>

  <form>
    <label for="count">Enter the number of primes (N):</label>
    <input type="number" id="count" required>

    <button type="button" onclick="generatePrimes()">Generate Primes</button>
  </form>

  <h3>Prime Numbers:</h3>
  <p id="result"></p>

  <script>
    function isPrime(num) {
      for (let i = 2; i < num; i++) {
        if (num % i === 0) {
          return false;
        }
      }
      return num > 1;
    }

    function generatePrimes() {
      var count = parseInt(document.getElementById('count').value);
      var primes = [];
      var num = 2;

      while (primes.length < count) {
        if (isPrime(num)) {
          primes.push(num);
        }
        num++;
      }

      document.getElementById('result').innerHTML = primes.join(', ');
    }
  </script>

</body>
</html>
```
## OUTPUT:
![3 html js ss](https://github.com/Bhuvanesh-Suresh/ODD23-24-WT-JavaScript/assets/145742661/7ceab82b-52f7-449f-94eb-bf07bb88fc88)
## RESULT:
Thus the java code executed to construct a JavaScript code to generate ‘N’ prime numbers.
## Exp-09:(iv)
## AIM:
To construct a JavaScript program to implement a simple calculator.
## PROCEDURE:
### STEP 1:
Start define the document as HTML.
### STEP 2:
Open the HTML structure with necessary head and body .Give the script type as text/javascript.
### STEP 3:
Define the function for the program as function f1() for addition, function f2() for subtraction, function f3() for multiplication, function f4() for division, function f5() for sin(a), function f6() for cos(a) ,function f7() for tan(a), function f8() for a*a , function f9() for clear.
### STEP 4:
Give the necessary input that is required to implement a simple calculator. Get the number for input using document.getElementById.
### STEP 5:
Close the script and head tags.
### STEP 6:
Give the input type in the body of the HTML.
### STEP 7:
End the HTML structure.
## PROGRAM:
```
<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8">
  <meta name="viewport" content="width=device-width, initial-scale=1.0">
  <title>Simple Calculator</title>
  <style>
    body {
      font-family: Arial, sans-serif;
      text-align: center;
    }
    input {
      width: 50px;
      margin: 5px;
    }
  </style>
</head>
<body>

  <h2>Simple Calculator</h2>

  <form>
    <input type="text" id="result" readonly>
    <br>
    <button type="button" onclick="appendToResult('1')">1</button>
    <button type="button" onclick="appendToResult('2')">2</button>
    <button type="button" onclick="appendToResult('3')">3</button>
    <button type="button" onclick="appendToResult('+')">+</button>
    <br>
    <button type="button" onclick="appendToResult('4')">4</button>
    <button type="button" onclick="appendToResult('5')">5</button>
    <button type="button" onclick="appendToResult('6')">6</button>
    <button type="button" onclick="appendToResult('-')">-</button>
    <br>
    <button type="button" onclick="appendToResult('7')">7</button>
    <button type="button" onclick="appendToResult('8')">8</button>
    <button type="button" onclick="appendToResult('9')">9</button>
    <button type="button" onclick="appendToResult('*')">*</button>
    <br>
    <button type="button" onclick="appendToResult('0')">0</button>
    <button type="button" onclick="clearResult()">C</button>
    <button type="button" onclick="calculateResult()">=</button>
    <button type="button" onclick="appendToResult('/')">/</button>
  </form>

  <script>
    function appendToResult(value) {
      document.getElementById('result').value += value;
    }

    function clearResult() {
      document.getElementById('result').value = '';
    }

    function calculateResult() {
      var result = eval(document.getElementById('result').value);
      document.getElementById('result').value = result;
    }
  </script>

</body>
</html>
```
## OUTPUT:
![4 html js ss](https://github.com/Bhuvanesh-Suresh/ODD23-24-WT-JavaScript/assets/145742661/543ce7d3-bfb3-46c7-840f-3121d720d985)
## RESULT:
Thus the java code executed to implement a simple calculator.
## Exp-09:(v)
## AIM:
To design a simple text editor JavaScript application where we can manipulate the user input in different styles, edit the input, capitalize, and many string operations.
## PROCEDURE:
### STEP 1:
Start define the document as HTML.



