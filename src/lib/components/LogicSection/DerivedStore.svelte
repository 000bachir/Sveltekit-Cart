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
	<section class="relative grid h-96 w-full grid-cols-2 overflow-hidden">
		<!-- explanation -->
		<article
			class="relative col-span-1 flex h-full w-full flex-col items-center justify-center gap-10 overflow-hidden border-r-[1px] border-gray-50"
		>
			<h1 class="text-center text-2xl font-semibold text-balance text-white">
				A store that calculates things automatically 🤑
			</h1>
			<button
				onclick={() => (showModal = true)}
				type="button"
				class="me-2 mb-2 cursor-pointer rounded-lg bg-gradient-to-br from-purple-600 to-blue-500 px-5 py-2.5 text-center text-sm font-medium text-white hover:bg-gradient-to-bl focus:ring-4 focus:ring-blue-300 focus:outline-none dark:focus:ring-blue-800"
			>
				Display Code
			</button>
			<Modal bind:showModal>
				{#snippet header()}
					<h1 class="text-lg font-semibold text-white">
						{title}
					</h1>
				{/snippet}
				<DerivedStoreCode />
			</Modal>
		</article>
		<!-- code snippet -->
		<article
			class="relative col-span-1 h-full w-full overflow-hidden border-l-[1px] border-gray-50"
		>
			<div class="mx-auto flex h-full w-[95%] flex-col items-start justify-evenly">
				<h1 class="text-center text-lg font-semibold text-balance">
					important takeaway : think of the reduce methode as a way to shrink an array of number
					into it's cumulative
				</h1>
				<ul class="flex flex-col gap-2">
					<li class="font-semibold">
						<span class="text-yellow-400"><strong>ItemCount</strong></span> : count how many items in
						the Cart
					</li>
					<li class="font-semibold">
						<span class="text-yellow-400"><strong>subTotal</strong></span> : the total price of the selected
						items
					</li>
					<li class="font-semibold">
						<span class="text-yellow-400"><strong>formattedSubtotal</strong></span> : format the total
						to get something like 100$
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
		<article id="logic-cart-section" class="grid h-96 w-full grid-cols-3 grid-rows-2">
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
