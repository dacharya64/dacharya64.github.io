<script>
	let projects = [
		{
			id: 'ttrpg',
			priority: true,
			tag: 'research',
			name: 'Tabletop Roleplaying Game AI Assistant',
			role: 'Lead Researcher, Developer',
			slug: 'ttrpg.png',
			description: 'A computational support tool for game masters of tabletop roleplaying games.',
			url: 'https://www.devi-a.com/CompExamPortfolio/ttrpg.html'
		},
		{
			id: 'warmer',
			priority: true,
			tag: 'games',
			name: 'Warmer',
			role: 'Unity Developer',
			slug: 'warmer.png',
			description: 'An NSF-funded game about climate change and human impacts on the environment using real environmental models.',
			url: 'https://github.com/dacharya64/UCSCClimateGame'
		},
		{
			id: 'vr',
			priority: true,
			tag: 'research',
			role: 'Researcher, Unity Developer',
			name: 'Spatial Cognition in VR',
			slug: 'vr.jpg',
			description: 'Studying the effects of teleporting in virtual reality using triangle completion tasks in Unity enviroments.',
			url: 'https://dr.lib.iastate.edu/entities/publication/b2750a5d-70af-4fd3-81ce-69c2f338effd'
		},
		{
			id: 'escape_room',
			priority: false,
			tag: 'research',
			role: 'Researcher, Mentor',
			name: 'VR / Physical Escape Room',
			slug: 'escape.png',
			description: "An escape room with asymmetrical puzzle-solving in physical and virtual reality spaces. Made for UCSC's Science Internship Program.",
			url: 'https://www.devi-a.com/CompExamPortfolio/escaperoom.html'
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
			url: 'https://apps.apple.com/us/app/fusion-galaxy/id999077925#?platform=ipad'
		},
		{
			id: 'red_survivor',
			priority: false,
			tag: 'games',
			name: 'Red Survivor',
			role: 'UI Artist',
			slug: 'rs.jpg',
			description: 'A strategy game where the player fights to survive against killer robots in a war-torn Russia. Made with a team at Mustachio Games. Shown at Boston Festival of Indie Games, 2014.',
			url: 'https://mustachiogames.itch.io/red-survivor'
		},
		{
			id: 'if',
			priority: false,
			tag: 'games',
			name: 'The Abyss and The Ark',
			role: 'Writer',
			slug: 'abyss.jpg',
			description: 'Authored and co-authored several interactive fiction games, including The Abyss--a surreal exploration of the mind--and The Ark--a puzzle game set aboard a derelict spaceship.',
			url: 'https://textadventures.co.uk/games/view/ob1-nceir0a6dpocknuxyw/the-abyss'
		},
		{
			id: 'subq',
			priority: false,
			tag: 'other',
			name: 'sub-Q Magazine',
			role: 'Editor',
			slug: 'subq.jpg',
			description: 'Online literary magazine for interactive fiction fantasy, science fiction, and horror. Reviewed submissions, edited pieces, and interviewed authors.',
			url: 'https://sub-q.com/'
		},
		{
			id: 'oet',
			priority: false,
			tag: 'other',
			name: 'On Equal Terms',
			role: 'Research Assistant',
			slug: 'equalterms.jpg',
			description: "Developed interactive digital exhibit about the experiences of tradeswomen with the Women's Studies Research Center at Brandeis University.",
			url: 'https://onequalter.ms/'
		},
		{
			id: 'film',
			priority: false,
			tag: 'other',
			name: 'Films and animation',
			role: 'Cinematographer, animator, editor',
			slug: 'animation.gif',
			description: 'Created short films and animations as part of the CET study abroad program in Prague and the Getz Media Lab at Brandeis University.',
			url: 'https://vimeo.com/showcase/5756343'
		}
	];
</script>

<section class="projects">
	<div class="grid grid-cols-3 gap-8">
		{#each projects as project}
			{#if project.priority == true}
				<div class="card p-4 card-hover">
					<h2>{project.name}</h2>
					<p>{project.description}</p>
				</div>
			{/if}
		{/each}
	</div>
</section>
