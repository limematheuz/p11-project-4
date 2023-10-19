<script>
  import Header from "./components/Header.svelte";
  import Movies from "./components/Movies.svelte";
  import Hero from "./components/Hero.svelte";
</script>


  
  <Header />

  <Hero />

  <h2>Descúbre</h2>
  <Movies
    url="https://api.themoviedb.org/3/discover/movie?include_adult=false&include_video=false&language=en-US&page=1&sort_by=popularity.desc"
  />

  <h2>Más valoradas</h2>
  <Movies
    url="https://api.themoviedb.org/3/movie/top_rated?language=en-US&page=1"
  />

  <h2>ESTRENOS</h2>
  <Movies
    url="https://api.themoviedb.org/3/movie/upcoming?language=en-US&page=1"
  />

