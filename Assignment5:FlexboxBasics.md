...HTML 
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Flexbox Layout</title>
    <link rel="stylesheet" href="styles.css">
</head>
<body>
    <header>
        <h1>Fruits</h1>
    </header>
    <main>
        <div class="flex-container">
            <div class="flex-item">APPLE</div>
            <div class="flex-item">MANGO</div>
            <div class="flex-item">GUAVA</div>
        </div>
    </main>
    <footer>
        <p>&copy; 2024 Different types of fruits</p>
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
}

.flex-container {
    display: flex;
    justify-content: space-between;
    align-items: center;
    width: 80%;
    max-width: 1200px;
    margin: auto;
    padding: 20px;
    border: 1px solid #c617ac;
}

.flex-item {
    background-color: #34db5b;
    color: white;
    padding: 20px;
    margin: 0 10px;
    text-align: center;
    flex: 1;
    border-radius: 5px;
}


.flex-container {
    display: flex;
    flex-direction: row;
    justify-content: space-between;
    align-items: center;
}
