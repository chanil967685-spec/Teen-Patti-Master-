<!DOCTYPE html>
<html>
<head>
  <title>Dragon vs Tiger</title>
  <style>
    body {
      font-family: Arial;
      text-align: center;
      background: #111;
      color: white;
    }
    button {
      padding: 15px 30px;
      margin: 10px;
      font-size: 18px;
      border-radius: 8px;
    }
  </style>
</head>

<body>

  <h1>🐉 Dragon vs 🐯 Tiger</h1>
  <h2 id="points">Points: 100</h2>
  <h3 id="result">Choose One</h3>

  <button onclick="play('Dragon')">Dragon</button>
  <button onclick="play('Tiger')">Tiger</button>
  <button onclick="play('Tie')">Tie</button>

<script>
  let points = 100;
  let lastResult = "";

  function play(choice) {

    let outcomes = ["Dragon","Tiger","Dragon","Tiger","Tie"];
    let result = outcomes[Math.floor(Math.random()*outcomes.length)];

    document.getElementById("result").innerText =
      "Result: " + result;

    if (choice === result) {
      points += (result === "Tie") ? 80 : 10;
    } else {
      points -= 10;
    }

    document.getElementById("points").innerText =
      "Points: " + points;
  }
</script>

<p style="margin-top:20px;font-size:12px;">
Entertainment only. No real money.
</p>

</body>
</html>
