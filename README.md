<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8">
  <title>Happy Birthday Sanu</title>
  <style>
    body {
      margin: 0;
      font-family: 'Comic Sans MS', cursive;
      background: #fff0f5;
      text-align: center;
      overflow: hidden;
    }
    .page {
      display: none;
      padding: 40px;
    }
    .active {
      display: block;
    }
    h1, h2 {
      color: #d63384;
      text-shadow: 1px 1px 3px #000;
    }
    p {
      font-size: 1.2em;
      color: #333;
      max-width: 700px;
      margin: 0 auto 20px;
    }
    button {
      background-color: #ff69b4;
      border: none;
      color: white;
      padding: 10px 25px;
      font-size: 1.2em;
      border-radius: 25px;
      cursor: pointer;
      margin-top: 20px;
      transition: background 0.3s;
    }
    button:hover {
      background-color: #ff1493;
    }
    .cake {
      position: relative;
      width: 200px;
      height: 150px;
      background: #ffb347;
      margin: 40px auto;
      border-radius: 10px;
      box-shadow: 0 8px #e07b39;
      cursor: pointer;
    }
    .candle {
      position: absolute;
      top: -60px;
      left: 90px;
      width: 20px;
      height: 40px;
      background: #fff;
      border-radius: 5px;
    }
    .flame {
      position: absolute;
      top: -20px;
      left: 5px;
      width: 10px;
      height: 20px;
      background: orange;
      border-radius: 50% 50% 0 0;
      animation: flicker 0.4s infinite alternate;
    }
    @keyframes flicker {
      from { transform: scaleY(1); opacity: 1; }
      to   { transform: scaleY(1.2); opacity: 0.7; }
    }
    .cake.cut {
      transform: scale(0.95) rotate(-2deg);
      transition: transform 0.3s ease;
    }
    img {
      max-width: 90%;
      border-radius: 20px;
      margin: 20px auto;
      display: block;
    }
    audio {
      display: none; /* hide controls */
    }
  </style>
</head>
<body>

  <!-- Autoplaying “Happy Birthday” song -->
  <audio id="bgSong" autoplay loop>
    <source src="https://cdn.pixabay.com/download/audio/2022/03/15/audio_d70c6ad04b.mp3?filename=happy-birthday-to-you-11235.mp3" type="audio/mpeg">
    <!-- If that link ever breaks, download your own MP3 and replace the src with "happy_birthday_song.mp3" -->
  </audio>

  <!-- PAGE 1: Love Letter -->
  <div class="page active" id="page1">
    <h1>Happy Birthday, Sanu ❤️</h1>
    <p>
      My dearest Penguin,<br>
      Today is not just your birthday—it's the celebration of the day the most beautiful soul entered the world and then into my life. 💖
    </p>
    <button onclick="nextPage()">Next ❤️</button>
  </div>

  <!-- PAGE 2: Blow Candle -->
  <div class="page" id="page2">
    <h1>Make a Wish & Blow the Candle 🎂</h1>
    <div class="cake" onclick="blowCandle()">
      <div class="candle" id="candle">
        <div class="flame" id="flame"></div>
      </div>
    </div>
    <button onclick="nextPage()">Next ❤️</button>
  </div>

  <!-- PAGE 3: Cut Cake -->
  <div class="page" id="page3">
    <h1>Now Cut the Cake 🍰</h1>
    <div class="cake" id="cutCake" onclick="cutCake()">Click to Cut</div>
    <button onclick="nextPage()">Next ❤️
