# Ex.08 Design of Interactive Image Gallery
## Date:17/12/2024

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
gallery.html
<!DOCTYPE html>
<html lang="en">

<head>

    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
   
    <style>
        body {
           
            background-image: url('bgg.png');
            background-repeat: no-repeat;
            background-size: cover;
        }

        header {
            
            font-size: 30px;
            font-family: fantasy;
            letter-spacing: 1px;
            color: white+6;
            background-color: orangered;
            text-align: center;
           
           
        }

        div img {
            width: 225px;
            height: 225px;
            cursor: pointer;
            border-radius: 10px;
        }
        .img{
            overflow: hidden;
        }
        div{
            transition: 0.25s;
        }

        div :hover {
            transform: scale(1.1);
            border-radius: 10px;
        }
        
        
        .col1 {
            display: flex;
            gap: 30px;
            margin-top: 30px;
            justify-content: center;
        }
        .col2 {
            display: flex;
            gap: 30px;
            margin-top: 30px;
            justify-content: center;
        }

        

        span {
            color: white;
            position: absolute;
            top: 5%;
            right: 5%;
            font-size: 50px;
            cursor: pointer;
        }
        #dis{
            width: 100%;
            height: 100%;
            background: rgba(0,0,0,0.8);
            position: fixed;
            top: 0;
            bottom: 0;
            display: none;
            align-items: center;
            justify-content: center;
            z-index: 100;
        }
        #dis img{
            width: 400px;
            height: 400px;
        }
        footer {
            background-color: green;
            color: #fff;
            padding: 12px 30px;
            text-align: center;
            width: 100%;
            position: fixed;
            bottom: 0;

         
        }
       
       
    </style>
    
</head>

<body>
    <header>
        <h1><font size="7" color="orange">INTERACTIVE IMAGE GALLERY</font></h1>
    </header>

    <div class="col1">
        <div class="img">
            <img src="india gate.jpg" onclick="opens(this.src)" id="img1" alt="">
        </div>
        <div class="img">
            <img src="Taj-Mahal3.jpg" onclick="opens(this.src)" id="img2" alt="">
        </div>
        <div class="img">
            <img src="kolakataa.jpeg" onclick="opens(this.src)" id="img3" alt="">
        </div>
        <div class="img">
            <img src="khajuraho.jpg" onclick="opens(this.src)" id="img4" alt="">
        </div>
    </div>
    <div class="col2">
        <div class="img">
            <img src="qutub 2.webp" onclick="opens(this.src)" id="img5" alt="">
        </div>
        <div class="img">
            <img src="new-parliament-building-.webp" onclick="opens(this.src)" id="img6" alt="">
        </div>
        <div class="img">
            <img src="Hawa-Mahal.jpg" onclick="opens(this.src)" id="img7" alt="">
        
    </div>
    
    <footer>
        <p>Designed by GERIUS G(24900086)</p>
    </footer>
    
    <script>
        const allPhotos = document.querySelectorAll('.img');
        const viewer = document.querySelector('.viewer');
        const viewerImage = viewer.querySelector('img');
        const closeBtn = viewer.querySelector('.close-btn');
    
        allPhotos.forEach((img) => {
            img.addEventListener('click', function() {
                viewer.style.display = 'flex';
                viewerImage.src = this.src;
            });
        });
    
        closeBtn.addEventListener('click', () => {
            viewer.style.display = 'none';
        });
    
        viewer.addEventListener('click', (e) => {
            if (e.target === viewer) {
                viewer.style.display = 'none';
            }
        });
    </script>
    
    
</body>
</html>

```

## OUTPUT:
![alt text](<Screenshot (87)-1.png>)

## RESULT:
The program for designing an interactive image gallery using HTML, CSS and JavaScript is executed successfully.
