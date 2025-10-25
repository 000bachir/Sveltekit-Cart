<script>
	import Modal from '../ui/Modal.svelte';
	import AddItems from '../ui/second_section_code_block/actions/AddItems.svelte';
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
			class="text-black font-semibold underline decoration-4 sm:text-sm md:text-lg lg:text-xl xl:text-2xl 2xl:text-3xl"
		>
			Let's make it useful 
		</h1>
	</section>

    <!--Derived Store for Totals-->
    <section class="h-96 w-full relative overflow-hidden  grid grid-cols-2 ">
        <!-- explanation -->
        <article class="border-r-[1px] border-gray-50 h-full w-full relative overflow-hidden col-span-1 flex flex-col items-center justify-center gap-10">
            <h1 class="font-semibold text-2xl text-white text-center text-balance">A store that calculates things automatically 🤑 </h1>
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
        <article class="border-l-[1px] border-gray-50 h-full w-full relative overflow-hidden col-span-1 ">
            <div class="h-full w-[95%] mx-auto  flex items-start justify-evenly flex-col ">
                <h1 class="font-semibold text-center text-balance text-lg">
                    important takeaway : think of the reduce methode as a way to shrink an array of number into it's cumulative
                </h1>
                <ul class="flex flex-col gap-2">
                    <li class="font-semibold ">
                        <span class="text-yellow-400"><strong>ItemCount</strong></span> : count how many items in the Cart 
                    </li>
                    <li class="font-semibold ">
                        <span class="text-yellow-400"><strong>subTotal</strong></span> : the total price of the selected items
                    </li>
                    <li class="font-semibold ">
                        <span class="text-yellow-400"><strong>formattedSubtotal</strong></span> : format the total to get something like 100$
                    </li>
                </ul>
            </div>

        </article>

    </section>
    <!-- ⚙️ 5. The Actions Object-->
    <section class="h-auto w-full overflow-hidden">
        <article id="title_of_the_blog" class="relative flex h-28 w-full items-center justify-center overflow-hidden bg-amber-400">
		<h1
			class="text-black font-semibold underline decoration-4 sm:text-sm md:text-lg lg:text-xl xl:text-2xl 2xl:text-3xl"
		>
			Now the cart the actions object ⚙️
		</h1>
        </article>
        <!--the idea here is to have modal button right and as far as am conserned for each of the action am gonna make it"s code snippet inside of it -->
        <article class="h-96 w-full grid grid-cols-3 grid-rows-2">
            <!--each of these div will contain a specific action and if the ui is good a tiny desc -->

            <!--!add items-->
            <div class="bg-red-500">
            </div> 
            <!--! remove items-->
            <div class="bg-green-500"></div>
            <!--!update quantity items-->
            <div class="bg-yellow-500"></div>
            <!--!increment quantity items-->
            <div class="bg-white"></div>
            <!--!decrement quantity items-->
            <div class="bg-purple-500"></div>

            <!-- ? clear cart and get cart am gonna combine them since they are not that hard-->   
            <div class="bg-fuchsia-700"></div>
        </article>


    </section>


</main>
