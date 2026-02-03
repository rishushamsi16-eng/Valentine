<!DOCTYPE html>
<html lang="en">
<head>
<meta charset="UTF-8">
<title>For Irene ❤️</title>
<meta name="viewport" content="width=device-width, initial-scale=1.0">

<style>
body {
  margin: 0;
  height: 100vh;
  background: radial-gradient(circle at top, #1a1a1a, #000);
  display: flex;
  align-items: center;
  justify-content: center;
  font-family: Arial, sans-serif;
  color: white;
  overflow: hidden;
}

/* Instagram Story size */
.story {
  width: 360px;
  height: 640px;
  background: #111;
  border: 2px solid #e50914;
  border-radius: 25px;
  box-shadow: 0 0 40px rgba(229,9,20,0.6);
  padding: 28px;
  text-align: center;
  display: flex;
  flex-direction: column;
  justify-content: center;
  animation: fadeIn 1.2s ease;
}

@keyframes fadeIn {
  from { opacity: 0; transform: scale(0.95); }
  to { opacity: 1; transform: scale(1); }
}

h1 {
  color: #e50914;
  font-size: 22px;
  margin-bottom: 5px;
}

.subtitle {
  font-size: 13px;
  color: #aaa;
  margin-bottom: 15px;
}

p {
  font-size: 15px;
  color: #ddd;
  line-height: 1.5;
}

h2 {
  margin-top: 15px;
  font-size: 17px;
}

.countdown {
  margin: 12px 0;
  font-size: 15px;
  color: #ffb3b3;
  font-weight: bold;
}

button {
  padding: 12px 24px;
  font-size: 15px;
  border-radius: 30px;
  border: none;
  cursor: pointer;
  margin: 8px auto;
  width: 75%;
}

.yes {
  background: #e50914;
  color: white;
}

.yes:hover {
  box-shadow: 0 0 15px #e50914;
}

.no {
  background: #444;
  color: #bbb;
  position: absolute;
}

/* Hidden Letter */
.letter {
  display: none;
  background: #000;
  border: 1px solid #e50914;
  border-radius: 15px;
  padding: 18px;
  margin-top: 10px;
  font-size: 14px;
  animation: fadeIn 1s ease;
}

/* Kiss animation */
.kiss {
  position: fixed;
  font-size: 28px;
  animation: kissFloat 2.5s ease forwards;
}

@keyframes kissFloat {
  0% { transform: scale(0); opacity: 0; }
  30% { transform: scale(1.2); opacity: 1; }
  100% { transform: translateY(-120px); opacity: 0; }
}
</style>
</head>

<body>

<!-- Music -->
<audio id="music" loop>
  <source src="https://cdn.pixabay.com/download/audio/2022/10/03/audio_8f02c2b7a5.mp3" type="audio/mpeg">
</audio>

<div class="story" id="card">

  <h1>ROHAN ORIGINAL ❤️</h1>
  <div class="subtitle">A Netflix-style love story</div>

  <p>
    Irene,<br>
    This rom-com only works<br>
    if you’re the lead character 😌
  </p>

  <div class="countdown" id="countdown"></div>

  <h2>Will you be my Valentine? 💘</h2>

  <button class="yes" onclick="yesClick()">Yes 💋</button>
  <button class="no" onmouseover="moveNo()">No 🙈</button>

</div>

<script>
// Countdown
function updateCountdown() {
  const valentine = new Date(new Date().getFullYear(), 1, 14);
  const now = new Date();
  const diff = valentine - now;

  if (diff <= 0) {
    countdown.innerHTML = "💖 It's Valentine’s Day 💖";
    return;
  }

  const d = Math.floor(diff / (1000*60*60*24));
  const h = Math.floor((diff / (1000*60*60)) % 24);
  const m = Math.floor((diff / (1000*60)) % 60);

  countdown.innerHTML = `⏳ ${d} days ${h} hrs ${m} mins left`;
}
setInterval(updateCountdown, 1000);
updateCountdown();

// YES click
function yesClick() {
  document.getElementById("music").play();

  card.innerHTML = `
    <h1>SHE SAID YES 💕</h1>
    <p>
      New favorite series unlocked 😍<br><br>
      <strong>“Rohan & Irene”</strong><br>
      Valentine Special ❤️
    </p>

    <button class="yes" onclick="showLetter()">Open Love Letter 💌</button>
    <button class="yes" onclick="shareScreen()">Share This 💖</button>

    <div class="letter" id="letter">
      Irene,<br><br>
      I don’t need a special day to love you,
      but I’ll happily use Valentine’s Day
      as an excuse to remind you how special
      you are to me 💕<br><br>
      — Yours, Rohan ❤️
    </div>
  `;

  setInterval(createKiss, 300);
}

// Hidden letter
function showLetter() {
  document.getElementById("letter").style.display = "block";
}

// Share screen
function shareScreen() {
  card.innerHTML = `
    <h1>❤️ SHE SAID YES ❤️</h1>
    <p>
      Officially taken 💍<br><br>
      Valentine: <strong>Irene</strong><br>
      Lucky guy: <strong>Rohan</strong><br><br>
      Screenshot this 📸<br>
      & share the love 💕
    </p>
  `;
}

// NO button
function moveNo() {
  const btn = document.querySelector('.no');
  btn.style.left = Math.random() * (window.innerWidth - 80) + 'px';
  btn.style.top = Math.random() * (window.innerHeight - 50) + 'px';
}

// Kiss animation
function createKiss() {
  const kiss = document.createElement('div');
  kiss.className = 'kiss';
  kiss.innerHTML = '💋';
  kiss.style.left = Math.random() * 100 + 'vw';
  kiss.style.top = Math.random() * 100 + 'vh';
  document.body.appendChild(kiss);
  setTimeout(() => kiss.remove(), 2500);
}
</script>

</body>
</html><!DOCTYPE html>
<html lang="en">
<head>
<meta charset="UTF-8">
<title>For Irene ❤️</title>
<meta name="viewport" content="width=device-width, initial-scale=1.0">

<style>
body {
  margin: 0;
  height: 100vh;
  background: radial-gradient(circle at top, #1a1a1a, #000);
  display: flex;
  align-items: center;
  justify-content: center;
  font-family: Arial, sans-serif;
  color: white;
  overflow: hidden;
}

/* Instagram Story size */
.story {
  width: 360px;
  height: 640px;
  background: #111;
  border: 2px solid #e50914;
  border-radius: 25px;
  box-shadow: 0 0 40px rgba(229,9,20,0.6);
  padding: 28px;
  text-align: center;
  display: flex;
  flex-direction: column;
  justify-content: center;
  animation: fadeIn 1.2s ease;
}

@keyframes fadeIn {
  from { opacity: 0; transform: scale(0.95); }
  to { opacity: 1; transform: scale(1); }
}

h1 {
  color: #e50914;
  font-size: 22px;
  margin-bottom: 5px;
}

.subtitle {
  font-size: 13px;
  color: #aaa;
  margin-bottom: 15px;
}

p {
  font-size: 15px;
  color: #ddd;
  line-height: 1.5;
}

h2 {
  margin-top: 15px;
  font-size: 17px;
}

.countdown {
  margin: 12px 0;
  font-size: 15px;
  color: #ffb3b3;
  font-weight: bold;
}

button {
  padding: 12px 24px;
  font-size: 15px;
  border-radius: 30px;
  border: none;
  cursor: pointer;
  margin: 8px auto;
  width: 75%;
}

.yes {
  background: #e50914;
  color: white;
}

.yes:hover {
  box-shadow: 0 0 15px #e50914;
}

.no {
  background: #444;
  color: #bbb;
  position: absolute;
}

/* Hidden Letter */
.letter {
  display: none;
  background: #000;
  border: 1px solid #e50914;
  border-radius: 15px;
  padding: 18px;
  margin-top: 10px;
  font-size: 14px;
  animation: fadeIn 1s ease;
}

/* Kiss animation */
.kiss {
  position: fixed;
  font-size: 28px;
  animation: kissFloat 2.5s ease forwards;
}

@keyframes kissFloat {
  0% { transform: scale(0); opacity: 0; }
  30% { transform: scale(1.2); opacity: 1; }
  100% { transform: translateY(-120px); opacity: 0; }
}
</style>
</head>

<body>

<!-- Music -->
<audio id="music" loop>
  <source src="https://cdn.pixabay.com/download/audio/2022/10/03/audio_8f02c2b7a5.mp3" type="audio/mpeg">
</audio>

<div class="story" id="card">

  <h1>ROHAN ORIGINAL ❤️</h1>
  <div class="subtitle">A Netflix-style love story</div>

  <p>
    Irene,<br>
    This rom-com only works<br>
    if you’re the lead character 😌
  </p>

  <div class="countdown" id="countdown"></div>

  <h2>Will you be my Valentine? 💘</h2>

  <button class="yes" onclick="yesClick()">Yes 💋</button>
  <button class="no" onmouseover="moveNo()">No 🙈</button>

</div>

<script>
// Countdown
function updateCountdown() {
  const valentine = new Date(new Date().getFullYear(), 1, 14);
  const now = new Date();
  const diff = valentine - now;

  if (diff <= 0) {
    countdown.innerHTML = "💖 It's Valentine’s Day 💖";
    return;
  }

  const d = Math.floor(diff / (1000*60*60*24));
  const h = Math.floor((diff / (1000*60*60)) % 24);
  const m = Math.floor((diff / (1000*60)) % 60);

  countdown.innerHTML = `⏳ ${d} days ${h} hrs ${m} mins left`;
}
setInterval(updateCountdown, 1000);
updateCountdown();

// YES click
function yesClick() {
  document.getElementById("music").play();

  card.innerHTML = `
    <h1>SHE SAID YES 💕</h1>
    <p>
      New favorite series unlocked 😍<br><br>
      <strong>“Rohan & Irene”</strong><br>
      Valentine Special ❤️
    </p>

    <button class="yes" onclick="showLetter()">Open Love Letter 💌</button>
    <button class="yes" onclick="shareScreen()">Share This 💖</button>

    <div class="letter" id="letter">
      Irene,<br><br>
      I don’t need a special day to love you,
      but I’ll happily use Valentine’s Day
      as an excuse to remind you how special
      you are to me 💕<br><br>
      — Yours, Rohan ❤️
    </div>
  `;

  setInterval(createKiss, 300);
}

// Hidden letter
function showLetter() {
  document.getElementById("letter").style.display = "block";
}

// Share screen
function shareScreen() {
  card.innerHTML = `
    <h1>❤️ SHE SAID YES ❤️</h1>
    <p>
      Officially taken 💍<br><br>
      Valentine: <strong>Irene</strong><br>
      Lucky guy: <strong>Rohan</strong><br><br>
      Screenshot this 📸<br>
      & share the love 💕
    </p>
  `;
}

// NO button
function moveNo() {
  const btn = document.querySelector('.no');
  btn.style.left = Math.random() * (window.innerWidth - 80) + 'px';
  btn.style.top = Math.random() * (window.innerHeight - 50) + 'px';
}

// Kiss animation
function createKiss() {
  const kiss = document.createElement('div');
  kiss.className = 'kiss';
  kiss.innerHTML = '💋';
  kiss.style.left = Math.random() * 100 + 'vw';
  kiss.style.top = Math.random() * 100 + 'vh';
  document.body.appendChild(kiss);
  setTimeout(() => kiss.remove(), 2500);
}
</script>

</body>
</html>
