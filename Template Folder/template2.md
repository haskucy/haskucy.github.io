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
                inlineMath: [['$', '$'], ['\(', '\)']]
            }
        };
    </script>
</head>
<body>
    <header>
        <h1>Header Title</h1>
        <h4>Subheading</h4>
        <p>Author Name</p>
        <nav>
            <button id="menu-toggle">Menu</button>
            <ul id="navbar" class="hidden">
                <li><a href="#section1">Section 1</a></li>
                <li><a href="#section2">Section 2</a></li>
                <li><a href="#section3">Section 3</a></li>
            </ul>
        </nav>
    </header>

    <section id="section-id">
        <h2>Section Title</h2>
        <p>Paragraph text with <i>italic</i> and <b>bold</b> styles. Math example: $ϕ = \frac{1 + \sqrt{5}}{2}$.</p>
        <div class="image-container">
            <img src="image-path.jpg" alt="Image Description">
        </div>
        <figcaption>Caption for the image.</figcaption>
    </section>

    <footer>
        <p>&copy; 2024 Your Name. All rights reserved.</p>
    </footer>

    <script>
        const toggleButton = document.getElementById('menu-toggle');
        const navbar = document.getElementById('navbar');

        toggleButton.addEventListener('click', () => {
            navbar.classList.toggle('hidden');
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

header, footer {
    text-align: center;
}

nav {
    margin-top: 10px;
}

#menu-toggle {
    background-color: #333;
    color: white;
    border: none;
    padding: 10px 20px;
    cursor: pointer;
    font-family: 'EB Garamond', serif;
}

#navbar {
    list-style-type: none;
    padding: 0;
    margin: 0;
    display: flex;
    justify-content: center;
    gap: 20px;
}

#navbar.hidden {
    display: none;
}

#navbar li {
    display: inline;
}

#navbar a {
    text-decoration: none;
    color: #333;
    font-weight: bold;
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

---

### Documentation

#### Headings
- **h1**: Used for the main title, centered in the header.
- **h2**: Used for section titles, with a bottom border for emphasis.
- **h3, h4**: Used for subheadings, with progressively smaller sizes.
- **Styling**: Bold font with appropriate margins to create visual separation.

#### Paragraphs
- **Spacing**: `margin-bottom: 20px` ensures clear separation between paragraphs.
- **Text Alignment**: Justified for a clean and professional appearance.
- **Font**: 'EB Garamond' serif font for a classic and readable style.

#### MathJax Integration
- **Purpose**: Enables rendering of LaTeX-style math expressions.
- **Configuration**: Inline math is wrapped with `$...$` or `\(...\)`.
- **Example**: `$ϕ = \frac{1 + \sqrt{5}}{2}$` renders the golden ratio formula.

#### Images
- **Container**: Images are wrapped in a `.image-container` div to ensure alignment and responsiveness.
- **Styling**:
  - `max-width: 100%`: Ensures images do not exceed the container width.
  - `margin: 0 auto`: Centers the image within the container.
- **Captions**: Use `<figcaption>` below images for descriptions, styled with smaller font size and muted color.

#### Interactive Elements
- **Controls**: Sliders, buttons, and input elements styled for consistency with the site’s font and layout.
- **Canvas**: Used for interactive visualizations, centered within the content area.

#### Navbar
- **Structure**: A `<nav>` element containing a button for toggling visibility and a list of links.
- **Styling**:
  - `#menu-toggle`: Styled as a button to control visibility.
  - `#navbar`: Hidden by default using the `.hidden` class.
  - `#navbar a`: Styled for emphasis with bold font and no underline.
- **Functionality**: JavaScript toggles the `.hidden` class to show or hide the navbar.

#### Footer
- **Content**: Includes copyright information, centered at the bottom of the page.
- **Styling**: Matches the header for visual symmetry.

---

This template and documentation provide a foundation to replicate the style and structure of the provided website, with flexibility for customization.

