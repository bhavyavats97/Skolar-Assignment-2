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
    <header>
        <h1>Responsive Images Example</h1>
    </header>
    <main class="grid-container">
        <div class="grid-item content">
            <img 
                src="images/large-image.jpg" 
                srcset="images/small-image.jpg 480w,
                        images/medium-image.jpg 800w,
                        images/large-image.jpg 1200w"
                sizes="(max-width: 600px) 480px,
                       (max-width: 900px) 800px,
                       1200px"
                alt="Example Image">
            <p>This image adjusts to different screen sizes using the srcset attribute.</p>
        </div>
    </main>
    <footer>
        <p>&copy; 2024 Responsive Images Example</p>
    </footer>
</body>
</html>

...CSS
body {
    font-family: Arial, Helvetica, sans-serif;
    margin: 0;
    padding: 0;
    display: flex;
    flex-direction: column;
    min-height: 100vh;
}

header, footer {
    background-color: #333;
    color: white;
    text-align: center;
    padding: 20px;
}

main {
    flex: 1;
    display: flex;
    justify-content: center;
    align-items: center;
    padding: 20px;
}

.grid-container {
    display: grid;
    grid-template-columns: 1fr;
    grid-template-rows: auto;
    grid-template-areas:
        "content";
    width: 100%;
    max-width: 1200px;
    padding: 20px;
}

.grid-item {
    background-color: #3498db;
    color: white;
    padding: 20px;
    text-align: center;
    border-radius: 5px;
}

.content {
    grid-area: content;
}

/* Responsive image styles */
img {
    max-width: 100%;
    height: auto;
    border-radius: 5px;
}





