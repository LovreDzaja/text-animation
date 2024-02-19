# Text animation

Simple text animation written using JavaScript, HTML, CSS

## HTML Documentation 
```
<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8">
  <meta name="viewport" content="width=device-width, initial-scale=1.0">
  <link rel="stylesheet" href="./style.css" > <!-- External stylesheet link -->
  <title>Document</title>
</head>
<body>
  <div id="container">
    <span id="text1"></span> <!-- Placeholder for text content, will be manipulated by JavaScript -->
    <span id="text2"></span> <!-- Placeholder for text content, will be manipulated by JavaScript -->
  </div>

  <svg id="filters"> <!-- SVG element for defining filters -->
    <defs>
        <filter id="threshold"> <!-- Filter definition, used in the CSS -->
            <feColorMatrix in="SourceGraphic" type="matrix" values="1 0 0 0 0
									0 1 0 0 0
									0 0 1 0 0
									0 0 0 255 -140" />
        </filter>
    </defs>
  </svg>

  <script src="script.js"></script> <!-- Link to JavaScript file -->
</body>
</html>
```

## CSS Documentation
The provided CSS file ('styles.css') contains styling rules for the HTML elements. Here is a summary 
of the styles applied:

```
@import url("https://fonts.googleapis.com/css?family=Raleway:900&display=swap"); /* Imports the Raleway font with font weight 900 */

body {
    margin: 0px; /* Resets default margin */
    background: #4d1616; /* Sets background color */
}

#container {
    position: absolute; /* Positioned absolutely */
    margin: auto; /* Centers the container */
    width: 100vw; /* 100% of viewport width */
    height: 80pt; /* Fixed height */
    top: 0;
    bottom: 0;
    filter: url(#threshold) blur(0.5px); /* Applies filter effect */
}

#text1,
#text2 {
    position: absolute; /* Positioned absolutely */
    width: 100%; /* Full width */
    display: inline-block; /* Displays as inline-block */
    color: #7c4b4b; /* Text color */
    font-family: "Raleway", sans-serif; /* Font family */
    font-size: 80pt; /* Font size */
    text-align: center; /* Centers text horizontally */
    user-select: none; /* Prevents text selection */
}
```

## JavaScript Documentation
The provided

The provided JavaScript file (script.js) contains code that dynamically updates the text content and applies animation effects to the text elements. Below are the main functionalities:

1. Dynamic Text Update: The script dynamically updates the text content of text1 and text2 elements.

2. Morphing Animation: It applies a morphing animation effect to transition between two texts (text1 and text2).

3. Cooldown Mechanism: It implements a cooldown mechanism to control the timing of animations.

4. Animate Function: This function orchestrates the overall animation process by updating text content and applying animation effects.

5. Filters: It applies a filter effect defined in the SVG element with the ID threshold to the #container element.

6. Speed Control: The speed of animation casting is controlled by the dt variable.

These functionalities collectively create a morphing text animation effect on the webpage.

# Explanation

In crafting this project, I employed my expertise in JavaScript, leveraging mathematical concepts to meticulously manage the blur transition over specific time intervals. Beyond mere manipulation of visual effects, several critical handlers were meticulously devised to orchestrate the seamless workflow of the program. These handlers not only govern the morph effect with precision but also oversee the intricacies of cooldowns, ensuring smooth transitions and captivating animations that captivate the user's attention during text switches.

Furthermore, I intricately managed the timing of animations, ensuring a fluid and engaging user experience. Through a delicate balance of mathematical calculations and event handling, every aspect of the animation process was meticulously crafted to deliver a polished and visually appealing end result.
