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
			<a href="https://claytonoffroad.com" target="_blank">Live Site &#8663;</a>
			<a
				href="https://claytonoffroad.com/products/jeep-gladiator-diesel-3-5-premium-lift-kit-2021-2023-jt"
				target="_blank">Live Site (Product Page) &#8663;</a
			>
		</div>
		<figure class="m-top-md">
			<img
				style:view-transition-name={transitionImageName}
				src="/images/projects/clayton-home.webp"
				alt="Clayton Offroad's home page"
				width="600"
				height="240"
				class="thumbnail-img"
			/>
			<figcaption>Clayton Offroad's homepage</figcaption>
		</figure>

		<div class="fade-in prose">
			<p>
				This client wanted to move away from their Drupal site into a Shopify website, however they
				had a lot of custom requests that basic Shopify themes couldn't handle.
			</p>
			<p>Requirements for this project:</p>
			<ul>
				<li>
					Lift Kit Customization
					<ul>
						<li>
							Lift Kits contain many individual products from Clayton's catalog. Kits needed to be
							dynamically linked with these products.
						</li>
					</ul>
				</li>
				<li>Advanced product filtering</li>
				<li>Dynamic files that needed to be attached to products</li>
				<li>Specific shipping requirements</li>
			</ul>
			<h3>Lift Kits</h3>
			<p>
				Each lift kit contains multiple products in it. A customer can choose to purchase the entire
				lift kit, or specific parts from the kit.
			</p>
			<figure>
				<img
					src="/images/projects/clayton-product-1.webp"
					alt="Clayton Offroad's Lift kit product page"
					width="600"
					height="240"
					class="thumbnail-img"
				/>
				<figcaption>Lift kit product page</figcaption>
			</figure>
			<p>
				In the image above we can see what the product page looks like. Notice the "Kit Includes"
				section, this is where a customer can select and deselect items in the kit that they want.
			</p>
			<p>
				Kits and Individual product all have their own unique SKUs, this creates a challenge when
				linking everything together. Luckily Shopify has metafields which makes creating
				interactions like this much easier.
			</p>
			<p>
				I was able to create a product list metafield in order to link kits together with their
				individual parts.
			</p>
			<h3>Dynamic Data</h3>
			<p>There's a lot of other metadata that these products needed as well.</p>
			<figure>
				<img
					src="/images/projects/clayton-product-2.webp"
					alt="Product page instruction tab with list of files"
					width="600"
					height="240"
					class="thumbnail-img"
				/>
				<figcaption>Instruction files for this lift kit</figcaption>
			</figure>
			<p>At the bottom of the product page there are multiple tabs filled with dynamic data.</p>
			<p>
				The image above shows the Instruction tab for this product. Again, each product and lift kit
				contains a specific set of instructions, so we needed another set of metafields.
			</p>
			<p>
				Another example of this comes with the packaging tab. Due to the nature of lift kits being a
				parent of individual products, packaging differs when a user orders a whole kit versus half
				of the kit.
			</p>
			<figure>
				<img
					src="/images/projects/clayton-product-3.webp"
					alt="Product page packaging tab with list of boxes"
					width="600"
					height="240"
					class="thumbnail-img"
				/>
				<figcaption>Packaging tab with list of boxes for the kit</figcaption>
			</figure>
			<p>
				For this kit, if a customer orders the entire kit they would receive 7 different boxes,
				however if a customer deselected one item they would receive a separate package for each
				product.
			</p>
			<p>
				This is also reflected with the shipping price which dynamically changes based on what the
				user selects.
			</p>
			<h3>Collection Pages & Product Filters</h3>
			<p>
				There's a lot of dynamic data going on with this website, so naturally when users are
				searching for products, there needs to be a robust system for them to find exactly what
				they're looking for.
			</p>
			<figure>
				<img
					src="/images/projects/clayton-collection.webp"
					alt="Collection page with live updates based on filters"
					width="600"
					height="240"
					class="thumbnail-img"
				/>
				<figcaption>Collection page with live updates based on filters</figcaption>
			</figure>
			<p>
				In the picture above we can see a bunch of filters available for customers. These filters
				also update based on the products that are being listed on the page.
			</p>
			<p>
				This means that a filter updates the product list and the product list updates the available
				filters to narrow things down for the customer.
			</p>
		</div>
	</div>
</main>
