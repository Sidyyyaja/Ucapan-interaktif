<!DOCTYPE html><html lang="id">
<head>
  <meta charset="UTF-8" />
  <meta name="viewport" content="width=device-width, initial-scale=1.0" />
  <title>Ucapan Spesial!</title>
  <style>
    body {
      font-family: 'Comic Sans MS', cursive;
      text-align: center;
      background-color: #fffbe7;
      color: #333;
      padding: 20px;
    }
    .container {
      max-width: 400px;
      margin: auto;
      background: #fff;
      padding: 20px;
      border-radius: 15px;
      box-shadow: 0 0 10px rgba(0,0,0,0.1);
    }
    button {
      padding: 10px 20px;
      margin-top: 15px;
      background-color: #ffb6c1;
      border: none;
      border-radius: 10px;
      font-size: 16px;
      cursor: pointer;
    }
    .hidden { display: none; }
    .gift-options button {
      display: block;
      margin: 10px auto;
      background-color: #ffd700;
    }
  </style>
</head>
<body>
  <div class="container">
    <h2>Masukin Nama Kamu 💌</h2>
    <input type="text" id="nameInput" placeholder="Namaku..." />
    <br>
    <button onclick="showMessage()">Lanjut</button><div id="messageSection" class="hidden">
  <h3 id="greeting"></h3>
  <p>Yuk pilih salah satu hadiah di bawah ini~ 🎁</p>
  <div class="gift-options">
    <button onclick="revealGift(1)">🎁 Hadiah 1</button>
    <button onclick="revealGift(2)">🎁 Hadiah 2</button>
    <button onclick="revealGift(3)">🎁 Hadiah 3</button>
  </div>
  <div id="giftMessage" class="hidden">
    <p id="giftText"></p>
  </div>
</div>

  </div>  <script>
    function showMessage() {
      const name = document.getElementById("nameInput").value;
      if (name.trim() === "") return alert("Tulis nama dulu donggg🙈");

      document.getElementById("greeting").textContent = `Haloooo ${name}~ Ini ada sesuatu untukmu 💖`;
      document.getElementById("messageSection").classList.remove("hidden");
    }

    function revealGift(number) {
      let message = "";
      if (number === 1) message = "Ceileh dapat pelukan virtual paling hangattt dari aku yang comel ini wkwk! 🤗💞";
      else if (number === 2) message = "Selamat! Kamu dapet kupon senyum gratis dari aku 😙✨";
      else if (number === 3) message = "Waduuhh sabar yaa, hadiahnya masih otw nich🫢";

      document.getElementById("giftText").textContent = message;
      document.getElementById("giftMessage").classList.remove("hidden");
    }
  </script></body>
</html>
