<!--TODO : need to add responsiveness-->

<script>
	import StoreSveltekit from '$lib/assets/Icons/StoreSveltekit.svelte';
	import CheckingTheBrowser from '../ui/first_section_code_block/CheckingTheBrowser.svelte';
	import CreateTheStore from '../ui/first_section_code_block/CreateTheStore.svelte';
	import LocalStorageSync from '../ui/first_section_code_block/LocalStorageSync.svelte';
	import { onMount, onDestroy } from 'svelte';
	import gsap from 'gsap';
	import { ScrollTrigger } from 'gsap/dist/ScrollTrigger';
	import { browser } from '$app/environment';

	let scrollTriggerInstance;

	onMount(() => {
		if (browser) {
			gsap.registerPlugin(ScrollTrigger);
		}
		let rightCard = document.getElementById('right-card');
		const triggerAnimation = document.getElementById('animation-trigger');
		if (!rightCard) {
			console.error('error could not find the right card element');
			return;
		}
		if (!triggerAnimation) {
			console.error('error could not find the trigger animation container');
			return;
		}
		let TimeLine = gsap.timeline({
			scrollTrigger: {
				trigger: triggerAnimation,
				top: 'top top',
				end: 'bottom bottom',
				scrub: true
			}
		});
		TimeLine.fromTo(
			rightCard,
			{
				opacity: 0
			},
			{
				opacity: 1,
				duration: 1.5,
				ease: 'back.inOut'
			}
		);

		scrollTriggerInstance = TimeLine.scrollTrigger;
	});
	onDestroy(() => {
		if (scrollTriggerInstance) {
			scrollTriggerInstance.kill();
		}
	});
</script>

