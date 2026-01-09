<script>
	let { data } = $props();

	const transitionTitleName = $derived(
		`title-${data?.title?.toLowerCase().replace(/[^a-z0-9]/g, '-')}`
	);
	const transitionImageName = $derived(
		`image-${data?.title?.toLowerCase().replace(/[^a-z0-9]/g, '-')}`
	);
</script>

<main id="main-content">
	<div class="wrapper-lg flex flex-col align-center">
		<h1 style:view-transition-name={transitionTitleName}>
			{data.title}
		</h1>
		<div class="flex gap-sm flex-wrap">
			<a
				href="https://racetechtitanium.com/product/titanium-linkage-bolts-talaria-sting-mx4/"
				target="_blank">Live Site &#8663;</a
			>
		</div>
		<figure class="m-top-md">
			<img
				style:view-transition-name={transitionImageName}
				src="/images/projects/racetech-colors.webp"
				alt="Variant selection for products on Racetech Titanium"
				width="600"
				height="240"
				class="thumbnail-img"
			/>
			<figcaption>Variant selection for products on Racetech Titanium</figcaption>
		</figure>

		<div class="fade-in prose">
			<p>
				This is a client I worked with when I was working at a marketing company. They had a
				WordPress website and they had some specific requirements for a variant selection plugin.
				After looking for an existing plugin that met their exact requirements, I was unable to find
				a perfect solution.
			</p>
			<p>The requirements:</p>
			<ul>
				<li>Variant buttons need to have an image, not a solid color.</li>
				<li>Variant buttons need to have a tooltip.</li>
				<li>
					The main picture needs to change based on the selected color
					<ul>
						<li>
							The plugin has the functionality for individual images per color, however in most
							cases the client opted for a single image that shows all the colors.
						</li>
					</ul>
				</li>
				<li>
					The selected variant and colored image need to appear with the line item in the cart.
				</li>
			</ul>
			<figure>
				<img
					src="/images/projects/racetech-color-select.webp"
					alt="Variant selection when hovered and clicked"
					width="600"
					height="240"
					class="thumbnail-img"
				/>
				<figcaption>Variant selection when hovered and clicked</figcaption>
			</figure>
			<figure>
				<img
					src="/images/projects/racetech-cart.webp"
					alt="Variant selection displayed in cart"
					width="600"
					height="240"
					class="thumbnail-img"
				/>
				<figcaption>Variant selection displayed in cart</figcaption>
			</figure>
			<p>
				This was one of my first ventures into creating plugins for Wordpress, and I used AI to help
				me bridge some gaps in my knowledge to get everything working as intended.
			</p>
			<p>
				Overall the client was very happy with how this turned out and has been using this plugin
				for over three years now.
			</p>
		</div>
	</div>
</main>
