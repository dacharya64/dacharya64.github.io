<script>
	export let showOnPx = 150;
	let hidden = true;

	function goTop() {
		document.body.scrollIntoView();
	}

	function scrollContainer() {
		return document.documentElement || document.body;
	}

	function handleOnScroll() {
		if (!scrollContainer()) {
			return;
		}

		if (scrollContainer().scrollTop > showOnPx) {
			hidden = false;
		} else {
			hidden = true;
		}
	}
</script>

<svelte:window on:scroll={handleOnScroll} />

<footer class="flex p-4 justify-between">
	<div>
		<p>
			Made with <i class="fa-solid fa-heart"></i> by <a href="../" class="anchor">Devi Acharya</a> |
			<a class="anchor" href="https://github.com/dacharya64/dacharya64.github.io"> Fork me on <i class="fa-brands fa-github"></i></a>
		</p>
	</div>
	<div><a href="../" class="btn-icon variant-filled"><i class="fa-solid fa-house"></i></a></div>
</footer>
