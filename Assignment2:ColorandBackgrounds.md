...HTML
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Color Properties in CSS</title>
    <link rel="stylesheet" href="styles.css">
</head>
<body>
    <header>
        <h1>Color Properties in CSS</h1>
    </header>
    <main>
        <section class="solid-color">
            <h2>Solid Colors</h2>
            <p>This text is styled with a solid color using the <code>color</code> property.</p>
        </section>
        <section class="background-color">
            <h2>Background Colors</h2>
            <p>This section has a background color using the <code>background-color</code> property.</p>
        </section>
        <section class="gradient-background">
            <h2>Gradient Background</h2>
            <p>This section has a gradient background using the <code>background-image</code> property.</p>
        </section>
        <section class="image-background">
            <h2>Image Background</h2>
            <p>This section has a background image with specific background properties.</p>
        </section>
    </main>
    <footer>
        <p>&copy; 2024 Color Properties in CSS</p>
    </footer>
</body>
</html>

...CSS
body {
    font-family: Arial, Helvetica, sans-serif;
    margin: 0;
    padding: 0;
}

header {
    background-color: #333;
    color: white;
    padding: 20px;
    text-align: center;
}

h1, h2 {
    margin: 0;
    padding: 10px 0;
}

main {
    padding: 20px;
}

section {
    margin-bottom: 20px;
    padding: 20px;
    border: 1px solid #ddd;
}

/* Solid color text */
.solid-color p {
    color: #e74c3c;
}

/* Background color */
.background-color {
    background-color: #3498db;
    color: white;
}

/* Gradient background */
.gradient-background {
    background-image: linear-gradient(to right, #8e44ad, #3498db);
    color: white;
}

/* Image background with properties */
.image-background {
    background-image: url('https://via.placeholder.com/800x400');
    background-repeat: no-repeat;
    background-size: cover;
    background-position: center;
    color: white;
    height: 200px;
    display: flex;
    align-items: center;
    justify-content: center;
    text-align: center;
}


