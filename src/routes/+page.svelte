<script>
  import ProjectCard from "./ProjectCard.svelte";
</script>

<svelte:head>
	<meta name="description" content="Portfolio Dani Verschoor, webontwikkelaar" />
	<link rel="stylesheet" href="aspekta/font-face.css" />
</svelte:head>

<main>
<div class="card">
  <h1>Dani Verschoor</h1>
  <h2>Webontwikkelaar</h2>
</div>
<ProjectCard title="Manor Madness" image="background.png">
  <p>
  <strong>Role</strong>: Game Designer
  <br>
  <strong>Technologies</strong>: Unity 3D
  <br>
  <em>Manor Madness is a 3D, third-person sandbox game. In this game, you play a young ghost, Ghustav, who wants to learn how to become a real poltergeist.</em></p>
  <a href="">GitHub Repository</a>
  <br>
  <a href="">Steam Page</a>
  <br>
  <a href="">Website</a>
</ProjectCard>
<ProjectCard title="Charon Login" image="background.png">
</ProjectCard>
<ProjectCard title="Claire" image="background.png">
</ProjectCard>
<ProjectCard title="MissMatch" image="background.png">
</ProjectCard>

<a class="link card" href="#">GitHub</a>
<a class="link card" href="#">LinkedIn</a>
<a class="link card" href="#">Curriculum Vitae</a>
</main>

<style>
:global(body) {
  background-color: #bbb;
  margin: 0;
}

main :global(*) {
  box-sizing: border-box;
}

main h1 {
  margin: 0;
  text-align: center;
}

main {
  margin: 14px;
  font-family: "Aspekta", serif;
}

:global(.card) {
  width: 100%;
  margin: 12px 0;
  background-color: #fafafa;
  box-shadow: 4px 4px 0 0 #000;
  color: #222;
}

a.link {
  padding: 2px;
  display: block;
  font-size: 24px;
  font-weight: 700;
  text-decoration: none;
  text-align: center;
}
</style>
