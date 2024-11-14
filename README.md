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
# Step 1:
Clone the repository from GitHub.

# step 2:
Create Django Admin project.

# Step 3:
Create a New App under the Django Admin project.

# Step 4:
Create python programs for views and urls to perform server side processing.

# Step 5:
Create a HTML file to implement form based input and output.

# Step 6:
Publish the website in the given URL.

PROGRAM :
DEVELOPED BY : Kamalesh y
REGISTER NO : 24004024

```
 <html>
<head>
<meta charset='utf-8'>
<meta http-equiv='X-UA-Compatible' content='IE=edge'>
<title>Area of Surface</title>
<meta name='viewport' content='width=device-width, initial-scale=1'>
<style type="text/css">
body {
    background-color: #f10a0af2;
}
.edge {
    width: 100%;
    padding-top: 180px;
    text-align: center;
}
.box {
    display: inline-block;
    border: thick dashed #1a7c74;
    width: 500px;
    min-height: 300px;
    font-size: 20px;
    background-color: rgb(9, 253, 54);
}
.formelt {
    color: rgb(206, 235, 12);
    text-align: center;
    margin-top: 8px;
    margin-bottom: 6px;
}
h1 {
    color: rgb(219, 219, 17);
    padding-top: 20px;
}
</style>
</head>
<body>
<div class="edge">
    <div class="box">
        <h1>Surface Area of Right Cylinder</h1>
        <h3>KAMALESH Y(24004024)</h3>
        <form method="POST">
            % csrf_token %
            <div class="formelt">
                Radius: <input type="text" name="radius" value="r"></input>m<br/>
            </div>
            <div class="formelt">
                Height: <input type="text" name="height" value="h"></input>m<br/>
            </div>
            <div class="formelt">
                <input type="submit" value="Calculate"></input><br/>
            </div>
            <div class="formelt">
                Area: <input type="text" name="area" value="area">m<sup>2</sup><br/>
            </div>
        </form>
    </div>
</div>
</body>
</html>
```
# OUTPUT
![Screenshot 2024-11-14 045624](https://github.com/user-attachments/assets/664d01a3-7c7d-49d8-a7f1-c436392065c4)

# RESULT:
The program for performing server side processing is completed successfully.
