<script>
  import ProjectCard from "../ProjectCard.svelte";
  import Dami from "../Dami.svelte";
  import Subtitle from "../Subtitle.svelte";
  import IconLink from "../IconLink.svelte";
  import SiteObject from "../SiteObject.svelte";
</script>

<svelte:head>
	<meta name="description" content="Portfolio Dani Verschoor, webontwikkelaar" />
  <title>Dani Verschoor, Webontwikkelaar</title>
	<link rel="stylesheet" href="ptsans_caption/font-face.css" />
	<link rel="stylesheet" href="ptsans/font-face.css" />
</svelte:head>

<main>
<SiteObject>
  <h1>Dani Verschoor</h1>
  <h3>Creatief Ontwikkelaar</h3>
  <p class="tagline">Stabiele en toegankelijke software aan het bouwen.</p>
</SiteObject>
<div class="project-wrapper">
<SiteObject>
  <Subtitle>Web Ontwikkeling</Subtitle>
</SiteObject>
<div class="section">
  <ProjectCard image="claire.png" alt="Houten omhulsel met electronica. Tekst erop: Claire. Het woord air is gemarkeerd.">
    <h2>Claire</h2>
    <IconLink href="https://github.com/unlimited-hr/Claire-api/" src="icons/Github.svg">Github</IconLink>
    <IconLink href="https://cmgt.hr.nl/projecten/claire/" src="icons/Website.svg">Web</IconLink>
    <p slot="description">
    <strong>Rol</strong>: Back-end Ontwikkelaar
    <br>
    <strong>Technologieën</strong>: NodeJS
    <br>
    <br>
    <em>Claire is een sensor die op basis van de luchtkwaliteit binnen jouw huis gepersonaliseerd advies geeft. I heb de API gebouwd, die met zowel een IoT apparaat als een mobiele app communiceert.</em>
    </p>
  </ProjectCard>
  <ProjectCard image="charon_login.png" alt="Login prompt asking for a code and a password in Dutch. Text saying Charon Login." layout="invert">
    <h2>Charon Login</h2>
    <IconLink href="https://github.com/weareyipyip/charon_login/" src="icons/Github.svg">Github</IconLink>
    <p slot="description">
    <strong>Rol</strong>: Back-end Ontwikkelaar
    <br>
    <strong>Technologieën</strong>: Elixir
    <br>
    <br>
    <em>CharonLogin is een Elixir library om modulair authenticatie op te zetten. Ontwikkelaars kunnen in een paar lijnen aan configuratie multi-factor authenticatie opzetten. Ik heb dit bij YipYip ontwikkeld.</em>
    </p>
  </ProjectCard>
  <ProjectCard image="missmatch.png" alt="Color wheel with a face and a bow. Text saying MissMatch.">
    <h2>MissMatch</h2>
    <IconLink href="https://github.com/MattPermentier/MisMatch/" src="icons/Github.svg">Github</IconLink>
    <IconLink href="https://cmgt.hr.nl/projecten/missmatch/" src="icons/Website.svg">Showcase Site</IconLink>
    <p slot="description">
    <strong>Rol</strong>: Ontwikkelaar
    <br>
    <strong>Technologieën</strong>: PHP, WordPress
    <br>
    <br>
    <em>missMatch is een WordPress plugin om sites toegankelijker te maken. Het kijkt naar de kleuren op een site en verandert ze om het contrast te verhogen in lijn met de WCAG.</em>
    </p>
  </ProjectCard>
  <ProjectCard image="catch.png" alt="3D rendered face with mouth open reaching for an apple." layout="invert">
    <h2>Catch</h2>
    <IconLink href="https://github.com/UpperCi/catch/" src="icons/Github.svg">Github</IconLink>
    <IconLink href="https://upperci.github.io/catch/" src="icons/Website.svg">Live Demo</IconLink>
    <p slot="description">
    <strong>Rol</strong>: Solo Project
    <br>
    <strong>Technologieën</strong>: ML5.js, HTML Canvas
    <br>
    <br>
    <em>Een webgame om ML5.js uit te proberen. Het gebruikt je webcam om de bewegingen die je gezicht maakt bij te houden, dit gebruik je om het spel te besturen.</em>
    </p>
  </ProjectCard>
