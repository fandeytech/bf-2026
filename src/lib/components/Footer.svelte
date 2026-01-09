<script>
	import { resolve } from '$app/paths';
	import Github from '$lib/assets/svgs/Github.svelte';
	import Linkedin from '$lib/assets/svgs/Linkedin.svelte';
</script>

<footer class="bottom-footer">
	<div class="wrapper-lg">
		<nav class="top-nav flex space-between align-center">
			<a href={resolve('/')} class="logo">
				<span>B</span>
			</a>
			<ul class="nav-links flex">
				<li>
					<a href="https://github.com/fandeytech" target="_blank">
						<span class="sr-only">Github</span>
						<Github />
					</a>
					<a href="https://www.linkedin.com/in/bijan-fandey-6b5511146/" target="_blank">
						<span class="sr-only">Linkedin</span>
						<Linkedin />
					</a>
				</li>
			</ul>
		</nav>
	</div>
</footer>

<style>
	.bottom-footer {
		margin-top: 4rem;
		padding-block: 1rem;
		border-top: 1px solid currentColor;
	}
	.bottom-footer .logo {
		text-decoration: none;
		font-weight: 600;
		font-size: 2rem;
		font-family: 'Stardos Stencil', system-ui;
	}
	.nav-links {
		list-style: none;
	}
	.nav-links :global(svg) {
		width: 28px;
		height: 28px;
	}
</style>
