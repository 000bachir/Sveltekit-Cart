
<section
	id="main-container"
	class="relative grid h-auto w-full grid-cols-2 border-b-[5px] border-red-600/40"
>
	<article id="left-grid" class="h-96 w-full border-r-[2.5px] border-red-600/40">
		<div class="mx-auto flex h-full w-[95%] items-center justify-center">
			<p class="text-center leading-relaxed text-balance text-white">
				This blog will show you how to make a cart across pages in SvelteKit the minor drawback is
				that it is not going to with a database usage just the local storage while easy we tho to
				use LocalStorage and SvelteKit stores check the official docs for better undersatandign : <span
					class="text-sky-400 text-shadow-neutral-700"
					><a href="https://svelte.dev/docs/svelte/stores">stores</a></span
				>
			</p>
		</div>
	</article>
	<article id="right-grid" class="h-96 w-full border-l-[2.5px] border-red-600/40">
		<div class="mx-auto flex h-full w-[95%] items-center justify-center">
			<p class="text-center leading-relaxed text-balance text-white">
				Just to be clear in the project i used typescript and i downloaded the icons from :
				<span class="text-sky-400 text-shadow-neutral-700"
					><a href="https://iconify.design/docs/icon-components/svelte/">Svelte iconify</a></span
				>
				and here is the complete code if you wanna take a look :<span
					class="text-sky-400 text-shadow-neutral-700"
					><a href="https://github.com/000bachir/universal_cart_svelte">Github</a></span
				>
			</p>
		</div>
	</article>
</section>

<style>
	@media screen and (max-width:768px){
		#main-container{
			display: flex;
			flex-direction: column;
			align-items: center;
			justify-content: center;
		}
		#left-grid{
			border-right: 0;
			border-bottom: solid 2.5px rgb(220 38 38 / 0.4);
		}
		#right-grid{
			border-left: 0;
		}
	}

	@media screen and (max-width:425px){
		#main-container{
			display: flex;
			flex-direction: column;
			align-items: center;
			justify-content: center;
		}
		#left-grid{
			border-right: 0;
			border-bottom: solid 2.5px rgb(220 38 38 / 0.4);
		}
		#right-grid{
			border-left: 0;
		}
	}


</style>