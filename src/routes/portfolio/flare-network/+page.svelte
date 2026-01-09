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
		<figure>
			<img
				style:view-transition-name={transitionImageName}
				src="/images/projects/flarenetwork-home.webp"
				alt="Preview of FlareNetwork home page"
				width="600"
				height="240"
				class="thumbnail-img"
			/>
			<figcaption>A preview of FlareNetwork's homepage</figcaption>
		</figure>

		<div class="fade-in prose">
			<p>
				FlareNetwork is my passion project that I've been working on for about a year now as I've
				grown tired with how the internet is shaping out to be; With an infinite amount of ads,
				bots, and slop, instead of complaining, I've decided to be the change I want to see in the
				world.
			</p>
			<p>
				What makes FlareNetwork unique is a specialized global point system for the platform called <em
					>Ember</em
				>. Users will be able to contribute Ember to content that they enjoy, boosting it's ranking
				on the platform. Content with the most Ember will be show as
				<em>Wildfire</em> on the front page of the website. Ember only lasts 24 hours, after this
				period it will extinguish into
				<em>Ash</em>. Ash is a historical metric so people can know how much total Ember a piece of
				content has ever had.
			</p>
			<figure>
				<img src="/images/projects/flarenetwork-channel.webp" alt="FlareNetwork channel page" />
				<figcaption>A preview of a FlareNetwork channel page.</figcaption>
			</figure>
			<p>
				Rather than a free-with-ads business model, users will have to pay for video storage and
				interactive features.
			</p>
			<p>
				FlareNetwork is designed to create a platform with a much more intentional consumer
				experience. It's designed for more unique content because there is no algorithmic bias. It's
				built with love and passion and I want people to enjoy every aspect of the website.
			</p>
			<h3>The Tech Behind FlareNetwork</h3>
			<p>
				This project has put me in a jack-of-all-trades position. I'm doing everything from front &
				backend, to database design, to server management, and so much more. The tech stack
				includes:
			</p>
			<ul>
				<li>SvelteKit</li>
				<li>
					Go
					<ul>
						<li>API for creating and queuing jobs</li>
						<li>Go Routines for checking queue and running ffmpeg commands</li>
					</ul>
				</li>
				<li>FFMPEG</li>
				<li>Postgres</li>
				<li>
					Redis
					<ul>
						<li>Caching pre-signed URLs</li>
						<li>Queue for video processing</li>
					</ul>
				</li>
				<li>
					s3 Buckets
					<ul>
						<li>Storing media assets and video content</li>
						<li>Creating pre-signed URLs</li>
					</ul>
				</li>
				<li>
					Shaka Packager & Player
					<ul>
						<li>Segmentation of media</li>
						<li>Adaptive bitrate streaming</li>
					</ul>
				</li>
				<li>Stripe (Payments)</li>
				<li>FusionAuth (User accounts)</li>
			</ul>
			<p>
				There's a lot going on! It's been the best learning experience I've ever had and I'm super
				excited to get this live and start to share and test it with the world. Hopefully reclaiming
				some of what the original internet felt like.
			</p>

			<h3>What's Needed for Launch</h3>
			<p>
				While the core functionality is complete (with video uploads and processing, as well as the
				interactive experience with sending Ember, posting comments, and all the other features you
				would want in a social platform), there is still quite a bit left before I'm ready to launch
				this website.
			</p>
			<p>
				First, there's a lot of design updates I have to make. My main focus thus far has been
				getting everything to work the way I want, the next step is making it all look the way I
				want.
			</p>
			<p>
				After the design there are some analytics features I have to fix, things like view counts. I
				already have a system in place, but it's a very simple system, and needs to be a bit more
				robust.
			</p>
			<p>These are the two main areas I need to work on before actually launching this website.</p>
		</div>
	</div>
</main>
