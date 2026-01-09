<script lang="ts">
	import favicon from '$lib/assets/favicon.svg';

	let { children } = $props();
</script>

<svelte:head>
	<link rel="icon" href={favicon} />
</svelte:head>
<div class="portfolio">
	{@render children()}
</div>

<style>
	.portfolio :global(img) {
		width: 100%;
		height: auto;
	}
	.portfolio :global(h1) {
		text-align: center;
		font-size: 4rem;
	}
</style>
