<script>
  import { url, params } from '@sveltech/routify'
  const { source } = $params;
</script>

<style>
  nav {
    width: 100%;
    height: calc(100vh - 16px);
    display: flex;
    align-items: center;
    flex-wrap: wrap;
  }

  nav a {
    display: flex;
    align-items: center;
    justify-content: center;
    width: 50%;
    position: relative;
    flex-direction: column;
  }

  nav a::after {
    content: '';
    position: absolute;
    width: 90px;
    height: 90px;
    border-radius: 50%;
    background-color: #ffffff;
    top: 50%;
    left: 50%;
    transform: translate(-50%, -50%);
    z-index: -1;
  }

  img {
    width: 40px;
    height: 40px;
  }
</style>

<nav>
  <a href={$url(`/${source}/egg`)}>
    <img src="images/egg.png" alt="Huevo." />
    Huevo
  </a>
  <a href={$url(`/${source}/vegetable`)}>
      <img src="images/carrot.png"  alt="Vegetal."/>
      Vegetal
    </a>
  <a href={$url(`/${source}/cereal`)}>
    <img src="images/cereal.png" alt="Cereal."/>
    Cereal
  </a>
  <a href={$url(`/${source}/fat`)}>
    <img src="images/hamburger.png" alt="Grasas." />
    Grasas
  </a>
  {#if source !== 'longo'}
    <a href={$url(`/${source}/fish`)}>
      <img src="images/fish.png" alt="Pescado." />
      Pescado
    </a>
  {/if}
  <a href={$url(`/${source}/meat`)}>
    <img src="images/meat.png" alt="Carne." />
    Carne
  </a>
  <a href={$url(`/${source}/fruit`)}>
    <img src="images/lemon.png" alt="Fruta." />
    Fruta
  </a>
  <a href={$url(`/${source}/milk`)}>
    <img src="images/milk.png" alt="Leche." />
    Leche
  </a>
  <a href={$url(`/${source}/misc`)}>
    <img src="images/popcorn.png" alt="Misc." />
    Misc
  </a>
  {#if source !== 'longo'}
    <a href={$url(`/${source}/prod-az`)}>
      <img src="images/lollipop.png" alt="Prod AZ." />
      Prod AZ
    </a>
  {/if}
</nav>
