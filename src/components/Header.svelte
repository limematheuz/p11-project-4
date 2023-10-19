<script>
  import Logo from "./Logo.svelte";
  import Link from "./Link.svelte";
  import GreenButton from "./GreenButton.svelte";
  import IniciarButton from "./IniciarButton.svelte";
  import Lupa from "./Lupa.svelte";
</script>

<header>
  <Logo />
  <nav>
    <Link text="Inicio" />
    <Link text="Películas" />
    <Link text="Series" />
    <Link text="Colecciones" />
    <Link text="Festivales" />
    <Link text="Más" />
    <Link text="⬇"/>
  </nav>
  <div class="end-btns">
    <GreenButton />
    <IniciarButton />
    <Lupa />
  </div>
</header>

<style>
  header {
    display: flex;
    justify-content: flex-start;
    align-items: center;
    margin: 20px 40px;
    gap: 20px;
    margin-bottom: 150px;
    padding-top: none;
    margin-top: 0;
    
  }
  .end-btns {
    display: flex;
    justify-content: end;
    align-items: center;
    margin-left: auto;
   
  }
</style>
