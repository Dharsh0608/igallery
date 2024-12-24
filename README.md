# Ex.08 Design of Interactive Image Gallery
## Date:22/12/2024

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
~~~
<!DOCTYPE html>
<html lang="en">
<head>
<meta charset="UTF-8">
<meta name="viewport" content="width=device-width, initial-scale=1.0">
<title>Interactive Image Gallery</title>
<style>
.lightbox {
display: none;
position: fixed;
z-index: 1000;
left: 0;
top: 0;
width: 100%;
height: 100%;
background-color: rgba(0, 0, 0, 0.8);
align-items: center;
justify-content: center;
}
.lightbox-content {
width: 80%;
height: auto;
max-width: 900px;
}
.close-btn {
position: absolute;
top: 20px;
right: 20px;
font-size: 30px;
color: white;
cursor: pointer;
background: none;
border: none;
}
.close-btn:hover {
color: #ccc;
}
</style>
</head>
<body>
<div class="gallery">
<div class="gallery-item">
<img src="tinytan.jpg" alt="Image 1" class="gallery-img">
</div>
<div class="gallery-item">
<img src="heart.jpg" alt="Image 2" class="gallery-img">
</div>
<div class="gallery-item">
<img src="image1.jpg" alt="Image 3" class="gallery-img">
</div>
<div class="gallery-item">
<img src="image2.jpg" alt="Image 4" class="gallery-img">
</div>
<!-- Add more gallery items as needed -->
</div>
<!-- The Modal (lightbox) -->
<div id="lightbox" class="lightbox">
<span class="close-btn">&times;</span>
<img class="lightbox-content" id="lightbox-img">
</div>
<script>
// Get all the images in the gallery
const galleryImages = document.querySelectorAll('.gallery-img');
// Get the lightbox and lightbox image elements
const lightbox = document.getElementById('lightbox');
const lightboxImg = document.getElementById('lightbox-img');
const closeBtn = document.querySelector('.close-btn');

    // Add click event to each image to open the lightbox
    galleryImages.forEach(image => {
        image.addEventListener('click', () => {
            lightbox.style.display = 'flex';
            lightboxImg.src = image.src; // Set the clicked image as the lightbox image
        });
    });
    
    // Close the lightbox when the close button is clicked
    closeBtn.addEventListener('click', () => {
        lightbox.style.display = 'none';
    });
    
    // Close the lightbox when the user clicks outside the image
    lightbox.addEventListener('click', (event) => {
        if (event.target === lightbox) {
            lightbox.style.display = 'none';
        }
    });
</script>

</body>
</html>
~~~

## OUTPUT:
![alt text](image.png)

## RESULT:
The program for designing an interactive image gallery using HTML, CSS and JavaScript is executed successfully.
