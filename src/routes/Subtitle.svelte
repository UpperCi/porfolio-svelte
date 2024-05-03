<div>
  <div class="line"></div>
  <h2><slot /></h2>
  <div class="line"></div>
</div>

<style>
div {
  width: 100%;
  height: 2em;
  display: flex;
  align-items: center;
}

h2 {
  width: fit-content;
  margin: 0 -8px;
  height: 1.5em;
  white-space: nowrap;
}

.line {
  height: 1px;
  border-top: 2px solid #EAD823;
  margin: 0 1em;
}
</style>
