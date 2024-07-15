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
        <h1>CSS Transforms Demonstration</h1>
        <p>Hover over the boxes to see the transforms.</p>
        
        <div class="box box1">Translate</div>
        <div class="box box2">Rotate</div>
        <div class="box box3">Scale</div>
        <div class="box box4">Skew</div>
        <div class="box box5">Combined</div>
    </div>
</body>
</html>
...CSSbody {
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
    background-color: lightcoral;
    color: white;
    display: flex;
    align-items: center;
    justify-content: center;
    font-size: 18px;
    transition: transform 0.5s ease;
}
.box1:hover {
    transform: translateX(50px);
}
.box2:hover {
    transform: rotate(45deg);
}
.box3:hover {
    transform: scale(1.5);
}
.box4:hover {
    transform: skew(20deg, 20deg);
}
.box5:hover {
    transform: translateX(50px) rotate(45deg) scale(1.5) skew(10deg, 10deg);
}
