<script>
  import ProjectCard from "./ProjectCard.svelte";
  import Dami from "./Dami.svelte";
  import Subtitle from "./Subtitle.svelte";
  import IconLink from "./IconLink.svelte";
  import SiteObject from "./SiteObject.svelte";
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
  <h3>Creative Developer</h3>
  <p class="tagline">Building stable and accessible software.</p>
</SiteObject>
<div class="project-wrapper">
<SiteObject>
  <Subtitle>Web Development</Subtitle>
</SiteObject>
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
    <IconLink href="https://cmgt.hr.nl/projecten/missmatch/" src="icons/Website.svg">Showcase Site</IconLink>
    <p slot="description">
    <strong>Role</strong>: Developer
    <br>
    <strong>Technologies</strong>: PHP, WordPress
    <br>
    <br>
    <em>MissMatch is WordPress plug-in to make your site more accessible. It looks at the colors used on your site and transforms them to increase the contrast, taking into account the WCAG.</em>
    </p>
  </ProjectCard>
  <ProjectCard image="catch.png" alt="3D rendered face with mouth open reaching for an apple." layout="invert">
    <h2>Catch</h2>
    <IconLink href="https://github.com/UpperCi/catch/" src="icons/Github.svg">Github</IconLink>
    <IconLink href="https://upperci.github.io/catch/" src="icons/Website.svg">Live Demo</IconLink>
    <p slot="description">
    <strong>Role</strong>: Solo Project
    <br>
    <strong>Technologies</strong>: ML5.js, HTML Canvas
    <br>
    <br>
    <em>A webgame to try out ML5.js. Using your webcam, it tracks facial movement and uses this as the controls.</em>
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
    <strong>Role</strong>: Game Designer
    <br>
    <strong>Technologies</strong>: Unity 3D
    <br>
    <br>
    <em>Manor Madness is a 3D, third-person sandbox game. It focuses on fun derived from physical comedy. As a designer, I conducted weekly playtests and helped shape the gameplay mechanics.</em>
    </p>
  </ProjectCard>
  <ProjectCard image="gamejams.png" alt="Four game titles: Unplugged, Pursuit, Earth Apple and Wager." layout="invert">
    <h2>Game Jams</h2>
    <IconLink href="https://upperc.itch.io/" src="icons/Website.svg">Itch.io</IconLink>
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

<SiteObject>
  <Subtitle>About Dani</Subtitle>
<IconLink href="https://cmgt.hr.nl/projecten/claire/" src="icons/Github.svg" dark={true}>GitHub</IconLink>
<IconLink href="https://cmgt.hr.nl/projecten/claire/" src="icons/LinkedIn.svg" dark={true}>LinkedIn</IconLink>
<IconLink href="https://cmgt.hr.nl/projecten/claire/" src="icons/Website.svg" dark={true}>Curriculum Vitae</IconLink>
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
