<!DOCTYPE html>
<html lang="en">
<head>
<meta charset="UTF-8" />
<meta name="viewport" content="width=device-width, initial-scale=1.0" />
<title>Valentine 💘</title>

<style>
  body {
    margin: 0;
    font-family: 'Arial', sans-serif;
    background: linear-gradient(135deg, #ffb6c1, #ff69b4);
    height: 100vh;
    display: flex;
    align-items: center;
    justify-content: center;
    overflow: hidden;
  }

  .card {
    background: white;
    padding: 30px 20px;
    border-radius: 20px;
    text-align: center;
    width: 90%;
    max-width: 350px;
    box-shadow: 0 10px 30px rgba(0,0,0,0.2);
  }

  h1 {
    font-size: 1.6rem;
    color: #ff4d6d;
  }

  .buttons {
    margin-top: 30px;
    position: relative;
    height: 120px;
  }

  button {
    padding: 12px 25px;
    font-size: 1rem;
    border: none;
    border-radius: 30px;
    cursor: pointer;
  }

  #yes {
    background: #ff4d6d;
    color: white;
  }

  #no {
    background: #ffd6e0;
    color: #ff4d6d;
    position: absolute;
    left: 60%;
    top: 50%;
  }

  .bee {
    font-size: 2.5rem;
    animation: float 2s infinite ease-in-out;
  }

  @keyframes float {
    0% { transform: translateY(0); }
    50% { transform: translateY(-10px); }
    100% { transform: translateY(0); }
  }
</style>
</head>

<body>

<audio autoplay loop>
  <source src="music.mp3" type="audio/mpeg">
</audio>

<div class="card">
  <div class="bee">🐝</div>
  <h1>Will you bee my Valentine, Macho?</h1>

  <div class="buttons">
    <button id="yes" onclick="goYes()">Yes 💖</button>
    <button id="no">No 🙄</button>
  </div>
</div>

<script>
  const noBtn = document.getElementById("no");

  noBtn.addEventListener("mouseover", moveButton);
  noBtn.addEventListener("click", moveButton);

  function moveButton() {
    const x = Math.random() * 200 - 100;
    const y = Math.random() * 200 - 100;
    noBtn.style.transform = `translate(${x}px, ${y}px)`;
  }

  function goYes() {
    window.location.href = "yes.html";
  }
</script>

</body>
</html>
