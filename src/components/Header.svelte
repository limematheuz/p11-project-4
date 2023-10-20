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
    width: 100vw;
    position: fixed;
    font-size: 18px;
    height: 100px;
    background-color: #0606139a;
    display: flex;
    justify-content: start;
    align-items: center;
    gap: 18px;
    z-index: 999;
  }
  .end-btns {
    display: flex;
    justify-content: end;
    align-items: center;
    margin-left: auto;
    margin-right: 70px;
  }
</style>
