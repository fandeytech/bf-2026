<script>
	import React from '$lib/assets/svgs/React.svelte';
	import Html from '$lib/assets/svgs/Html.svelte';
	import Css from '$lib/assets/svgs/Css.svelte';
	import Net from '$lib/assets/svgs/Net.svelte';
	import CSharp from '$lib/assets/svgs/CSharp.svelte';
	import Javascript from '$lib/assets/svgs/Javascript.svelte';
	import Typescript from '$lib/assets/svgs/Typescript.svelte';
	import Sveltekit from '$lib/assets/svgs/Sveltekit.svelte';
	import Wordpress from '$lib/assets/svgs/Wordpress.svelte';
	import Shopify from '$lib/assets/svgs/Shopify.svelte';
	import Article from '$lib/components/Article.svelte';
	import Golang from '$lib/assets/svgs/Golang.svelte';
	import Fema from '$lib/assets/svgs/Fema.svelte';
</script>

<main id="main-content">
	<div class="wrapper-lg">
		<section>
			<h1>Bijan Fandey</h1>
			<div>
				<h2>Full-Stack Web Developer</h2>
				<p>Maryland, USA</p>
			</div>
			<div class="prose">
				<p>
					Hi, I'm Bijan. I've been developing websites for over 5 years. I've worked at a marketing
					company using traditional tools like HTML, CSS and JavaScript as well as a contractor
					under the Federal Government working for FEMA using .NET and C#.
				</p>
			</div>
			<div class="languages m-top-lg flex flex-col gap-lg align-end">
				<h3>The Tech I Use</h3>
				<div class="flex gap-md flex-wrap justify-end">
					<Html />
					<Css />
					<Javascript />
					<Typescript />
					<CSharp />
					<Net />
					<React />
					<Sveltekit />
					<Golang />
					<Wordpress />
					<Shopify />
				</div>
			</div>
		</section>
		<hr />
		<section class="section-spacer flex flex-col gap-sm">
			<h2>My Work</h2>
			<div class="flex gap-md m-top-lg">
				<div>
					<Fema />
				</div>
				<div>
					<h3>FEMA Webmaster</h3>
					<small>January 2025 - January 2026</small>
					<ul class="job-responsibilities m-top-md flex flex-col gap-sm">
						<li>Worked with .NET Framework 4 and C# for training.fema.gov.</li>
						<li>Updated legacy pages to USWDS 3.</li>
						<li>
							Refactored code base, removing and fixing repetitive, insecure, and outdated code.
						</li>
						<li>Worked within a development and production pipeline.</li>
					</ul>
				</div>
			</div>
			<div class="projects m-top-md">
				<Article
					title="NDEMU"
					subTitle=".NET & C#"
					imgPath="/images/projects/ndemu.webp"
					description="The National Disaster and Emergency Management University and the updates I made to this website."
					projectLink="https://training.fema.gov/"
					href="/portfolio/ndemu"
				/>
			</div>
			<div class="flex gap-md section-spacer">
				<img
					src="/images/icons/impakt-logo.jpg"
					class="company-logo"
					alt="Impakt Results logo"
					width="50"
					height="50"
				/>
				<div>
					<h3>Impakt Results</h3>
					<small>January 2021 - January 2025</small>
					<ul class="job-responsibilities m-top-md flex flex-col gap-sm">
						<li>
							Communicated directly with business owners and shareholders to discuss technical
							needs.
						</li>
						<li>
							Worked in various CMSs (Shopify, WordPress, etc.) to edit existing websites, and
							develop new websites.
						</li>
						<li>Created full-stack applications using SvelteKit, JavaScript, SQL.</li>
						<li>
							Integrated custom functionality and additional features for existing websites that
							matched current design systems.
						</li>
						<li>
							Lead the development and creation of many successful Conversion Rate Optimization
							tests
						</li>
					</ul>
				</div>
			</div>
			<div class="projects m-top-md">
				<Article
					title="Calyton Offroad"
					subTitle="Shopify"
					imgPath="/images/projects/clayton-home.webp"
					description="Moving a website from Drupal to a custom Shopify theme."
					projectLink="https://claytonoffroad.com/"
					href="/portfolio/clayton-offroad"
				/>
				<Article
					title="Racetech Titanium"
					subTitle="WordPress & PHP"
					imgPath="/images/projects/racetech-colors.webp"
					description="A custom WordPress plugin for variant selection with images for variants."
					projectLink="https://racetechtitanium.com/product/titanium-linkage-bolts-talaria-sting-mx4/"
					href="/portfolio/racetech"
				/>
			</div>
		</section>
		<section class="section-spacer flex flex-col gap-sm">
			<h2>Open Source</h2>
			<p>Some projects I've made and open sourced to provide simple tools for web developers.</p>

			<div class="projects">
				<Article
					title="VanillaHTML"
					subTitle="Accessibility (WCAG), HTML & CSS"
					imgPath="/images/projects/vanilla-html-section.webp"
					description="A project to help beginners learn the basics of semantic markup to build a more
				accessible internet"
					gitLink="https://github.com/fandeytech/VanillaHTML"
					projectLink="https://vanillahtml.fandeytech.com/"
					href="/portfolio/vanilla-html"
				/>
				<Article
					title="SVG Wave Generator"
					subTitle="JavaScript"
					imgPath="/images/projects/wave-gen.webp"
					description="An SVG Wave Generator for creative web designs and how I used AI to help build this project."
					gitLink="https://github.com/fandeytech/Wave-Generator"
					projectLink="https://wave-generator.fandeytech.com/index.html"
					href="/portfolio/wave-generator"
				/>
			</div>
		</section>

		<section class="section-spacer flex flex-col gap-sm">
			<h2>Work In Progress</h2>
			<p>
				Some of my hobby projects that are still in development and unreleased. You'll notice I'm a
				big fan of SvelteKit :)
			</p>
			<div class="projects">
				<Article
					title="FlareNetwork"
					subTitle="SvelteKit, TypeScript & Go"
					imgPath="/images/projects/flarenetwork-home.webp"
					description="No Ads, No Algorithms. A video hosting website where users get to decide whats popular and what's not. With plans for decentralized content with EmberForgery."
					href="/portfolio/flare-network"
				/>
				<Article
					title="EmberForgery"
					subTitle="SvelteKit, TypeScript"
					imgPath="/images/projects/emf-theme.webp"
					description="A lightweight website builder and content management system for creators to host their own content. Designed to integrate with FlareNetwork."
					href="/portfolio/ember-forgery"
				/>
			</div>
		</section>
	</div>
</main>

<style>
	.languages :global(svg) {
		width: 48px;
		height: 48px;
	}
	.projects {
		--columns: 2;
		display: grid;
		grid-template-columns: repeat(var(--columns), 1fr);
		gap: 1rem;
	}
	.company-logo {
		max-width: 50px;
		width: 100%;
		object-fit: contain;
		margin-bottom: auto;
	}
	.job-responsibilities {
		margin-left: 2rem;
	}
	@media (max-width: 674px) {
		.projects {
			--columns: 1;
		}
		h1 {
			font-size: 6rem;
		}
	}
</style>
