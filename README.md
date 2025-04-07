# CSS Layouts and Responsive Design

## Objectives

Implement Flexbox and Grid for layout design.
Make the webpage responsive using media queries.
Ensure proper alignment and spacing.

## Instructions

- use Flexbox or CSS Grid.
- Add a navigation bar and structure the content.
- Use media queries to adjust layout for mobile, tablet, and desktop.

>[!NOTE]
>  - Include at least:
>  - navigation bar
>  - media queries

# Tasks

- Apply Flexbox or Grid for layout.
- Make the page responsive.
- Test across different screen sizes.

Happy Coding! 💻✨


Step 1: HTML Structure

First, we need to structure the HTML. Let's create a basic structure for a webpage with a navigation bar and content sections.

<!DOCTYPE html>
<html>
<head>
    <title>Responsive Layout</title>
    <link rel="stylesheet" type="text/css" href="styles.css">
</head>
<body>
    <header>
        <nav>
            <ul>
                <li><a href="#home">Home</a></li>
                <li><a href="#about">About</a></li>
                <li><a href="#contact">Contact</a></li>
            </ul>
        </nav>
    </header>

    <main>
        <section>
            <h1>Welcome to My Website</h1>
            <p>This is a sample text</p>
        </section>
        <section>
            <h2>About Us</h2>
            <p>This is another sample text</p>
        </section>
        <section>
            <h3>Contact Us</h3>
            <p>Sample contact information</p>
        </section>
    </main>
</body>
</html>
Step 2: CSS Using Flexbox

Now, let's apply Flexbox to our layout. We'll make the navigation bar a flex container and align items to the center. For the main content, we'll use Flexbox to layout sections.

/* styles.css */
* {
    margin: 0;
    padding: 0;
    box-sizing: border-box;
}

body {
    font-family: Arial, sans-serif;
}

header {
    background-color: #f8f9fa;
    padding: 1rem;
    display: flex;
    justify-content: space-between;
    align-items: center;
    border-bottom: 1px solid #ccc;
}

nav ul {
    list-style: none;
    padding: 0;
}

nav ul li a {
    text-decoration: none;
    color: #333;
    padding: 0.5rem 1rem;
}

main {
    display: flex;
    flex-direction: column;
    align-items: stretch;
}

section {
    padding: 1rem;
    border: 1px solid #eee;
}

@media screen and (max-width: 600px) {
    header {
        flex-direction: column;
        align-items: flex-start;
    }
    nav ul {
        flex: 1;
        justify-content: flex-start;
    }
    section {
        flex: 1;
    }
}

@media screen and (min-width: 601px) and (max-width: 992px) {
    header {
        flex-direction: row;
        justify-content: space-around;
    }
    section {
        flex: 1 1 100%;
    }
}

@media screen and (min-width: 993px) {
    header {
        justify-content: space-between;
    }
    section {
        flex: 1 1 300px; /* Set a fixed width for each section on desktop */
    }
}
