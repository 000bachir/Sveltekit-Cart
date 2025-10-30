<script>
	import Modal from '../ui/Modal.svelte';
	import AddItems from '../ui/second_section_code_block/actions/AddItems.svelte';
	import DerivedStoreCode from '../ui/second_section_code_block/Derived_store_code.svelte';
	import CartActions from './CartActions.svelte';

	let showModal = $state(false);
	let title = 'derive store for total code';
</script>

<main class="relative h-auto w-full overflow-hidden">
	<section
		id="title_of_the_blog"
		class="relative flex h-28 w-full items-center justify-center overflow-hidden bg-amber-400"
	>
		<h1
			class="font-semibold text-black underline decoration-4 sm:text-sm md:text-lg lg:text-xl xl:text-2xl 2xl:text-3xl"
		>
			Let's make it useful
		</h1>
	</section>

	<!--Derived Store for Totals-->
	<section
		class="relative grid w-full grid-cols-1 overflow-hidden border-t border-b border-gray-700 py-10 md:grid-cols-2"
	>
		<!-- Explanation -->
		<article
			class="flex flex-col items-center justify-center gap-6 border-b border-gray-700 px-4 py-6 text-center md:border-r md:border-b-0"
		>
			<h1 class="text-xl font-semibold text-balance text-white sm:text-2xl md:text-3xl">
				A store that calculates things automatically 🤑
			</h1>

			<button
				onclick={() => (showModal = true)}
				type="button"
				class="rounded-lg bg-gradient-to-br from-purple-600 to-blue-500 px-5 py-2.5 text-sm font-medium text-white transition-all duration-300 hover:from-purple-500 hover:to-blue-400 focus:ring-4 focus:ring-blue-300 focus:outline-none sm:text-base dark:focus:ring-blue-800"
			>
				Display Code
			</button>

			<Modal bind:showModal>
				{#snippet header()}
					<h1 class="text-lg font-semibold text-white">{title}</h1>
				{/snippet}
				<DerivedStoreCode />
			</Modal>
		</article>

		<!-- Code snippet / Explanation list -->
		<article
			class="flex flex-col items-center justify-center px-4 py-6 text-center md:px-8 md:text-left"
		>
			<div class="w-full max-w-[600px] space-y-6">
				<h1 class="text-base font-semibold text-balance text-white sm:text-lg md:text-xl">
					Important takeaway: think of the
					<span class="font-bold text-yellow-400">reduce</span> method as a way to shrink an array of
					numbers into its cumulative value.
				</h1>

				<ul class="flex flex-col gap-3">
					<li class="text-sm font-semibold text-white sm:text-base md:text-lg">
						<span class="font-bold text-yellow-400">ItemCount</span> — counts how many items are in the
						cart.
					</li>
					<li class="text-sm font-semibold text-white sm:text-base md:text-lg">
						<span class="font-bold text-yellow-400">subTotal</span> — the total price of the selected
						items.
					</li>
					<li class="text-sm font-semibold text-white sm:text-base md:text-lg">
						<span class="font-bold text-yellow-400">formattedSubtotal</span> — formats the total,
						e.g. <span class="text-green-300">100$</span>.
					</li>
				</ul>
			</div>
		</article>
	</section>

	<!-- ⚙️ 5. The Actions Object-->
	<section class="h-auto w-full overflow-hidden">
		<article
			id="title_of_the_blog"
			class="relative flex h-28 w-full items-center justify-center overflow-hidden bg-amber-400"
		>
			<h1
				class="font-semibold text-black underline decoration-4 sm:text-sm md:text-lg lg:text-xl xl:text-2xl 2xl:text-3xl"
			>
				Now the cart the actions ⚙️
			</h1>
		</article>
		<!--the idea here is to have modal button right and as far as am conserned for each of the action am gonna make it"s code snippet inside of it -->
		<!-- <article id="logic-cart-section" class="grid h-96 w-full grid-cols-3 grid-rows-2 py-4 ">
			<CartActions />
		</article> -->
		
		
		<article id="logic-cart-section" class="grid w-full grid-cols-1 sm:grid-cols-2 md:grid-cols-3 gap-4 p-4 sm:p-6 md:p-8">
			<CartActions />
		</article> 
		
	</section>
</main>

<style>
	#logic-cart-section {
		background-image: radial-gradient(rgba(255, 255, 255, 0.2) 8%, transparent 8%);
		background-position: 0% 0%;
		background-size: 5vmin 5vmin;
	}
</style>
