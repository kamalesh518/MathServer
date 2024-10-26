# Ex.05 Design a Website for Server Side Processing
# Name: Kamalesh y
# Reg no: 24004024
# Date:26.10.2024

AIM:
To design a website to find surface area of a Right Cylinder in server side.

FORMULA:
Surface Area = 2Πrh + 2Πr2
r --> Radius of Right Cylinder
h --> Height of Right Cylinder

DESIGN STEPS:
Step 1:
Clone the repository from GitHub.

Step 2:
Create Django Admin project.

Step 3:
Create a New App under the Django Admin project.

Step 4:
Create python programs for views and urls to perform server side processing.

Step 5:
Create a HTML file to implement form based input and output.

Step 6:
Publish the website in the given URL.

PROGRAM :
DEVELOPED BY : RUDESH KANNA R
REGISTER NO : 24900303

math.html:

<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Lamp Filament Power Calculator</title>
    <style>
        body {
            font-family: Arial, sans-serif;
            background-color: #f0f0f0;
            margin: 0;
            padding: 0;
        }

        .container {
            max-width: 600px;
            margin: 50px auto;
            padding: 20px;
            background-color: #ffffff;
            box-shadow: 0 0 10px rgba(0, 0, 0, 0.1);
            border-radius: 8px;
        }

        h1 {
            text-align: center;
            color: #333;
        }

        .input-group {
            margin-bottom: 20px;
        }

        label {
            display: block;
            font-weight: bold;
            color: #555;
            margin-bottom: 5px;
        }

        input[type="number"] {
            width: 100%;
            padding: 10px;
            border: 1px solid #ccc;
            border-radius: 4px;
        }

        button {
            width: 100%;
            padding: 10px;
            background-color: #007bff;
            color: #fff;
            border: none;
            border-radius: 4px;
            font-size: 16px;
            cursor: pointer;
        }

        button:hover {
            background-color: #0056b3;
        }

        .result {
            margin-top: 20px;
            font-size: 18px;
            text-align: center;
            color: #333;
        }
    </style>
</head>
<body>
    <div class="container">
        <h1>Lamp Filament Power Calculator</h1>
        <div class="input-group">
            <label for="current">Current (I) in Amps:</label>
            <input type="number" id="current" placeholder="Enter current (in Amps)" required>
        </div>
        <div class="input-group">
            <label for="resistance">Resistance (R) in Ohms:</label>
            <input type="number" id="resistance" placeholder="Enter resistance (in Ohms)" required>
        </div>
        <button onclick="calculatePower()">Calculate Power</button>
        <div class="result" id="result"></div>
    </div>

    <script>
        function calculatePower() {
            var current = document.getElementById('current').value;
            var resistance = document.getElementById('resistance').value;
            if (current && resistance) {
                var power = Math.pow(current, 2) * resistance;
                document.getElementById('result').innerHTML = 'Power (P) = ' + power.toFixed(2) + ' Watts';
            } else {
                document.getElementById('result').innerHTML = 'Please enter valid values for current and resistance.';
            }
        }
    </script>
</body>
</html>
views.py:

from django.shortcuts import render
def sqprismarea(request):
    context={}
    context['area'] = "0"
    context['a'] = "0"
    context['h'] = "0"
    if request.method == 'POST':
        print("POST method is used")
        a = request.POST.get('side','0')
        h = request.POST.get('height','0')
        print('request=',request)
        print('side=',a)
        print('height=',h)
        area = 2*int(a)*int(a) + 4*int(a)*int(h)
        context['area'] = area
        context['a'] = a
        context['h'] = h
        print('Area=',area)
    return render(request,'mathapp/math.html',context)
urls.py:

from django.contrib import admin
from django.urls import path
from math import views
urlpatterns = [
    path('admin/', admin.site.urls),
    path('areaofsqprism/',views.sqprismarea,name="areaofsqprism"),
    path('',views.sqprismarea,name="areaofsqprismroot")
]
HOMEPAGE:
Screenshot 2024-10-24 110413

RESULT:
The program for performing server side processing is completed successfully.
