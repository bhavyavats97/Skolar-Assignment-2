...HTML
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>CSS Grid Layout</title>
    <link rel="stylesheet" href="styles.css">
</head>
<body>
    <header>
        <h1>CSS Grid Layout</h1>
    </header>
    <main class="grid-container">
        <div class="grid-item header">Header</div>
        <div class="grid-item sidebar">Sidebar</div>
        <div class="grid-item content">Content</div>
        <div class="grid-item footer">Footer</div>
    </main>
    <footer>
        <p>&copy; 2024 CSS GRID LAYOUT EXPLANATION</p>
    </footer>
</body>
</html>

...CSS

body {
    font-family:Arial, Helvetica, sans-serif;
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
    grid-template-columns: 1fr 3fr;
    grid-template-rows: auto 1fr auto;
    grid-template-areas:
        "header header"
        "sidebar content"
        "footer footer";
    grid-gap: 20px;
    width: 80%;
    max-width: 1200px;
}

.grid-item {
    background-color: #3498db;
    color: white;
    padding: 20px;
    text-align: center;
    border-radius: 5px;
}

..c
