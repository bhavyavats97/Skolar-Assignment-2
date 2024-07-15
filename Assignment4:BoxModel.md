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
    <div class="info">
        <h2>CSS Box Model Demonstration</h2>
        <p>The box model consists of: content, padding, border, and margin.</p>
        <p>Below are examples of the effects of padding, border, and margin on elements.</p>
    </div>

    <div class="info">
        <h3>Content-box Model</h3>
        <p>With <code>box-sizing: content-box</code>, the width and height include only the content area. Padding and border are added outside of the specified width and height.</p>
    </div>
    <div class="box content-box">Content-box example</div>

    <div class="info">
        <h3>Border-box Model</h3>
        <p>With <code>box-sizing: border-box</code>, the width and height include the content, padding, and border. This makes the element's overall width and height easier to control.</p>
    </div>
    <div class="box border-box">Border-box example</div>

    <div class="info">
        <h3>Effect of Padding</h3>
        <p>Padding increases the space between the content and the border.</p>
    </div>
    <div class="box" style="padding: 40px;">Padding example (40px padding)</div>

    <div class="info">
        <h3>Effect of Border</h3>
        <p>Border adds a visible line around the content and padding.</p>
    </div>
    <div class="box" style="border: 20px solid darkblue;">Border example (20px border)</div>

    <div class="info">
        <h3>Effect of Margin</h3>
        <p>Margin creates space outside the border.</p>
    </div>
    <div class="box" style="margin: 40px;">Margin example (40px margin)</div>


</body>
</html>

...CSS
.box {
    width: 200px;
    height: 100px;
    background-color: lightblue;
    margin: 20px;
    padding: 20px;
    border: 10px solid darkblue;
}

.content-box {
    box-sizing: content-box;
}

.border-box {
    box-sizing: border-box;
}

.info {
    font-family:Arial, Helvetica, sans-serif;
    margin-bottom: 10px;
}
