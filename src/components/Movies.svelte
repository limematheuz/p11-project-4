<script>
  const url =
    "https://api.themoviedb.org/3/discover/movie?include_adult=false&include_video=false&language=en-US&page=1&sort_by=popularity.desc";
  const options = {
    method: "GET",
    headers: {
      accept: "application/json",
      Authorization:
        "Bearer eyJhbGciOiJIUzI1NiJ9.eyJhdWQiOiJiYjQ5NzUzYTFiZTgzN2FkMjA4YzRlNDQwYTJiMWU3NyIsInN1YiI6IjY1MmZhZTRjMGNiMzM1MTZmNzQ5ODE0ZiIsInNjb3BlcyI6WyJhcGlfcmVhZCJdLCJ2ZXJzaW9uIjoxfQ.OY3iqx89juRheOjZpvA3u9JwNVY-Qr5EVX7mAiPbJb0",
    },
  };

  let movies = [];

  fetch(url, options)
    .then((response) => response.json())
    .then((data) => (movies = data.results))
    .catch((err) => console.error(err));
</script>

<div>
  {#each movies as movie}
    <img
      src={`https://image.tmdb.org/t/p/original/${movie.poster_path}`}
      alt="Cover"
    />
    <img
      src={`https://image.tmdb.org/t/p/original/${movie.poster_path}`}
      alt="Cover"
    />
    <img
      src={`https://image.tmdb.org/t/p/original/${movie.poster_path}`}
      alt="Cover"
    />
  {/each}
</div>

<style>
  div {
    display: flex;
    flex-wrap: wrap;
    justify-content: center;
    gap: 15px;
  }

  img {
    width: 235px;
    object-fit: cover;
    border: none;
    border-radius: 10px;
  }
 
</style>
