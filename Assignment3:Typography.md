...HTML
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Typography Showcase</title>
    <link rel="stylesheet" href="styles.css">
</head>
<body>

    <div class="section">
        <div class="heading">Font Families</div>
        <div class="example font-family-1">
            <p>Georgia, serif</p>
            <p>I am a web developer.</p>
        </div>
        <div class="example font-family-2">
            <p>Courier New, monospace</p>
            <p>I am a web developer.</p>
        </div>
        <div class="example font-family-3">
            <p>Verdana, sans-serif</p>
            <p>I am a web developer..</p>
        </div>
    </div>

    <div class="section">
        <div class="heading">Font Sizes</div>
        <div class="example large-text">
            <p>Large Text (2em)</p>
            <p>I am a web developer.</p>
        </div>
        <div class="example small-text">
            <p>Small Text (0.8em)</p>
            <p>I am a web developer.</p>
        </div>
    </div>

    <div class="section">
        <div class="heading">Font Styles</div>
        <div class="example bold-text">
            <p>Bold Text</p>
            <p>I am a web developer.</p>
        </div>
        <div class="example italic-text">
            <p>Italic Text</p>
            <p>I am a web developer..</p>
        </div>
        <div class="example uppercase-text">
            <p>Uppercase Text</p>
            <p>I am a web developer..</p>
        </div>
        <div class="example capitalize-text">
            <p>Capitalize Text</p>
            <p>I am a web developer..</p>
        </div>
    </div>

</body>
</html>

...CSS
body {
    font-family: Arial, Helvetica, sans-serif;
    line-height: 1.6;
    margin: 20px;
}

.section {
    margin-bottom: 40px;
}

.heading {
    font-size: 2em;
    font-weight: bold;
    margin-bottom: 10px;
}

.subheading {
    font-size: 1.5em;
    font-style: italic;
    margin-bottom: 10px;
}

.example {
    margin-bottom: 20px;
}

.example p {
    margin: 5px 0;
}

.font-family-1 {
    font-family: 'Georgia', serif;
}

.font-family-2 {
    font-family: 'Courier New', monospace;
}

.font-family-3 {
    font-family: 'Verdana', sans-serif;
}

.large-text {
    font-size: 2em;
}

.small-text {
    font-size: 0.8em;
}

.bold-text {
    font-weight: bold;
}

.italic-text {
    font-style: italic;
}

.uppercase-text {
    text-transform: uppercase;
}

.capitalize-text {
    text-transform: capitalize;
}
