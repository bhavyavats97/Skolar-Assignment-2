...HTML
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>CSS VARIABLES</title>
    <link rel="stylesheet" href="styles.css">
</head>
<body>
    <div class="container">
        <h1>CSS Variables Demonstration</h1>
        <p>This example demonstrates the use of CSS variables for common values like colors, font sizes, and spacing. By using variables, we can easily maintain consistency and make global changes in one place.</p>
        <input type="text" class="input-field" placeholder="Enter text...">
        <button class="button">Click Me</button>
    </div>
</body>
</html>
...CSS
:root {
    --primary-color: #007BFF;
    --secondary-color: #6c757d;
    --background-color: #f0f0f0;
    --font-color: #333;
    --font-size: 16px;
    --heading-font-size: 24px;
    --padding: 10px;
    --margin: 20px;
    --border-radius: 4px;
}

body {
    font-family: Arial, sans-serif;
    margin: 0;
    padding: var(--padding);
    background-color: var(--background-color);
    color: var(--font-color);
    font-size: var(--font-size);
}

.container {
    max-width: 800px;
    margin: var(--margin) auto;
    padding: var(--padding);
    background-color: white;
    border-radius: var(--border-radius);
    box-shadow: 0 4px 8px rgba(0, 0, 0, 0.1);
}

h1 {
    font-size: var(--heading-font-size);
    color: var(--primary-color);
}

p {
    margin-bottom: var(--margin);
}

.button {
    display: inline-block;
    padding: var(--padding);
    background-color: var(--primary-color);
    color: white;
    text-align: center;
    border: none;
    border-radius: var(--border-radius);
    cursor: pointer;
    transition: background-color 0.3s ease;
}

.button:hover {
    background-color: var(--secondary-color);
}

.input-field {
    width: 100%;
    padding: var(--padding);
    margin-bottom: var(--margin);
    border: 1px solid #ccc;
    border-radius: var(--border-radius);
    font-size: var(--font-size);
}

.input-field:focus {
    border-color: var(--primary-color);
    outline: none;
}
