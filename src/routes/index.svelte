<style>
  :root {
    --black: color();
  }
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
    background-color: var(--black);
    border-radius: 50%;
    color: #fff;
    font-size: 1rem;
    height: 1.5rem;
    width: 1.5rem;
  }

  .icon--no-border {
    color: var(--black);
    font-size: 1.5rem;
    line-height: 1;
  }

  .icon__img {
    height: 1rem;
    width: 1rem;
    filter: invert(1);
    display: inline-block;
  }
</style>

<svelte:head>
  <title>Sapper project template</title>
  <script
    src="https://kit.fontawesome.com/8cab238fe7.js"
    crossorigin="anonymous">

  </script>
</svelte:head>

<main>
  <img class="logo" alt="Logo" src="logo_black.png" />
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
</main>
