# Ex.08 Design of Interactive Image Gallery
## Date:12.03.2026

## AIM:
To design a web application for an inteactive image gallery with minimum five images.

## DESIGN STEPS:

### Step 1:
Clone the github repository and create Django admin interface.

### Step 2:
Change settings.py file to allow request from all hosts.

### Step 3:
Use CSS for positioning and styling.

### Step 4:
Write JavaScript program for implementing interactivity.

### Step 5:
Validate the HTML and CSS code.

### Step 6:
Publish the website in the given URL.

## PROGRAM :
```
<html>
    <head>
        <title>Intractive Image Gallery</title>
    </head>
    <style>
        body
        {
            background:linear-gradient(45deg,rgb(243, 137, 243),rgb(236, 138, 154),rgb(147, 239, 147));
            text-align: center;
        }
        .header
        {
            background:red;
            color:white;
            padding:15px;
            font-size:20px;
        }
        .container
        {
            display:flex;
            justify-content:center;
            align-items:center;
            height:80vh;
        }
        .card
        {
            background:rgb(232, 196, 129);
            padding:20px;
            border: 5px solid blue;
            border-radius:120px;
            width:350px;  
            height:350px;
        }
        .card img
        {
            width:300px;
            height:250px;
            border: 5px solid red;
            border-radius:120px;
        }
        .caption
        {
            margin-top:10px;
            font-size:20px;
            color:red;
        }
        button
        {
            padding:8px 18px;
            margin:5px;
            border:4px solid red;
            border-radius:10px;
            background:black;
            color:white;
            font-size:14px;
        }
        button:hover
        {
            background:#3b3bb3;
        }
        .footer
        {
            background:cyan;
            color:black;
            padding:10px;
            position:fixed;
            bottom:30;
            width:100%;
            font-size:20px;
        }
    </style>
    <body>
        <div class="header">
            Top 5 Tamil Actor
        </div>
        <div class="container">
            <div class="card">
                <img id="galleryImage" src="5actor.jpg">
                <div class="caption" id="caption">
                    Top 5 Tamil Actor
                </div>
                <div class="buttons">
                    <button onclick="previous()">Previous</button>
                    <button onclick="next()">Next</button>
                </div>
            </div>
            <div class="footer">
                DEEPAK B(25018314)
            </div>
        </div>
        <script>
            let images=[
            {src:"5actor.jpg",caption:"Top 5 Actors"},
            {src:"vijay.jpg",caption:"Vijay"},
            {src:"ajith.png",caption:"Ajith"},
            {src:"Danush1.jpg",caption:"Danush"},
            {src:"Rajini.jpeg",caption:"Rajini"},
            {src:"kamal.jpg",caption:"Kamal"}
            ];
            let index=0;

            function showImage()
            {
                document.getElementById("galleryImage").src = images[index].src;
                document.getElementById("caption").innerText = images[index].caption;
            }
            function next()
            {
                index++;
                if(index >= images.length)
                {
                    index = 0;
                }
                showImage();
            }
            function previous()
            {
                index--;
                if(index < 0)
                {
                index=images.length-1;
                }
                showImage();
            }
        </script>
    </body>
</html>
```
## OUTPUT:
![alt text](<Screenshot (45).png>)

## RESULT:
The program for designing an interactive image gallery using HTML, CSS and JavaScript is executed successfully.
