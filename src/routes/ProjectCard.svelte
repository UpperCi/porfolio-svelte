<script>
  export let title;
  export let image;
  let expanded = false;
</script>

<div on:click={() => expanded = !expanded} class={`card ${expanded ? "full" : ""}`}>
  <img src={image}>
  <div class="card-body">
    <h2>{title}</h2>
    <slot />
  </div>
</div>

<style>
:global(h2) {
  font-size: 24px;
  margin: 0;
  width: 100%;
  text-align: center;
  font-weight: 700;
}

:global(p) {
}

img {
  height: 200px;
  width: 100%;
  margin: 0;
  object-fit: cover;
}

div.card-body {
  padding: 0px 6px 4px 6px;
  max-height: 38px;
  transition: max-height linear 0.1s;
}

div.full div.card-body {
  max-height: 400px;
}

div.card {
  overflow: hidden;
  cursor: pointer;
  font-size: 14px;
}

div.card:hover {
}
</style>
