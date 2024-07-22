<script>
	import Publications from './publications.svelte';
	import Projects from './projects.svelte';
	import Bio from './bio.svelte';
	import { LightSwitch } from '@skeletonlabs/skeleton';
</script>

<header class="flex p-4 justify-between">
	<div>
		<h4 class="h4">
			<strong>Devi Acharya</strong>
			| AI in Games
		</h4>
	</div>
	<div><LightSwitch /></div>
</header>

<section class="homepage">
	<Bio />
	<Projects />
	<Publications />
</section>
