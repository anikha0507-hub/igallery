# Ex.07 Design of Interactive Image Gallery
## Date:24.12.2025

## AIM:
To design a web application for an inteactive image gallery for a minimum five images with next and previous buttons.

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

## PROGRAM:
gallery.html
```
<html>
<head>
    <title>Interactive Image Gallery</title>
    <link rel="stylesheet" href="gallery.css">

    <script>
        const gallery = [
            { src: "india.png", caption: "INDIA" },
            { src: "europe.png", caption: "EUROPE" },
            { src: "staue.png", caption: "USA" },
            { src: "christ.png", caption: "BRAZIL" },
            { src: "china.png", caption: "CHINA" },
        ];

        let index = 0;

        function updateImage()
         {
            document.getElementById("img").src = gallery[index].src;
            document.getElementById("text").innerHTML = gallery[index].caption;
        }

        function next()
         {
            index++;
            if(index >= gallery.length){
               index = 0;
             }
            updateImage();
        }

        function previous()
         {
            index--;
            if(index < 0){
               index = gallery.length - 1;
            }
            updateImage();
        }
    </script>
</head>
<body>
    <div class="title">
        <h1>INTERACTIVE IMAGE GALLERY</h1>
    </div>
    <div class="allign">
        <div class="image">
            <img id="img" src="india.png" alt="Gallery Image">
            <h2 id="text">INDIA</h2>
            <div class="button1">
                <button onclick="previous()">Previous</button>
                <button onclick="next()">Next</button>
            </div>
        </div>
    </div>
    <footer class="copyrights">
        <h4> &copy; Designed by Anikha Pillai (25009524)</h4>
    </footer>
</body>
</html>

```

style.css
```
body{
    background-image: url(world.png);
}

.title {
    height: 60px;
    width: 100%;
    background-color: rgb(146, 115, 176);
    color: black;
    text-align: center;
    line-height: 60px;
    
}

.allign {
    display: flex;
    justify-content: center;
    align-items: center;
    margin-top: 80px;
}

.image {
    width: 320px;
    background-color: lightgray;
    border: 1px solid black;
    border-radius: 12px;
    padding: 20px;
    box-shadow: 0 8px 18px rgba(0, 0, 0, 0.2);

    display: flex;
    flex-direction: column;
    align-items: center;
    gap: 15px;
}

.image img {
    height: 220px;
    width: 200px;
    border-radius: 10px;
    object-fit: cover;
}

.image h2 {
    font-size: 20px;
    margin: 0;
    text-align: center;
}

.button1 {
    display: flex;
    gap: 25px;
}

button {
    background-color: darkgreen;
    color: white;
    padding: 10px 18px;
    font-size: 15px;
    border: none;
    border-radius: 8px;
    cursor: pointer;
}

button:hover {
    background-color: darkgreen;
}

.copyrights {
    background-color: rgb(146, 115, 176);
    color: black;
    padding: 10px;
    position: fixed;
    bottom: 0;
    width: 100%;
    font-size: 14px;
    text-align: center;
}

```

## OUTPUT:

## RESULT:
The program for designing an interactive image gallery using HTML, CSS and JavaScript is executed successfully.
