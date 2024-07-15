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
        <h1>CSS Pseudo-Classes and Pseudo-Elements Demonstration</h1>
        
        <button class="button">Hover and Click Me</button>
        
        <div class="input-container">
            <label for="input-field">Focus on the input field:</label>
            <input type="text" id="input-field" placeholder="Type something...">
        </div>
        
        <ul class="list">
            <li>Item 1</li>
            <li>Item 2</li>
            <li>Item 3</li>
            <li>Item 4</li>
        </ul>
        
        <div class="box">
            Box Content
        </div>
    </div>
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
.button {
    background-color: #c300ff;
    color: white;
    padding: 10px 20px;
    border: none;
    cursor: pointer;
    font-size: 16px;
    transition: background-color 0.3s ease;
}
.button:hover {
    background-color: #00b3a4;
}
.button:active {
    background-color: #004080;
}
.input-container {
    margin: 20px;
}
.input-container input {
    padding: 10px;
    font-size: 16px;
}
.input-container input:focus {
    border: 2px solid #007BFF;
}
.list {
    list-style: none;
    padding: 0;
}
.list li:nth-child(odd) {
    background-color: #e9e9e9;
}
.list li:nth-child(even) {
    background-color: #c9c9c9;
}
.box {
    position: relative;
    width: 200px;
    height: 100px;
    margin: 20px auto;
    background-color: #9447ff;
    color: white;
    display: flex;
    align-items: center;
    justify-content: center;
    font-size: 18px;
}
.box::before {
    content: '::before content';
    position: absolute;
    top: -20px;
    left: 10px;
    font-size: 12px;
    color: black;
}
.box::after {
    content: '::after content';
    position: absolute;
    bottom: -20px;
    right: 10px;
    font-size: 12px;
    color: black;
}
