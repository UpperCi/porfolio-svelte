<script>
  import { onMount } from 'svelte';
  import BezierEasing from 'bezier-easing';
  export let image;
  export let alt;
  export let layout = "";
  let card;
  let flipStart = 0;
  const FLIP_TIME = 500;
  const smooth = BezierEasing(0, 0, 0.2, 1)

  const onKey = (e) => {
    if (e.key == "Enter") {
      onFlip();
    }
  }

  const onFlip = () => {
    if (flipStart != 0) return;
    const flipFrame = (back = false) => (ms) => {
      if (flipStart == 0) {
        flipStart = ms;
      } 
      const diff = smooth((ms - flipStart) / FLIP_TIME);
      const deg = diff * 180;
      const flip_y = back ? -1 : 1;
      if (!back && deg > 90) {
        back = true;
        card.classList.toggle("front")
        card.classList.toggle("back")
      }
      card.style.transform = `rotate3d(0, 1, 0, ${deg}deg) scaleX(${flip_y})`;
      // card.style.transform = `rotate3d(1, 0, 0, ${deg}deg) scaleY(${flip_y})`;
    if (ms - flipStart > FLIP_TIME) {
        flipStart = 0;
        card.style.transform = "";
      } else {
        requestAnimationFrame(flipFrame(back));
      }
    }
    requestAnimationFrame(flipFrame(false))
  }
  // set card to front
  onMount(async () => {
    card.classList.remove("back")
    card.classList.add("front")
  });
</script>

<div class="card-container">
  <div bind:this={card} on:click={onFlip} on:keydown={onKey} class="card back" tabindex="0">
    <div class={`card-back ${layout == "invert" ? "invert" : ""}`}>
      <div class="summary">
        <slot />
      </div>
      <div class="description">
        <slot name="description">
        </slot>
      </div>
    </div>
    <div class="card-front">
      <img src={image} alt={alt}>
    </div>
  </div>
</div>

<style>
div.card {
  overflow: hidden;
  font-size: 12px;
  cursor: pointer;
  max-width: 400px;
  width: 100%;
  min-height: 200px;
  height: 100%;
  border-radius: 2px;
}

img {
  height: 100%;
  width: 100%;
  object-fit: cover;
  margin: 0;
  border-radius: 2px;
}

div.card-back {
  height: 100%;
  margin: 18px 0;
  display: flex;
}

div.card-back.invert {
  flex-direction: row-reverse;
}

div.summary {
  width: 40%;
}

div.card-back .description {
  width: 60%;
  margin-left: 8px;
  line-height: 1.25em;
}

div.card-back.invert .description {
  margin-left: 0;
  margin-right: 8px;
}

:global(.card-back .description p) {
  color: #2C2541;
  background-color: #BCB18A;
  padding: 8px;
  border-radius: 4px 0 0 4px;
  margin: 0;
  font-size: 14px !important;
}

:global(.card-back.invert .description p) {
  border-radius: 0 1em 1em 0;
}

div.card-front {
  max-width: 400px;
  width: 100%;
  height: 100%;
  position: absolute;
  bottom: 0;
  top: 0;
}

div.card-container {
  perspective: 600px;
  perspective-origin: center center;
  width: fit-content;
}

div.card.front div.card-back {
  opacity: 0%;
}

div.card.back div.card-front {
  display: none;
}

:global(.card-back h2) {
  color: #747147;
  font-size: 24px;
  margin: 0;
  width: 100%;
  font-weight: 700;
  padding-left: 12px;
  border-left: 4px solid #747147;
  line-height: 1.25;
  margin-bottom: 1rem;
}

:global(.card-back.invert h2) {
  border-right: 4px solid #787445;
  border-left: none;
}
</style>
