# Temperature-
<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8">
  <meta name="viewport" content="width=device-width, initial-scale=1.0">
  <title>Temperature Converter</title>
  <style>
    body {
      font-family: Arial, sans-serif;
      text-align: center;
      margin: 50px;
    }

    #converter {
      display: inline-block;
      padding: 20px;
      border: 1px solid #ccc;
      border-radius: 10px;
      box-shadow: 0 0 10px rgba(0, 0, 0, 0.1);
    }

    input {
      padding: 8px;
      margin-bottom: 10px;
      width: 200px;
    }

    button {
      padding: 10px;
      background-color: #4CAF50;
      color: white;
      border: none;
      border-radius: 5px;
      cursor: pointer;
    }

    #result {
      margin-top: 20px;
    }
  </style>
</head>
<body>

  <div id="converter">
    <h2>Temperature Converter</h2>
    <label for="celsius">Celsius:</label>
    <input type="number" id="celsius" placeholder="Enter Celsius">

    <br>

    <label for="fahrenheit">Fahrenheit:</label>
    <input type="number" id="fahrenheit" placeholder="Enter Fahrenheit">

    <br>

    <button onclick="convert()">Convert</button>

    <div id="result"></div>
  </div>

  <script>
    function convert() {
      var celsius = document.getElementById("celsius").value;
      var fahrenheit = document.getElementById("fahrenheit").value;

      if (celsius !== "") {
        fahrenheit = (celsius * 9/5) + 32;
        document.getElementById("fahrenheit").value = fahrenheit;
        document.getElementById("result").innerText = celsius + " Celsius is " + fahrenheit + " Fahrenheit.";
      } else if (fahrenheit !== "") {
        celsius = (fahrenheit - 32) * 5/9;
        document.getElementById("celsius").value = celsius;
        document.getElementById("result").innerText = fahrenheit + " Fahrenheit is " + celsius + " Celsius.";
      } else {
        document.getElementById("result").innerText = "Please enter a value.";
      }
    }
  </script>

</body>
</html>
