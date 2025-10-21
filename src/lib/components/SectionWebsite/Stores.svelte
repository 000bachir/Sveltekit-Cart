<script>
	import StoreSveltekit from '$lib/assets/Icons/StoreSveltekit.svelte';
	import CheckingTheBrowser from '../ui/LogicExplanation/CheckingTheBrowser.svelte';
	import CreateTheStore from '../ui/LogicExplanation/CreateTheStore.svelte';
</script>

<main class="relative h-auto w-auto overflow-hidden">
	<div class="flex h-32 w-full items-center justify-center bg-amber-400">
		<h1
			class=" font-semibold underline decoration-4 sm:text-sm md:text-lg lg:text-xl xl:text-2xl 2xl:text-3xl"
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

	<section class="relative grid h-96 w-full grid-cols-2">
		<article
			class="col-span-1 flex h-full w-full items-center justify-center overflow-hidden bg-fuchsia-300"
		>
			<StoreSveltekit />
		</article>
		<article class="col-span-1 h-full w-full overflow-hidden">
			<div class="mx-auto flex h-full w-[95%] items-center justify-center">
				<p class="flex flex-col items-start justify-start gap-5 font-semibold text-white">
					For this we are gonna use :
					<span class="">
						<strong class="underline decoration-2">writable</strong>: a store you can read and
						update (like a variable that reacts)
					</span>
					<span class="">
						<strong class="underline decoration-2">readable</strong>: a store you can only read, not
						update directly
					</span>
					<span class="">
						<strong class="underline decoration-2">derived</strong>: a store whose value depends on
						other stores
					</span>
					<span class="">
						<strong class="underline decoration-2">get</strong>: instantly read a store’s current
						value (outside components)
					</span>
				</p>
			</div>
		</article>
	</section>

	<!--cheking the browser for previous data -->
	<section class="relative h-auto w-full overflow-hidden">
		<div class="mx-auto flex h-32 w-[95%] items-center justify-center">
			<h1
				class="font-semibold text-white sm:text-sm md:text-lg lg:text-xl xl:text-2xl 2xl:text-3xl"
			>
				Step one : Checking the browser for existing data
			</h1>
		</div>

		<article class="relative grid h-40 w-full grid-cols-2 overflow-hidden">
			<div class="col-span-1 h-full w-full overflow-hidden">
				<div class="mx-auto h-full w-[95%]">
					<CheckingTheBrowser />
				</div>
			</div>
			<div class="col-span-1 h-full w-full overflow-hidden">
				<div class="mx-auto flex h-full w-[95%] flex-col items-center justify-center">
					<p class="text-center text-lg font-semibold text-white">
						this checks if we’re in the browser and loads existing data.
					</p>
					<p class="text-center text-lg font-semibold text-white">
						do not forget to import the &#123; browser &#125; from $app/environment;
					</p>
				</div>
			</div>
		</article>
	</section>

	<!--create the store : -->
	<section class="relative h-auto w-full overflow-hidden">
		<div class="mx-auto flex h-32 w-[95%] items-center justify-center">
			<h1
				class="font-semibold text-white sm:text-sm md:text-lg lg:text-xl xl:text-2xl 2xl:text-3xl"
			>
				Step Two : Create the store
			</h1>
		</div>

		<article class="relative grid h-40 w-full grid-cols-2 overflow-hidden">
			<div class="col-span-1 h-full w-full overflow-hidden">
				<div class="mx-auto flex h-full w-[95%] items-center justify-center">
					<p class="text-center text-lg font-semibold text-balance text-white">
						writable makes a reactive value you can read & update think of it as a magic reactive
						box
					</p>
				</div>
			</div>
			<div class="col-span-1 h-full w-full overflow-hidden">
				<div class="mx-auto h-full w-[95%]">
					<CreateTheStore />
				</div>
			</div>
		</article>
	</section>

    <!--Local Storage Sync to the ui-->
    <section class="h-auto w-full relative overflow-hidden">
        <div class="mx-auto flex h-32 w-[95%] items-center justify-center">
			<h1
				class="font-semibold text-white sm:text-sm md:text-lg lg:text-xl xl:text-2xl 2xl:text-3xl"
			>
				Step Three : keep the browser memory updated
			</h1>
		</div>
    </section>

</main>

<style>
</style>
