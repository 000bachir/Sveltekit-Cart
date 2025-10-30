<script>
	import Hero from '$lib/components/InitSection/Hero.svelte';
	import Stores from '$lib/components/InitSection/Stores.svelte';
	import Types from '$lib/components/InitSection/Types.svelte';
	import DerivedStore from '$lib/components/LogicSection/DerivedStore.svelte';
</script>

<svelte:head>
	<title>Cart Blog</title>

	<meta
		name="description"
		content="Learn how to build a universal cart using SvelteKit with simple explanations and clean examples."
	/>
	<meta name="author" content="Peak" />
	<meta name="keywords" content="SvelteKit, shopping cart, web development, JavaScript, frontend" />

	<!-- Open Graph (for social media) -->
	<meta property="og:title" content="Cart Blog" />
	<meta
		property="og:description"
		content="Learn how to build a universal cart using SvelteKit with clean examples and simple explanations."
	/>
	<meta property="og:type" content="website" />
	<meta property="og:url" content="https://sveltekit-ecommerce-cart.netlify.app/" />
	<meta property="og:image" content="https://sveltekit-ecommerce-cart.netlify.app/banner.jpg" />
	<meta property="og:image:width" content="1200" />
	<meta property="og:image:height" content="630" />

	<!-- Twitter cards -->
	<meta name="twitter:card" content="summary_large_image" />
	<meta name="twitter:title" content="Cart Blog" />
	<meta
		name="twitter:description"
		content="Learn how to build a universal cart using SvelteKit with clean examples and simple explanations."
	/>
	<meta name="twitter:image" content="https://sveltekit-ecommerce-cart.netlify.app/banner.jpg" />
</svelte:head>

<!-- <svelte:head>
	<title>Shopping Cart</title>
	<meta
		name="description"
		content="A developer blog sharing tutorials and projects built with SvelteKit, JavaScript, and modern web technologies."
	/>
</svelte:head> -->

<main class="relative h-auto w-full overflow-hidden text-white">
	<section
		id="title_of_the_blog"
		class="relative flex h-28 w-full items-center justify-center overflow-hidden bg-amber-400"
	>
		<h1
			class="font-semibold text-black underline decoration-4 sm:text-sm md:text-lg lg:text-xl xl:text-2xl 2xl:text-3xl"
		>
			The Easiest Way to Make a Cart in SvelteKit
		</h1>
	</section>

	<!-- ? this part will be kind of an intro on how to import initialise and the sync the tools needed -->

	<Hero />
	<Types />
	<Stores />
	<!-- !the logic part -->
	<DerivedStore />
</main>

<style>
	@media screen and (max-width: 375px) {
		#title_of_the_blog > h1 {
			text-align: center;
			text-wrap: balance;
		}
	}
</style>
