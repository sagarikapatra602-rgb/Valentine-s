<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8">
  <title>Loading...</title>
  <style>
    body {
      font-family: Arial, sans-serif;
      background: #000;
      color: #fff;
      display: flex;
      align-items: center;
      justify-content: center;
      height: 100vh;
      margin: 0;
    }
    .box {
      text-align: center;
      background: #111;
      padding: 30px;
      border-radius: 15px;
      width: 320px;
    }
    button {
      padding: 10px 20px;
      margin: 10px;
      border-radius: 20px;
      border: none;
      font-size: 16px;
      cursor: pointer;
    }
    #yes { background: #ff4d6d; color: #fff; }
    #no { background: #444; position: absolute; }
    #final {
      display: none;
      color: #ff4d6d;
      font-size: 18px;
      margin-top: 20px;
    }
  </style>
</head>
<body>

<div class="box" id="loading">
  <h2>🔒 Opening secure link...</h2>
  <p>Please wait ❤️</p>
</div>

<div class="box" id="question" style="display:none;">
  <h2>Sanket 💖</h2>
  <p>Will you be my Valentine?</p>
  <button id="yes" onclick="yesClick()">Yes</button>
  <button id="no" onmouseover="moveNo()">No</button>
  <div id="final">YAY! 💘  
    <br>You’re officially my Valentine 😌  
    <br>— Sagarika ❤️
  </div>
</div>

<script>
  setTimeout(() => {
    document.getElementById("loading").style.display = "none";
    document.getElementById("question").style.display = "block";
  }, 2500);

  function moveNo() {
    const noBtn = document.getElementById("no");
    noBtn.style.left = Math.random() * (window.innerWidth - 100) + "px";
    noBtn.style.top = Math.random() * (window.innerHeight - 50) + "px";
  }

  function yesClick() {
    document.getElementById("final").style.display = "block";
  }
</script>

</body>
</html>
