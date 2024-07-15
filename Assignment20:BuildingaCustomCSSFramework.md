...HTML
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>SimpleCSS Framework</title>
    <link rel="stylesheet" href="styles.css">
</head>
<body>
    <div class="container">
        <h1 class="text-center">SimpleCSS Framework</h1>
        
        
        <h2>Grid System</h2>
        <div class="row">
            <div class="col col-4">Column 4</div>
            <div class="col col-4">Column 4</div>
            <div class="col col-4">Column 4</div>
        </div>
        <div class="row">
            <div class="col col-6">Column 6</div>
            <div class="col col-6">Column 6</div>
        </div>

        <!-- Button Example -->
        <h2>Buttons</h2>
        <button class="btn">Primary Button</button>

        <!-- Card Example -->
        <h2>Cards</h2>
        <div class="card">
            <h3>Card Title</h3>
            <p>This is a simple card component.</p>
        </div>

        <!-- Form Example -->
        <h2>Forms</h2>
        <form>
            <label for="name">Name</label>
            <input type="text" id="name" name="name" required>

            <label for="email">Email</label>
            <input type="email" id="email" name="email" required>

            <label for="message">Message</label>
            <textarea id="message" name="message" rows="4" required></textarea>

            <button class="btn" type="submit">Submit</button>
        </form>

        <!-- Utility Classes Example -->
        <h2>Utility Classes</h2>
        <div class="mt-2 p-2 text-center" style="background-color: var(--primary-color); color: white;">
            Margin Top 2 and Padding 2 with Centered Text
        </div>
    </div>
</body>
</html>
...CSS
:root {
    --primary-color: #007BFF;
    --secondary-color: #6c757d;
    --background-color: #f8f9fa;
    --font-color: #333;
    --font-size: 16px;
    --border-radius: 4px;
    --padding: 16px;
    --margin: 16px;
}

/* Grid System */
.container {
    width: 100%;
    max-width: 1200px;
    margin: 0 auto;
    padding: 0 var(--padding);
}

.row {
    display: flex;
    flex-wrap: wrap;
    margin: 0 -var(--padding) / 2;
}

.col {
    flex: 1;
    padding: var(--padding) / 2;
}

.col-1 { flex: 0 0 8.33%; }
.col-2 { flex: 0 0 16.66%; }
.col-3 { flex: 0 0 25%; }
.col-4 { flex: 0 0 33.33%; }
.col-5 { flex: 0 0 41.66%; }
.col-6 { flex: 0 0 50%; }
.col-7 { flex: 0 0 58.33%; }
.col-8 { flex: 0 0 66.66%; }
.col-9 { flex: 0 0 75%; }
.col-10 { flex: 0 0 83.33%; }
.col-11 { flex: 0 0 91.66%; }
.col-12 { flex: 0 0 100%; }

/* Buttons */
.btn {
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

.btn:hover {
    background-color: var(--secondary-color);
}

/* Cards */
.card {
    background-color: white;
    border-radius: var(--border-radius);
    box-shadow: 0 4px 8px rgba(0, 0, 0, 0.1);
    padding: var(--padding);
    margin: var(--margin) 0;
}

/* Forms */
input[type="text"],
input[type="email"],
input[type="password"],
textarea {
    width: 100%;
    padding: var(--padding);
    margin-bottom: var(--margin);
    border: 1px solid #ccc;
    border-radius: var(--border-radius);
    font-size: var(--font-size);
}

input:focus,
textarea:focus {
    border-color: var(--primary-color);
    outline: none;
}
.mt-1 { margin-top: var(--margin); }
.mt-2 { margin-top: calc(var(--margin) * 2); }
.mb-1 { margin-bottom: var(--margin); }
.mb-2 { margin-bottom: calc(var(--margin) * 2); }
.p-1 { padding: var(--padding); }
.p-2 { padding: calc(var(--padding) * 2); }
.text-center { text-align: center; }
.text-right { text-align: right; }
