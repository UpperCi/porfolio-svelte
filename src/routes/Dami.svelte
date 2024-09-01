<script>
  import { onMount } from 'svelte';
  import BezierEasing from 'bezier-easing';
  let dami;
  let flipStart = 0;
  let flipPos = 0;
  const FLIP_TIME = 900;
  const smooth = BezierEasing(0, 0.0, 0.1, 1)

  let gameStarted = false;
  const startEvent = new Event("startGame");
  const endEvent = new Event("endGame");

  const onKey = (e) => {
    if (e.key == "Enter") {
      onFlip();
    }
  }

  const onFlip = () => {
    if (!gameStarted) {
      gameStarted = true;
      // window.dispatchEvent(startEvent);
    } else {
      gameStarted = false;
      // window.dispatchEvent(endEvent);
    }

    if (flipStart != 0) {
      if (flipPos > 0.8) {
        flipStart = 0;
        flipPos = 0;
      }
      return;
    }
    dami.classList.add("flipping");
    const flipFrame = (ms) => {
      if (flipStart == 0) {
        flipStart = ms;
      } 
      flipPos = smooth((ms - flipStart) / FLIP_TIME);
      let deg = flipPos * 360;
      dami.style.transform = `rotate3d(1, 0, 0, ${deg}deg)`;
    if (ms - flipStart > FLIP_TIME) {
        flipStart = 0;
        flipPos = 0;
        dami.style.transform = "";
      } else {
        requestAnimationFrame(flipFrame);
      }
    }
    requestAnimationFrame(flipFrame)
  }
  // set dami to front
  onMount(() => {
    requestAnimationFrame((_) => {
      dami.classList.remove("back")
      dami.classList.add("front")
    });
  });
</script>

<div class="dani-wrapper">
  <img src="dani.png" bind:this={dami} on:click={onFlip} on:keydown={onKey} tabindex="0">
</div>

<style>
div.dani-wrapper {
  margin-bottom: -8px;
  perspective: 500px;
  perspective-origin: center center;
}

div.dani-wrapper img {
  object-fit: contain;
  margin-bottom: -8px;
  margin-left: auto;
  width: 100%;
  max-width: 600px;
}
</style>
