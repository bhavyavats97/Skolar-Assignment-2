...HTML
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Document</title>
    <link rel="stylesheet" href="styles.css">
</head>
<body>
    <div class="container">
        <h1>CSS z-index Demonstration</h1>
        <p>This page demonstrates the use of <code>z-index</code> to control the stacking order of overlapping elements.</p>
        
        <div class="box box1">Box 1 (z-index: 1)</div>
        <div class="box box2">Box 2 (z-index: 2)</div>
        <div class="box box3">Box 3 (z-index: 3)</div>
        <div class="box box4">Box 4 (fixed, z-index: 4)</div>
        <div class="box box5">Box 5 (sticky, z-index: 5)</div>

        <p>Scroll down to see the effect of the sticky positioned element.</p>
        <p style="height: 2000px;">This is some filler content to enable scrolling.</p>
</body>
</html>
...CSS
body {
    font-family: Arial, Helvetica, sans-serif;
    margin: 0;
    padding: 0;
}
.container {
    margin: 20px;
    position: relative; 
}
.box {
    width: 200px;
    height: 200px;
    position: absolute;
    opacity: 0.8;
    color: white;
    display: flex;
    align-items: center;
    justify-content: center;
    font-size: 24px;
}
.box1 {
    background-color: red;
    top: 50px;
    left: 50px;
    z-index: 1;
}
.box2 {
    background-color: blue;
    top: 100px;
    left: 100px;
    z-index: 2;
}
.box3 {
    background-color: green;
    top: 150px;
    left: 150px;
    z-index: 3;
}
.box4 {
    background-color: orange;
    top: 200px;
    left: 200px;
    position: fixed;
    z-index: 4;
}
.box5 {
    background-color: purple;
    top: 250px;
    left: 250px;
    position: sticky;
    z-index: 5;
    padding: 10px;
}
