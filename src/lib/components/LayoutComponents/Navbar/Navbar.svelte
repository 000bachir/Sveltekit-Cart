<script>
	import Home from '$lib/assets/Icons/Home.svelte';
</script>

<nav class="mx-auto h-20 w-[85%] overflow-hidden">
	<div class="grid h-full w-full grid-cols-3">
		<div class="col-span-1 flex h-full w-full items-center">
			<a href="/">
				<Home />
			</a>
		</div>
		<div id="link-container" class="col col-span-2 flex items-center justify-end gap-10">
			<h1 class=" link 2xl:text-3xl xl:text-2xl lg:text-xl md:text-lg sm:text-sm font-semibold text-white">
				<a href="/about"> About </a>
			</h1>

			<h1 class="link 2xl:text-3xl xl:text-2xl lg:text-xl md:text-lg sm:text-sm font-semibold text-white">
				<a href="/about"> Contact </a>
			</h1>
		</div>
	</div>
</nav>

<style>

    .link{
        transition: color  0.3s ease-in-out;
    }
    .link:hover{
        color: #31572c;
    }

</style>
