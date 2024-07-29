<script lang="ts">
	import Publications from './publications.svelte';
	import Projects from './projects.svelte';
	import Bio from './bio.svelte';

	import { createEventDispatcher } from 'svelte';

	const dispatch = createEventDispatcher();

	/**
	 * @param {{ detail: { text: any; }; }} event
	 */
	function handleMessage(event: { detail: { text: any } }) {
		dispatch('message', {
			text: event.detail.text
		});
	}
</script>

<Bio />
<Projects on:message={handleMessage} />
<Publications />
