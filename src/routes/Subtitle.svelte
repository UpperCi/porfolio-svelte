<div class="subtitle">
  <div class="line before"></div>
  <h2><slot /></h2>
  <div class="line after"></div>
</div>

<style>
div {
  width: 100%;
  height: 2em;
  display: flex;
  align-items: center;
}

div.subtitle {
  margin: 20px 0;
}

h2 {
  width: fit-content;
  margin: 0 -8px;
  height: 1.5em;
  white-space: nowrap;
}

.line {
  height: 1px;
  border-top: 2px solid #EEEDE2;
  margin: 0;
}

.line.before {
  margin-right: 1em;
}

.line.after {
  margin-left: 1em;
}
</style>
