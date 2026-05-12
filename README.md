<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8" />
  <meta name="viewport" content="width=device-width, initial-scale=1.0" />
  <title>Movie Website</title>
  <style>
    body {
      font-family: Arial, sans-serif;
      margin: 0;
      background: #111;
      color: #fff;
    }

    header {
      background: #222;
      padding: 20px;
      text-align: center;
    }

    .movies {
      display: grid;
      grid-template-columns: repeat(auto-fit, minmax(200px, 1fr));
      gap: 20px;
      padding: 20px;
    }

    .movie {
      background: #1c1c1c;
      border-radius: 8px;
      overflow: hidden;
      box-shadow: 0 4px 10px rgba(0,0,0,0.4);
    }

    .movie img {
      width: 100%;
      display: block;
    }

    .movie-content {
      padding: 15px;
    }

    .movie h3 {
      margin: 0 0 10px;
    }
  </style>
</head>
<body>
  <header>
    <h1>Movie Hub</h1>
  </header>

  <section class="movies" id="movies"></section>

  <script>
    const moviesContainer = document.getElementById("movies");

    const totalMovies = 100; // change this as needed

    for (let i = 1; i <= totalMovies; i++) {
      const movie = document.createElement("article");
      movie.className = "movie";
      movie.innerHTML = `
        <img src="https://via.placeholder.com/300x450?text=Movie+${i}" alt="Movie poster for Movie ${i}" />
        <div class="movie-content">
          <h3>Movie ${i}</h3>
          <p>Action • 2024</p>
        </div>
      `;
      moviesContainer.appendChild(movie);
    }
  </script>
</body>
</html>
