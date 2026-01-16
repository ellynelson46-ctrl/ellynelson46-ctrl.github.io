<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8">
  <title>My Games</title>
  <meta name="viewport" content="width=device-width, initial-scale=1.0">

  <style>
    * {
      box-sizing: border-box;
      font-family: Arial, Helvetica, sans-serif;
    }

    body {
      margin: 0;
      background: #0f0f0f;
      color: #fff;
    }

    header {
      background: #1b1b1b;
      padding: 20px;
      text-align: center;
      border-bottom: 2px solid #2e2e2e;
    }

    header h1 {
      margin: 0;
      font-size: 36px;
      color: #00ff88;
    }

    header p {
      margin-top: 5px;
      color: #aaa;
    }

    .search-box {
      margin: 20px auto;
      max-width: 400px;
      display: flex;
    }

    .search-box input {
      width: 100%;
      padding: 10px;
      border-radius: 5px;
      border: none;
      outline: none;
      font-size: 16px;
    }

    .games {
      display: grid;
      grid-template-columns: repeat(auto-fill, minmax(180px, 1fr));
      gap: 20px;
      padding: 30px;
      max-width: 1200px;
      margin: auto;
    }

    .game-card {
      background: #1c1c1c;
      border-radius: 10px;
      padding: 15px;
      text-align: center;
      cursor: pointer;
      transition: transform 0.2s, background 0.2s;
    }

    .game-card:hover {
      transform: scale(1.05);
      background: #262626;
    }

    .game-card img {
      width: 100%;
      height: 120px;
      object-fit: cover;
      border-radius: 8px;
    }

    .game-card h3 {
      margin: 10px 0 0;
      font-size: 18px;
    }

    footer {
      text-align: center;
      padding: 15px;
      background: #1b1b1b;
      color: #777;
      font-size: 14px;
    }
  </style>
</head>

<body>

  <header>
    <h1>My Games</h1>
    <p>Play unblocked browser games</p>
  </header>

  <div class="search-box">
    <input type="text" id="search" placeholder="Search games..." onkeyup="searchGames()">
  </div>

  <section class="games" id="gameList">
    <div class="game-card">
      <img src="https://via.placeholder.com/300x150" alt="">
      <h3>Game One</h3>
    </div>

    <div class="game-card">
      <img src="https://via.placeholder.com/300x150" alt="">
      <h3>Game Two</h3>
    </div>

    <div class="game-card">
      <img src="https://via.placeholder.com/300x150" alt="">
      <h3>Game Three</h3>
    </div>

    <div class="game-card">
      <img src="https://via.placeholder.com/300x150" alt="">
      <h3>Game Four</h3>
    </div>
  </section>

  <footer>
    © 2026 My Games | Hosted on GitHub Pages
  </footer>

  <script>
    function searchGames() {
      let input = document.getElementById("search").value.toLowerCase();
      let games = document.getElementsByClassName("game-card");

      for (let i = 0; i < games.length; i++) {
        let title = games[i].innerText.toLowerCase();
        games[i].style.display = title.includes(input) ? "block" : "none";
      }
    }
  </script>

</body>
</html>

