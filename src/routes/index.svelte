<script>
  import Logo from "../components/svg/Logo";
  import SandboxLogo from "../components/svg/Sandbox";
  import Icon from '../components/Icon'

  let darkMode = false;
  function toggleDarkMode() {
    darkMode = !darkMode;
    document.documentElement.setAttribute("data-dark-theme", darkMode);
  }
</script>

<style lang="scss">
  @import "../styles/theme.scss";
  $icon-size: 2rem;

  main {
    text-align: center;
  }
  .logo {
    display: inline-block;
    width: 4rem;
  }

  .icons {
    display: inline-flex;
    width: 10rem;
    justify-content: space-between;
  }

  .icon {
    background-color: var(--main-color);
    border-radius: 50%;
    color: var(--bg-color);
    height: $icon-size;
    width: $icon-size;
    display: flex;
    align-items: center;
    justify-content: center;

    :global(.icon__img) {
      height: $icon-size * 0.7;
      width: $icon-size * 0.7;
      display: block;
      color: var(--bg-color);
    }
  }

  .icon--no-border {
    color: var(--main-color);
    height: $icon-size;
    width: $icon-size;
  }

  .dark-mode {
    appearance: none;
    position: fixed;
    top: 16px;
    right: 16px;
    color: var(--main-color);
    height: 1.8rem;
    width: 1.8rem;
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
  <div class="logo">
    <Logo />
  </div>
  <h1>Daniel Navarrete</h1>
  <h2>Web developer</h2>

  <div class="icons">
    <a class="icon" href="https://twitter.com/dnlnav" target="_blank">
      <Icon name="mdiTwitter" class="icon__img"/>
    </a>
    <a
      class="icon"
      href="https://www.linkedin.com/in/daniel-navarrete-349220b4/" target="_blank">
      <Icon name="mdiLinkedin" class="icon__img"/>
    </a>
    <a class="icon--no-border" href="https://github.com/dnlnav" target="_blank">
      <Icon name="mdiGithub" viewBox="2 2 20 20"/>
    </a>
    <a class="icon" href="https://codesandbox.io/u/dnlnav" target="_blank">
      <SandboxLogo class="icon__img"/>
    </a>
  </div>
  <div class="dark-mode" on:click={toggleDarkMode}>
    {#if darkMode}
      <Icon name="mdiLightbulbOn"/>
    {:else}
      <Icon name="mdiLightbulb"/>
    {/if}
  </div>
</main>
