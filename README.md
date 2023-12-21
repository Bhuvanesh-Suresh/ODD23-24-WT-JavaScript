# Exp-09 JavaScript
## Exp-09:(i)
## AIM:
To create a form with java script code to calculate electricity bill.
## PROCEDURE:
## STEP 1:
Start define the document as HTML.
## STEP 2:
Open the HTML structure with necessary head and body .Give the script type as text/javascript.
## STEP 3:
Define the function for the program as calc().
## STEP 4:
Give the necessary input that is required for calculating the electricity bill like var prev,curr,units,amt. Get the number for input using document.getElementById.
## STEP 5:
Give the necessary condition using if-else condition. Close the script and head tags.
## STEP 6:
Give the input type in the body of the HTML.
## STEP 7:
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
