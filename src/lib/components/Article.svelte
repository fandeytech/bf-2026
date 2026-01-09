<script>
	import { resolve } from '$app/paths';

	let {
		title,
		subTitle = '',
		description,
		href,
		imgPath = '',
		gitLink = '',
		projectLink = ''
	} = $props();

	const transitionTitleName = $derived(`title-${title.toLowerCase().replace(/[^a-z0-9]/g, '-')}`);
	const transitionImageName = $derived(`image-${title.toLowerCase().replace(/[^a-z0-9]/g, '-')}`);
</script>

<article class="article flex flex-col gap-sm">
	<a href={resolve(href)}>
		<h3 style:view-transition-name={transitionTitleName}>
			{title}
		</h3>
		{#if subTitle != ''}
			<small class="subtitle">{subTitle}</small>
		{/if}
		{#if imgPath != ''}
			<img
				style:view-transition-name={transitionImageName}
				src={imgPath}
				alt={title}
				width="200"
				height="120"
				class="thumbnail-img"
			/>
		{/if}
	</a>
	<p>{description}</p>
	<div class="links flex gap-sm align-center">
		{#if gitLink != ''}
			<a class="read-more inline" href={gitLink} target="_blank">Github &#8663;</a>
		{/if}
		{#if projectLink != ''}
			<a class="read-more inline" href={projectLink} target="_blank">Live Site &#8663;</a>
		{/if}
		<a class="read-more" href={resolve(href)}>Read More</a>
	</div>
</article>

<style>
	.article {
		padding: 1rem;
		border: 1px solid currentColor;
		border-radius: var(--border-radius);
		background-color: white;
	}
	.article a {
		text-decoration: none;
	}
	.article p {
		font-size: 1.15rem;
	}
	.article .subtitle {
		display: block;
		margin-top: 0.25rem;
		margin-bottom: 1rem;
	}
	.article .thumbnail-img {
		display: block;
		max-width: 100%;
		width: fit-content;
		margin: auto;
		margin-bottom: 0.5rem;
		height: auto;
		max-height: 200px;
		object-fit: contain;
		box-shadow: 0 0 15px 0 rgba(0 0 0 / 0.5);
	}
	.article .read-more {
		display: block;
		width: fit-content;
		color: var(--color-light);
		background-color: var(--color-dark);
		padding: 0.5rem 1rem;
		border-radius: 9999px;

		&.inline {
			padding: 0;
			color: var(--color-dark);
			background-color: transparent;
			text-decoration: underline;
		}
	}
	.article .links {
		margin-top: auto;
		align-self: flex-end;
	}
</style>
