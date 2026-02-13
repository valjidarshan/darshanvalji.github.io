<!DOCTYPE html>
<html lang="en">
<head>
<meta charset="UTF-8">
<title>Be My Valentine</title>
<style>
    html, body {
        width: 100%;
        height: 100%;
        margin: 0;
        font-family: Arial, sans-serif;
        background-color: #ffe6f0;
        overflow: hidden;
        position: relative;
    }

    h1 {
        text-align: center;
        margin-top: 80px;
    }

    button {
        padding: 12px 24px;
        font-size: 18px;
        border: none;
        border-radius: 8px;
        cursor: pointer;
    }

    #yes-button {
        background-color: #ff4d6d;
        color: white;
        margin-right: 20px;
        position: relative;
        z-index: 1;
    }

    #no-button {
        background-color: #ccc;
        position: absolute;
        top: 200px;
        left: 60%;
        z-index: 1;
    }

    #penguins {
        display: none;
        text-align: center;
        margin-top: 40px;
    }

    #penguins img {
        width: 250px;
        border-radius: 12px;
    }
</style>
</head>
<body>

<h1 id="question">Will you be my Valentine? ❤️</h1>

<button id="yes-button">Yes</button>
<button id="no-button">No</button>

<div id="penguins">
    <h2>Yay! ❤️</h2>
    <img src="https://media.giphy.com/media/3oriO0OEd9QIDdllqo/giphy.gif" alt="Hugging penguins">
</div>

<script>
window.addEventListener('load', function () {
    const noButton = document.getElementById('no-button');
    const yesButton = document.getElementById('yes-button');
    const penguins = document.getElementById('penguins');
    const question = document.getElementById('question');

    function moveNoButton() {
        // Get the visible width/height of the viewport
        const maxX = window.innerWidth - noButton.offsetWidth;
        const maxY = window.innerHeight - noButton.offsetHeight;

        // Random position inside the screen
        const x = Math.floor(Math.random() * maxX);
        const y = Math.floor(Math.random() * maxY);

        noButton.style.left = x + "px";
        noButton.style.top = y + "px";
    }

    // Mouse hover moves the No button
    noButton.addEventListener('mouseenter', moveNoButton);

    // Click Yes shows penguins
    yesButton.addEventListener('click', function () {
        question.style.display = 'none';
        yesButton.style.display = 'none';
        noButton.style.display = 'none';
        penguins.style.display = 'block';
    });
});
</script>

</body>
</html>