</div>

<SiteObject>
<Subtitle>Game Dev & Design</Subtitle>
</SiteObject>
<div class="section">
  <ProjectCard image="manor_madness.jpg" alt="Ghost zapping through a hallway and scaring people. Text saying Manor Madness.">
    <h2>Manor Madness</h2>
    <IconLink href="https://github.com/ApericotStudio/Poltergeist/" src="icons/Github.svg">Github</IconLink>
    <IconLink href="https://store.steampowered.com/app/2719710/Manor_Madness/" src="icons/Steam.svg">Steam</IconLink>
    <IconLink href="https://project.cmi.hr.nl/2023_2024/game_apricot/" src="icons/Website.svg">Apericot Studio</IconLink>
    <p slot="description">
    <strong>Rol</strong>: Game Designer
    <br>
    <strong>Technologieën</strong>: Unity 3D
    <br>
    <br>
    <em>Manor Madness is een 3D, third-person sanbox spel. Het richt zich op grappige situaties. Als designer heb ik wekelijks playtests afgenomen, en geholpen met het vormen van de gameplay.</em>
    </p>
  </ProjectCard>
  <ProjectCard image="gamejams.png" alt="Four game titles: Unplugged, Pursuit, Earth Apple and Wager." layout="invert">
    <h2>Game Jams</h2>
    <IconLink href="https://upperc.itch.io/" src="icons/Website.svg">Itch.io</IconLink>
    <p slot="description">
    <strong>Rol</strong>: Ontwikkelaar, Designer, Artiest
    <br>
    <strong>Technologieën</strong>: Godot, PICO-8
    <br>
    <br>
    <em>Over de loop van jaren heb ik aan meerdere game jams meegedaan, hierbij moet ik in korte tijd een game maken, meestal een weekend.</em>
    </p>
  </ProjectCard>
</div>
</div>

<SiteObject>
  <Subtitle>Over Dani</Subtitle>
<IconLink href="https://cmgt.hr.nl/projecten/claire/" src="icons/Github.svg" dark={true}>GitHub</IconLink>
<IconLink href="https://cmgt.hr.nl/projecten/claire/" src="icons/LinkedIn.svg" dark={true}>LinkedIn</IconLink>
<IconLink href="/CV_NL.pdf" src="icons/Website.svg" dark={true}>Curriculum Vitae</IconLink>
</SiteObject>
<Dami />
</main>

<style>
:global(body) {
  background-color: #827249;
  margin: 0;
}

:global(h1, h2, h3, h4, h5, h6) {
  font-family: "PTSansCaption", sans-serif;
}

main :global(*) {
  box-sizing: border-box;
}

main h1, main h3{
  margin: 0;
  text-align: center;
  width: 100%;
  color: #EEEDE2;
}

main h1 {
  font-size: 36px;
}

main h3 {
  font-size: 24px;
  margin-top: -4px;
}

main p {
  color: #EEEDE2;
  font-size: 16px;
  line-height: 1.25em;
}

main .card p {
  color: #261D39;
}

p.tagline {
  width: 100%;
  text-align: center;
}

main {
  padding: 10px;
  font-family: "PTSans";
  overflow: hidden;
  margin: 0 auto;
  max-width: 816px;
}

div.project-wrapper {
  width: fit-content;
  margin: 0 auto;
}

div.section {
  max-width: 400px;
  display: flex;
  flex-wrap: wrap;
  flex-direction: row;
  gap: 1rem;
}

:global(.card) {
  width: 100%;
  margin: 0;
  background-color: #DDDBC4;
  color: #222;
  box-shadow: 0 8px 8px 0 #0007;
}

@media only screen and (min-width: 1000px) {
  div.section {
    max-width: 816px;
  }

  :global(.card) {
    margin: 0;
  }
}

:global(h1, h2, h3) {
  color: #EEEDE2;
}
</style>
