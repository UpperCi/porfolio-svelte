<script>
  import { onMount } from 'svelte';
  export let src = "";
  export let href = "";
  let svgRoot;

  onMount(() => {
    fetch(src)
    .then(response => response.text())
    .then(text => {
      svgRoot.innerHTML = text;
    });
  });
</script>

<a href={href}>
  <div bind:this={svgRoot}></div>
  <p><slot /></p>
</a>

<style>
:global(svg) {
  width: 1.75em;
  height: 1.75em;
  color: #9F9FED;
  margin-bottom: -3px;
}

a {
  font-weight: 700;
  text-decoration: none;
  font-size: 12px;
  margin-left: 16px;
  color: #9F9FED;
  display: flex;
  flex-wrap: wrap;
  align-items: center;
  margin-bottom: 4px;
}

p {
  margin: 0;
  margin-left: 8px;
  width: fit-content;
}

div {
}
</style>
