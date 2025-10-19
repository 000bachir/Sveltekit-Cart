<script>
	import StoreSveltekit from "$lib/assets/Icons/StoreSveltekit.svelte";


</script>


<main class="h-auto w-auto relative overflow-hidden">
    <div class="h-32 w-full flex items-center justify-center bg-amber-400">
        <h1 class=" font-semibold underline decoration-4 sm:text-sm md:text-lg lg:text-xl xl:text-2xl 2xl:text-3xl">Now the logic</h1>
    </div>

    <div class="h-32 w-[95%] mx-auto flex items-center ">
        <h1 class="text-white font-semibold sm:text-sm md:text-lg lg:text-xl xl:text-2xl 2xl:text-3xl">
            First : 
            <a href="https://svelte.dev/docs/svelte/stores" class="text-sky-400 underline decoration-4">SvelteKit Stores</a>
        </h1>
    </div>

    <section class="h-96 w-full relative grid grid-cols-2">
        <article class="col-span-1 overflow-hidden flex items-center justify-center h-full w-full bg-fuchsia-300">
            <StoreSveltekit />
        </article>
        <article class="col-span-1 overflow-hidden h-full w-full">
            <div class="h-full w-[95%] mx-auto  flex items-center justify-center">
                <p class="font-semibold flex flex-col items-start justify-start gap-5 text-white">For this we are gonna use :
                    <span class="">
                        <strong class="underline decoration-2">writable</strong>: a store you can read and update (like a variable that reacts)
                    </span>
                    <span class="">
                        <strong class="underline decoration-2">readable</strong>: a store you can only read, not update directly
                    </span>
                    <span class="">
                        <strong class="underline decoration-2">derived</strong>: a store whose value depends on other stores
                    </span>
                    <span class="">
                        <strong class="underline decoration-2">get</strong>: instantly read a store’s current value (outside components)
                    </span>
                </p>
            </div>
        </article>
    </section>

</main>


<style>

</style>