<script>
</script>

<svelte:head>
	<title>About | Cart Blog</title>

	<meta
		name="description"
		content="Learn about Peak, the developer behind Cart Blog, and the inspiration for building a universal cart using SvelteKit."
	/>
	<meta name="author" content="Peak" />
	<meta
		name="keywords"
		content="SvelteKit, shopping cart, web development, JavaScript, frontend, developer story, about"
	/>

	<!-- Open Graph (Social Media Preview) -->
	<meta property="og:title" content="About | Cart Blog" />
	<meta
		property="og:description"
		content="Discover why this blog was created and the motivation behind building a universal cart with SvelteKit."
	/>
	<meta property="og:type" content="website" />
	<meta property="og:url" content="https://sveltekit-ecommerce-cart.netlify.app/about" />
	<meta property="og:image" content="https://sveltekit-ecommerce-cart.netlify.app/banner.jpg" />
	<meta property="og:image:width" content="1200" />
	<meta property="og:image:height" content="630" />

	<!-- Twitter Card -->
	<meta name="twitter:card" content="summary_large_image" />
	<meta name="twitter:title" content="About | Cart Blog" />
	<meta
		name="twitter:description"
		content="Discover why this blog was created and the motivation behind building a universal cart with SvelteKit."
	/>
	<meta name="twitter:image" content="https://sveltekit-ecommerce-cart.netlify.app/banner.jpg" />
</svelte:head>

<main class="relative h-auto w-full overflow-hidden">
	<section id="intro-section" class="flex h-dvh w-full items-center justify-center">
		<div id="content-card" class=" h-[90%] w-[90%] rounded-2xl border-[1px] border-gray-400 shadow">
			<div
				id="text-container"
				class="relative mx-auto flex h-full w-[95%] flex-col items-center justify-around"
			>
				<h1 id="greeting-header" class="text-2xl font-semibold text-white">
					Hey am the developer : 🙋‍♂️
				</h1>

				<p id="intro-paragraph" class="text-lg font-semibold text-white">
					A bit of a talk — this “blog” is about how to make a universal cart in SvelteKit. I know a
					real one would use a proper database, and I highly advise avoiding localStorage for
					real-world projects due to security reasons. However, if you’re just exploring or
					experimenting, you can use this example to play around and learn. I tried to add some
					colors and images to make it feel a bit more welcoming. It might not look very
					professional, but I enjoy learning with some color around and straightforward explanations
					and code samples
				</p>
			</div>
		</div>
	</section>
</main>

<style>
	@media screen and (max-width: 425px) {
		#intro-section {
			height: auto;
			width: 100%;
			padding: 2rem 0rem;
		}

		#text-container {
			padding: 1rem;
			display: flex;
			align-items: center;
			justify-content: center;
			flex-direction: column;
			gap: 2rem;
		}

		#greeting-header {
			font-size: 1.2rem;
		}

		#intro-paragraph {
			font-size: 1rem;
		}
	}
</style>
