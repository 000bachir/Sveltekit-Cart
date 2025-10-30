<script>
	import Modal from '../ui/Modal.svelte';
	import AddItems from '../ui/second_section_code_block/actions/AddItems.svelte';
	import ClearAndGetCart from '../ui/second_section_code_block/actions/ClearAndGetCart.svelte';
	import DecrementQuantity from '../ui/second_section_code_block/actions/DecrementQuantity.svelte';
	import IncrementQuantity from '../ui/second_section_code_block/actions/IncrementQuantity.svelte';
	import RemoveItems from '../ui/second_section_code_block/actions/RemoveItems.svelte';
	import UpdateQuantity from '../ui/second_section_code_block/actions/UpdateQuantity.svelte';

	let showModal = $state(false);
	let activeModal = $state(null);
</script>

<!--!add items-->
<div class="relative flex h-full w-full items-center justify-center">
	<button
		onclick={() => {
			showModal = true;
			console.log('add items btn clicked');
			activeModal = 'add';
		}}
		type="button"
		class="me-2 mb-2 cursor-pointer rounded-lg bg-gray-300 px-4 py-2 text-center text-xs font-semibold text-black transition-all duration-300 hover:bg-gray-400 hover:bg-gradient-to-bl focus:ring-4 focus:ring-blue-300 focus:outline-none sm:px-5 sm:py-2.5 sm:text-sm md:px-6 md:py-3 md:text-base dark:focus:ring-blue-800"
	>
		Adding items
	</button>
	{#if showModal && activeModal === 'add'}
		<Modal bind:showModal>
			{#snippet header()}
				<h1 class="font-semibold text-white">Add items</h1>
			{/snippet}
			<AddItems />
		</Modal>
	{/if}
</div>
<!--! remove items-->
<div class="relative flex h-full w-full items-center justify-center overflow-hidden">
	<button
		onclick={() => {
			showModal = true;
			activeModal = 'remove';
			console.log('remove items btn clicked');
		}}
		type="button"
		class="me-2 mb-2 cursor-pointer rounded-lg bg-gray-300 px-4 py-2 text-center text-xs font-semibold text-black transition-all duration-300 hover:bg-gray-400 hover:bg-gradient-to-bl focus:ring-4 focus:ring-blue-300 focus:outline-none sm:px-5 sm:py-2.5 sm:text-sm md:px-6 md:py-3 md:text-base dark:focus:ring-blue-800"
	>
		Remove Items
	</button>
	{#if showModal && activeModal === 'remove'}
		<Modal bind:showModal>
			<RemoveItems />
		</Modal>
	{/if}
</div>
<!--!update quantity items-->
<div class="flex h-full w-full items-center justify-center overflow-hidden">
	<button
		onclick={() => {
			showModal = true;
			activeModal = 'update';
			console.log('remove items btn clicked');
		}}
		type="button"
		class="me-2 mb-2 cursor-pointer rounded-lg bg-gray-300 px-4 py-2 text-center text-xs font-semibold text-black transition-all duration-300 hover:bg-gray-400 hover:bg-gradient-to-bl focus:ring-4 focus:ring-blue-300 focus:outline-none sm:px-5 sm:py-2.5 sm:text-sm md:px-6 md:py-3 md:text-base dark:focus:ring-blue-800"
	>
		Update Quantity
	</button>
	{#if showModal && activeModal === 'update'}
		<Modal bind:showModal>
			<UpdateQuantity />
		</Modal>
	{/if}
</div>
<!--!increment quantity items-->
<div class="flex h-full w-full items-center justify-center overflow-hidden">
	<button
		onclick={() => {
			showModal = true;
			activeModal = 'increment';
			console.log('remove items btn clicked');
		}}
		type="button"
		class="me-2 mb-2 cursor-pointer rounded-lg bg-gray-300 px-4 py-2 text-center text-xs font-semibold text-black transition-all duration-300 hover:bg-gray-400 hover:bg-gradient-to-bl focus:ring-4 focus:ring-blue-300 focus:outline-none sm:px-5 sm:py-2.5 sm:text-sm md:px-6 md:py-3 md:text-base dark:focus:ring-blue-800"
	>
		Increment amount
	</button>
	{#if showModal && activeModal === 'increment'}
		<Modal bind:showModal>
			<IncrementQuantity />
		</Modal>
	{/if}
</div>
<!--!decrement quantity items-->
<div class="flex h-full w-full items-center justify-center overflow-hidden">
	<button
		onclick={() => {
			showModal = true;
			activeModal = 'decrement';
		}}
		type="button"
		class="me-2 mb-2 cursor-pointer rounded-lg bg-gray-300 px-4 py-2 text-center text-xs font-semibold text-black transition-all duration-300 hover:bg-gray-400 hover:bg-gradient-to-bl focus:ring-4 focus:ring-blue-300 focus:outline-none sm:px-5 sm:py-2.5 sm:text-sm md:px-6 md:py-3 md:text-base dark:focus:ring-blue-800"
	>
		Decrement amount
	</button>
	{#if showModal && activeModal === 'decrement'}
		<Modal bind:showModal>
			<DecrementQuantity />
		</Modal>
	{/if}
</div>
<!-- ? clear cart and get cart am gonna combine them since they are not that hard-->
<div class=" flex h-full w-full flex-col items-center justify-center overflow-hidden">
	<button
		onclick={() => {
			showModal = true;
			activeModal = 'ClearAndGetCart';
		}}
		type="button"
		class="me-2 mb-2 cursor-pointer rounded-lg bg-gray-300 px-4 py-2 text-center text-xs font-semibold text-black transition-all duration-300 hover:bg-gray-400 hover:bg-gradient-to-bl focus:ring-4 focus:ring-blue-300 focus:outline-none sm:px-5 sm:py-2.5 sm:text-sm md:px-6 md:py-3 md:text-base dark:focus:ring-blue-800"
	>
		Clear / Get Cart
	</button>
	{#if showModal && activeModal === 'ClearAndGetCart'}
		<Modal bind:showModal>
			<ClearAndGetCart />
		</Modal>
	{/if}
</div>

<style>
</style>
