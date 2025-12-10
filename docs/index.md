

<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Hannah's Portfolio Layout</title>

 <style>
        /* BASE STYLES */
        body {
            margin: 0;
            padding: 0;
            font-family: 'Arial', sans-serif; /* Fallback font */
            background-color: #f4f4f4;
            text-align: center; /* Center the whole layout */
        }

        /* ---------------------------------------------------- */
        /* 1. TOP HEADER TEXT (HI I'M HANNAH / HOPE YOU ENJOY MY WORK) 
        /* ---------------------------------------------------- */
        .header-text-container {
            width: 100%;
            background-color: white; /* White background as requested */
            padding: 40px 0;
            margin-bottom: 20px;
        }

        .main-title {
            font-size: 3em;
            font-weight: bold;
            /* Simulating the chrome/silver look with a text shadow and gray color */
            color: #555;
            text-shadow: 
                0 1px 0 #ccc, 
                0 2px 0 #c9c9c9, 
                0 3px 0 #bbb, 
                0 4px 0 #b9b9b9, 
                0 5px 0 #aaa, 
                0 6px 1px rgba(0,0,0,.1), 
                0 0 5px rgba(0,0,0,.1), 
                0 1px 3px rgba(0,0,0,.3), 
                0 3px 5px rgba(0,0,0,.2), 
                0 5px 10px rgba(0,0,0,.25), 
                0 10px 10px rgba(0,0,0,.2), 
                0 20px 20px rgba(0,0,0,.15);
            margin: 0;
        }

        .subtitle {
            font-size: 1.2em;
            color: #777;
            margin-top: 10px;
        }

        /* ---------------------------------------------------- */
        /* 2. MIDDLE SECTION (FULL-WIDTH IMAGE/CONTENT BOX) 
        /* ---------------------------------------------------- */
        .top-full-screen-box {
            width: 100%;
            max-width: 100%; /* Ensure it spans full width */
            min-height: 400px; 
            background-color: white; 
            margin-bottom: 20px; 
            display: flex;
            justify-content: center;
            align-items: center;
            /* Placeholder Text/Content for the top box */
            font-size: 2em;
            font-weight: bold;
            color: #333;
            border-bottom: 1px solid #ddd;
        }
        
        /* Full-fill image inside the top box if used */
        .top-full-screen-box img {
            width: 100%;
            height: 100%;
            object-fit: cover;
        }


        /* ---------------------------------------------------- */
        /* 3. BOTTOM 3-COLUMN IMAGE GRID (TERM 1, 2, 3) 
        /* ---------------------------------------------------- */
        .bottom-grid-container {
            display: grid;
            grid-template-columns: repeat(3, 1fr); 
            gap: 20px;
            max-width: 1200px; 
            margin: 0 auto 50px auto; 
            padding: 0 20px; 
        }

        /* Styles for each link box (Image & Text Overlay) */
        .term-link-box {
            text-decoration: none; 
            color: #fff; 
            display: block; 
            position: relative; 
            overflow: hidden; 
            
            /* Apply the requested border color and style */
            border: 5px solid #c3c62f; 
            min-height: 300px; 
            transition: box-shadow 0.3s ease, transform 0.3s ease;
        }

        .term-link-box:hover {
            box-shadow: 0 8px 16px rgba(0, 0, 0, 0.15);
            transform: translateY(-5px);
        }

        /* Image inside the link box */
        .term-link-box img {
            width: 100%;       
            height: 100%;      
            object-fit: cover; 
            display: block;
        }
        
        /* Overlay for the text to be readable */
        .overlay-text {
            position: absolute;
            bottom: 0;
            left: 0;
            width: 100%;
            padding: 15px 10px;
            background-color: rgba(0, 0, 0, 0.6); /* Slightly darker overlay for better contrast */
            text-align: center;
        }

        .link-title {
            font-size: 1.5em;
            font-weight: bold;
            margin: 0;
        }

        .link-subtitle {
            font-size: 0.9em;
            color: #ccc;
            margin: 0;
        }
    </style>
</head>
<body>

<div class="header-text-container">
        <h1 class="main-title">HI I'M HANNAH</h1>
        <p class="subtitle">HOPE YOU ENJOY MY WORK</p>
    </div>

  <div class="top-full-screen-box">
        <img src="../docs/images/HI IM HANNAH HOPE YOU EMJOY 2 WEBSITE.jpg" alt="Top Full-Width Content" style="width: 100%; height: 100%; object-fit: cover; display: block;">
    </div>

  <div class="bottom-grid-container">
        
  <a href="term1.html" class="term-link-box">
            <img src="../docs/images/HOME PAGE TERM 1.jpg" alt="Term 1 Project Image">
            <div class="overlay-text">
                <p class="link-title">TERM 1</p>
                <p class="link-subtitle">View detailed projects</p>
            </div>
        </a>

  <a href="term2.html" class="term-link-box">
            <img src="../docs/images/HOME PAGE TERM 2.jpg" alt="Term 2 Project Image">
            <div class="overlay-text">
                <p class="link-title">TERM 2</p>
                <p class="link-subtitle">View detailed projects</p>
            </div>
        </a>

  <a href="term3.html" class="term-link-box">
            <img src="../docs/images/HOME PAGE TERM 3.jpgg" alt="Term 3 Project Image">
            <div class="overlay-text">
                <p class="link-title">TERM 3</p>
                <p class="link-subtitle">View detailed projects</p>
            </div>
        </a>
        
  </div>

</body>
</html>