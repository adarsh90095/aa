<!DOCTYPE html>
<html lang="en">
<head>
<meta charset="UTF-8">
<title>Will You Go Out With Me?</title>

<style>
body {
    margin: 0;
    padding: 0;
    font-family: Arial, sans-serif;
    background: linear-gradient(to right, #ff9a9e, #fad0c4);
    text-align: center;
    overflow: hidden;
}

.container {
    margin-top: 40px;
}

h1 {
    font-size: 40px;
    color: #fff;
}

.girl-img {
    width: 250px;
    height: auto;
    margin: 20px 0;
    border-radius: 20px;
}

.buttons {
    margin-top: 20px;
    position: relative;
}

button {
    padding: 15px 30px;
    font-size: 18px;
    border: none;
    border-radius: 10px;
    cursor: pointer;
}

#yesBtn {
    background-color: #4CAF50;
    color: white;
    margin-right: 20px;
}

#noBtn {
    background-color: #f44336;
    color: white;
    position: absolute;
}
</style>

</head>

<body>

<div class="container">

    <h1>Will you go out with me? ❤️</h1>

    <!-- Girl Image -->
    <img src="https://i.imgur.com/1X5QH6p.png" class="girl-img">

    <div class="buttons">
        <button id="yesBtn">Yes ❤️</button>
        <button id="noBtn">No 😢</button>
    </div>

</div>

<script>

const noBtn = document.getElementById("noBtn");
const yesBtn = document.getElementById("yesBtn");

function moveNoButton() {

    const x = Math.floor(Math.random() * window.innerWidth - 100);
    const y = Math.floor(Math.random() * window.innerHeight - 100);

    noBtn.style.left = x + "px";
    noBtn.style.top = y + "px";
}

noBtn.addEventListener("mouseover", moveNoButton);
noBtn.addEventListener("click", moveNoButton);

yesBtn.addEventListener("click", function() {

    document.body.innerHTML = `
        <h1 style="margin-top:200px; color:white;">
        Yayyy! ❤️ You said YES 😍
        </h1>
    `;

});

</script>

</body>
</html>
