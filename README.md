# Ex.08 Design of Interactive Image Gallery
# Date:16-12-2024
# AIM:
To design a web application for an inteactive image gallery with minimum five images.

# DESIGN STEPS:
## Step 1:
Clone the github repository and create Django admin interface.

## Step 2:
Change settings.py file to allow request from all hosts.

## Step 3:
Use CSS for positioning and styling.

## Step 4:
Write JavaScript program for implementing interactivity.

## Step 5:
Validate the HTML and CSS code.

## Step 6:
Publish the website in the given URL.

# PROGRAM :
```
<h2 align="center">SEVEN WOUNDERS OF THE WORLD</h2>
<!DOCTYPE html>


<html lang="en">
<head>
  <meta charset="UTF-8">
  <meta name="viewport" content="width=device-width, initial-scale=1.0">
 
  <title>Image Gallery</title>
  

  <link rel="stylesheet" href="styles.css">

</head>
<style>
 
body {
  font-family: Arial, sans-serif;
  margin: 0;
  padding: 0;
  background-color: #f0f0f0;
}

.gallery {
  display: grid;
  grid-template-columns: repeat(3, 1fr);
  gap: 10px;
  padding: 20px;
}

.image-container {
  position: relative;
  overflow: hidden;
  width: 500px;
  height: 400px;
}

.gallery-item {
  width: 100%;
  height: auto;
  cursor: pointer;
  transition: transform 0.3s ease;
}

.gallery-item:hover {
  transform: scale(1.1);
}


.modal {
  display: none; 
  position: fixed;
  z-index: 1;
  padding-top: 100px;
  left: 0;
  top: 0;
  width: 100%;
  height: 100%;
  background-color: rgba(0, 0, 0, 0.9);
  overflow: auto;
}

.modal-content {
  display: block;
  margin: auto;
  max-width: 80%;
  max-height: 80%;
}

.close {
  color: #fff;
  font-size: 40px;
  font-weight: bold;
  position: absolute;
  top: 10px;
  right: 25px;
  transition: 0.3s;
  cursor: pointer;
}

.close:hover,
.close:focus {
  color: #ddd;
  text-decoration: none;
  cursor: pointer;
}

#caption {
  text-align: center;
  color: #fff;
  font-size: 20px;
  padding: 10px;
}

</style>
<body>

  <div class="gallery">
    <div class="image-container">
      <img src="macchu.png.png"  alt="MACHU PICCHU" class="gallery-item">
    </div>
    <div class="image-container">
      <img src="tajmahal.png.png"  alt="TAJMAHAL" class="gallery-item">
    </div>
    <div class="image-container">
      <img src="COLOSSEUM.png.png"  alt="THE COLOSSEUM" class="gallery-item">
    </div>
    <div class="image-container">
      <img src="GREAT WALL OF CHINA.png.png" alt="GREAT WALL OF CHINA" class="gallery-item">
    </div>
    <div class="image-container">
      <img src="petra.png.png"  alt="PETRA" class="gallery-item">
    </div>
    <div class="image-container">
      <img src="CHICHEN.png.png"  alt="CHICHEN ITZA" class="gallery-item">
    </div>
    <div class="image-container">
      <img src="christ.png.png"  alt="CHRIST THE REDEEMER" class="gallery-item">
    </div>    
  </div>

  
  <div id="myModal" class="modal">
    <span class="close">&times;</span>
    <img class="modal-content" id="img01">
    <div id="caption"></div>
  </div>

  <script>
  
const modal = document.getElementById("myModal");
const modalImg = document.getElementById("img01");
const captionText = document.getElementById("caption");
const closeBtn = document.getElementsByClassName("close")[0];


const images = document.querySelectorAll(".gallery-item");


images.forEach(img => {
  img.onclick = function() {
    modal.style.display = "block";
    modalImg.src = this.src;
    captionText.innerHTML = this.alt;
  };
});


closeBtn.onclick = function() {
  modal.style.display = "none";
};


window.onclick = function(event) {
  if (event.target === modal) {
    modal.style.display = "none";
  }
};

  </script>
  <footer>
    <h2 align="center">Designed and developed by Charan reddy B</h2>
  </footer>
</body>
</html>
```
# OUTPUT:
![alt text](<Screenshot 2024-12-22 223423.png>)
![alt text](<Screenshot 2024-12-22 223436.png>)
![alt text](<Screenshot 2024-12-22 223448.png>)
![alt text](<Screenshot 2024-12-22 223701.png>)
![alt text](<Screenshot 2024-12-22 223716.png>)
![alt text](<Screenshot 2024-12-22 223728.png>)
![alt text](<Screenshot 2024-12-22 223737.png>)
![alt text](<Screenshot 2024-12-22 223749.png>)
![alt text](<Screenshot 2024-12-22 223800.png>)
# RESULT:
The program for designing an interactive image gallery using HTML, CSS and JavaScript is executed successfully.
