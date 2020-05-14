<script>
  import * as icons from "@mdi/js";
  export let name;
  export let viewBox = "0 0 24 24";
  let icon;
  $: path = icons[name];
</script>
{#if path}
  <svg class={$$props.class} {viewBox} >
    <path fill="currentColor" d={path} />
  </svg>
{/if}