<main class="relative h-auto w-auto overflow-hidden">
	<div class="flex h-32 w-full items-center justify-center bg-amber-400">
		<h1
			class="px-4 text-center text-lg font-semibold text-balance text-black underline decoration-2 sm:text-xl md:text-2xl lg:text-3xl"
		>
			Now the logic
		</h1>
	</div>

	<div class="mx-auto flex h-32 w-[95%] items-center">
		<h1 class="font-semibold text-white sm:text-sm md:text-lg lg:text-xl xl:text-2xl 2xl:text-3xl">
			First :
			<a href="https://svelte.dev/docs/svelte/stores" class="text-sky-400 underline decoration-4"
				>SvelteKit Stores</a
			>
		</h1>
	</div>

	<section id="sveltekit_store_part" class="relative grid h-96 w-full grid-cols-2">
		<article
			class="col-span-1 flex h-full w-full items-center justify-center overflow-hidden bg-fuchsia-300"
		>
			<StoreSveltekit />
		</article>
		<article class="col-span-1 h-full w-full overflow-hidden">
			<div class="mx-auto flex h-full w-[95%] items-center justify-center">
				<p
					class="flex flex-col items-start justify-start gap-4 px-4 text-sm leading-relaxed font-semibold text-white sm:gap-5 sm:text-base md:text-lg"
				>
					For this we are gonna use :
					<span>
						<strong class="underline decoration-2">writable</strong>: a store you can read and
						update (like a variable that reacts)
					</span>
					<span>
						<strong class="underline decoration-2">readable</strong>: a store you can only read, not
						update directly
					</span>
					<span>
						<strong class="underline decoration-2">derived</strong>: a store whose value depends on
						other stores
					</span>
					<span>
						<strong class="underline decoration-2">get</strong>: instantly read a store’s current
						value (outside components)
					</span>
				</p>
			</div>
		</article>
	</section>

	<!--?cheking the browser for previous data -->

	<section class="relative w-full overflow-hidden py-8">
		<!-- Title -->
		<div class="mx-auto flex w-[95%] items-center justify-center">
			<h1
				class="text-center text-lg font-semibold text-white sm:text-xl md:text-2xl lg:text-3xl xl:text-4xl"
			>
				Step One : Checking the browser for existing data
			</h1>
		</div>

		<!-- Content -->
		<article
			id="checking_the_browser_article_tag"
			class="relative mt-8 grid w-full grid-cols-1 gap-6 overflow-hidden md:grid-cols-2"
		>
			<!-- Left (Component) -->
			<div class="flex items-center justify-center px-4">
				<div class="w-full max-w-[95%]">
					<CheckingTheBrowser />
				</div>
			</div>

			<!-- Right (Text) -->
			<div class="flex flex-col items-center justify-center space-y-4 px-4">
				<p
					class="text-center text-sm leading-relaxed font-semibold text-white sm:text-base md:text-lg lg:text-xl"
				>
					This checks if we’re in the browser and loads existing data.
				</p>
				<p
					class="text-center text-sm leading-relaxed font-semibold text-white sm:text-base md:text-lg lg:text-xl"
				>
					Don’t forget to import <code class="text-[#00FFFF]">{browser}</code> from
					<code class="text-[#00FFFF]">$app/environment</code>;
				</p>
			</div>
		</article>
	</section>

	<!--!create the store : -->

	<section class="relative w-full overflow-hidden py-8">
		<!-- Title -->
		<div class="mx-auto flex w-[95%] items-center justify-center">
			<h1
				class="text-center text-lg font-semibold text-white sm:text-xl md:text-2xl lg:text-3xl xl:text-4xl"
			>
				Step Two : Create the store
			</h1>
		</div>

		<!-- Content -->
		<article class="relative mt-8 grid w-full grid-cols-1 gap-6 overflow-hidden md:grid-cols-2">
			<!-- Text section -->
			<div class="flex items-center justify-center px-4">
				<p
					class="text-center text-sm leading-relaxed font-semibold text-balance text-white sm:text-base md:text-lg lg:text-xl"
				>
					<span class="italic">writable</span> makes a reactive value you can read & update — think of
					it as a magic reactive box
				</p>
			</div>

			<!-- Component section -->
			<div class="flex items-center justify-center px-4">
				<div class="w-full max-w-[95%]">
					<CreateTheStore />
				</div>
			</div>
		</article>
	</section>

	<!--Local Storage Sync to the ui-->
	
	<section id="sveltekit_memory_browser_updated" class="relative w-full overflow-hidden py-8">
		<!-- Title -->
		<div class="mx-auto flex w-[95%] items-center justify-center">
			<h1
				class="text-center text-lg font-semibold text-white sm:text-xl md:text-2xl lg:text-3xl xl:text-4xl"
			>
				Step Three : Keep the browser memory updated
			</h1>
		</div>

		<!-- Content -->
		<div
			id="animation-trigger"
			class="relative mt-8 grid w-full grid-cols-1 gap-6 overflow-hidden md:grid-cols-2"
		>
			<!-- Left (LocalStorageSync Component) -->
			<div id="right-card" class="flex items-center justify-center px-4">
				<div
					class="aspect-video w-full max-w-[90%] overflow-hidden rounded-2xl border border-gray-600 shadow-2xl md:aspect-[4/3]"
				>
					<LocalStorageSync />
				</div>
			</div>

			<!-- Right (Text Card) -->
			<div id="left-card" class="flex items-center justify-center px-4">
				<div
					class="flex aspect-video w-full max-w-[90%] items-center justify-center overflow-hidden rounded-2xl border border-gray-600 shadow-2xl md:aspect-[4/3]"
				>
					<p
						class="px-4 text-center text-sm leading-relaxed font-semibold text-balance text-white sm:text-base md:text-lg lg:text-xl"
					>
						Every store change is saved to <span class="text-[#00FFFF]">localStorage</span>.
					</p>
				</div>
			</div>
		</div>
	</section>
</main>

<style>
	@media screen and (max-width: 1024px) {
		/* #cheking_the_browser_article_tag {
			padding: 1rem 0rem;
			display: flex;
			align-items: center;
			justify-content: center;
			flex-direction: column;
			height: auto;
			gap: 3rem;
		} */
	}

	@media screen and (max-width: 768px) {
		#sveltekit_store_part {
			height: auto;
			padding: 1rem 0rem;
		}

		/* #cheking_the_browser_article_tag {
			padding: 1rem 0rem;
			display: flex;
			align-items: center;
			justify-content: center;
			flex-direction: column;
		} */
	}

	@media screen and (max-width: 425px) {
		#sveltekit_store_part {
			height: auto;
			padding: 1rem 0rem;
			display: flex;
			align-items: center;
			justify-content: center;
			flex-direction: column;
			gap: 3rem;
		}
	}
</style>
