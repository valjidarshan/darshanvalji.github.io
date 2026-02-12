<script>
    const noButton = document.getElementById('no-button');
    const yesButton = document.getElementById('yes-button');

    function moveNoButton() {
        const x = Math.random() * (window.innerWidth - noButton.offsetWidth);
        const y = Math.random() * (window.innerHeight - noButton.offsetHeight);
        noButton.style.position = 'absolute';
        noButton.style.left = `${x}px`;
        noButton.style.top = `${y}px`;
    }

    noButton.addEventListener('mouseover', moveNoButton);

    yesButton.addEventListener('click', () => {
        noButton.removeEventListener('mouseover', moveNoButton);
        alert('You clicked Yes!');
    });
</script>
