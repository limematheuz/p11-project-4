<script>
    import Derecha from "../assets/arrowRight.png"
    import Izquierda from "../assets/arrowLeft.png"

    export let movies;

    const rotateLeft = e => {
        const transitioningImage = movies[movies.length -1]
        movies = [movies[movies.length -1],...movies.slice(0, movies.lenght -1)]  
}
    const rotateRight = e => {
        const transitioningImage = movies[0]
        movies = [...movies.slice(1, movies.lenght), movies[0]]
}
</script>

<div id=carouselContainer>
    <div id=carouselImages>
        {#each movies as movie (movie.id)}
            <img src={movie.path} alt={movie.id} id={movie.id}/>
        {/each}
    </div>
    <button id="left" on:click={rotateLeft}>
        <slot name="=leftControl">
            <img src={Izquierda}>
        </slot>
    </button>
    <button id="right" on:click={rotateRight}>
        <slot name="=leftControl">
            <img src={Derecha}>
        </slot>
    </button>
</div>

