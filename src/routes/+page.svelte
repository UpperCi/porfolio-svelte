<script>
  import ProjectCard from "./ProjectCard.svelte";
  import Subtitle from "./Subtitle.svelte";
  import IconLink from "./IconLink.svelte";
</script>

<svelte:head>
	<meta name="description" content="Portfolio Dani Verschoor, webontwikkelaar" />
	<link rel="stylesheet" href="aspekta/font-face.css" />
</svelte:head>

<main>
<h1>Dani Verschoor</h1>
<h3>Creative Developer</h3>
<p class="tagline">Building stable and accessible software.</p>
<div class="project-wrapper">
<Subtitle>Web Development</Subtitle>
<div class="section">
  <ProjectCard image="claire.png" alt="Wooden case containing electronics. Text saying Claire with air highlighted.">
    <h2>Claire</h2>
    <IconLink href="https://github.com/unlimited-hr/Claire-api/" src="icons/Github.svg">Github</IconLink>
    <IconLink href="https://cmgt.hr.nl/projecten/claire/" src="icons/Website.svg">Web</IconLink>
    <p slot="description">
    <strong>Role</strong>: Back-end Developer
    <br>
    <strong>Technologies</strong>: NodeJS
    <br>
    <br>
    <em>Claire is an air quality sensor that gives personalized advice based on your indoor climate. I developed it's API, which accomodates both an IoT device and a mobile app.</em>
    </p>
  </ProjectCard>
  <ProjectCard image="charon_login.png" alt="Login prompt asking for a code and a password in Dutch. Text saying Charon Login." layout="invert">
    <h2>Charon Login</h2>
    <IconLink href="https://github.com/weareyipyip/charon_login/" src="icons/Github.svg">Github</IconLink>
    <p slot="description">
    <strong>Role</strong>: Back-end Developer
    <br>
    <strong>Technologies</strong>: Elixir
    <br>
    <br>
    <em>CharonLogin is an Elixir library for modular authentication procedures. Developers can define multi-factor authentication flows with a couple lines of configuration. Developed at YipYip.</em>
    </p>
  </ProjectCard>
  <ProjectCard image="missmatch.png" alt="Color wheel with a face and a bow. Text saying MissMatch.">
    <h2>MissMatch</h2>
    <IconLink href="https://github.com/MattPermentier/MisMatch/" src="icons/Github.svg">Github</IconLink>
    <IconLink href="https://cmgt.hr.nl/projecten/missmatch/" src="icons/Website.svg">Apericot Studio</IconLink>
    <p slot="description">
    <strong>Role</strong>: Developer
    <br>
    <strong>Technologies</strong>: PHP, WordPress
    <br>
    <br>
    <em>MissMatch is WordPress plug-in to make your site more accessible. It looks at the colors used on your site and transforms them to increase the contrast, taking into account the WCAG.</em>
    </p>
  </ProjectCard>
</div>

<Subtitle>Game Development</Subtitle>
<div class="section">
  <ProjectCard layout="invert" image="manor_madness.jpg" alt="Ghost zapping through a hallway and scaring people. Text saying Manor Madness.">
    <h2>Manor Madness</h2>
    <IconLink href="https://github.com/ApericotStudio/Poltergeist/" src="icons/Github.svg">Github</IconLink>
    <IconLink href="https://store.steampowered.com/app/2719710/Manor_Madness/" src="icons/Steam.svg">Steam</IconLink>
    <IconLink href="https://project.cmi.hr.nl/2023_2024/game_apricot/" src="icons/Website.svg">Apericot Studio</IconLink>
    <p slot="description">
    <strong>Role</strong>: Game Designer
    <br>
    <strong>Technologies</strong>: Unity 3D
    <br>
    <br>
    <em>Manor Madness is a 3D, third-person sandbox game. It focuses on fun derived from physical comedy and strategy. As a designer, I conducted weekly playtests and helped shape the gameplay mechanics.</em>
    </p>
  </ProjectCard>
  <ProjectCard image="gamejams.png" alt="Four game titles: Unplugged, Pursuit, Earth Apple and Wager.">
    <h2>Game Jams</h2>
    <IconLink href="https://cmgt.hr.nl/projecten/missmatch/" src="icons/Website.svg">Itch.io</IconLink>
    <p slot="description">
    <strong>Role</strong>: Developer, Designer, Artist
    <br>
    <strong>Technologies</strong>: Godot, PICO-8
    <br>
    <br>
    <em>Over the years I have participated in multiple game jams, forcing me to design and develop games in a short time-span, typically a weekend.</em>
    </p>
  </ProjectCard>
</div>
</div>

<Subtitle>About Dani</Subtitle>
<IconLink href="https://cmgt.hr.nl/projecten/claire/" src="icons/Github.svg">GitHub</IconLink>
<IconLink href="https://cmgt.hr.nl/projecten/claire/" src="icons/LinkedIn.svg">LinkedIn</IconLink>
<IconLink href="https://cmgt.hr.nl/projecten/claire/" src="icons/Website.svg">Curriculum Vitae</IconLink>
<div class="person-wrapper">
  <img src="dani.png">
</div>
</main>

<style>
:global(body) {
  background-color: #000000;
  margin: 0;
}

main :global(*) {
  box-sizing: border-box;
}

main h1, main h3{
  margin: 0;
  text-align: center;
}

main h3 {
  font-size: 20px;
  margin-top: -4px;
}

main p {
  color: white;
}

p.tagline {
  width: 100%;
  text-align: center;
}

main {
  padding: 10px;
  font-family: "Aspekta", serif;
  overflow: hidden;
  margin: 0 auto;
  max-width: 400px;
}

div.person-wrapper {
  margin-bottom: -8px;
}

div.person-wrapper img {
  object-fit: scale-down;
  margin-bottom: -8px;
  width: 100%;
}

div.project-wrapper {
  width: fit-content;
  margin: 0 auto;
}

div.section {
  max-width: 820px;
}

:global(.card) {
  width: 100%;
  margin: 12px 0;
  background-color: #021C34;
  color: #222;
}

:global(h1, h2, h3) {
  color: #EAD823;
}
</style>
