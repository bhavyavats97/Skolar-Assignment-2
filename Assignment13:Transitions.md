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
        <h1>CSS Transitions Demonstration</h1>
        <p>Hover over the boxes to see the transitions.</p>
        
        <div class="box box1">box 1</div>
        <div class="box box2">Box 2</div>
        <div class="box box3">Box 3</div>
        <div class="box box4">box 4</div>
        <div class="box box5">box 5</div>
</body>
</html>
...CSS
body {
    font-family: Arial, Helvetica, sans-serif;
    margin: 0;
    padding: 0;
    display: flex;
    justify-content: center;
    align-items: center;
    height: 100vh;
    background-color: #f0f0f0;
}
.container {
    text-align: center;
}
.box {
    width: 100px;
    height: 100px;
    margin: 20px;
    display: inline-block;
    transition: all 0.5s ease;
}
.box1 {
    background-color: red;
    transition: background-color 1s ease-in-out;
}
.box1:hover {
    background-color: blue;
}
.box2 {
    background-color: green;
    transition: width 2s ease-in, height 2s ease-out;
}
.box2:hover {
    width: 200px;
    height: 200px;
}
.box3 {
    background-color: orchid;
    transition: transform 1s cubic-bezier(0.68, -0.55, 0.27, 1.55);
}
.box3:hover {
    transform: rotate(45deg);
}
.box4 {
    background-color: purple;
    transition: opacity 1s ease, background-color 2s ease 1s;
}
.box4:hover {
    opacity: 0.5;
    background-color: pink;
}
.box5 {
    background-color: orange;
    transition: color 0.5s ease-in-out;
}
.box5:hover {
    color: white;
    background-color: brown;
}
