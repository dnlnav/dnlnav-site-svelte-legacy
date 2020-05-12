<script>
  let darkMode = false;
  function toggleDarkMode() {
    darkMode = !darkMode;
    document.documentElement.setAttribute("data-dark-theme", darkMode);
  }
</script>

<style lang="scss">
  @import "../styles/theme.scss";

  main {
    text-align: center;
  }
  .logo {
    width: 4rem;
  }

  .icons {
    display: inline-flex;
  }

  .icon {
    display: block;
    text-align: center;
    background-color: var(--main-color);
    border-radius: 50%;
    color: var(--bg-color);
    font-size: 1rem;
    height: 1.5rem;
    width: 1.5rem;
  }

  .icon--no-border {
    color: var(--main-color);
    font-size: 1.5rem;
    line-height: 1;
  }

  .icon__img {
    height: 1rem;
    width: 1rem;
    filter: invert(1);
    display: inline-block;
  }
  .dark-mode {
    appearance: none;
    position: fixed;
    top: 16px;
    right: 16px;
    color: var(--main-color);
  }
</style>

<svelte:head>
  <title>Daniel Navarrete | Web Developer</title>
  <script
    src="https://kit.fontawesome.com/8cab238fe7.js"
    crossorigin="anonymous">

  </script>
</svelte:head>

<main>
{#if darkMode}
    <img class="logo" alt="Logo" src="logo_white.png" />
  {:else}
    <img class="logo" alt="Logo" src="logo_black.png" />
  {/if}
  <h1>Daniel Navarrete</h1>
  <h2>Web developer</h2>

  <div class="icons">
    <a class="icon" href="https://twitter.com/dnlnav">
      <i class="fab fa-twitter" />
    </a>
    <a
      class="icon"
      href="https://www.linkedin.com/in/daniel-navarrete-349220b4/">
      <i class="fab fa-linkedin-in" />
    </a>
    <a class="icon--no-border" href="https://github.com/dnlnav">
      <i class="fab fa-github" />
    </a>
    <a class="icon" href="https://codesandbox.io/u/dnlnav">
      <img class="icon__img" src="codesandbox.svg" alt="CodeSandBox" />
    </a>
  </div>
  <div class="dark-mode" on:click={toggleDarkMode}>
  {#if darkMode}
    <i class="fas fa-lightbulb"></i>
  {:else}
    <i class="far fa-lightbulb"></i>
  {/if}
  </div>
</main>
