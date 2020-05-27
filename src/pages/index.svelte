<script>
  import { url } from '@sveltech/routify'
</script>

<style>
  nav {
    width: 100%;
    display: flex;
    flex-direction: column;
    align-items: center;
    justify-content: center;
  }

  nav a {
    width: 100%;
    text-align: center;
    line-height: 2;
    display: block;
    padding: 2rem;
    border: 1px solid var(--purple);
    margin-bottom: 1rem;
    font-size: 1.3rem;
  }

  h1 {
    text-transform: uppercase;
    line-height: 2;
    text-align: center;
  }

  .container {
    width: 75%;
    margin: 0 auto;
  }
</style>

<div class="container">
  <h1>Elegi la fuente que queres usar:</h1>
  <nav>
    <a href={$url("/longo")}>
      Tecnica Dietoterapica, Elsa Longo, Elizabeth Navarro
    </a>
    <a href={$url("/lujan")}>
      Universidad Nacional de Lujan
    </a>
  </nav>
</div>
