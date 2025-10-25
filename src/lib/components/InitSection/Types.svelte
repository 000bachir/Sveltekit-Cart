<script>
	import KickOffTypes from '$lib/assets/Icons/KickOffTypes.svelte';
	import DummyJsonTypes from '../ui/first_section_code_block/DummyJsonTypes.svelte';
	import Modal from '../ui/Modal.svelte';

	let showModal = $state(false);
	const title = "dummy json api"
</script>

<section class="relative h-auto w-full overflow-hidden">
	<!--little disclaimer-->

	<div class="relative flex h-32 w-full items-center justify-center">
		<h1
			class=" text-center leading-relaxed font-semibold text-balance text-white underline decoration-4 sm:text-sm md:text-lg lg:text-xl xl:text-2xl 2xl:text-3xl"
		>
			Disclaimer : Im gonna use types that refer to dummy json api just to make it a bit clear
		</h1>
	</div>

	<div class="relative grid h-96 w-full grid-cols-2 overflow-hidden">
		<article
			class="relative col-span-1 flex flex-col h-full w-full items-center justify-center gap-10 overflow-hidden"
		>
			<h1 class="font-semibold text-2xl text-white text-center text-balance">Create a CartProduct.ts file in the lib directory then add the types</h1>
			<button
				onclick={() => (showModal = true)}
				type="button"
				class="me-2 mb-2 cursor-pointer rounded-lg bg-gradient-to-br from-purple-600 to-blue-500 px-5 py-2.5 text-center text-sm font-medium text-white hover:bg-gradient-to-bl focus:ring-4 focus:ring-blue-300 focus:outline-none dark:focus:ring-blue-800"
			>
				Display Types
			</button>

			<Modal bind:showModal>
				{#snippet header()}
					<h1 class="text-lg font-semibold text-white"> {title} </h1>
				{/snippet}
				<DummyJsonTypes />
			</Modal>
		</article>
		<article class="col-span-1 flex h-full w-full items-center justify-center">
			<!-- ui icon -->
			<KickOffTypes />
		</article>
	</div>
</section>
