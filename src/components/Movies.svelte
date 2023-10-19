<script>
  import { onMount } from "svelte";

  export let url;

  const options = {
    method: "GET",
    headers: {
      accept: "application/json",
      Authorization:
        "Bearer eyJhbGciOiJIUzI1NiJ9.eyJhdWQiOiJiYjQ5NzUzYTFiZTgzN2FkMjA4YzRlNDQwYTJiMWU3NyIsInN1YiI6IjY1MmZhZTRjMGNiMzM1MTZmNzQ5ODE0ZiIsInNjb3BlcyI6WyJhcGlfcmVhZCJdLCJ2ZXJzaW9uIjoxfQ.OY3iqx89juRheOjZpvA3u9JwNVY-Qr5EVX7mAiPbJb0",
    },
  };

  let movies = [];

  onMount(async () => {
    fetch(url, options)
      .then((response) => response.json())
      .then((data) => {
        movies = data.results;
      })
      .catch((err) => console.error(err));
  });
</script>


<div>
  {#each movies as movie}
    <img
      src={`https://image.tmdb.org/t/p/original/${movie.poster_path}`}
      alt="Cover"
    />
  {/each}
</div>

<style>
  div {
    display: flex;
    flex-direction: row;
    justify-content: center;
    gap: 20px;
    overflow-x: scroll;
    margin-bottom: 80px;
  }

  div::-webkit-scrollbar {
    height: 12px;
    background-color: rgba(240, 248, 255, 0);
    behavior: smooth;
  }
  div::-webkit-scrollbar-thumb {
    background-color: rgb(51, 49, 49);
    border-radius: 20px;
    border: 1px solid rgb(136, 134, 134);
    width: 10px;
    behavior: smooth;
  }

  img {
    height: 500px;
    width: 335px;
    object-fit: cover;
    border: none;
    border-radius: 10px;
    margin-bottom: 16px;
    margin-top: 20px;
  }
  img{
    width: 250px;
    flex-grow: 6;
    object-fit: cover;
    opacity: .6;
    transition: .5s ease;
    box-shadow: 5px 5px 25px 8px rgba(74, 22, 143, 0.5);
  }
  img:hover{
    cursor: grab;
    width: 600px;
    opacity: 1;
    box-shadow:  inset 0 -3em 3em rgba(0, 0, 0, 0.1),
    0 0 0 2px rgb(76, 13, 94),
    0.3em 0.3em 1em rgba(0, 0, 0, 0.3);;
    filter: contrast(100%);
  }

</style>
