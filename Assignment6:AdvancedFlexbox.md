...HTML
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Complex Flexbox Layout</title>
    <link rel="stylesheet" href="styles.css">
</head>
<body>
    <header>
        <h1>Complex Flexbox Layout</h1>
    </header>
    <main>
        <div class="flex-container">
            <div class="flex-item order-3">Item 1</div>
            <div class="flex-item order-1">Item 2</div>
            <div class="flex-item order-2">Item 3</div>
            <div class="flex-item nested-container">
                <div class="nested-item">Nested Item 1</div>
                <div class="nested-item">Nested Item 2</div>
                <div class="nested-item">Nested Item 3</div>
                <div class="nested-item">Nested Item 4</div>
            </div>
            <div class="flex-item order-4">Item 4</div>
        </div>
    </main>
    <footer>
        <p>&copy; 2024 Complex Flexbox Layout Example</p>
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

.flex-container {
    display: flex;
    flex-wrap: wrap;
    justify-content: space-between;
    align-content: center;
    width: 80%;
    max-width: 1200px;
    border: 1px solid #ddd;
    padding: 20px;
}

.flex-item {
    background-color: #3498db;
    color: white;
    padding: 20px;
    margin: 10px;
    text-align: center;
    flex: 1 1 calc(25% - 40px);
    border-radius: 5px;
    order: 0; /* Default order */
}

.order-1 { order: 1; }
.order-2 { order: 2; }
.order-3 { order: 3; }
.order-4 { order: 4; }

.nested-container {
    display: flex;
    flex-wrap: wrap;
    justify-content: space-between;
    align-content: center;
    background-color: #2ecc71;
    padding: 20px;
    margin: 10px;
    border-radius: 5px;
}

.nested-item {
    background-color: #e74c3c;
    color: white;
    padding: 10px;
    margin: 10px;
    text-align: center;
    flex: 1 1 calc(50% - 40px);
    border-radius: 5px;
}
