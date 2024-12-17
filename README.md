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
    <title>Image Gallery</title>
    <link rel="stylesheet" href="style.css">
</head>
<body>
    <header  class="h1">
        <nav>
            <ul>
                <li ><a href="#INTERACTIVE IMAGE GALLERY" class="heading">INTERACTIVE IMAGE GALLERY</a></li>
            </ul>
        </nav>
    </header>

    <main id="gallery">
        <div class="gallery-container">
            <img src="12.webp" alt="Image 1""height="200" width="300">
            <img src="Taj-Mahal3.jpg" alt="Image 2""height="200" width="300">
            <img src="Red-Fort-.webp" alt="Image 3""height="200" width="300">
            <img src="qutub 2.webp" alt="Image 4""height="200" width="300">
            <img src="kolakataa.jpeg" alt="Image 5""height="200" width="300">
            <img src="new-parliament-building-.webp" alt="Image 6""height="200" width="300">
            <img src="khajuraho web.webp" alt="Image 7""height="200" width="300">
            <img src="Hawa-Mahal.jpg" alt="Image 8""height="200" width="300">
            
        </div>
    </main>

    <footer>
        <p>
            © DESIGNED BY: GERIUS G</p>
    </footer>
    <script>
        const allPhotos = document.querySelectorAll('.gallery');
        const viewer = document.querySelector('.viewer');
        const viewerImage = viewer.querySelector('gallery');
        const closeBtn = viewer.querySelector('.close-btn');
    
        allPhotos.forEach((img) => {
            img.addEventListener('click', function() {
                viewer.style.display = 'flex';
                viewerImage.src = this.src;
            });
        });
    
        closeBtn.addEventListener('click', (gallery) => {
            viewer.style.display = 'none';
        });
    
        viewer.addEventListener('click', (gallery) => {
            if (e.target === viewer) {
                viewer.style.display = 'none';
            }
        });
    </script>
</body>
</html>

style.css

body {
    font-family: Arial, sans-serif;
    margin: 0;
    padding: 0;
}

header {
    background-color: #333;
    color: rgb(2, 2, 2);
    padding: 10px 0;
}

nav ul {
    list-style: none;
    padding: 0;
    display: flex;
    justify-content: center;
}

nav ul li {
    margin: 0 15px;
}

nav ul li a {
    color: white;
    text-decoration: none;
}

.gallery-container {
    display: grid;
    grid-template-columns: repeat(4, 1fr);
    gap: 10px;
    padding: 20px;
    background-color: wheat;
}

.gallery-container img {
    width: 100%;
    height: auto;
    border-radius: 8px;
}

footer {
    text-align: center;
    font-size: 20px;
    padding: 10px 0;
    background-color: rgb(85, 84, 84);
    margin-top: 20px;
}
.heading{
    font-size: 30px;
    font-family: fantasy;
    letter-spacing: 1px;
    color:krgb(232, 255, 244);
}
.h1{
    background-color: rgb(19, 89, 194);
}

```

## OUTPUT:
![alt text](<Screenshot (86)-1.png>)

## RESULT:
The program for designing an interactive image gallery using HTML, CSS and JavaScript is executed successfully.
