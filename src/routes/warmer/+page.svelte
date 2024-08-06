<script>
	import Header from '../header.svelte';
</script>

<Header />

<section class="projectpage">
	<a href="../" type="button" class="btn-icon variant-filled cardbutton"><i class="fa-solid fa-reply"></i></a>

	<div>
		<h1 class="h1">Warmer</h1>
		<h5 class="h5">An NSF-funded game about climate change.</h5>
		<p>
			From June - August 2021, I was a developer on <em>Warmer</em>, a game about climate change. Made in Unity and funded by the NSF,
			<em>Warmer</em> is a game made to help students learn about climate change and how different actions could impact the world's temperatures in different ways. The game provided several different minigames
			and choices for the player to help explore which actions affected global temperatures of their simulated planet, using real climate data to model changes in temperature and precipitation based on
			emissions.
		</p>
		<p>
			While much of the initial work was done by a team of undergraduate game developers, I was brought onto the project to help bring it into a place where it could be ready for testing with schools.
			This included development work in Unity to implement the following:
		</p>

		<ul class="list-disc list-inside">
			<li><span>Getting the minigames into a core loop for the game, where the player can interact with the different games and see the resulting changes in global temperature</span></li>
			<li>Polishing up and fixing any issues with existing minigames</li>
			<li>
				Hooking the game up to our <a class="anchor" href="https://github.com/dacharya64/UCSCClimateGame/tree/master/ClimatePrototypes/Assets/Scripts/Model">climate model</a> so that temperatures and precipitation
				could use accurate simulated data
			</li>
			<li>General polish for game feel, including adding animations, sound effects, new art, etc</li>
			<li>Adding screens at the end of the game describing what the results of the world (emissions, etc.) at the end of the game</li>
		</ul>

		<p>At the end of this period, the game was ready to be shared with classrooms for research studies.</p>

		<h2 class="h2">About the game</h2>
		<p>
			The game begins with the player picking a name for their planet, and then seeing the overworld of the game, displaying the different regions of the planet and stats about their world such as
			temperature, emissions, and popular support.
		</p>
		<figure>
			<img
				src="https://camo.githubusercontent.com/f950fb6212401725dc71057f3f90945aa9f455cd5bde51139de3aea739bcbc2c/68747470733a2f2f692e696d6775722e636f6d2f31665067326b722e706e67"
				alt="Overworld of game Warmer" />
		</figure>

		<p>
			There are four different minigames available to play, one in each region. The difficulty and contents of these games vary based on global temperature, emissions, and precipitation. The player's
			choices and performance in these minigames change the world's stats as well, resulting in a loop where the player can see the impacts of their actions on their planet.
		</p>
		<h3 class="h3">Pass Bills</h3>
		<p>
			One minigame allows the player to pass bills that influence the planet. The player is presented with several pairs of bills, and can see the resulting effects of each bill (although these are
			somewhat abstracted--such as a large increase in emissions, or a small decrease in popular support). They must choose one of each pair to enact. These bills directly impact the stats of the
			planet, and players must balance the importance of different factors such as emissions and popular support, as these will impact global temperature and the other minigames.
		</p>
		<figure>
			<img
				src="https://camo.githubusercontent.com/cc6d5e03ae678d762aaf3dbc5052f3c6ba9d4a1dd480e555372d674aa43b190d/68747470733a2f2f692e696d6775722e636f6d2f7a5638514874712e706e67"
				alt="The city minigame" />
		</figure>

		<h3 class="h3">Protest Emissions</h3>
		<p>
			Another minigame lets the player send people to different areas to help mitigate the effects of climate change. The number of people that the player gets to place is dependent on their current
			popular support. They have the option to place people in one of three locations:
		</p>
		<ul class="list-disc list-inside">
			<li><strong>The factory</strong> -- people placed here will protest, helping to reduce emissions and raise public opinion</li>
			<li><strong>The forest</strong> -- people placed here will help to mitigate deforestation of the area by planting trees, which will help to somewhat reduce emissions</li>
			<li><strong>The carbon sequestration plant</strong> -- people placed here will reduce emissions more, but this costs more money overall</li>
		</ul>
		<figure>
			<img
				src="https://camo.githubusercontent.com/cba8f28080cdec274c7c717da2cd387224cf31f991ee96deb0e0797bc1497ca0/68747470733a2f2f692e696d6775722e636f6d2f6f684c494344452e706e67"
				alt="The protest minigame" />
		</figure>
		<h3 class="h3">Fight Wildfires</h3>
		<p>
			The third minigame allows the player to react to the effects of climate change. As the world becomes hotter and drier, wildfires spread. This minigame allows the player to fly a helicopter,
			picking up water from reservoirs and using this water to put out fires in the area. The size of reservoirs and fires is dependent on global stats, making the game harder as the planet heats up.
		</p>
		<figure>
			<img
				src="https://camo.githubusercontent.com/999bed0c77f49d2145630fa9476bc91d18912ce0affccb745be612d6681e0ee0/68747470733a2f2f692e696d6775722e636f6d2f31646c7a5157382e706e67"
				alt="The wildfire minigame" />
		</figure>
		<h3 class="h3">Protect the Arctic</h3>
		<p>
			The last minigame allows the player to attempt to protect ice in the Arctic from being destroyed. The player controls a paddle and must deflect incoming longwave radiation that destroys the ice.
			This minigame also becomes more difficult as the planet warms, reflecting the change in polar clouds and cloud cover reflecting more longwave radiation.
		</p>
		<figure>
			<img
				src="https://camo.githubusercontent.com/d7598a2b117a324ad3c15a1b4016b93251c3916c0edf803911193f1cbf359ce6/68747470733a2f2f692e696d6775722e636f6d2f673654584b56712e706e67"
				alt="The arctic minigame" />
		</figure>
	</div>
	<section class="grid grid-cols-3 gap-8">
		<a type="button" class="btn btn-xl variant-filled" href="../"><span><i class="fa-solid fa-circle-chevron-left"></i></span><span>Back to home</span></a>
		<a type="button" class="btn btn-xl variant-filled-primary" href="https://github.com/dacharya64/UCSCClimateGame"><span><i class="fa-brands fa-github"></i></span><span>Project Github</span></a>
		<a type="button" class="btn btn-xl variant-filled-primary" href="https://www.devi-a.com/ClimateGamePlayable/"><span><i class="fa-solid fa-gamepad"></i></span><span>Play now!</span></a>
	</section>
</section>
