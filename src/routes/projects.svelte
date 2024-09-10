<script lang="ts">
	let projects = [
		// {
		// 	id: 'aai',
		// 	priority: true,
		// 	tag: 'research',
		// 	name: 'Applied AI Games + Tooling',
		// 	role: 'Senior Data Scientist',
		// 	slug: 'aai.jpg',
		// 	description: "Working on tools for games and creatives on Zynga's Applied AI Team",
		// 	url: '',
		// 	github_url: 'https://github.com/devibri/FatalFrequenciesFrontend',
		// 	demo_url: 'https://devibri.github.io/FatalFrequenciesFrontend'
		// },
		{
			id: 'ttrpg',
			priority: true,
			tag: 'research',
			name: 'TTRPG AI Assistant',
			role: 'Lead Researcher, Developer',
			slug: 'ttrpg2.png',
			description: 'A co-creative AI assistant for game masters of tabletop roleplaying games.',
			url: 'https://devibri.github.io/CompExamPortfolio/ttrpg.html',
			github_url: 'https://github.com/devibri/FatalFrequenciesFrontend',
			demo_url: 'https://devibri.github.io/FatalFrequenciesFrontend'
		},
		{
			id: 'warmer',
			priority: true,
			tag: 'games',
			name: 'Warmer',
			role: 'Unity Developer',
			slug: 'warmer.png',
			description: 'An NSF-funded game about climate change and human impacts on the environment using real environmental models.',
			url: 'https://github.com/devibri/UCSCClimateGame',
			demo_url: 'https://devibri.github.io/ClimateGamePlayable/'
		},
		// {
		// 	id: 'vr',
		// 	priority: false,
		// 	tag: 'research',
		// 	role: 'Researcher, Unity Developer',
		// 	name: 'Spatial Cognition in VR',
		// 	slug: 'vr.jpg',
		// 	description: 'Studying the effects of teleporting in virtual reality using triangle completion tasks in Unity enviroments.',
		// 	url: 'https://dr.lib.iastate.edu/entities/publication/b2750a5d-70af-4fd3-81ce-69c2f338effd'
		// },
		{
			id: 'escaperoom',
			priority: false,
			tag: 'research',
			role: 'Researcher, Mentor',
			name: 'VR / Physical Escape Room',
			slug: 'escape.png',
			description: "An escape room made in Unity with asymmetrical puzzle-solving in physical and virtual reality spaces. Made at UCSC's Science Internship Program.",
			url: 'https://devibri.github.io/CompExamPortfolio/escaperoom.html',
			demo_url: 'https://github.com/devibri/SIP-Unity-Escape-Room'
		},
		{
			id: 'terasology',
			priority: false,
			tag: 'games',
			name: 'Terasology: Light and Shadow',
			role: 'Java Developer',
			slug: 'terasology.jpg',
			description: 'A capture-the-flag game mode made for open-source voxel game Terasology, made as part of Google Summer of Code.',
			url: 'https://dacharya64.postach.io/post/gsoc-final-project-wrapup'
		},
		{
			id: 'fusion',
			priority: true,
			tag: 'games',
			name: 'Fusion Galaxy',
			role: 'Lead Artist',
			slug: 'cl.jpg',
			description: 'A mobile game about collecting and crafting elements together to discover the universe, made with the Massachusetts Digital Games Institute.',
			url: 'https://apps.apple.com/us/app/fusion-galaxy/id999077925#?platform=ipad',
			demo_url: 'https://apps.apple.com/us/app/fusion-galaxy/id999077925?ls=1'
		},
		{
			id: 'red_survivor',
			priority: false,
			tag: 'games',
			name: 'Red Survivor',
			role: 'UI Artist',
			slug: 'rs2.png',
			description: 'A strategy game where the player fights to survive against killer robots in a war-torn Russia. Made with a team at Mustachio Games. Shown at Boston Festival of Indie Games, 2014.',
			url: 'https://mustachiogames.itch.io/red-survivor'
		}
		// {
		// 	id: 'if',
		// 	priority: false,
		// 	tag: 'games',
		// 	name: 'The Abyss and The Ark',
		// 	role: 'Writer',
		// 	slug: 'abyss.jpg',
		// 	description: 'Authored and co-authored several interactive fiction games, including The Abyss--a surreal exploration of the mind--and The Ark--a puzzle game set aboard a derelict spaceship.',
		// 	url: 'https://textadventures.co.uk/games/view/ob1-nceir0a6dpocknuxyw/the-abyss'
		// }
	];
</script>

<section class="projects">
	<h1 class="h1">Projects</h1>
	<section class="other-projects">
		<!-- <h1 class="h1">Other Games</h1> -->
		<div class="grid grid-cols-1 md:grid-cols-2 xl:grid-cols-3 gap-8">
			{#each projects as project}
				<!-- {#if project.priority == true} -->
				<div class="card card-hover flex flex-col">
					<img src="/img/{project.slug}" class="rounded-lg w-full h-60 object-cover" alt="Thumbnail for project {project.name}" />
					<section class="p-6">
						<h3 class="h3">{project.name}</h3>
						<h4 class="h4"><strong>{project.role}</strong></h4>
						<p>{project.description}</p>
					</section>
					<footer class="card-footer mt-auto">
						<div class="cardbuttoncontainer">
							<div>
								{#if project.url != ''}
									<a href={project.url} type="button" class="btn variant-filled cardbutton"><span>Check it out</span><span><i class="fa-solid fa-circle-chevron-right"></i></span></a>
								{/if}
							</div>
						</div>
					</footer>
				</div>
				<!-- {/if} -->
			{/each}
		</div>
		<!-- <h1 class="h1">Other Projects</h1>
		<div class="grid grid-cols-1 gap-4">
			{#each projects as project}
				{#if project.priority == false}
					
					<div class="grid grid-cols-4 gap-4">
						<div class="col-span-1"><img src="/img/{project.slug}" class="rounded-lg w-full h-60 object-cover" alt="Thumbnail for project {project.name}" /></div>
						<div class="col-span-3 description">
							<h3 class="h3">{project.name}</h3>
							<h4 class="h4"><strong>{project.role}</strong></h4>
							<p>{project.description}</p>
							{#if project.url != ''}
								<a href={project.url} type="button" class="btn variant-filled cardbutton"><span>Check it out</span><span><i class="fa-solid fa-circle-chevron-right"></i></span></a>
							{/if}
						</div>
					</div>
					<div class="list-dl">
						<div class="article">
							<span class="flex-auto">
								<span></span>
								<span><section class="p-6"></section></span>
							</span>
							<span
								><footer class="card-footer mt-auto">
									<div class="cardbuttoncontainer">
										<div></div>
									</div>
								</footer></span>
						</div>
					</div>
				{/if}
			{/each}
		</div> -->
	</section>
</section>
