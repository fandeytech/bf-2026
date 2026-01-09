<script>
	import { resolve } from '$app/paths';

	let { data } = $props();
	const transitionTitleName = $derived(
		`title-${data?.title?.toLowerCase().replace(/[^a-z0-9]/g, '-')}`
	);
</script>

<main id="main-content">
	<div class="wrapper-lg flex flex-col align-center">
		<h1 style:view-transition-name={transitionTitleName}>
			{data.title}
		</h1>

		<div class="fade-in prose">
			<figure>
				<img
					src="/images/projects/emf-home.webp"
					alt="Preview of EmberForgery's home page"
					width="600"
					height="240"
					class="thumbnail-img"
				/>
				<figcaption>A preview of EmberForgery's homepage</figcaption>
			</figure>
			<p>
				EmberForgery is a lightweight website builder that allows creators to host their own
				content, set their own rules, and create online communities that they own.
			</p>
			<p>
				In addition, it's designed to integrate into the FlareNetwork, which is a network of
				websites intended for a new way to discover content on the internet.
			</p>
			<h3>What's included in the FlareNetwork?</h3>
			<h4>FlareNetwork.com</h4>
			<p>
				FlareNetwork is a social platform free from ads and algorithms. Please read <a
					href={resolve('/portfolio/flare-network')}>my project breakdown</a
				> for more information.
			</p>
			<h4>FlareFinder.net</h4>
			<p>
				FlareFinder is a search engine that specifically lists websites created with EmberForgery.
			</p>
			<h3>How does EmberForgery work?</h3>
			<p>EmberForgery is still in it's very early stages. FlareNetwork will be released first.</p>
			<p>
				However, EmberForgery is designed to be a minimal, easy to use, website builder. It doesn't
				allow for full website customization, but rather it's designed to be a cohesive experience
				so users know that they are on a website connected to the FlareNetwork.
			</p>
			<figure>
				<img
					src="/images/projects/emf-theme.webp"
					alt="Preview of EmberForgery's home page"
					width="600"
					height="240"
					class="thumbnail-img"
				/>
				<figcaption>An early preview of the EmberForgery Theme Builder</figcaption>
			</figure>
			<figure>
				<img
					src="/images/projects/emf-content.webp"
					alt="Preview of EmberForgery's home page"
					width="600"
					height="240"
					class="thumbnail-img"
				/>
				<figcaption>An early preview of the EmberForgery Content Editor</figcaption>
			</figure>
			<p>
				In the images above we can start to get the idea of how people will create websites and
				content. The theme builder is quite simple, rather than a drag and drop editor, the theme is
				already pre-designed and the creator can edit the aesthetic of the website to math their
				personality.
			</p>
			<p>
				The content editor supports blog content in it's current form but it will be released to
				support blogs, videos, images, and other basic content forms.
			</p>
			<h3>The TechStack</h3>
			<p>
				There are two tech stacks involved in this project. One for the main website
				EmberForgery.com and the other for creator websites.
			</p>
			<h4>Main Website</h4>
			<ul>
				<li>SvelteKit</li>
				<li>Postgres</li>
			</ul>
			<h4>Creator Websites</h4>
			<ul>
				<li>SvelteKit Static Adapter</li>
				<li>SQL Lite</li>
			</ul>
		</div>
	</div>
</main>
