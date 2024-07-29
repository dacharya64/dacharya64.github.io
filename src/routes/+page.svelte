<script>
	import { LightSwitch } from '@skeletonlabs/skeleton';
	import Landing from './landing.svelte';
</script>

<!-- Header -->
<header class="flex p-4 justify-between">
	<div>
		<h4 class="h4">
			<strong>Devi Acharya</strong>
			| <i class="fa-solid fa-gears"></i> AI in Games
		</h4>
	</div>

	<div>
		<LightSwitch />
	</div>
</header>

<!-- Main body -->
<section class="homepage">
	<Landing />
</section>

<!-- Contact me button -->
<div class="fixed bottom-0 w-full">
	<a href="mailto:dacharya64@proton.me" target="blank" type="button" class="btn-icon btn-icon-xl variant-filled float-right contact"><i class="fa-solid fa-envelope"></i></a>
</div>
