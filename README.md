# Valentines-gift-
Click here for a surprise 
<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8">
  <title>Loading…</title>
  <style>
    body {
      font-family: Arial, sans-serif;
      background: linear-gradient(135deg, #ff9a9e, #fad0c4);
      display: flex;
      align-items: center;
      justify-content: center;
      height: 100vh;
      margin: 0;
      text-align: center;
    }
    .box {
      background: white;
      padding: 35px;
      border-radius: 18px;
      box-shadow: 0 15px 30px rgba(0,0,0,0.15);
      max-width: 340px;
      position: relative;
    }
    .heart {
      font-size: 48px;
      animation: pulse 1s infinite;
    }
    .btn {
      margin: 12px 8px 0;
      padding: 10px 22px;
      border: none;
      border-radius: 25px;
      font-size: 16px;
      cursor: pointer;
    }
    .yes {
      background: #ff4d6d;
      color: white;
    }
    .yes:hover {
      background: #e63950;
    }
    .no {
      background: #ddd;
      color: #555;
      position: absolute;
    }
    @keyframes pulse {
      0% { transform: scale(1); }
      50% { transform: scale(1.25); }
      100% { transform: scale(1); }
    }
  </style>
</head>
<body>

<div class="box" id="content">
  <p>Loading something special…</p>
</div>

<script>
  setTimeout(() => {
    document.title = "👀 Wait a sec…";
    document.getElementById("content").innerHTML = `
      <div class="heart">❤️</div>
      <h2>Hey Danaysia 😏</h2>
      <p>I tried not to make this obvious…</p>
      <p>but you stay on my mind.</p>
      <p><strong>So let’s not pretend.</strong></p>
      <p>Will you be my Valentine? 💘</p>
      <button class="btn yes" onclick="finalReveal()">Yes</button>
      <button class="btn no" id="noBtn">No</button>
    `;

    const noBtn = document.getElementById("noBtn");
    noBtn.style.top = "220px";
    noBtn.style.left = "120px";

    noBtn.addEventListener("mouseover", () => {
      const box = document.querySelector(".box");
      const maxX = box.clientWidth - noBtn.offsetWidth;
      const maxY = box.clientHeight - noBtn.offsetHeight;

      const randX = Math.random() * maxX;
      const randY = Math.random() * maxY;

      noBtn.style.left = randX + "px";
      noBtn.style.top = randY + "px";
    });
  }, 2200);

  function finalReveal() {
    document.getElementById("content").innerHTML = `
      <div class="heart">💖</div>
      <h2>Knew you’d say yes, Danaysia.</h2>
      <p>You look real good as my Valentine 😌</p>
      <p>Happy Valentine’s Day 💕</p>
    `;
  }
</script>

</body>
</html>
