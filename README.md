# Ex.05 Design a Website for Server Side Processing
## Date: 11.12.2024

## AIM:
 To design a website to calculate the power of a lamp filament in an incandescent bulb in the server side. 


## FORMULA:
P = I<sup>2</sup>R
<br> P --> Power (in watts)
<br> I --> Intensity
<br> R --> Resistance

## DESIGN STEPS:

### Step 1:
Clone the repository from GitHub.

### Step 2:
Create Django Admin project.

### Step 3:
Create a New App under the Django Admin project.

### Step 4:
Create python programs for views and urls to perform server side processing.

### Step 5:
Create a HTML file to implement form based input and output.

### Step 6:
Publish the website in the given URL.

## PROGRAM :

<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Lamp Filament Power Calculator</title>
    <style>
        body {
            font-family: Arial, sans-serif;
            margin: 0;
            padding: 0;
            display: flex;
            justify-content: center;
            align-items: center;
            height: 100vh;
            background-color: #f5f5f5;
        }
        .calculator {
            background: #fff;
            padding: 20px;
            border-radius: 8px;
            box-shadow: 0 4px 8px rgba(0, 0, 0, 0.2);
            text-align: center;
            width: 300px;
        }
        .calculator h1 {
            font-size: 20px;
            margin-bottom: 20px;
        }
        .calculator input {
            width: 100%;
            padding: 10px;
            margin: 10px 0;
            border: 1px solid #ccc;
            border-radius: 4px;
            box-sizing: border-box;
        }
        .calculator button {
            width: 100%;
            padding: 10px;
            background-color: #28a745;
            color: white;
            border: none;
            border-radius: 4px;
            font-size: 16px;
            cursor: pointer;
        }
        .calculator button:hover {
            background-color: #218838;
        }
        .result {
            margin-top: 20px;
            font-size: 18px;
            color: #333;
        }
    </style>
</head>
<body>
    <div class="calculator">
        <h1>Power Calculator</h1>
        <label for="intensity">Intensity (I in Amps):</label>
        <input type="number" id="intensity" placeholder="Enter intensity (I)">

        <label for="resistance">Resistance (R in Ohms):</label>
        <input type="number" id="resistance" placeholder="Enter resistance (R)">

        <button onclick="calculatePower()">Calculate Power</button>

        <div class="result" id="result"></div>
    </div>

    <script>
        function calculatePower() {
            const intensity = parseFloat(document.getElementById('intensity').value);
            const resistance = parseFloat(document.getElementById('resistance').value);

            if (isNaN(intensity) || isNaN(resistance)) {
                document.getElementById('result').innerText = "Please enter valid numbers for both Intensity and Resistance.";
                return;
            }

            // Calculate Power using P = I^2 * R
            const power = Math.pow(intensity, 2) * resistance;

            // Display the result
            document.getElementById('result').innerText = `Power (P): ${power.toFixed(2)} Watts`;
        }
    </script>
</body>
</html>



## SERVER SIDE PROCESSING:
![alt text](<Screenshot 2024-12-11 144823.png>)

## HOMEPAGE:
![alt text](<Screenshot 2024-12-11 144111.png>)

## RESULT:
The program for performing server side processing is completed successfully.
