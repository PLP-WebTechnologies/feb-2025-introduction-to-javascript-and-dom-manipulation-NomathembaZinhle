//Step 1: Create an HTML file
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>JavaScript DOM Manipulation</title>
    <link rel="stylesheet" href="styles.css">
</head>
<body>
    <header>
        <h1>DOM Manipulation with JavaScript</h1>
        <p id="intro">This page demonstrates basic DOM manipulation using JavaScript.</p>
    </header>

    <section>
        <h2>Interactive Section</h2>
        <button id="changeTextButton">Change Text</button>
        <button id="toggleColorButton">Toggle Background Color</button>
        <button id="addElementButton">Add New Element</button>
    </section>

    <section id="contentSection">
        <h3>Content Section</h3>
        <p>This is a sample paragraph.</p>
    </section>

    <footer>
        <p>© 2025 JavaScript DOM Manipulation Example</p>
    </footer>

    <script src="script.js"></script>
</body>
</html>

//Step 2: Create the JavaScript file
// Function to change the text content of a paragraph
function changeText() {
    document.getElementById('intro').textContent = 'The text has been changed!';
}

// Function to toggle the background color of the page
function toggleBackgroundColor() {
    let body = document.body;
    body.style.backgroundColor = body.style.backgroundColor === 'lightblue' ? '' : 'lightblue';
}

// Function to add a new element (e.g., a paragraph) when a button is clicked
function addNewElement() {
    let newElement = document.createElement('p');
    newElement.textContent = 'This is a newly added paragraph!';
    document.getElementById('contentSection').appendChild(newElement);
}

// Event listeners for button clicks
document.getElementById('changeTextButton').addEventListener('click', changeText);
document.getElementById('toggleColorButton').addEventListener('click', toggleBackgroundColor);
document.getElementById('addElementButton').addEventListener('click', addNewElement);

//Step 3: Create a CSS file
/* Basic page styling */
body {
    font-family: Arial, sans-serif;
    margin: 0;
    padding: 0;
    background-color: #f4f4f4;
}

header {
    background-color: #4CAF50;
    color: white;
    text-align: center;
    padding: 20px;
}

section {
    margin: 20px;
    padding: 20px;
    background-color: white;
    border-radius: 8px;
    box-shadow: 0px 4px 6px rgba(0, 0, 0, 0.1);
}

button {
    padding: 10px 20px;
    margin: 5px;
    border: none;
    border-radius: 5px;
    cursor: pointer;
    background-color: #007BFF;
    color: white;
    font-size: 16px;
}

button:hover {
    background-color: #0056b3;
}

//Step 4: File structure
/project-folder
    /index.html
    /script.js
    /styles.css


