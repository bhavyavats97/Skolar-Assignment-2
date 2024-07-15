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
        <h1>CSS Animations Demonstration</h1>
        <p>Observe the various animations applied to the boxes.</p>
        
        <div class="box box1">Box 1</div>
        <div class="box box2">Box 2</div>
        <div class="box box3">Box 3</div>
        <div class="box box4">Box 4</div>
        <div class="box box5">Box 5</div>
    </div>
</body>
</html>
...CSS
body {
    font-family: Arial, sans-serif;
    margin: 0;
    padding: 0;
    display: flex;
    flex-direction: column;
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
}

@keyframes colorChange {
    0% { background-color: red; }
    50% { background-color: blue; }
    100% { background-color: red; }
}
.box1 {
    animation: colorChange 3s linear infinite;
}

@keyframes moveAndScale {
    0% { transform: translateX(0) scale(1); }
    50% { transform: translateX(100px) scale(1.5); }
    100% { transform: translateX(0) scale(1); }
}
.box2 {
    animation: moveAndScale 4s ease-in-out 1s infinite;
}

@keyframes rotate {
    0% { transform: rotate(0deg); }
    100% { transform: rotate(360deg); }
}
.box3 {
    animation: rotate 2s cubic-bezier(0.68, -0.55, 0.27, 1.55) infinite;
}

@keyframes fadeInOut {
    0%, 100% { opacity: 0; }
    50% { opacity: 1; }
}
.box4 {
    animation: fadeInOut 5s ease-in-out infinite;
}

@keyframes slideDown {
    0% { transform: translateY(-100px); opacity: 0; }
    100% { transform: translateY(0); opacity: 1; }
}
.box5 {
    animation: slideDown 3s ease-out 2s forwards;
}
