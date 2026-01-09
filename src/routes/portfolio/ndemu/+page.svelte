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
			<a href="https://training.fema.gov/" target="_blank">Live Site &#8663;</a>
		</div>
		<figure class="m-top-md">
			<img
				style:view-transition-name={transitionImageName}
				src="/images/projects/ndemu.webp"
				alt="Front page of training.fema.gov"
				width="600"
				height="240"
				class="thumbnail-img"
			/>
			<figcaption>The front page of training.fema.gov</figcaption>
		</figure>

		<div class="fade-in prose">
			<p>
				Since 2025 I have been working as a contractor for FEMA specifically working as a Webmaster
				updating <a href="https://training.fema.gov">training.fema.gov</a>.
			</p>
			<p>
				There have been two major goals for updating this website. The first has been pushing old
				content into the new <a href="https://designsystem.digital.gov/"
					>United States Web Design System</a
				> <abbr>USWDS</abbr>. The new updates currently reside on the testing server, however many
				pages are already using the new standard.
			</p>
			<p>
				The second goal is switching from a database architecture to an API architecture for
				students to view and signup for courses. On the current live website, looking at courses
				under the Independent Study curriculum will show a table where all the courses have been
				manually entered into a database. The new way of doing things is using the new <a
					href="https://www.fema.gov/about/openfema/api">OpenFEMA API</a
				> to get all of the updated courses. This streamlines the process and makes it better for students
				to get up to date information.
			</p>
		</div>
	</div>
</main>
