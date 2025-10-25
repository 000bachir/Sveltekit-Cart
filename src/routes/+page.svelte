<script>
	import Hero from '$lib/components/InitSection/Hero.svelte';
	import Stores from '$lib/components/InitSection/Stores.svelte';
	import Types from '$lib/components/InitSection/Types.svelte';
	import DerivedStore from '$lib/components/LogicSection/DerivedStore.svelte';



</script>

<svelte:head>
	<title>Shopping Cart</title>
	<meta
		name="description"
		content="A developer blog sharing tutorials and projects built with SvelteKit, JavaScript, and modern web technologies."
	/>
</svelte:head>

<main class="relative h-auto w-full overflow-hidden text-white">
	<section
		id="title_of_the_blog"
		class="relative flex h-28 w-full items-center justify-center overflow-hidden bg-amber-400"
	>
		<h1
			class="font-semibold underline decoration-4 sm:text-sm md:text-lg lg:text-xl xl:text-2xl 2xl:text-3xl"
		>
			The Easiest Way to Make a Cart in SvelteKit
		</h1>
	</section>


	<!-- ? this part will be kind of an intro on how to import initialise and the sync the tools needed -->

	<Hero />
    <Types />
	<Stores />

	<!-- ! Now the logic part -->

	<DerivedStore />

</main>
