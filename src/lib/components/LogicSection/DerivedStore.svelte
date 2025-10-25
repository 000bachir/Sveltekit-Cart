<script>
	import Modal from '../ui/Modal.svelte';
	import DerivedStoreCode from '../ui/second_section_code_block/Derived_store_code.svelte';

    let showModal = $state(false)
    let title = "derive store for total code"
</script>

<main class="relative h-auto w-full overflow-hidden">
	<section
		id="title_of_the_blog"
		class="relative flex h-28 w-full items-center justify-center overflow-hidden bg-amber-400"
	>
		<h1
			class="font-semibold underline decoration-4 sm:text-sm md:text-lg lg:text-xl xl:text-2xl 2xl:text-3xl"
		>
			Let's make it useful 
		</h1>
	</section>

    <!--Derived Store for Totals-->
    <section class="h-96 w-full relative overflow-hidden  grid grid-cols-2">
        <!-- explanation -->
        <article class="h-full w-full relative overflow-hidden col-span-1 flex flex-col items-center justify-center gap-10">
            <h1 class="font-semibold text-2xl text-white text-center text-balance">A store that calculates things automatically</h1>
			<button
				onclick={() => (showModal = true)}
				type="button"
				class="me-2 mb-2 cursor-pointer rounded-lg bg-gradient-to-br from-purple-600 to-blue-500 px-5 py-2.5 text-center text-sm font-medium text-white hover:bg-gradient-to-bl focus:ring-4 focus:ring-blue-300 focus:outline-none dark:focus:ring-blue-800"
			>
				Display Code
            </button>
        </article>
        <!-- code snippet -->
        <article class="h-full w-full relative overflow-hidden col-span-1 flex items-center justify-center">
            <Modal bind:showModal>
                {#snippet header()}
                <h1 class="text-lg font-semibold text-white">
                    {title}
                </h1>
                {/snippet}
                <DerivedStoreCode />
            </Modal>
        </article>

    </section>
</main>
