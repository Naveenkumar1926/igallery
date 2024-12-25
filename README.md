# Ex.08 Design of Interactive Image Gallery

## Date:16/12/2024

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
'''

<html lang="en">
<head>
  <meta charset="UTF-8">
  <meta name="viewport" content="width=device-width, initial-scale=1.0">
  <title>Dynamic Photo Showcase</title>
  <style>
    body {
      font-family: 'Segoe UI', Tahoma, Geneva, Verdana, sans-serif;
      margin: 0;
      padding: 0;
      background-color: #f0f8ff;
      color: #333;
    }

    h1 {
      background-color:rgb(157, 85, 238);
      color: black;
      padding: 1rem;
      margin: 0;
      text-align: center;
      text-shadow: 2px 2px 5px rgba(0, 0, 0, 0.3);
    }

    .gallery-container {
      display: flex;
      flex-wrap: wrap;
      justify-content: center;
      gap: 20px;
      padding: 20px;
      margin: 20px;
      background-color: #ffffff;
      border-radius: 15px;
      box-shadow: 0 4px 6px rgba(0, 0, 0, 0.1);
    }

    .gallery-item {
      position: relative;
      width: 250px;
      height: 250px;
      border: 3px solid #4CAF50;
      border-radius: 12px;
      overflow: hidden;
      box-shadow: 0 4px 6px rgba(0, 0, 0, 0.1);
      transition: transform 0.3s ease, box-shadow 0.3s ease;
      background-color: #ffffff;
      display: flex;
      justify-content: center;
      align-items: center;
    }

    .gallery-item:hover {
      transform: scale(1.05);
      box-shadow: 0 6px 12px rgba(0, 0, 0, 0.2);
    }

    .gallery-item img {
      width: 100%;
      height: 100%;
      object-fit: cover;
    }

    #lightbox {
      display: none;
      position: fixed;
      top: 0;
      left: 0;
      width: 100%;
      height: 100%;
      background: rgba(0, 0, 0, 0.8);
      justify-content: center;
      align-items: center;
      z-index: 1000;
    }

    #lightboxContent {
      background: #fff;
      padding: 20px;
      border-radius: 15px;
      text-align: center;
      box-shadow: 0 8px 16px rgba(0, 0, 0, 0.3);
      border: 3px solid #1E90FF;
    }

    #lightboxContent img {
      max-width: 90%;
      max-height: 70vh;
      border-radius: 8px;
      border: 2px solid #4CAF50;
    }

    .close-button {
      background-color: #ff4d4d;
      color: white;
      border: none;
      padding: 12px 24px;
      border-radius: 8px;
      cursor: pointer;
      font-size: 16px;
      margin-top: 20px;
      transition: background-color 0.3s ease;
    }

    .close-button:hover {
      background-color: #e63939;
    }

    footer {
      background-color: #1E90FF;
      color: white;
      text-align: center;
      padding: 10px;
      position: fixed;
      width: 100%;
      bottom: 0;
      font-size: 14px;
    }
  </style>
  <script>
    function displayLightbox(imageSrc, imageAlt) {
      const lightbox = document.getElementById("lightbox");
      const lightboxImage = document.getElementById("lightboxImage");

      lightboxImage.src = imageSrc;
      lightboxImage.alt = imageAlt;
      lightbox.style.display = "flex";
    }

    function hideLightbox() {
      const lightbox = document.getElementById("lightbox");
      lightbox.style.display = "none";
    }
  </script>
</head>
<body>
  <h1>Dynamic Photo Showcase</h1>

  <div class="gallery-container">
    <div class="gallery-item">
      <img src="cr7.jpeg" alt="Guest 1" onclick="displayLightbox('cr7.jpeg', 'Delicious Dish 1')">
    </div>
    <div class="gallery-item">
      <img src="Neymar Jr.jpeg" alt="Guest 2" onclick="displayLightbox('Neymar jr.jpeg', 'Delicious Dish 2')">
    </div>
    <div class="gallery-item">
      <img src="leo.jpeg" alt="Guest 3" onclick="displayLightbox('leo.jpeg', 'Delicious Dish 3')">
    </div>
  </div>

  <div id="lightbox">
    <div id="lightboxContent">
      <img id="lightboxImage" src="Neymar Jr.jpeg" alt="Guest 2">
      <button class="close-button" onclick="hideLightbox()">Close</button>
    </div>
  </div>

  <footer>
    Design and Developed by NAVEEN KUMAR S
  </footer>
</body>
</html>

'''

## OUTPUT:

![alt text](<Screenshot 2024-12-16 182654.png>)

![alt text](<Screenshot 2024-12-16 182709.png>)


## RESULT:
The program for designing an interactive image gallery using HTML, CSS and JavaScript is executed successfully.
