<script>
	import Header from '../header.svelte';
	import Projects from '../projects.svelte';

	let otherProjects = [
		{
			id: 'vr',
			priority: false,
			tag: 'research',
			role: 'Researcher, Unity Developer',
			name: 'Spatial Cognition in VR',
			slug: 'vr.jpg',
			description: 'Studying the effects of teleporting in virtual reality using triangle completion tasks in Unity enviroments.',
			url: 'https://dr.lib.iastate.edu/entities/publication/b2750a5d-70af-4fd3-81ce-69c2f338effd'
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
			id: 'red_survivor',
			priority: false,
			tag: 'games',
			name: 'Red Survivor',
			role: 'UI Artist',
			slug: 'rs2.png',
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
		}
		// {
		// 	id: 'subq',
		// 	priority: false,
		// 	tag: 'other',
		// 	name: 'sub-Q Magazine',
		// 	role: 'Editor',
		// 	slug: 'subq.jpg',
		// 	description: 'Online literary magazine for interactive fiction fantasy, science fiction, and horror. Reviewed submissions, edited pieces, and interviewed authors.',
		// 	url: 'https://sub-q.com/'
		// },
		// {
		// 	id: 'oet',
		// 	priority: false,
		// 	tag: 'other',
		// 	name: 'On Equal Terms',
		// 	role: 'Research Assistant',
		// 	slug: 'equalterms.jpg',
		// 	description: "Developed interactive digital exhibit about the experiences of tradeswomen with the Women's Studies Research Center at Brandeis University.",
		// 	url: 'https://onequalter.ms/'
		// }
		// {
		// 	id: 'film',
		// 	priority: false,
		// 	tag: 'other',
		// 	name: 'Films and animation',
		// 	role: 'Cinematographer, animator, editor',
		// 	slug: 'animation.gif',
		// 	description: 'Created short films and animations as part of the CET study abroad program in Prague and the Getz Media Lab at Brandeis University.',
		// 	url: 'https://vimeo.com/showcase/5756343'
		// }
	];
</script>

<Header />
<section class="all-projects-page">
	<Projects />

	<section class="other-projects">
		<!-- <h1 class="h1">Other Games</h1> -->
		<div class="grid grid-cols-1 md:grid-cols-2 xl:grid-cols-4 gap-8">
			{#each otherProjects as project}
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
								<a href={project.url} type="button" class="btn variant-filled cardbutton"><span>Check it out</span><span><i class="fa-solid fa-circle-chevron-right"></i></span></a>
							</div>
						</div>
					</footer>
				</div>
			{/each}
		</div>
	</section>
</section>
