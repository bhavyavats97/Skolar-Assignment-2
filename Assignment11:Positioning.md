...HTML
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Responsive Images</title>
    <link rel="stylesheet" href="styles.css">
</head>
<body>
    <div class="container">
        <h1>CSS Positioning Techniques</h1>
        <p>This page demonstrates different CSS positioning techniques.</p>
        
        <div class="static">
            <h2>Static Positioning</h2>
            <p>This element is positioned static, which is the default positioning method.</p>
        </div>
        
        <div class="relative">
            <h2>Relative Positioning</h2>
            <p>This element is positioned relative to its normal position, with an offset of 20px from the top and left.</p>
        </div>
        
        <div class="absolute">
            <h2>Absolute Positioning</h2>
            <p>This element is positioned absolutely, 50px from the top and left of its nearest positioned ancestor.</p>
        </div>
        
        <div class="fixed">
            <h2>Fixed Positioning</h2>
            <p>This element is fixed to the bottom-right corner of the viewport, regardless of scrolling.</p>
        </div>
        
        <div class="sticky">
            <h2>Sticky Positioning</h2>
            <p>This element becomes sticky and remains at the top of the viewport when you scroll past it.</p>
        </div>
        
        <p>Scroll down to see the effect of the sticky positioned element.</p>
        <p style="height: 2000px;">This is some filler content to enable scrolling.</p>
    </div>
</body>
</html>
...CSS
body {
    font-family: Arial, Helvetica, sans-serif;
}
.container {
    margin: 20px;
}
.static {
    background-color: rgb(211, 211, 211);
    padding: 10px;
    position: static;
}
.relative {
    background-color: rgb(32, 187, 68);
    padding: 10px;
    position: relative;
    top: 20px;
    left: 20px;
}
.absolute {
    background-color: lightblue;
    padding: 10px;
    position: absolute;
    top: 50px;
    left: 50px;
}
.fixed {
    background-color: lightgreen;
    padding: 10px;
    position: fixed;
    bottom: 20px;
    right: 20px;
}
.sticky {
    background-color: lightgoldenrodyellow;
    padding: 10px;
    position: -webkit-sticky; /* For Safari */
    position: sticky;
    top: 0;
}
