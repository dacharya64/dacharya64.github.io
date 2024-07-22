<script>
	import { Accordion, AccordionItem } from '@skeletonlabs/skeleton';

	let publications = [
		{
			id: 'shoelace',
			name: 'Shoelace: A Storytelling Assistant for GUMSHOE One-2-One',
			authors: 'Devi Acharya, Jack Kelly, William Tate, Maxwell Joslyn, Michael Mateas, Noah Wardrip-Fruin',
			venue: 'International Conference on the Foundations of Digital Games',
			year: '2023',
			award: 'Best Paper Award',
			url: 'https://www.devi-a.com/papers/Shoelace_FDG23.pdf',
			abstract:
				'In creative roleplaying games, game masters take on many roles, including keeping track of the game’s story, remembering past actions, and improvising new content based on player choices and desires. This dynamic storytelling can be quite difficult, particularly in real-time play, and this paper explores how digital tools might be able to assist GMs with elements of this process. In particular, we explore issues that game masters experience in running the GUMSHOE One-2-One system by analyzing posts from the online role playing game community, and discuss the design of a digital tool that helps to address common problems. The resulting tool, Shoelace, helps game masters keep track of story events with a graph-based game world visualization, while also providing creative suggestions using Prolog queries over a database of game information.'
		},
		{
			id: 'requirements_analysis',
			name: 'Requirements analysis and speculative design of support tools for TTRPG game masters',
			authors: 'Devi Acharya, Michael Mateas, and Noah Wardrip-Fruin',
			venue: 'Digital Games Research Association',
			year: '2022',
			url: 'https://www.devi-a.com/papers/Acharya_DiGRA2022.pdf',
			abstract:
				"In running tabletop roleplaying games (TTRPGs), game masters (GMs) are tasked with helping create and facilitate the building of a shared story between players based on player choices. In this paper, we look at how we can inform the design of computational tools for GMs through the use of qualitative interviews. We interview GMs about their process in preparing for and running a beginner TTRPG module, Lost Mine of Phandelver, and present to them a prototype of a computational tool built based on this module that has some of the features we believe would be useful in a GMing assistant, such as consolidating information for easier reference, serving as a brainstorming tool for GMs, and helping GMs keep track of what has happened in the game world. From these interviews, we collected insights into how the GMing process works within the context of a specific scenario and found which features GMs liked and what could be improved with our digital prototype. We also compare the results of these interviews to online advice for GMing the module. We use these insights in order to speculate about possible design directions for further development of a GM's computational assistant."
		},
		{
			id: 'thesis',
			name: 'Computational Support for Game Masters of Tabletop Roleplaying Games',
			authors: 'Devi Acharya',
			venue: "Master's Thesis, Computational Media, University of California - Santa Cruz",
			year: '2021',
			url: 'https://www.devi-a.com/papers/thesis.pdf',
			abstract:
				'In tabletop roleplaying games (TTRPGs), game masters (GMs) facilitate shared story creation using improvisational techniques that let them anticipate and respond to what players want to see in the world. In order to examine the process by which GMs co-create such player-driven narratives, we conduct interviews with GMs about their process preparing for and running TTRPG campaigns. We qualitatively code these interviews in order to synthesize a list of techniques GMs use to move the story forward even when players behave unexpectedly. We then perform a second round of interviews, looking at how GMs would run a specific scenario (Lost Mine of Phandelver) and using this as a common baseline for understanding GMing techniques. We also provide GMs with a limited prototype of a digital tool for GMs and use this in our interviews to evaluate what GMs might want to see in a computational assistant. We compare our interview findings to online advice for running Lost Mine in order to see if these techniques were shared across a wider sample of GMs. Based on these interviews and analysis, we provide some speculative directions for further designs of computational tools for GMs, such as creating better tools for information visualization and generative content.'
		},
		{
			id: 'story_improvisation',
			name: 'Story Improvisation in Tabletop Roleplaying Games: Towards a Computational Assistant for Game Masters',
			authors: 'Devi Acharya, Michael Mateas, and Noah Wardrip-Fruin',
			venue: 'Conference on Games',
			year: '2021',
			url: 'https://www.devi-a.com/papers/cog_2021.pdf',
			abstract:
				'In tabletop roleplaying games (TTRPGs), game masters (GMs) facilitate creating an improvisational shared story, responding in real time to the actions that players take and the things that they want to see in the world. In order to examine the process by which GMs co-create such player-driven narratives, we conduct interviews with GMs about their process preparing for and running TTRPG campaigns. We qualitatively code these interviews in order to synthesize a list of techniques GMs can use to move the story forward. We also compare these interviews to other sources of advice for GMing in sourcebooks and essays. Using the GMing techniques found through this analysis, we discuss insights into the GMing process and how this can be used to inform the design of a computational assistant for GMs.'
		},
		{
			id: 'interviews_towards',
			name: 'Interviews towards designing support tools for TTRPG game masters',
			authors: 'Devi Acharya, Michael Mateas, and Noah Wardrip-Fruin',
			venue: 'Poster presentation, International Conference on Interactive Digital Storytelling',
			year: '2021',
			url: 'https://www.devi-a.com/papers/icids_2021.pdf',
			abstract:
				'In running tabletop roleplaying games (TTRPGs), game masters (GMs) are tasked with helping create and facilitate the building of a shared story between players based on player choices. In this paper, we look at how we can inform the design of computational tools for GMs through the use of qualitative interviews. We present GMs with a prototype of a computational tool built based on a beginner TTRPG module that has some of the features we believe would be useful in a GMing assistant, such as consolidating information for easier reference and helping GMs keep track of what has happened in the game world. From these interviews, we found which features GMs liked and what could be improved with our digital prototype.'
		},
		{
			id: 'ttrpg_PCG',
			name: 'Tabletop Roleplaying Games as Procedural Content Generators',
			authors: 'Matthew Guzdial, Devi Acharya, Max Kreminski, Michael Cook, Mirjam Eladhari, Antonios Liapis, Anne Sullivan',
			venue: 'International Conference on the Foundations of Digital Games',
			year: '2020',
			url: 'https://www.devi-a.com/papers/ttrpg_pcg.pdf',
			abstract:
				'Tabletop roleplaying games (TTRPGs) and procedural content generators can both be understood as systems of rules for producing content. In this paper, we argue that TTRPG design can usefully be viewed as procedural content generator design. We present several case studies linking key concepts from PCG research -- including possibility spaces, expressive range analysis, and generative pipelines -- to key concepts in TTRPG design. We then discuss the implications of these relationships and suggest directions for future work uniting research in TTRPGs and PCG.'
		},
		{
			id: 'spatial_cognitive',
			name: 'Spatial cognitive implications of teleporting through virtual environments',
			authors: 'Lucia A Cherep, Alex F Lim, Jonathan W Kelly, Devi Acharya, Alfredo Velasco, Emanuel Bustamante, Alec G Ostrander, and Stephen B Gilbert',
			venue: 'Journal of Experimental Psychology: Applied',
			year: '2020',
			award: 'Raymond S. Nickerson Award for best paper',
			url: 'https://www.devi-a.com/papers/spatial.pdf',
			abstract:
				'Teleporting is a popular interface to allow virtual reality users to explore environments that are larger than the available walking space. When teleporting, the user positions a marker in the virtual environment and is instantly transported without any self-motion cues. Five experiments were designed to evaluate the spatial cognitive consequences of teleporting and to identify environmental cues that could mitigate those costs. Participants performed a triangle completion task by traversing 2 outbound path legs before pointing to the unmarked path origin. Locomotion was accomplished via walking or 2 common implementations of the teleporting interface distinguished by the concordance between movement of the body and movement through the virtual environment. In the partially concordant teleporting interface, participants teleported to translate (change position) but turned the body to rotate. In the discordant teleporting interface, participants teleported to translate and rotate. Across all 5 experiments, discordant teleporting produced larger errors than partially concordant teleporting which produced larger errors than walking, reflecting the importance of translational and rotational self-motion cues. Furthermore, geometric boundaries (room walls or a fence) were necessary to mitigate the spatial cognitive costs associated with teleporting, and landmarks were helpful only in the context of a geometric boundary.'
		},
		{
			id: 'cozy_mystery',
			name: 'Cozy mystery construction kit: Prototyping toward an AI-assisted collaborative storytelling mystery game',
			authors: 'Max Kreminski, Devi Acharya, Nick Junius, Elisabeth Oliver, Kate Compton, Melanie Dickinson, Cyril Focht, Stacey Mason, Stella Mazeika, and Noah Wardrip-Fruin',
			venue: 'Procedural Generation Workshop, International Converence on the Foundations of Digital Games',
			year: '2019',
			url: 'https://www.devi-a.com/papers/CozyMysteryConstructionKit.pdf',
			abstract:
				'This paper presents a case study in the experience-first prototyping of a generative game. Our goal in this process was to create a PCG-based mystery story construction game ncentered on a social simulation of characters and their motivations, and driven by a set of core themes and experiences we wanted players to encounter. In pursuit of this goal, we created a series of prototypes to test how a variety of generative and AI-based techniques--including character generation, character action suggestion based on game state, story sifting, and social simulation--may be used in support of collaborative storytelling. In this paper we catalogue these prototypes and what we have learned by creating them, detailing design elements we found to be successful in supporting player creativity and that may be useful to the developers of similar games and experiences going forward.'
		},
		{
			id: 'building_worlds',
			name: 'Building worlds together: understanding collaborative co-creation of game worlds',
			authors: 'Devi Acharya and Noah Wardrip-Fruin',
			venue: 'International Conference on the Foundations of Digital Games',
			year: '2019',
			url: 'https://www.devi-a.com/papers/Acharya_BuildingWorldsTogether.pdf',
			abstract:
				"This paper presents a preliminary exploration of games as sites of collaborative game world creation. By this, we mean the processes in games by which players take on a dual role as player within the game world and maker of the game world, sharing authorship of the world and its design with the game's designers and other players. We explore several examples of games featuring game world co-creation at the core of their gameplay, and use this to create a model for understanding the commonalities across these various games and how they facilitate this collaborative process. By examining similar structures in the design and play of these games, we can better understand how to identify this process in existing games and how to better create games that allow for this in the future."
		}
	];
</script>

<section class="publications">
	<h1 class="h1">Publications</h1>
	{#each publications as publication}
		<div class="list-dl">
			<div class="article">
				<span class="flex-auto">
					<dt><h4 class="h4">{publication.name}</h4></dt>
					<dd>{publication.authors}</dd>
					<dd>
						<em>{publication.venue}</em>
						, {publication.year}
					</dd>
				</span>
				<span>
					<a href={publication.url} type="button" class="btn-icon variant-filled"><span><i class="fa-regular fa-file-pdf"></i></span></a>
				</span>
			</div>
		</div>
	{/each}
</section>
