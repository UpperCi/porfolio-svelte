<script>
  import { onMount } from 'svelte';
  export let src = "";
  export let href = "";
  export let dark = false;
  let svgRoot;

  onMount(() => {
    fetch(src)
    .then(response => response.text())
    .then(text => {
      svgRoot.innerHTML = text;
    });
  });
</script>

<a class:dark={dark} href={href}>
  <div bind:this={svgRoot}></div>
  <p><slot /></p>
</a>

<style>
:global(svg) {
  width: 1.75em;
  height: 1.75em;
  color: #5E4F89;
  margin-bottom: -3px;
}

a {
  font-weight: 700;
  text-decoration: none;
  font-size: 14px;
  margin-left: 16px;
  color: #5E4F89;
  display: flex;
  flex-wrap: wrap;
  align-items: center;
  margin-bottom: 4px;
}

a:hover {
  text-decoration: underline;
}

a.dark, a.dark :global(svg) {
  color: #EEEDE2;
}

p {
  margin: 0;
  margin-left: 8px;
  width: fit-content;
}

div {
}
</style>
