<script>
	let { data } = $props();

	const transitionName = $derived(`title-${data?.title?.toLowerCase().replace(/[^a-z0-9]/g, '-')}`);
</script>

<main id="main-content">
	<div class="wrapper-lg flex flex-col align-center">
		<h1 style:view-transition-name={transitionName}>
			{data.title}
		</h1>
		<div class="flex gap-sm flex-wrap">
			<a href="https://vanillahtml.fandeytech.com/" target="_blank">Live Site &#8663;</a>
			<a href="https://github.com/fandeytech/VanillaHTML" target="_blank">Github &#8663;</a>
		</div>
		<div class="fade-in prose">
			<p>
				Website accessibility is often overlooked, despite being an incredibly important aspect of
				web-development. I think this is because of a perceived notion that it's difficult to learn,
				or at least there's a lot to learn.
			</p>
			<p>
				While that may be true in some more advanced cases, the basics of accessible markup is
				actually very simple and it has more benefits than a lot of people realize.
			</p>
			<p>
				Accessibility isn't just about making your website accessible for users with disabilities,
				but it's also about structuring your website in a way that makes it easy for bots to
				understand.
			</p>
			<p>
				When we think about bots it's often a bad thing, but we should also remember that there are
				good and bad bots out there. For example, Google uses bots to crawl your website and index
				it within their search results. If it's hard for the bot to understand what your website is
				about, then it's harder for Google to list your website in relevant search results.
			</p>
			<p>
				Website accessibility has a direct impact on Search Engine Optimization <abbr>SEO</abbr>,
				and as a result it will have an impact on new search opportunities like Generative Engine
				Optimization <abbr>GEO</abbr>.
			</p>
			<h3>What is VanillaHTML and How Does it Help?</h3>
			<p>
				VanillaHTML is actually a CSS file that redesigns default HTML in a way that makes it easy
				to see what your markup is actually doing.
			</p>
			<p>It's intended purpose is to help beginners learn the fundamentals of semantic markup.</p>
			<figure>
				<img
					src="/images/projects/vanilla-html-section.webp"
					width="600"
					height="200"
					alt="VanillaHTML section element"
				/>
				<figcaption>
					An example <span>&#60;</span>section<span>&#62;</span> element using VanillaHTML.
				</figcaption>
			</figure>
			<p>
				In the example above the code looks just like generic HTML. It has a section, a header, and
				an hgroup element. The code looks like this:
			</p>
			<pre>
<code>
    <span>&#60;</span>section<span>&#62;</span>
        <span>&#60;</span>header<span>&#62;</span>
            <span>&#60;</span>hgroup<span>&#62;</span>
                <span>&#60;</span>h2<span>&#62;</span>VanillaHTML<span>&#60;</span>/h2<span
						>&#62;</span
					>
                <span>&#60;</span>small<span>&#62;</span>Version 1.1.1 | April 24, 2025<span
						>&#60;</span
					>/small<span>&#62;</span>
		<span>&#60;</span>p<span>&#62;</span>
		    Build Better Websites
		<span>&#60;</span>/p<span>&#62;</span>
            <span>&#60;</span>/hgroup<span>&#62;</span>
        <span>&#60;</span>/header<span>&#62;</span>
    <span>&#60;</span>/section<span>&#62;</span>
</code>
</pre>
			<p>
				Now the caveat with VanillaHTML is that it's quite verbose. In this example the CSS enforces
				us to have a header element within a section. This is to get people used to the fact that a
				section element should always have a header (as in h1, h2, h3...) but not necessarily the
				header element itself. For the purposes of education I thought it would be beneficial to
				have the header element enforced so people get used to this idea of "sections have headers"
			</p>
			<p>Here's the CSS for this:</p>
			<pre>
<code>
    section &#123;
      border: var(--section-border);
      display: grid;
      gap: 1rem;
      margin-block: 4rem;
    &#125;

    section:first-child &#123;
      margin-block-start: 2rem;
    &#125;

    section > :last-child &#123;
      margin-block-end: 1rem;
    &#125;

    section > header &#123;
      background: var(--surface-dark);
      color: var(--text-inverse);
      padding: 1rem;
    &#125;
</code>
			</pre>

			<h3>Future Plans for VanillaHTML</h3>
			<p>
				This project definitely has a long way to go to be a great learning tool. The documentation
				only shows examples and expects the user to check MDN documentation as they go along. This
				could really be improved with integrated lessons on the website.
			</p>
			<p>
				I also don't teach anything about attributes for elements, this is strictly contained to
				markup so people can visually understand what their semantic markup is doing.
			</p>
			<p>
				I'm planning on going back through and making the CSS file a full on helper and doing things
				like adding red borders when something is wrong so that the user knows in real time that
				there is an issue and continues to reinforce good markup for websites.
			</p>
		</div>
	</div>
</main>
