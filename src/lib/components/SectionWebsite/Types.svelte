<script>
	import KickOffTypes from '$lib/assets/Icons/KickOffTypes.svelte';
	import Modal from '../ui/Modal.svelte';

	let showModal = $state(false);
</script>

<section class="relative h-auto w-full">

	<!--little disclaimer-->

	<div class="relative flex h-32 w-full items-center justify-center">
		<h1
			class=" text-center leading-relaxed font-semibold text-balance text-white underline decoration-4 sm:text-sm md:text-lg lg:text-xl xl:text-2xl 2xl:text-3xl"
		>
			Disclaimer : Im gonna use types that refer to dummy json api just to make it a bit clear
		</h1>
	</div>

	<div class="grid h-96 w-full grid-cols-2 relative overflow-hidden">
		<article class="relative col-span-1 flex h-full w-full items-center justify-center overflow-hidden">
			<button
				onclick={()=> showModal = true }
				type="button"
				class="cursor-pointer me-2 mb-2 rounded-lg bg-gradient-to-br from-purple-600 to-blue-500 px-5 py-2.5 text-center text-sm font-medium text-white hover:bg-gradient-to-bl focus:ring-4 focus:ring-blue-300 focus:outline-none dark:focus:ring-blue-800"
			>
				Display Types
			</button>

			<Modal bind:showModal>
				{#snippet header()}
					<h2>
						Dummy json types
					</h2>
				{/snippet}

				<pre aria-label="code snippet" class="bg-zinc-900 text-zinc-100 text-sm text-left  overflow-y-scroll h-40 min-w-auto  ">
					<code class="language-ts">
						export type Product = &#123;
							id: number;
							title: string;
							description: string;
							category: string;
							price: number;
							discountPercentage: number;
							rating: number;
							stock: number;
							tags: string[];
							brand: string;
							sku: string;
							weight: number;
							dimensions: Dimensions;
							warrantyInformation: string;
							shippingInformation: string;
							availabilityStatus: string;
							reviews: Review[];
							returnPolicy: string;
							minimumOrderQuantity: number;
							meta: Meta;
							thumbnail: string;
							images: string[];
							&#125;
							export type CartProduct = &#123;
							id: string;
							product: Product;
							quantity: number;
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
