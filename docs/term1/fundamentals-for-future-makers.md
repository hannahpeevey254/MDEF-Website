<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Full-Fill Image Grid Layout</title>

 <style>
        /* * 1. THE OVERALL CONTAINER AND GRID SETUP 
         */
        body {
            margin: 0;
            padding: 20px;
            font-family: Arial, sans-serif;
            background-color: #f4f4f4; /* Light background for visibility */
        }
        
        .main-grid-container {
            display: grid;
            /* Define 4 columns: 1.5fr for the left, 1fr for the rest */
            grid-template-columns: 1.5fr 1fr 1fr 1fr; 
            
            /* Define 4 rows for the content alignment */
            grid-template-rows: repeat(4, auto); 
            gap: 20px; /* Space between all elements */
            max-width: 1400px;
            margin: auto;
        }

        /* * 2. STYLES FOR CONTENT BOXES (NO BORDERS)
         */
        .content-box {
            /* Border and padding removed as requested */
            background-color: white; 
            display: flex; 
            justify-content: center;
            align-items: center;
            min-height: 150px; /* Base height for all boxes */
            overflow: hidden;
            text-align: center;
        }


        /* * 3. IMAGE STYLES FOR FULL-FILL EFFECT 
         */
        .content-box img {
            width: 100%;       /* Fill the container width */
            height: 100%;      /* Fill the container height */
            object-fit: cover; /* Important: Ensures the image covers the area, cropping if necessary */
            display: block;
        }

        /* * 4. SPECIFIC GRID PLACEMENT FOR THE LARGE ELEMENTS 
         */
   
        /* Top-Left Large Image (Spans 1 column width, 2 rows height) */
        #top-left-img {
            grid-column: 1 / span 1; 
            grid-row: 1 / span 2;    
        }

        /* Bottom-Left Text Block (Spans 1 column width, 2 rows height) */
        #bottom-left-text {
            grid-column: 1 / span 1; 
            grid-row: 3 / span 2;    
            text-align: left;
            padding: 20px; /* Padding kept for text readability */
            font-size: 0.8em;
            min-height: 150px; 
            /* Optional: Add a light border to separate text block from background */
            border: 1px solid #ddd; 
        }
        
        /* Bottom-Right Large Image (Spans 3 columns width, 2 rows height) */
        #bottom-right-img {
            grid-column: 2 / span 3; 
            grid-row: 3 / span 2;    
        }
        
        /* Small Grid Item (3x2) specific styling for the placeholders */
        .small-grid-item {
            /* Optional: Add a subtle border around the small images to separate them visually */
             border: 1px solid #ddd; 
             overflow: hidden;
        }

    </style>
</head>
<body>
 <div class="main-grid-container">
        
  <div id="top-left-img" class="content-box">
            <img src="../images/FOFM DIAGRAM 1 2.jpg" alt="Large Image 1">
        </div>

   <div class="content-box small-grid-item">
            <img src="../images/FOFM PICTURE 2.jpg" alt="Small Image 1">
        </div> 
  <div class="content-box small-grid-item">
            <img src="../images/FOFM PICTURE 3.jpg" alt="Small Image 2">
        </div>
  <div class="content-box small-grid-item">
            <img src="../images/FOFM PICTURE 4.jpg" alt="Small Image 3">
        </div> 

  <div class="content-box small-grid-item">
            <img src="../images/FOFM PICTURE 5.jpg" alt="Small Image 4">
        </div>
   <div class="content-box small-grid-item">
            <img src="../images/FOFM PICTURE 6.jpg" alt="Small Image 5">
 </div>
   <div class="content-box small-grid-item">
            <img src="../images/FOFM PICTURE 1.jpg" alt="Small Image 6">
        </div>

   <div id="bottom-left-text" class="content-box">
            <p>
               The Fundamentals of Digital Fabrication seminar gave me a full reset on the tools and workflows in the Fab Lab, and I refreshed my skills in laser cutting, 3D printing, CNCing, working with molds, and even learned how to make biomaterials. Each week mixed software, machines, and electronics in a way that pushed me to get comfortable actually building things, not just designing them. It ended up being a solid foundation for everything I want to prototype moving forward.
            </p>
        </div>

  <div id="bottom-right-img" class="content-box">
             <img src="../images/FOFM DIAGRAM 2.jpg" alt="Large Image 2">
        </div>
        
 </div>

</body>
</html>