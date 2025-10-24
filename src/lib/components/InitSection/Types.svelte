<script>
	import KickOffTypes from '$lib/assets/Icons/KickOffTypes.svelte';
	import Modal from '../ui/Modal.svelte';

	let showModal = $state(false);
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
				{#snippet header()}{/snippet}
				<pre class=" text-sm text-zinc-100">
					<code id="language-ts" class="leading-relaxed font-semibold">
						<span style="color: #569cd6">export</span> <span style="color: #569cd6">type</span> <span style="color: #4ec9b8">Product</span> = &#123;
							<span style="color: #9cdcfe">id</span>: <span style="color: #569cd6">number</span>;
							<span style="color: #9cdcfe">title</span>: <span style="color: #569cd6">string</span>;
							<span style="color: #9cdcfe">description</span>: <span style="color: #569cd6">string</span>;
							<span style="color: #9cdcfe">category</span>: <span style="color: #569cd6">string</span>;
							<span style="color: #9cdcfe">price</span>: <span style="color: #569cd6">number</span>;
							<span style="color: #9cdcfe">discountPercentage</span>: <span style="color: #569cd6">number</span>;
							<span style="color: #9cdcfe">rating</span>: <span style="color: #569cd6">number</span>;
							<span style="color: #9cdcfe">stock</span>: <span style="color: #569cd6">number</span>;
							<span style="color: #9cdcfe">tags</span>: <span style="color: #569cd6">string</span>[];
							<span style="color: #9cdcfe">brand</span>: <span style="color: #569cd6">string</span>;
							<span style="color: #9cdcfe">sku</span>: <span style="color: #569cd6">string</span>;
							<span style="color: #9cdcfe">weight</span>: <span style="color: #569cd6">number</span>;
							<span style="color: #9cdcfe">dimensions</span>: <span style="color: #4ec9b8">Dimensions</span>;
							<span style="color: #9cdcfe">warrantyInformation</span>: <span style="color: #569cd6">string</span>;
							<span style="color: #9cdcfe">shippingInformation</span>: <span style="color: #569cd6">string</span>;
							<span style="color: #9cdcfe">availabilityStatus</span>: <span style="color: #569cd6">string</span>;
							<span style="color: #9cdcfe">reviews</span>: <span style="color: #4ec9b8">Review</span>[];
							<span style="color: #9cdcfe">returnPolicy</span>: <span style="color: #569cd6">string</span>;
							<span style="color: #9cdcfe">minimumOrderQuantity</span>: <span style="color: #569cd6">number</span>;
							<span style="color: #9cdcfe">meta</span>: <span style="color: #4ec9b8">Meta</span>;
							<span style="color: #9cdcfe">thumbnail</span>: <span style="color: #569cd6">string</span>;
							<span style="color: #9cdcfe">images</span>: <span style="color: #569cd6">string</span>[];
						&#125;
							<span style="color: #569cd6">export</span> <span style="color: #569cd6">type</span> <span style="color: #4ec9b8">CartProduct</span> = &#123;
							<span style="color: #9cdcfe">id</span>: <span style="color: #569cd6">string</span>;
							<span style="color: #9cdcfe">product</span>: <span style="color: #4ec9b8">Product</span>;
							<span style="color: #9cdcfe">quantity</span>: <span style="color: #569cd6">number</span>;
						&#125;
					</code>
				</pre>
			</Modal>
		</article>
		<article class="col-span-1 flex h-full w-full items-center justify-center">
			<KickOffTypes />
		</article>
	</div>
</section>
