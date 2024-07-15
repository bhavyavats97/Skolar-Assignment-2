...HTML
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>MY Webpage</title>
    <link rel="stylesheet" href="styles.css">
</head>
<body>
    <header>
        <h1>Responsive Webpage</h1>
    </header>
    <main class="grid-container">
        <div class="grid-item header">Header</div>
        <div class="grid-item sidebar">Sidebar</div>
        <div class="grid-item content">
            <div class="nested-grid">
                <div class="nested-item nested-header">Nested Header</div>
                <div class="nested-item nested-main">Nested Main</div>
                <div class="nested-item nested-footer">Nested Footer</div>
            </div>
        </div>
        <div class="grid-item extra">Extra</div>
        <div class="grid-item footer">Footer</div>
    </main>
    <footer>
        <p>&copy; 2024 MY WEBPAGE</p>
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
    grid-template-rows: auto 1fr auto;
    grid-template-areas:
        "header"
        "content"
        "sidebar"
        "extra"
        "footer";
    grid-gap: 20px;
    width: 100%;
    max-width: 1200px;
}

.grid-item {
    background-color: #3498db;
    color: white;
    padding: 20px;
    text-align: center;
    border-radius: 5px;
}

.header {
    grid-area: header;
}

.sidebar {
    grid-area: sidebar;
}

.content {
    grid-area: content;
}

.extra {
    grid-area: extra;
}

.footer {
    grid-area: footer;
}

/* Nested grid styles */
.nested-grid {
    display: grid;
    grid-template-columns: 1fr;
    grid-template-rows: auto 1fr auto;
    grid-template-areas:
        "nested-header"
        "nested-main"
        "nested-footer";
    grid-gap: 10px;
    background-color: #2ecc71;
    padding: 10px;
    border-radius: 5px;
}

.nested-item {
    background-color: #e74c3c;
    color: white;
    padding: 10px;
    text-align: center;
    border-radius: 5px;
}

.nested-header {
    grid-area: nested-header;
}

.nested-main {
    grid-area: nested-main;
}

.nested-footer {
    grid-area: nested-footer;
}

/* Media Queries */
@media (min-width: 600px) {
    .grid-container {
        grid-template-columns: 1fr 2fr;
        grid-template-areas:
            "header header"
            "content sidebar"
            "footer footer";
    }

    .extra {
        display: none;
    }

    .grid-item {
        font-size: 1.2em;
    }
}

@media (min-width: 900px) {
    .grid-container {
        grid-template-columns: 1fr 3fr 1fr;
        grid-template-areas:
            "header header header"
            "sidebar content extra"
            "footer footer footer";
    }

    .grid-item {
        font-size: 1.5em;
    }

    .nested-grid {
        grid-template-columns: 1fr 1fr;
        grid-template-areas:
            "nested-header nested-header"
            "nested-main nested-footer";
    }
}
