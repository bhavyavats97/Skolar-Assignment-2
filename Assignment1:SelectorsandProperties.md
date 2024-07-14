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
    <header>
        <h1 id="main-heading">MY Webpage</h1>
        <nav>
            <ul>
                <li><a href="#section1" class="nav-link">Section 1</a></li>
                <li><a href="#section2" class="nav-link">Section 2</a></li>
                <li><a href="#section3" class="nav-link">Section 3</a></li>
            </ul>
        </nav>
    </header>
    <main>
        <section id="section1">
            <h2>HTML</h2>
            <p>This content covers html.</p>
            <p class="highlight">This paragraph is highlighted using a class selector.</p>
        </section>
        <section id="section2">
            <h2>CSS</h2>
            <p>This gives you information about how to add stylesheet.</p>
            <a href="https://www.example.com" class="external-link">Visit Example.com</a>
        </section>
        <section id="section3">
            <h2>JAVA SCRIPT</h2>
            <p class="highlight">Another highlighted paragraph.</p>
            <p>This paragraph has an <span class="tooltip" title="This is a tooltip">inline element with a tooltip</span>.</p>
        </section>
    </main>
    <footer>
        <p>&copy; 2024 My  Webpage</p>
    </footer>
</body>
</html>

...CSS
/* Element selector: style all paragraphs */
p {
    font-size: 16px;
    color: #333;
}

/* Class selector: style elements with the 'highlight' class */
.highlight {
    background-color: yellow;
}

/* ID selector: style the unique element with the ID 'main-heading' */
#main-heading {
    color: blue;
    text-align: center;
}

/* Attribute selector: style links with the 'href' attribute */
a[href] {
    color: green;
    text-decoration: none;
}

/* Pseudo-class selector: style links on hover */
a:hover {
    text-decoration: underline;
}

/* Pseudo-element selector: style the first line of paragraphs */
p::first-line {
    font-weight: bold;
}

/* Class selector: style elements with the 'nav-link' class */
.nav-link {
    color: purple;
    margin-right: 10px;
}

/* Pseudo-class selector: style the first child of list items */
li:first-child {
    font-weight: bold;
}

/* Attribute selector: style elements with the 'title' attribute */
[title] {
    border-bottom: 1px dotted #000;
    cursor: help;
}
