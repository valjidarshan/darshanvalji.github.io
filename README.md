<!DOCTYPE html>
<html lang="en">
<head>
<meta charset="UTF-8">
<title>Be My Valentine</title>
<style>
    body {
        text-align: center;
        font-family: Arial, sans-serif;
        background-color: #ffe6f0;
        height: 100vh;
        margin: 0;
        overflow: hidden;
        position: relative;
    }

    h1 {
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
    }

    #no-button {
        background-color: #ccc;
        position: absolute;
        top: 200px;
        left: 60%;
    }

    #penguins {
        display: none;
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
window.onload = function () {
    const noButton = document.getElementById('no-button');
    const yesButton = document.getElementById('yes-button');
    const penguins = document.getElementById('penguins');
    const question = document.getElementById('question');

    function moveNoButton() {
        const x = Math.random() * (window.innerWidth - noButton.offsetWidth);
        const y = Math.random() * (window.innerHeight - noButton.offsetHeight);
        noButton.style.left = x + "px";
        noButton.style.top = y + "px";
    }

    noButton.addEventListener('mouseenter', moveNoButton);

    yesButton.addEventListener('click', function () {
        question.style.display = 'none';
        yesButton.style.display = 'none';
        noButton.style.display = 'none';
        penguins.style.display = 'block';
    });
};
</script>

</body>
</html>
