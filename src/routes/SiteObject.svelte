<script>
  import { onMount } from 'svelte';
  let container;
  const TIME = 200;
  let height = 0;
  let size = 1;
  let startMs = 0;

  const onGameStart = () => {
    if (height == 0) {
      height = container.getBoundingClientRect().height;
    }
    requestAnimationFrame(shrink(true));
  }

  const onGameEnd = () => {
    requestAnimationFrame(shrink(false));
    container.style.display = "inherit";
  }

  const shrink = (close) => (ms) => {
    if (startMs == 0) {
      startMs = ms;
    }
    const diff = (ms - startMs) / TIME;
    if (close) {
      container.style["max-height"] = `${height * (1 - diff)}px`;
    } else {
      container.style["max-height"] = `${height * diff}px`;
    }

    if (ms - startMs < TIME) {
      requestAnimationFrame(shrink(close));
    } else {
      startMs = 0;
      if (close) {
        container.style.display = "none";
      } else {
        container.style["max-height"] = `fit-content`;
      }
    }
  }

  onMount(async () => {
    window.addEventListener("startGame", onGameStart);
    window.addEventListener("endGame", onGameEnd);
  })
</script>

<div bind:this={container} class="">
  <slot />
</div>

<style>
div {
  overflow: hidden;
}
</style>