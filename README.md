

<!DOCTYPE html>

<html lang="en">

<head>

<meta charset="UTF-8" />

<title>Proposal 💖</title>

<style>

body {

margin: 0;

padding: 0;

text-align: center;

background: #ffe6f0;

overflow: hidden;

font-family: 'Segoe UI', sans-serif;

}

#question {

font-size: 28px;

margin-top: 80px;

color: #d81b60;

}

button {

font-size: 20px;

margin: 20px;

padding: 12px 25px;

border: none;

border-radius: 8px;

cursor: pointer;

transition: 0.3s;

}

#yes {

background: #e91e63;

color: white;

}

#no {

background: gray;

color: white;

position: relative;

}

#message {

margin-top: 30px;

font-size: 24px;

color: #c2185b;

}

.heart {

position: fixed;

top: -10px;

font-size: 20px;

color: red;

animation: fall 6s linear infinite;

}

@keyframes fall {

to {

transform: translateY(100vh) rotate(360deg);

opacity: 0;
  height: 5px;

background: #ff4081;

border-radius: 50%;

animation: explode 1s ease-out forwards;

}

@keyframes explode {

to {

transform: scale(20);

opacity: 0;

}

}

</style>

</head>

<body>

<div id="question">Will you be mine forever? 💖</div>

<button id="yes">Yes</button>

<button id="no">No</button>

<div id="message"></div>

<script>

const yesBtn = document.getElementById('yes');

const noBtn = document.getElementById('no');

const message = document.getElementById('message');

let noClick = 0;

setInterval(() => {

const heart = document.createElement('div');

heart.classList.add('heart');

heart.style.left = Math.random() * 100 + 'vw';

heart.innerText = '❤️

document.body.appendChild(heart);

setTimeout(() => heart.remove(), 6000);

}, 300);

noBtn.addEventListener('click', () => {

noClick++;

if (noClick === 1) {

message.textContent = "Think again... 💭";

}

});

noBtn.addEventListener('mouseenter', () => {

if (noClick >= 1) {

message.textContent = "You can't escape! 😅";

const x = Math.random() * (window.innerWidth - noBtn.offsetWidth);

const y = Math.random() * (window.innerHeight - noBtn.offsetHeight);

noBtn.style.position = 'absolute';

noBtn.style.left = x + 'px';

noBtn.style.top = y + 'px';

}

});

yesBtn.addEventListener('click', () => {

message.textContent = "I knew it! 💘";

yesBtn.disabled = true;

noBtn.disabled = true;

for (let i = 0; i < 30; i++) {

const spark = document.createElement('div');

spark.classList.add('firework');

spark.style.left = (window.innerWidth / 2) + 'px';

spark.style.top = (window.innerHeight / 2) + 'px';

spark.style.transform = `translate((Math.random() - 0.5) * 500px,{(Math.random() - 0.5) * 500}px)`;

document.body.appendChild(spark);

setTimeout(() => spark.remove(), 1000);

}

});

</script>

</body>

</html>

}

}

.firework {

position: fixed;

width: 5px;
