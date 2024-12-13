## Template and Documentation for Website Style and Functionality

### Template Structure

#### HTML
```html
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Template Title</title>
    <link rel="stylesheet" href="styles.css">
    <link href="https://fonts.googleapis.com/css2?family=EB+Garamond:wght@400;700&display=swap" rel="stylesheet">
    <script src="https://cdn.jsdelivr.net/npm/mathjax@3/es5/tex-mml-chtml.js" async></script>
    <script>
        window.MathJax = {
            tex: {
                inlineMath: [['$', '$'], ['\\(', '\\)']]
            }
        };
    </script>
</head>
<body>
    <nav class="navbar">
        <ul>
            <li><a href="#about-me">About Me</a></li>
            <li><a href="#publications">Publications</a></li>
            <li><a href="https://github.com" target="_blank">GitHub</a></li>
            <li><button id="theme-toggle">Toggle Light/Dark</button></li>
        </ul>
    </nav>

    <header>
        <h1>Header Title</h1>
        <h4>Subheading</h4>
        <p>Author Name</p>
    </header>

    <section id="section-id">
        <h2>Section Title</h2>
        <p>Paragraph text with <i>italic</i> and <b>bold</b> styles. Math example: $\varphi = \frac{1 + \sqrt{5}}{2}$.</p>
        <div class="image-container">
            <img src="image-path.jpg" alt="Image Description">
        </div>
        <figcaption>Caption for the image.</figcaption>
    </section>

    <footer>
        <p>&copy; 2024 Your Name. All rights reserved.</p>
    </footer>

    <script>
        const toggleButton = document.getElementById('theme-toggle');
        toggleButton.addEventListener('click', () => {
            document.body.classList.toggle('dark-mode');
        });
    </script>
</body>
</html>
```

#### CSS
```css
body {
    font-family: 'EB Garamond', serif;
    line-height: 1.6;
    margin: 20px;
    padding: 20px;
    box-sizing: border-box;
    max-width: 800px;
    margin-left: auto;
    margin-right: auto;
    text-align: justify;
}

.navbar {
    position: sticky;
    top: 0;
    background-color: #f8f9fa;
    border-bottom: 2px solid #ddd;
    padding: 10px 20px;
    z-index: 1000;
}

.navbar ul {
    list-style: none;
    display: flex;
    justify-content: space-around;
    margin: 0;
    padding: 0;
}

.navbar li {
    margin: 0 10px;
}

.navbar a, .navbar button {
    text-decoration: none;
    color: #333;
    font-weight: bold;
    padding: 5px 10px;
    border: 1px solid transparent;
    border-radius: 5px;
    transition: background-color 0.3s, color 0.3s;
}

.navbar a:hover, .navbar button:hover {
    background-color: #ddd;
    color: #000;
}

.dark-mode {
    background-color: #121212;
    color: #e0e0e0;
}

.dark-mode .navbar {
    background-color: #333;
    border-bottom-color: #555;
}

.dark-mode .navbar a, .dark-mode .navbar button {
    color: #e0e0e0;
}

.dark-mode .navbar a:hover, .dark-mode .navbar button:hover {
    background-color: #555;
    color: #fff;
}

header, footer {
    text-align: center;
}

h1, h2, h3, h4 {
    font-weight: bold;
    margin-top: 30px;
}

p {
    margin-bottom: 20px;
}

.image-container {
    display: flex;
    justify-content: center;
    align-items: center;
    margin: 20px 0;
}

.image-container img {
    max-width: 100%;
    height: auto;
}

figcaption {
    text-align: center;
    font-size: 14px;
    color: #555;
    margin-top: 10px;
}
```

