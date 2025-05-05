# Ex.08 Design of Interactive Image Gallery
# Date:04.05.2025
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
country.html

```
<!DOCTYPE html>
 <html lang="en">
 <head>
   <meta charset="UTF-8" />
   <meta name="viewport" content="width=device-width, initial-scale=1.0"/>
   <title>Country Gallery</title>
   <style>
     body {
       margin: 0;
       font-family: Arial, sans-serif;
       background: linear-gradient(to right, #a8c0ff, #3f2b96);
       padding: 40px;
       text-align: center;
     }
 
     h1 {
       color: #ffffff;
       font-size: 3em;
       margin-bottom: 40px;
       text-shadow: 2px 2px 5px rgba(0, 0, 0, 0.3);
     }
 
     .gallery-row-1,
     .gallery-row-2 {
       display: flex;
       justify-content: center;
       gap: 20px;
       margin-bottom: 30px;
       flex-wrap: wrap;
     }
 
     .gallery-row-1 img,
     .gallery-row-2 img {
       width: 400px;
       height: 400px;
       object-fit: cover;
       border: 10px solid transparent;
       border-radius: 50%;
       border-image: linear-gradient(45deg, #ff6a00, #f1c40f) 1;
       box-shadow: 0 0 20px rgba(0, 0, 0, 0.3);
       transition: transform 0.3s ease, box-shadow 0.3s ease;
       cursor: pointer;
     }
 
     .gallery-row-2 .centered-img {
       width: 500px;
       height: 500px;
     }
 
     img:hover {
       transform: scale(1.05);
       box-shadow: 0 0 30px rgba(0, 0, 0, 0.5);
     }
 
     .image-name {
       color: #ffffff;
       font-size: 1.2em;
       margin-top: 10px;
       font-weight: bold;
     }
 
     .footer {
       margin-top: 50px;
       font-size: 1.2em;
       font-weight: bold;
       color: #ffffff;
       text-shadow: 1px 1px 3px rgba(0, 0, 0, 0.5);
     }
 
     /* Modal Styles */
     .modal {
       display: none;
       position: fixed;
       z-index: 999;
       left: 0;
       top: 0;
       width: 100%;
       height: 100%;
       overflow: auto;
       background-color: rgba(0, 0, 0, 0.9);
     }
 
     .modal-content {
       margin: 5% auto;
       display: block;
       max-width: 90%;
       max-height: 80%;
       border-radius: 12px;
       box-shadow: 0 0 20px #fff;
     }
 
     .close {
       position: absolute;
       top: 20px;
       right: 40px;
       color: #fff;
       font-size: 40px;
       font-weight: bold;
       cursor: pointer;
     }
 
     .close:hover {
       color: #ccc;
     }
   </style>
 </head>
 <body>
 
   <h1>Country</h1>
 
   <!-- First Row -->
   <div class="gallery-row-1">
     <div>
       <img src="sin.jpg" alt="Singapore" onclick="openModal(this)" />
       <div class="image-name">Singapore</div>
     </div>
     <div>
       <img src="ger.jpg" alt="Germany" onclick="openModal(this)" />
       <div class="image-name">Germany</div>
     </div>
   </div>
 
   <!-- Second Row -->
   <div class="gallery-row-2">
     <div>
       <img src="usa.webp" alt="USA" onclick="openModal(this)" />
       <div class="image-name">USA</div>
     </div>
     <div>
       <img src="rus.jpg" alt="Russia" onclick="openModal(this)" />
       <div class="image-name">Russia</div>
     </div>
     <div>
       <img class="centered-img" src="hong.webp" alt="Hong Kong" onclick="openModal(this)" />
       <div class="image-name">Hong Kong</div>
     </div>
   </div>
 
   <!-- Third Row -->
   <div class="gallery-row-2">
     <div>
       <img src="ind.jpg" alt="India" onclick="openModal(this)" />
       <div class="image-name">India</div>
     </div>
   </div>
 
   <!-- Modal Popup -->
   <div id="myModal" class="modal" onclick="closeModal()">
     <span class="close" onclick="closeModal()">&times;</span>
     <img class="modal-content" id="modal-img" />
   </div>
 
   <!-- Footer -->
   <div class="footer">RAJA.P</div>
 
   <!-- JavaScript for Modal -->
   <script>
     function openModal(imgElement) {
       const modal = document.getElementById("myModal");
       const modalImg = document.getElementById("modal-img");
       modal.style.display = "block";
       modalImg.src = imgElement.src;
       modalImg.alt = imgElement.alt;
     }
 
     function closeModal() {
       document.getElementById("myModal").style.display = "none";
     }
 
     // Optional: close modal when pressing Escape key
     document.addEventListener("keydown", function (e) {
       if (e.key === "Escape") {
         closeModal();
       }
     });
   </script>
 
 </body>
 </html>
 
```
# OUTPUT:
![alt text](s1-2.png)
# RESULT:
The program for designing an interactive image gallery using HTML, CSS and JavaScript is executed successfully.
